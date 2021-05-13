# Snippetarium

- [Property list reader](#property-list-reader)
- [Increment](#increment)
- [Binding preview](#binding-preview)
- [FileManager with codable](#filemanager-with-codable)

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