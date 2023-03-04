## Предисловие:

Этот курс создан для того, чтобы Manual QA *поняли*, как писать ui-тесты на iOS. 

Есть мнение, что если человек что-то понял, он автоматически *научился*. Не достаточно пройти 1 курс, который хорошо всё объясняет, и ты сразу можешь делать всё то, о чём там говорится. Чтобы человек научился что-то делать, он должен тренироваться - то есть что-то делать. “Читать” или “Слушать” - это не “делать”. 

Если хочешь научиться автоматизировать, нужно как можно чаще: писать и дебажить автотесты. Но просто делать тоже не достаточно. Нужно делать правильно, получая обратную связь. И будет круто, если у вас получится найти ментора, который поможет вам в этом

## **Требования к участникам программы:**

- Xcode версии ≥ 12
- Знание Swift на базовом уровне([SwiftBook](https://swiftbook.ru/) / [книжка Усова](https://www.ozon.ru/product/swift-osnovy-razrabotki-prilozheniy-pod-ios-ipados-i-macos-usov-vasiliy-aleksandrovich-usov-233893622/?sh=S9LQvPChHg))
- Знание Git на базовом уровне(checkout, merge, rebase, revert, git workflow,  branch)
- Пройти курс Raywenderlich: [iOS and SwiftUI for Beginners](https://www.raywenderlich.com/ios/paths/learn)
- Свой проект для покрытия автотестами

# Beginner

## Урок 1

**Цель: научить работать с github**

1. создать аккаунт на [github](https://github.com/);
2. настроить ssh ключ;
3. добавить проект в удаленный репозиторий, созданный в рамках прохождения курса “[iOS and SwiftUI for Beginners](https://www.raywenderlich.com/ios/paths/learn)”, либо добавьте свой проект;
4. отвести ветку, в которой будете выполнять задания.

**Полезная информация:**

- [Connecting to GitHub with SSH](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

## Урок 2

**Цель: научить работать с локаторами: проставлять, находить и хранить их**

1. проставить accessibilityidentifier в:
    - storyboard
    - viewController
    - content(SwiftUI)
2. найти accessibilityidentifier в объектах при помощи:
    - accessibility Inspector
    - debug view hierarchy
    - console(debugDescription)
    - test recorder
3. создать enum для хранения локаторов

**Полезные материалы:**

- [Погружение в автотестирование на iOS. Часть 1. Как работать с accessibilityidentifier объектов](https://habr.com/ru/company/vivid_money/blog/533180/)
- [Идентификаторы элементов в XCUITest](https://habr.com/ru/company/hh/blog/647889/)
- [How to find elements on XCUITest](https://medium.com/xcuitest/how-to-find-elements-on-xcuitest-e457eb030353)
- [Easily manage accessibility attributes and accessing UI elements with XCTest on iOS](https://medium.com/super-dispatch/easily-manage-accessibility-attributes-and-accessing-ui-elements-with-xctest-on-ios-bb76b57f6a7d)
- [XCUITests — Best Practices for Organizing Locators with Swift Enumerations](https://medium.com/quality-engineering-university/xcuitests-best-practices-for-organizing-locators-with-swift-enumerations-452da45fe7d5)

## Урок 3

**Цель: научить взаимодействовать с ui-элементами в автотестах**

1. создать методы нажатия на элементы, которые нажимают по:
    - accessibilityidentifier
    - индексу элемента
    - координатам
    - по определенному лейблу в элементе(использовать NSPredicate)
2. создать метод закрытия алерта
3. создать метод нажатия на кнопку “назад” в Navigation bar
4. создать ассерты на:
    - элемент выделен
    - placeholder в textField равен текстовому значению
    - элемент отображается на экране

**Полезные материалы:**

- [Статья о том как взаимодействовать с ui-элементами iOS приложения в тестах](https://habr.com/ru/company/vivid_money/blog/538708/)
- [Xcode UI Testing Cheat Sheet](https://www.hackingwithswift.com/articles/148/xcode-ui-testing-cheat-sheet)
- [XCUITests — Set Date Time or Select value from Picker view](https://medium.com/quality-engineering-university/xcuitests-set-date-time-or-select-value-from-picker-view-58570727390)

## Урок 4

**Цель: научиться работать с жизненным циклом приложения во время прогона тестов**

1. открыть при старте приложения Safari
2. добавить launch argument и environment
3. сбросить любой пирмишен перед стартом приложения
4. использовать все методы жизненного цикла(setUp, tearDown и.т.д)

**Полезные материалы:**

- [Погружение в автотестирование на iOS. Часть 3. Жизненный цикл iOS приложения во время прогона тестов](https://habr.com/ru/company/vivid_money/blog/544254/)
- [XCUITests — Mobile Web Testing Using Safari](https://medium.com/quality-engineering-university/xcuitests-mobile-web-testing-using-safari-2416dc5fe758)
- [XCUITests — Pass Launch Arguments to the Target Application](https://medium.com/quality-engineering-university/xcuitests-pass-launch-arguments-to-the-target-application-3e6fa80d463b)

## Урок 5

**Цель: научиться использовать задержки**

1. написать неявную задержку
2. написать явную задержку используя:
    - XCTNSPredicateExpectation
    - XCTWaiter
    - XCTDarwinNotificationExpectation*
    - XCTNSNotificationExpectation*
    - XCTKVOExpectation*
    
> Задачка со звездочкой: эти классы редко используются в задержках, но знакомство с ними может быть сильно полезным

**Полезные материалы:**

- [Погружение в автотестирование на iOS. Часть 4. Ожидания в XCUITest](https://habr.com/ru/company/vivid_money/blog/547422/)
- [XCUITests — Why & How to apply WAIT for element to fulfil Expectations?](https://medium.com/quality-engineering-university/xcuitests-why-how-to-apply-wait-for-element-e42ef300ca93)
- [Waits in XCUITest](https://alexilyenko.github.io/xcuitest-waiting/#waiting-is-essential)
- [Waiting in XCTest](https://masilotti.com/xctest-waiting/)
- [Clean waiting in XCUITest](https://sourcediving.com/clean-waiting-in-xcuitest-43bab495230f)

## Урок 6

**Цель: Научиться работать с патернами POM(Page object model) и DRY(Don’t repeat yourself)**

1. создать папку для pages и tests
2. создать базовые классы: CommonPage и CommonTest и вынести туда общую логику
3. создать page для каждого экрана
4. прописать в каждом page, объекты и методы взаимодействия с ними

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
    - из таргета с тестами
    - пустой тест план и наполнить его тестами
3. изменить конфигурацию тест плана
    - переопределить launch arguments и launch environment для тестов
    - измените геолокацию, регион и язык для тестов
4. создать несколько настроек для тест плана(например: настройки для регрессионого прогона, для прогона на испанском языке и.т.д)

**Полезные материалы:**

- [WWDC19: Приступим к работе с Test Plan для XCTest](https://habr.com/ru/company/tinkoff/blog/457108/)
- [Get the Most Out of UI Tests With XCode Test Plans](https://medium.com/trendyol-tech/get-the-most-out-of-ui-tests-with-xcode-test-plans-d089a2252ba2)
- [Hands On XCTest Test Plans](https://ayaakl.medium.com/hands-on-xctest-test-plans-3e74924055d6)
- [XCUITests — Create Test Plan for Smoke, Regression suites](https://medium.com/quality-engineering-university/xcuitests-create-test-plan-for-smoke-regression-suites-56f8c37090e8)

# Advanced

## Урок 1

**Цель: научиться работать с Snapshot testing** 

1. выбрать библиотеку для Snapshot testing:
    - https://github.com/uber/ios-snapshot-test-case
    - https://github.com/pointfreeco/swift-snapshot-testing
2. реализовать метод:
    - создание скриншота всего экрана
    - создание скриншота отдельного элемента
3. написать 1 снэпшот тест с полным скриншотом экрана и 1 с снэпшотом определенного элемента

**Полезные материалы:**

- [Внедряем Snapshot testing в UI-тесты iOS](https://habr.com/ru/company/vivid_money/blog/569032/)
- [iOS snapshot testing](https://medium.com/@Apiumhub/ios-snapshot-testing-5084052fab7d)
- [Snapshot Testing Tutorial for SwiftUI: Getting Started](https://www.raywenderlich.com/24426963-snapshot-testing-tutorial-for-swiftui-getting-started)
- Automated Visual Testing With Snapshots(Part [1](https://medium.com/trendyol-tech/automated-visual-testing-with-snapshots-part-1-ee9c5cf58cca), [2](https://medium.com/trendyol-tech/automated-visual-testing-with-snapshots-part-2-19354052c6d9))
- Snapshot Testing. Testing the UI and Beyond (Part [1](https://medium.com/xmglobal/snapshot-testing-testing-the-ui-and-beyond-part-1-2369c9f84032),[2](https://medium.com/@ge.sotiropoulos/snapshot-testing-testing-the-ui-and-beyond-part-2-e56b0016d491),[3](https://medium.com/@ge.sotiropoulos/snapshot-testing-testing-the-ui-and-beyond-part-3-860bd9e175b8))
- [Snapshot XCUI Testing](https://joesusnick.medium.com/snapshot-xcui-testing-6a16c7ccd47b)

## Урок 2

**Цель: научиться внедрять мок сервер в свой проект**

1. выбрать библиотеку для реализации мок сервера:
    - https://github.com/tinkoff-mobile-tech/TinkoffMockStrapping
    - https://github.com/httpswift/swifter
    - https://github.com/envoy/Embassy
    - https://github.com/Subito-it/SBTUITestTunnel
2. пишем любой тест с использованием моков

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

1. распаралелить автотесты в xcode
2. выбрать раннер по душе:
    - [fastlane](https://docs.fastlane.tools/)
    - [marathon](https://github.com/MarathonLabs/marathon)
    - [Emcee](https://github.com/avito-tech/Emcee)
3. написать скрипт для запуска тестов по:
    - схеме
    - тест плану
    - без компиляции проекта на основе существующей derived data
    - распаралелить автотесты используя CLI

**Полезные материалы:**

- [Ускоряем прохождение iOS UI-тестов. Часть 1. Запуск тестов без сборки проекта](https://habr.com/ru/company/vivid_money/blog/649901/)
- [Ускоряем прохождение iOS UI-тестов. Часть 2. Распараллеливание тестов](https://habr.com/ru/company/vivid_money/blog/652397/)
- [Creating a scheduled XCUITest(iOS) regression pipeline using GitLab](https://medium.nextlevelswift.com/create-scheduled-xcuitest-ios-regression-pipeline-on-gitlab-6df57af22b95)

## Урок 4

**Цель: научиться работать с CI запускать тесты  удаленно на билд агенте**

1. выбираем ci на своё усмотрение:
    - [Jenkins](https://www.jenkins.io/)
    - [GitLab](https://about.gitlab.com/)
2. создаем билд агент
3. на основании скриптов из прошлых уроков, создаем pipeline с запуском тестов

**Полезные материалы:**
- [Setting up GitLab CI for iOS projects](https://about.gitlab.com/blog/2016/03/10/setting-up-gitlab-ci-for-ios-projects/)
