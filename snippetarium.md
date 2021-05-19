# Snippetarium

- [Property list reader](#property-list-reader)
- [Increment](#increment)
- [Binding preview](#binding-preview)
- [FileManager with codable](#filemanager-with-codable)
- [SwiftUI ImagePicker](#swiftui-imagepicker)
- [TODO finder](#todo-finder)
- [Save and load image from Document Directory](#save-and-load-image-from-document-directory)

### Property list reader
```swift
struct ProductIds {
    static func getIdentifier(withKey key: String) -> String? {
        if let url = Bundle.main.url(forResource: "Identifiers", withExtension: "plist") {
            do {
                let listData = try Data(contentsOf: url)
                let myPlist = try PropertyListSerialization.propertyList(from: listData, options: [], format: nil)
                guard let myDict = myPlist as? [String: String], let result = myDict[key]  else {
                    return nil
                }
                return result
            } catch {
                print(error.localizedDescription)
            }
        }
        return nil
    }
}
```

### Increment
```swift
postfix operator ++
prefix operator ++

extension Int {
    static postfix func ++(lhs: inout Int) -> Int {
        lhs += 1
        return lhs
    }
    
    static prefix func ++(rhs: inout Int) -> Int {
        rhs += 1
        return rhs
    }
}

var t = 3
t++

print("Post \(t)")
```

### Binding preview
```swift
struct EditView_Previews: PreviewProvider {
      
    static var previews: some View {
        EditView(record: .constant(Record(description: "aaaaa")))
    }
}
```

### FileManager with codable
```swift
extension FileManager {
    func decode<T: Codable>(_ file: String) -> T {
        let paths = FileManager.default.urls(for: .documentDirectory, in: .userDomainMask)

        let url = paths[0].appendingPathComponent(file)
        
        guard let data = try? Data(contentsOf: url) else {
            fatalError("Failed to load \(file) from bundle")
        }
        
        let decoder = JSONDecoder()
        let formatter = DateFormatter()
        formatter.dateFormat = "y-MM-dd"
        decoder.dateDecodingStrategy = .formatted(formatter)
        
        guard let loaded = try? decoder.decode(T.self, from: data) else {
            fatalError("Failed to decode \(file) from bundle")
        }
        
        return loaded
    }
}
```

### SwiftUI ImagePicker
```swift
struct ImagePicker: UIViewControllerRepresentable {
    @Binding var image: UIImage?
    @Environment(\.presentationMode) var presentationMode
    
    func makeUIViewController(context: Context) -> UIImagePickerController {
        let picker = UIImagePickerController()
        picker.delegate = context.coordinator
        return picker
    }
    
    func updateUIViewController(_ uiViewController: UIImagePickerController, context: Context) {
        
    }

    class Coordinator:NSObject, UIImagePickerControllerDelegate, UINavigationControllerDelegate {
        var parent: ImagePicker
        
        init(_ parent: ImagePicker) {
            self.parent = parent
        }
        
        func imagePickerController(_ picker: UIImagePickerController, didFinishPickingMediaWithInfo info: [UIImagePickerController.InfoKey : Any]) {
            if let uiImage = info[.originalImage] as? UIImage {
                parent.image = uiImage
            }
            
            parent.presentationMode.wrappedValue.dismiss()
        }
    }
    
    func makeCoordinator() -> Coordinator {
        Coordinator(self)
    }
}
```

### TODO finder
```sh
TAGS="TODO:|FIXME:"
ERRORTAG="ERROR:"
find "${SRCROOT}" \( -name "*.h" -or -name "*.m" -or -name "*.swift" \) -print0 | xargs -0 egrep --with-filename --line-number --only-matching "($TAGS).*\$|($ERRORTAG).*\$" | perl -p -e "s/($TAGS)/ warning: \$1/" | perl -p -e "s/($ERRORTAG)/ error: \$1/"
```

### Save and load image from Document Directory
```swift
func getDocumentDirectory() -> URL {
    let paths = FileManager.default.urls(for: .documentDirectory, in: .userDomainMask)
    return paths[0]
}

private func save(image: UIImage) -> String? {
    let fileName = "FileName"
    let fileURL = documentsUrl.appendingPathComponent(fileName)
    if let imageData = image.jpegData(compressionQuality: 1.0) {
       try? imageData.write(to: fileURL, options: .atomic)
       return fileName // ----> Save fileName
    }
    print("Error saving image")
    return nil
}

private func load(fileName: String) -> UIImage? {
    let fileURL = documentsUrl.appendingPathComponent(fileName)
    do {
        let imageData = try Data(contentsOf: fileURL)
        return UIImage(data: imageData)
    } catch {
        print("Error loading image : \(error)")
    }
    return nil
}
```