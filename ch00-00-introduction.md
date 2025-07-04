# Введение

> Примечание: это издание книги идентично версии [The Rust Programming Language][nsprust], доступной в печатном и электронном формате от [No Starch Press][nsp].

[nsprust]: https://nostarch.com/rust-programming-language-2nd-edition  
[nsp]: https://nostarch.com/

Добро пожаловать в _The Rust Programming Language_ — вводную книгу о Rust. Язык программирования Rust помогает создавать более быстрые и надёжные приложения. Часто в проектировании языков программирования приходится выбирать между удобством высокого уровня и возможностями низкоуровневого управления. Rust бросает вызов этому компромиссу. Сочетая мощные технические возможности и отличное качество работы для разработчика, Rust даёт вам контроль над деталями (например, использованием памяти) без традиционных неудобств.

## Кому подходит Rust

Rust подойдёт многим — по самым разным причинам. Ниже перечислены ключевые группы пользователей.

### Команды разработчиков

Rust отлично зарекомендовал себя как инструмент для продуктивной работы в больших командах, где у участников разный уровень подготовки в системном программировании. Низкоуровневый код подвержен множеству тонких ошибок, которые в других языках выявляются только при обширном тестировании и тщательном ревью. В Rust роль защитника играет компилятор: он просто не позволит собрать код с подобными ошибками, включая ошибки конкурентности. Вместо того чтобы тратить силы на отладку, команда может сосредоточиться на логике приложения.

Rust также приносит современные инструменты в мир системного программирования:

- **Cargo** — встроенный менеджер зависимостей и сборщик — упрощает подключение библиотек, компиляцию и управление зависимостями во всей экосистеме Rust.
- **Rustfmt** — инструмент форматирования, который обеспечивает единый стиль кода среди всех разработчиков.
- **rust-analyzer** — предоставляет автодополнение, подсказки и сообщения об ошибках прямо в редакторе.

Используя эти и другие инструменты Rust, разработчики могут эффективно писать код системного уровня.

### Студенты

Rust подходит студентам и всем, кто хочет изучать системные концепции. С его помощью многие изучают такие темы, как разработка операционных систем. Сообщество Rust дружелюбно и всегда готово помочь. Одной из целей книги и всей команды Rust является сделать системные темы доступными для большего числа людей — особенно для тех, кто только начинает программировать.

### Компании

Сотни компаний — как крупных, так и небольших — используют Rust в продакшене для самых разных задач: командные утилиты, веб-сервисы, инструменты DevOps, встраиваемые устройства, анализ и обработка аудио/видео, криптовалюты, биоинформатика, поисковые системы, IoT, машинное обучение и даже важные компоненты браузера Firefox.

### Разработчики Open Source

Rust — для тех, кто хочет развивать сам язык, сообщество, инструменты и библиотеки. Если хотите — присоединяйтесь к работе над Rust!

### Любители скорости и стабильности

Rust — для тех, кому важны скорость и стабильность. Под скоростью понимается как высокая производительность программ, так и скорость разработки. Проверки компилятора гарантируют стабильность при добавлении фич и рефакторинге, в отличие от хрупкого легаси-кода в других языках, которого боятся касаться. Rust стремится к _абстракциям без потерь_: высокоуровневые фичи, которые компилируются в столь же быстрый код, как если бы вы писали его вручную. Безопасный код в Rust может быть и быстрым.

Rust поддерживает и многих других пользователей — перечисленные здесь лишь самые крупные категории. Главная цель языка — устранить традиционные компромиссы: безопасность _и_ продуктивность, скорость _и_ удобство. Попробуйте Rust и решите сами, подходит ли он вам.

## Кому предназначена эта книга

Мы предполагаем, что вы уже писали код на каком-либо языке, но неважно на каком именно. Мы постарались сделать материал доступным для широкого круга программистов. Мы почти не обсуждаем, что такое программирование как таковое. Если вы впервые знакомитесь с программированием, вам больше подойдёт книга, специально предназначенная для абсолютных новичков.

