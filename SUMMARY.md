# Язык программирования Rust

[Язык программирования Rust](title-page.md)  
[Предисловие](foreword.md)  
[Введение](ch00-00-introduction.md)

## Начало работы

- [Начало работы](ch01-00-getting-started.md)  
  - [Установка](ch01-01-installation.md)  
  - [Привет, мир!](ch01-02-hello-world.md)  
  - [Привет, Cargo!](ch01-03-hello-cargo.md)

- [Программирование игры «Угадай число»](ch02-00-guessing-game-tutorial.md)

- [Общие концепции программирования](ch03-00-common-programming-concepts.md)  
  - [Переменные и изменяемость](ch03-01-variables-and-mutability.md)  
  - [Типы данных](ch03-02-data-types.md)  
  - [Функции](ch03-03-how-functions-work.md)  
  - [Комментарии](ch03-04-comments.md)  
  - [Управление потоком](ch03-05-control-flow.md)

- [Понимание владения](ch04-00-understanding-ownership.md)  
  - [Что такое владение?](ch04-01-what-is-ownership.md)  
  - [Ссылки и заимствование](ch04-02-references-and-borrowing.md)  
  - [Срезы](ch04-03-slices.md)

- [Использование структур для организации связанных данных](ch05-00-structs.md)  
  - [Определение и создание экземпляров структур](ch05-01-defining-structs.md)  
  - [Пример программы с использованием структур](ch05-02-example-structs.md)  
  - [Синтаксис методов](ch05-03-method-syntax.md)

- [Перечисления и сопоставление с образцом](ch06-00-enums.md)  
  - [Определение перечисления](ch06-01-defining-an-enum.md)  
  - [Конструкция управления потоком `match`](ch06-02-match.md)  
  - [Компактное управление потоком с помощью `if let` и `let else`](ch06-03-if-let.md)

## Основы Rust

