# Library

Сюда я буду сваливать ссылки на статьи, которые я прочитал и решил, что ссылки на них достойны того, чтобы быть сохранеными

## Содержание

- [iOS Development](#ios-development)
- [Development workflow](#development-workflow)
- [Job seeking](#job-seeking)
- [Learning paths](#learning-paths)
- [Style Guldes](#style-guides)
- [Misc](#misc)
- [Snippets](#snippets)


### iOS Development

- [Архитектурные паттерны в iOS](https://habr.com/en/company/badoo/blog/281162/) - статья про MVC, MVP, MVVM и VIPER
- [Списки захвата в Swift: в чём разница между ссылками weak, strong и unowned?](https://habr.com/ru/post/444336/)
- [Swift Best Practices and Tips by Toptal Developers](https://www.toptal.com/swift/tips-and-practices)
- [Справочник iOS дизайна (HIG на русском)](http://miloskiy.com/ios-design-guide-hig-na-russkom/)
- [What Every Junior iOS Developer Needs to Know](https://blog.teamtreehouse.com/every-junior-ios-developer-needs-know)
- [Using Swift Codable With Property Lists](https://useyourloaf.com/blog/using-swift-codable-with-property-lists/)
- [Немного практики функционального программирования в Swift для начинающих](https://habr.com/ru/post/440722/)
- [Списки захвата в Swift: в чём разница между ссылками weak, strong и unowned?](https://habr.com/ru/post/444336/)
- [Find memory leaks in iOS apps with XCode Instruments](https://www.surekhatech.com/blog/find-memory-leaks-in-ios-apps-with-xcode-instruments)
- [//TODO: — Make your notes on Xcode stand out](https://medium.com/@cboynton/todo-make-your-notes-on-xcode-stand-out-5f5124ec064c) - не нужно если есть SwiftLint
- [Паттерны проектирования, взгляд iOS разработчика. Часть 0. Синглтон-Одиночка](https://habr.com/ru/post/320728/)
- [Паттерны проектирования, взгляд iOS разработчика. Часть 1. Стратегия](https://habr.com/ru/post/321182/)
- [Адекватное MVC для начинающих и не только](https://habr.com/ru/post/500870/)
- [Настройка локализаций в Xcode 8 и Swift 3](https://tproger.ru/articles/localizations-in-swift/) - годно и для Swift 5 Xcode 11
- [Internationalizing Your iOS App: Getting Started](https://www.raywenderlich.com/250-internationalizing-your-ios-app-getting-started)
- [Design Pattern. Разбираем шаблоны iOS-разработки на реальных примерах.](https://swiftlab.ru/2019/01/12/design-pattern/)
- [Swift Singletons: A Design Pattern to Avoid (With Examples)](https://matteomanferdini.com/swift-singleton/)

##### Networking

- [Modern Networking in Swift 5 with URLSession, Combine and Codable](https://www.vadimbulavin.com/modern-networking-in-swift-5-with-urlsession-combine-framework-and-codable/)
- [Network Manager + Postman](https://swiftbook.ru/post/tutorials/network-manager-postman/)
- [Implement a Networking Layer Using Combine in Swift 5](https://medium.com/better-programming/implement-a-networking-layer-using-combine-in-swift-5-8a83e3ac9bae)

##### SwiftUI

- [SwiftUI Tutorials](https://developer.apple.com/tutorials/swiftui/) by Apple
- [Адаптируем существующее бизнес-решение под SwiftUI. Часть 1](https://habr.com/ru/post/500194/)
- [Адаптируем существующее бизнес-решение под SwiftUI. Часть 2](https://habr.com/ru/post/500386/)
- [Адаптируем существующее бизнес-решение под SwiftUI. Часть 3. Работаем с архитектурой](https://habr.com/ru/post/500470/)
- [Адаптируем существующее бизнес-решение под SwiftUI. Часть 4. Навигация и конфигурация](https://habr.com/ru/post/500492/)

##### SOLID

- [Возвращаемся к SOLID](https://medium.com/nuances-of-programming/%D0%B2%D0%BE%D0%B7%D0%B2%D1%80%D0%B0%D1%89%D0%B0%D0%B5%D0%BC%D1%81%D1%8F-%D0%BA-solid-1c258669af21)
- [SOLID в iOS разработке. Принцип единственной ответственности](https://medium.com/@zhukovios/solid-in-ios-srp-1f4d63641f10)
- [SOLID в iOS разработке. Принцип открытости закрытости](https://medium.com/@zhukovios/solid-in-ios-ocp-890a5aedf2e5)
- [Как работают принципы SOLID в Swift. Принцип единственной ответственности.](https://medium.com/@vladislav.mityuklyaev/%D0%BA%D0%B0%D0%BA-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D1%8E%D1%82-%D0%BF%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%D1%8B-solid-%D0%B2-swift-%D0%BF%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF-%D0%B5%D0%B4%D0%B8%D0%BD%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D0%B9-%D0%BE%D1%82%D0%B2%D0%B5%D1%82%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D1%81%D1%82%D0%B8-f019d6daab2d) - то что выше, но другими словами
- [Как работают принципы SOLID в Swift. Принцип открытости/закрытости.](https://medium.com/@vladislav.mityuklyaev/solid-%D0%BF%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF-%D0%BE%D1%82%D0%BA%D1%80%D1%8B%D1%82%D0%BE%D1%81%D1%82%D0%B8-%D0%B7%D0%B0%D0%BA%D1%80%D1%8B%D1%82%D0%BE%D1%81%D1%82%D0%B8-%D0%B2-swift-open-closed-principle-in-swift-fd7290fe7456)
- [Как работают принципы SOLID в Swift. Принцип подставновки Барбары Лисков](https://medium.com/@vladislav.mityuklyaev/%D0%BA%D0%B0%D0%BA-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D1%8E%D1%82-%D0%BF%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%D1%8B-solid-%D0%B2-swift-%D0%BF%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF-%D0%BF%D0%BE%D0%B4%D1%81%D1%82%D0%B0%D0%B2%D0%BD%D0%BE%D0%B2%D0%BA%D0%B8-%D0%B1%D0%B0%D1%80%D0%B1%D0%B0%D1%80%D1%8B-%D0%BB%D0%B8%D1%81%D0%BA%D0%BE%D0%B2-a6284b529456)



### Development workflow

- [GitHub Flow](https://habr.com/ru/post/346066/) - перевод [Understanding the GitHub flow](https://guides.github.com/introduction/flow/)
- [Удачная модель ветвления для Git](https://habr.com/ru/post/106912/) - перевод [A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/) - статьи про Git flow (на мой взгляд не самой удачной модели ветвления)
- [GitHub Flow: рабочий процесс Гитхаба](https://habr.com/ru/post/189046/) - Еще одна статья про GitHub Flow
- [Что может помешать разработчику самостоятельно создать успешное приложение](https://medium.com/nuances-of-programming/%D1%87%D1%82%D0%BE-%D0%BC%D0%BE%D0%B6%D0%B5%D1%82-%D0%BF%D0%BE%D0%BC%D0%B5%D1%88%D0%B0%D1%82%D1%8C-%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA%D1%83-%D1%81%D0%B0%D0%BC%D0%BE%D1%81%D1%82%D0%BE%D1%8F%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D1%82%D1%8C-%D1%83%D1%81%D0%BF%D0%B5%D1%88%D0%BD%D0%BE%D0%B5-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-1330333c9da2)

### Job seeking

- [How to Apply for an iOS Developer Job](https://www.raywenderlich.com/2618-how-to-apply-for-an-ios-developer-job)
- [iOS Developer Resume Examples](https://www.raywenderlich.com/2617-ios-developer-resume-examples)
- [Собеседование Swift — вопросы и ответы](https://swiftlab.ru/2019/05/07/sobesedovanie-swift/)

### Learning paths

- [So you think you can call yourself a "Senior iOS Developer"?](https://blog.undabot.com/so-you-think-you-can-call-yourself-a-senior-ios-developer-767fb9d6e423)
- [A Path to Mastery for iOS Development](https://trello.com/b/dOV9dvBu/a-path-to-mastery-for-ios-development)

### Style Guides

- [The Official raywenderlich.com Swift Style Guide](https://github.com/raywenderlich/swift-style-guide)
- [Swift Style Guide by Google](https://google.github.io/swift/)
- [Metova's Swift Style Guide](https://github.com/metova/swift-style-guide)
- [iOS Good Practices](https://github.com/futurice/ios-good-practices)

### Misc

- [Полная экипировка iOS-разработчика: сервисы, инструменты, фреймворки, веб-сайты](https://tproger.ru/digest/ios-development-kit/)
- [Хороший дизайн должен быть SOLID: TOP-5 архитектурных принципов](http://igor.quatrocode.com/2008/09/solid-top-5.html)

### Snippets

##### Property list reader
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