## Как пользоваться этой книгой

В целом книга предполагает последовательное чтение: главы построены друг на друге. Поздние главы развивают темы, затронутые ранее.

Книга состоит из двух типов глав: концептуальных и проектных. В концептуальных вы изучаете аспекты Rust, а в проектных — создаёте небольшие программы, применяя ранее полученные знания. Главы 2, 12 и 21 — проектные, остальные — концептуальные.

Глава 1 рассказывает, как установить Rust, написать «Hello, world!» и использовать Cargo. В Главе 2 вы сразу начнёте писать программу: игру “Угадай число”. Это вводный практический проект; подробности будут объяснены в следующих главах. Если хотите сразу начать писать — начинайте с Главы 2. Глава 3 рассказывает о знакомых конструкциях из других языков, а Глава 4 — об уникальной системе владения в Rust. Если вы предпочитаете изучать теорию до практики, можете сначала прочитать Главу 3, а затем вернуться к Главе 2, когда захотите применить знания.

Глава 5 — структуры и методы. Глава 6 — перечисления, конструкции `match` и `if let`. Вы научитесь создавать собственные типы.

Глава 7 — модульная система и правила видимости. Глава 8 — стандартные коллекции: векторы, строки, хеш-карты. Глава 9 — обработка ошибок.

Глава 10 — обобщения, трейты и времена жизни: они позволяют писать универсальный код. Глава 11 — тестирование: несмотря на гарантии безопасности, тесты нужны для проверки логики. В Главе 12 создаём свою версию утилиты `grep`, используя ранее изученные концепции.

Глава 13 — замыкания и итераторы (идеи из функциональных языков). Глава 14 — углублённо о Cargo и публикации библиотек. Глава 15 — умные указатели и трейты, обеспечивающие их поведение.

Глава 16 — модели конкурентности и как Rust делает многопоточность безопасной. Глава 17 — асинхронность: `async/await`, задачи, потоки и модель лёгкой параллельности.

Глава 18 — сравнение идиом Rust с принципами ООП. Глава 19 — паттерны и сопоставление с образцом. Глава 20 — расширенные темы: небезопасный Rust, макросы, времена жизни, трейты, типы, функции и замыкания.

В Главе 21 создаём многопоточный веб-сервер с низким уровнем доступа!

Приложения содержат справочную информацию:  
**Приложение A** — ключевые слова Rust  
**Приложение B** — операторы и символы  
**Приложение C** — автоматически реализуемые трейты  
**Приложение D** — полезные инструменты разработки  
**Приложение E** — редакции Rust  
**Приложение F** — переводы книги  
**Приложение G** — процесс разработки языка и ночные сборки

Читать книгу можно и не по порядку. Если что-то непонятно — возвращайтесь к нужной главе. Делайте так, как удобно вам.

<span id="ferris"></span>

Важная часть изучения Rust — умение читать сообщения об ошибках компилятора. Они помогают довести код до рабочего состояния. Мы приведём примеры, которые специально не компилируются, чтобы показать, какие ошибки выдает компилятор. Обратите внимание: если вы просто скопируете и запустите случайный пример, он может не сработать! Всегда читайте сопровождающий текст, чтобы понять, ожидается ли ошибка. Поможет вам и Феррис:

| Феррис                                                                                                           | Что значит                                        |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="Феррис с вопросом"/>                     | Этот код не компилируется!                        |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="Феррис в панике"/>                                 | Этот код вызывает панику (ошибку во время выполнения)! |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="Феррис пожимает лапами"/>            | Этот код не даёт желаемого результата.            |

Обычно после таких примеров мы покажем и их правильную версию.

## Исходный код

Файлы, из которых сгенерирована эта книга, доступны на [GitHub][book].

[book]: https://github.com/rust-lang/book/tree/main/src