- [Управление растущими проектами с помощью пакетов, crate'ов и модулей](ch07-00-managing-growing-projects-with-packages-crates-and-modules.md)  
  - [Пакеты и crate'ы](ch07-01-packages-and-crates.md)  
  - [Определение модулей для управления областью видимости и приватностью](ch07-02-defining-modules-to-control-scope-and-privacy.md)  
  - [Пути для обращения к элементам в дереве модулей](ch07-03-paths-for-referring-to-an-item-in-the-module-tree.md)  
  - [Импорт путей с помощью ключевого слова `use`](ch07-04-bringing-paths-into-scope-with-the-use-keyword.md)  
  - [Разделение модулей по разным файлам](ch07-05-separating-modules-into-different-files.md)

- [Общие коллекции](ch08-00-common-collections.md)  
  - [Хранение списков значений с помощью векторов](ch08-01-vectors.md)  
  - [Хранение текста в кодировке UTF-8 с помощью строк](ch08-02-strings.md)  
  - [Хранение ключей с соответствующими значениями в хэш-таблицах](ch08-03-hash-maps.md)

- [Обработка ошибок](ch09-00-error-handling.md)  
  - [Необрабатываемые ошибки с `panic!`](ch09-01-unrecoverable-errors-with-panic.md)  
  - [Обрабатываемые ошибки с `Result`](ch09-02-recoverable-errors-with-result.md)  
  - [Паниковать или не паниковать](ch09-03-to-panic-or-not-to-panic.md)

- [Обобщённые типы, трейты и времена жизни](ch10-00-generics.md)  
  - [Обобщённые типы данных](ch10-01-syntax.md)  
  - [Трейты: определение общего поведения](ch10-02-traits.md)  
  - [Проверка ссылок с помощью времён жизни](ch10-03-lifetime-syntax.md)

- [Написание автоматических тестов](ch11-00-testing.md)  
  - [Как писать тесты](ch11-01-writing-tests.md)  
  - [Управление выполнением тестов](ch11-02-running-tests.md)  
  - [Организация тестов](ch11-03-test-organization.md)

- [Проект с вводом-выводом: создание программы командной строки](ch12-00-an-io-project.md)  
  - [Обработка аргументов командной строки](ch12-01-accepting-command-line-arguments.md)  
  - [Чтение файла](ch12-02-reading-a-file.md)  
  - [Рефакторинг для повышения модульности и обработки ошибок](ch12-03-improving-error-handling-and-modularity.md)  
  - [Разработка функциональности библиотеки с использованием TDD](ch12-04-testing-the-librarys-functionality.md)  
  - [Работа с переменными окружения](ch12-05-working-with-environment-variables.md)  
  - [Вывод сообщений об ошибках в stderr вместо stdout](ch12-06-writing-to-stderr-instead-of-stdout.md)

## Мышление на Rust

- [Функциональные возможности языка: итераторы и замыкания](ch13-00-functional-features.md)  
  - [Замыкания: анонимные функции с захватом окружения](ch13-01-closures.md)  
  - [Обработка последовательностей с помощью итераторов](ch13-02-iterators.md)  
  - [Улучшение нашего проекта ввода-вывода](ch13-03-improving-our-io-project.md)  
  - [Сравнение производительности: циклы против итераторов](ch13-04-performance.md)

- [Подробнее о Cargo и Crates.io](ch14-00-more-about-cargo.md)  
  - [Настройка сборок с помощью профилей релиза](ch14-01-release-profiles.md)  
  - [Публикация crate'а на Crates.io](ch14-02-publishing-to-crates-io.md)  
  - [Рабочие области Cargo (workspaces)](ch14-03-cargo-workspaces.md)  
  - [Установка бинарников из Crates.io с помощью `cargo install`](ch14-04-installing-binaries.md)  
  - [Расширение Cargo пользовательскими командами](ch14-05-extending-cargo.md)

- [Умные указатели](ch15-00-smart-pointers.md)  
  - [Использование `Box<T>` для хранения данных в куче](ch15-01-box.md)  
  - [Обращение с умными указателями как с обычными ссылками с помощью `Deref`](ch15-02-deref.md)  
  - [Выполнение кода при очистке с помощью трейта `Drop`](ch15-03-drop.md)  
  - [`Rc<T>` — умный указатель со счётчиком ссылок](ch15-04-rc.md)  
  - [`RefCell<T>` и шаблон внутренней мутабельности](ch15-05-interior-mutability.md)  
  - [Циклические ссылки могут приводить к утечке памяти](ch15-06-reference-cycles.md)

- [Бесстрашная многопоточность](ch16-00-concurrency.md)  
  - [Использование потоков для параллельного выполнения кода](ch16-01-threads.md)  
  - [Обмен сообщениями между потоками](ch16-02-message-passing.md)  
  - [Общий доступ к состоянию между потоками](ch16-03-shared-state.md)  
  - [Расширяемая многопоточность с трейтом `Send` и `Sync`](ch16-04-extensible-concurrency-sync-and-send.md)

- [Основы асинхронного программирования: async, await, future'ы и stream'ы](ch17-00-async-await.md)  
  - [Future'ы и синтаксис async](ch17-01-futures-and-syntax.md)  
  - [Применение параллелизма с async](ch17-02-concurrency-with-async.md)  
  - [Работа с произвольным числом future'ов](ch17-03-more-futures.md)  
  - [Stream'ы — последовательные future'ы](ch17-04-streams.md)  
  - [Подробнее о трейтах для async](ch17-05-traits-for-async.md)  
  - [Future'ы, задачи и потоки](ch17-06-futures-tasks-threads.md)

- [Объектно-ориентированные возможности Rust](ch18-00-oop.md)  
  - [Черты объектно-ориентированных языков](ch18-01-what-is-oo.md)  
  - [Использование объектов трейтов для значений разных типов](ch18-02-trait-objects.md)  
  - [Реализация ООП-паттерна](ch18-03-oo-design-patterns.md)

## Продвинутые темы

- [Шаблоны и сопоставление](ch19-00-patterns.md)  
  - [Где можно использовать шаблоны](ch19-01-all-the-places-for-patterns.md)  
  - [Опровержимость: может ли шаблон не сработать](ch19-02-refutability.md)  
  - [Синтаксис шаблонов](ch19-03-pattern-syntax.md)

- [Продвинутые возможности](ch20-00-advanced-features.md)  
  - [Небезопасный Rust](ch20-01-unsafe-rust.md)  
  - [Продвинутые трейты](ch20-02-advanced-traits.md)  
  - [Продвинутые типы](ch20-03-advanced-types.md)  
  - [Продвинутые функции и замыкания](ch20-04-advanced-functions-and-closures.md)  
  - [Макросы](ch20-05-macros.md)

- [Финальный проект: создание многопоточного веб-сервера](ch21-00-final-project-a-web-server.md)  
  - [Создание однопоточного веб-сервера](ch21-01-single-threaded.md)  
  - [Преобразование сервера в многопоточный](ch21-02-multithreaded.md)  
  - [Корректное завершение и очистка](ch21-03-graceful-shutdown-and-cleanup.md)

- [Приложения](appendix-00.md)  
  - [A – Ключевые слова](appendix-01-keywords.md)  
  - [B – Операторы и символы](appendix-02-operators.md)  
  - [C – Трейты, поддерживающие `derive`](appendix-03-derivable-traits.md)  
  - [D – Полезные инструменты разработки](appendix-04-useful-development-tools.md)  
  - [E – Редакции Rust](appendix-05-editions.md)  
  - [F – Переводы книги](appendix-06-translation.md)  
  - [G – Как создаётся Rust и «ночные» сборки](appendix-07-nightly-rust.md)
