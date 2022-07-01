## Предусловие:

Этот курс, создан для того, чтобы Manual QA *поняли*, как писать ui-тесты на iOS. 

Есть мнение, что если человек, что-то понял, он автоматически *научился*. Не достаточно пройти 1 курс, который хорошо всё объясняет, и ты сразу можешь делать всё то, о чём там говорится. Чтобы человек научился что-то делать, он должен тренироваться - то есть что-то делать. “Читать” или “Слушать” - это не “делать”. 

Если хочешь научиться автоматизировать, нужно как можно чаще: писать и дебажить автотесты. Но просто делать тоже не достаточно. Нужно делать правильно, получая обратную связь. И будет круто, если у вас получится найти такого ментора.

## **Требования к участникам программы:**

- Xcode версии ≥ 11
- Знание Swift на базовом уровне([SwiftBook](https://swiftbook.ru/) / [книжка Усова](https://www.ozon.ru/product/swift-osnovy-razrabotki-prilozheniy-pod-ios-ipados-i-macos-usov-vasiliy-aleksandrovich-usov-233893622/?sh=S9LQvPChHg))
- Знание Git на базовом уровне(checkout, merge, rebase, revert, git workflow,  branch)
- Пройти курс Raywenderlich: “[iOS and SwiftUI for Beginners](https://www.raywenderlich.com/ios/paths/learn)”
- Свой проект для покрытия автотестами

# Beginner

## Урок 1

**Цель: научить работать с github**

1. Создать аккаунт на [github](https://github.com/);
2. Настроить ssh ключ;
3. Добавить проект в удаленный репозиторий, созданный в рамках прохождения курса “[iOS and SwiftUI for Beginners](https://www.raywenderlich.com/ios/paths/learn)” либо добавьте свой проект;
4. Отвести ветку в которой будете выполнять задания.

**Полезная информация:**

- [Connecting to GitHub with SSH](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

## Урок 2

**Цель: научить работать с локаторами: проставлять, находить и хранить их**

1. проставить accessibilityidentifier в:
    1. storyboard
    2. viewController
    3. content(SwiftUI)
2. найти accessibilityidentifier в объектах при помощи:
    1. accessibility Inspector
    2. debug view hierarchy
    3. console(debugDescription)
    4. test recorder
3. создать enum для хранения локаторов

**Полезные материалы:**

- [Погружение в автотестирование на iOS. Часть 1. Как работать с accessibilityidentifier объектов](https://habr.com/ru/company/vivid_money/blog/533180/)
- [Идентификаторы элементов в XCUITest](https://habr.com/ru/company/hh/blog/647889/)
- [How to find elements on XCUITest](https://medium.com/xcuitest/how-to-find-elements-on-xcuitest-e457eb030353)
- [Easily manage accessibility attributes and accessing UI elements with XCTest on iOS](https://medium.com/super-dispatch/easily-manage-accessibility-attributes-and-accessing-ui-elements-with-xctest-on-ios-bb76b57f6a7d)
- [XCUITests — Best Practices for Organizing Locators with Swift Enumerations](https://medium.com/quality-engineering-university/xcuitests-best-practices-for-organizing-locators-with-swift-enumerations-452da45fe7d5)

## Урок 3

**Цель: научить взаимодействовать с ui-элементами в автотестах**

- Создать методы нажатия на элементы, которые нажимают по:
    - accessibilityidentifier
    - индексу элемента
    - координатам
    - по определенному лейблу в элементе(использовать NSPredicate)
- Создать метод закрытия алерта
- Создать метод нажатия на кнопку “назад” в Navigation bar
- Создать ассерты на:
    - элемент выделен
    - placeholder в textField равен текстовому значению
    - элемент отображается на экране

**Полезные материалы:**

- [Статья о том как взаимодействовать с ui-элементами iOS приложения в тестах](https://habr.com/ru/company/vivid_money/blog/538708/)
- [Xcode UI Testing Cheat Sheet](https://www.hackingwithswift.com/articles/148/xcode-ui-testing-cheat-sheet)
- [XCUITests — Set Date Time or Select value from Picker view](https://medium.com/quality-engineering-university/xcuitests-set-date-time-or-select-value-from-picker-view-58570727390)

## Урок 4

**Цель: научиться работать с жизненным циклом приложения во время прогона тестов**

**Задание:**

- Открывать при старте приложения Safari
- Добавить launch argument и environment
- Сбросить любой пирмишен перед стартом приложения
- Использовать все методы жизненного цикла(setUp, tearDown и.т.д)

**Полезные материалы:**

- [Погружение в автотестирование на iOS. Часть 3. Жизненный цикл iOS приложения во время прогона тестов](https://habr.com/ru/company/vivid_money/blog/544254/)
- [XCUITests — Mobile Web Testing Using Safari](https://medium.com/quality-engineering-university/xcuitests-mobile-web-testing-using-safari-2416dc5fe758)
- [XCUITests — Pass Launch Arguments to the Target Application](https://medium.com/quality-engineering-university/xcuitests-pass-launch-arguments-to-the-target-application-3e6fa80d463b)

## Урок 5

**Цель: научиться использовать задержки**

- Написать явную задержку
- Написать неявную задержку используя:
    1. XCTNSPredicateExpectation
    2. XCTWaiter
    3. XCTDarwinNotificationExpectation***
    4. XCTNSNotificationExpectation***
    5. XCTKVOExpectation***

**Полезные материалы:**

- [Погружение в автотестирование на iOS. Часть 4. Ожидания в XCUITest](https://habr.com/ru/company/vivid_money/blog/547422/)
- [XCUITests — Why & How to apply WAIT for element to fulfil Expectations?](https://medium.com/quality-engineering-university/xcuitests-why-how-to-apply-wait-for-element-e42ef300ca93)
- [Waits in XCUITest](https://alexilyenko.github.io/xcuitest-waiting/#waiting-is-essential)
- [Waiting in XCTest](https://masilotti.com/xctest-waiting/)
- [Clean waiting in XCUITest](https://sourcediving.com/clean-waiting-in-xcuitest-43bab495230f)

## Урок 6

**Цель: Научиться работать с патернами POM(Page object model) и DRY(Don’t repeat yourself)**

1. Создать папку для pages и tests
2. Создать базовые классы: CommonPage и CommonTest и вынести туда общую логику
3. Создать page для каждого экрана
4. Прописать в каждом page, объекты и методы взаимодействия с ними

**Полезная информация:**

- [Implementation of Page-Object-Model (POM) to XCUITest (Native iOS Testing) with Swift](https://medium.com/@gunesmes/implementation-of-page-object-model-pom-to-xcuitest-native-ios-testing-with-swift-9f16cbbe2590)
- [UI Testing using Page Object pattern in Swift](https://swiftwithmajid.com/2021/03/24/ui-testing-using-page-object-pattern-in-swift/)
- [Page Object in XCTest UI Tests](https://alexilyenko.github.io/xcuitest-page-object/)
- [Introducing Page Object Pattern in iOS](https://medium.com/wantedly-engineering/introducing-page-object-pattern-in-ios-74e46c664d26)
- [Writing DRY XCUITest Tests With Base Classes](https://bitbar.com/blog/writing-dry-xcuitest-tests-with-base-classes/)

## Урок 7

**Цель: написать ui-тесты и сгруппировать их**

1. покрыть ui-тестами каждый экран приложения не менее 2 тестов на экран.
2. создать тест план для группировки тестов:
    1. Из таргета с тестами
    2. Пустой тест план и наполнить его тестами
3. изменить конфигурацию тест плана
    1. переопределить launch arguments и launch environment для тестов
    2. измените геолокацию, регион и язык для тестов
4. создать несколько настроек для тест плана(например: настройки для регрессионого прогона, для прогона на испанском языке и.т.д)

**Полезные материалы:**

- [WWDC19: Приступим к работе с Test Plan для XCTest](https://habr.com/ru/company/tinkoff/blog/457108/)
- [Get the Most Out of UI Tests With XCode Test Plans](https://medium.com/trendyol-tech/get-the-most-out-of-ui-tests-with-xcode-test-plans-d089a2252ba2)
- [Hands On XCTest Test Plans](https://ayaakl.medium.com/hands-on-xctest-test-plans-3e74924055d6)
- [XCUITests — Create Test Plan for Smoke, Regression suites](https://medium.com/quality-engineering-university/xcuitests-create-test-plan-for-smoke-regression-suites-56f8c37090e8)

# Advanced

## Урок 1

**Цель: научиться работать с Snapshot testing** 

1. Выбрать библиотеку для Snapshot testing:
    1. https://github.com/uber/ios-snapshot-test-case
    2. https://github.com/pointfreeco/swift-snapshot-testing
2. Реализовать метод:
    1. Создание скриншота всего экрана
    2. Создание скриншота отдельного элемента
3. Написать 1 снэпшот тест с полным скриншотом экрана и 1 с снэпшотом опред элемента

**Полезные материалы:**

- [Внедряем Snapshot testing в UI-тесты iOS](https://habr.com/ru/company/vivid_money/blog/569032/)
- [iOS snapshot testing](https://medium.com/@Apiumhub/ios-snapshot-testing-5084052fab7d)
- [Snapshot Testing Tutorial for SwiftUI: Getting Started](https://www.raywenderlich.com/24426963-snapshot-testing-tutorial-for-swiftui-getting-started)
- Automated Visual Testing With Snapshots(Part [1](https://medium.com/trendyol-tech/automated-visual-testing-with-snapshots-part-1-ee9c5cf58cca), [2](https://medium.com/trendyol-tech/automated-visual-testing-with-snapshots-part-2-19354052c6d9))
- Snapshot Testing. Testing the UI and Beyond (Part [1](https://medium.com/xmglobal/snapshot-testing-testing-the-ui-and-beyond-part-1-2369c9f84032),[2](https://medium.com/@ge.sotiropoulos/snapshot-testing-testing-the-ui-and-beyond-part-2-e56b0016d491),[3](https://medium.com/@ge.sotiropoulos/snapshot-testing-testing-the-ui-and-beyond-part-3-860bd9e175b8))
- [Snapshot XCUI Testing](https://joesusnick.medium.com/snapshot-xcui-testing-6a16c7ccd47b)

## Урок 2

**Цель: научиться внедрять мок сервер в свой проект**

1. Выбрать библиотеку для реализации мок сервера:
    1. https://github.com/tinkoff-mobile-tech/TinkoffMockStrapping
    2. https://github.com/httpswift/swifter
    3. https://github.com/envoy/Embassy
    4. https://github.com/Subito-it/SBTUITestTunnel
2. Пишем тест с использованием моков

**Полезные материалы:**

- [UI тесты в Xcode с Embassy и Succulent](https://habr.com/ru/company/otus/blog/412955/)
- [Network Stubbing options for XCTest and XCUITest in Swift](https://medium.com/xcblog/network-stubbing-options-for-xctest-and-xcuitest-in-swift-2e0dcce9a37d)
- [XCUITest (Swift) — Mock server setup for iOS automation with GraphQL](https://medium.com/@dilsreccse/ios-xcuitest-swift-automation-mock-server-setup-for-graphql-queries-3188f9526501)
- [Swift Localhost: Making XCUITest Great Again](https://medium.com/quick-code/swift-localhost-making-xcuitest-great-again-115d93954cf1)
- [Mocking network calls while UI Testing](https://medium.com/@Tovkal/mocking-network-calls-while-ui-testing-61e8a4a07f81)
- [Mocking API Calls in UI Tests](https://medium.com/trendyol-tech/mocking-api-calls-in-ui-tests-b908dbf6b305)
- [XCUITest Stubbing Network Calls](https://rlukasik.medium.com/xcuitest-stubbing-network-calls-c04cf69ddb7f)

## Урок 3

**Цель: научиться работать с ранерами и паралелить прохождение тестов**

1. Распаралелить автотесты в xcode
2. Выбрать раннер по душе:
    1. **[fastlane](https://docs.fastlane.tools/)**
    2. https://github.com/MarathonLabs/marathon
    3. https://github.com/avito-tech/Emcee
3. Написать скрипт для запуска тестов по:
    1. Схеме
    2. Тест плану
    3. Без компиляции проекта на основе существующей derived data
    4. Распаралелить автотесты используя CLI

**Полезные материалы:**

- [Ускоряем прохождение iOS UI-тестов. Часть 1. Запуск тестов без сборки проекта](https://habr.com/ru/company/vivid_money/blog/649901/)
- [Ускоряем прохождение iOS UI-тестов. Часть 2. Распараллеливание тестов](https://habr.com/ru/company/vivid_money/blog/652397/)
- [Creating a scheduled XCUITest(iOS) regression pipeline using GitLab](https://medium.nextlevelswift.com/create-scheduled-xcuitest-ios-regression-pipeline-on-gitlab-6df57af22b95)

## Урок 4

**Цель: научиться работать с CI запускать тесты  удаленно на билд агенте**

1. Выбираем ci на своё усмотрение:
    1. [Jenkins](https://www.jenkins.io/)
    2. [GitLab](https://about.gitlab.com/)
2. Создаем билд агент
3. На основании скриптов из прошлых уроков, создаем pipeline с запуском тестов

**Полезные материалы:**
