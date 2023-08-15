# Разработка Интернет Приложений (РИП) 2023

Отчеты по лабораторным работам и ДЗ отправлять на почту `aikanev@bmstu.ru`

## [Видеозаписи лекций в youtube](https://youtube.com/playlist?list=PLLELLTvDgUQ9cpB1XzSuZ0mNSBkbjVNJ_)
#### Образ виртуальной машины Linux [Ubuntu 20.04](https://github.com/iu5git/Standards/blob/main/Linux/Linux.md) для выполнения заданий курса 

## Лекции
### Бекенд
[Лекция 1. История Web, трехуровневая модель приложений, MVC](https://github.com/iu5git/web-2022/blob/main/lectures/web_intro.pdf) 

[Лекция 2. Методология Agile, состав команды. Диаграммы UML](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_2_Agile_UML.pdf)

[Лекция 3. Основы Web, шаблонизация, Django](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_3_Web_Django.pdf)

[Лекция 4. Базы данных, ER, PostgreSQL. ORM. Админка Django. Курсоры](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_4_Databases_Django_ORM.pdf)

[Лекция 5. Веб-сервис. Swagger. Микросервисы](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_5_Web_Service.pdf)

[Лекция 6. Работа в git. Примеры специализированных сервисов - S3, уведомления, очереди](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_6_Special_Services.pdf)

### Фронтенд
[Лекция 7. Введение в фронтенд и React](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_7_React_Introduction.pdf)

[Лекция 8. React, сборка, компоненты](/lectures/Lecture_8_React.pdf)

[Лекция 9. Redux, hooks](/lectures/Lecture_9_Redux.pdf)

[Лекция 10. Ajax, запросы на React. WebSocket](/lectures/Lecture_10_Ajax.pdf)

[Лекция 11. Авторизация, куки, хранилище сессий](/lectures/Lecture_11_Authorization.pdf) 

[Лекция 12. JWT. SSO](/lectures/Lecture_12_jwt.pdf) 

### Мобильные приложения

[Лекция 13. Общая лекция про мобильные приложения. PWA](/lectures/Lecture_13_PWA.pdf) 

[Лекция 14. Плюсы и минусы React Native. Сетевое взаимодействие на Swift](/lectures/Lecture_14_Swift.pdf) 

### Инфраструктура

[Лекция 15. Резюме, Tauri, Agile, DevOps](/lectures/Lecture_15_Deploy.pdf)

## Лабораторные работы
В рамках практических работ по курсу необходимо каждому разработать заявочную систему на услуги по своей предметной области. Система состоит из веб-сервиса, фронтенд приложения, нативного приложения и второго асинхронного сервиса.

У каждого своя предметная область на весь курс: бронирование отелей, билетов в театр/кинотеатр, онлайн-магазин по вариантам, тему выбирать из списка ниже. По каждой теме есть ключевой процесс, в котором `пользователь` оформляет `заявки` на `услуги`. Также есть `модератор`, который может редактировать список `услуг` и одобрять `заявки`. От предметной области зависят: названия ролей пользователей, названия сущностей `услуг` и `заявок`, список полей для них, возможные статусы и изменяемые в них поля. В `нативном приложении` нужно реализовать интерфейс `гостя` - только просмотр `услуг`.

Основной вариант лабораторных по бэкенду - это Django и `Go`. Но можно выполнять также на `Java`, `C#` и `Node.js`, при выполнении условия лабораторных работ. Для фронтенда только `React`+`Redux`+`axios`+`React-Bootstrap`

Каждая лабораторная - это `sprint`, этап разработки по `agile`. Каждая работа демонстрируется и защищается отдельно. При защите необходимо продемонстрировать работу приложения по своей теме, UML диаграмму (из `StarUML`), репозиторий github с кодом и ответить на вопросы. По первому модулю необходимо также сделать ТЗ, а по второму отчет по курсу - РПЗ.

* [Примеры UML и ER диаграмм](/tutorials/homework)

## Лабораторные 2023

#### Лабораторная 1 

- **Цель работы**: выбор варианта-темы на весь курс, знакомство с разработкой бэкенда и разработка базового дизайна 
- **Порядок показа**: показать две страницы приложения, объяснить шаблоны, контроллеры этих страниц и коллекцию данных
- **Контрольные вопросы**: MVC, Django/Go, шаблонизация, HTTP, Web, HTML
- **Задание**: Базовая шаблонизация в Django (для Go просто HTML) для `услуг`

Создание базового интерфейса, состоящего из двух страниц. Первая для просмотра списка `услуг` (отели, товары, рейсы и тд) в виде карточек с наименованием, ценой и картинкой. При клике по карточке происходит переход на вторую страницу с подробной информацией об `услуге` (даты, описание и тд) 

В приложении должны быть использованы стили, для каждого элемента списка подгружается свое изображение. Все данные для обеих страниц нужно брать прямо из коллекции, без использования БД.

Добавить поле input для фильтрации списка `услуг` по выбранному полю (наименование, цена), отображаемых на странице (по умолчанию отображать все).

* [Инструкция по работе c Python](/tutorials/python/python.md)
* [Методические указания Django](/tutorials/lab1-py/lab1_tutorial.md)
* [Методические указания Golang](/tutorials/lab1-go/README.md)

#### Лабораторная 2

- **Цель работы**: разработка структуры базы данных и ее подключение к бэкенду 
- **Порядок показа**: показать панель администратора/adminer, добавить запись, посмотреть данные через select в БД, показать шаблоны страниц. Объяснить модели, контроллеры для созданных таблиц
- **Контрольные вопросы**: ORM, SQL, модель и миграции
- **ER диаграмма**: таблицы, связи, столбцы, типы столбцов и их длина, первичные, внешние ключи
- **Задание**: Создание базы данных `PostgreSQL` по теме работы, подключение к созданному шаблонизатору

Необходимо разработать структуру БД по выбранной теме и ее реализовать с учетом требований ниже. Использовать таблицу `услуг` в страницах разработанного приложения. Наполнить таблицы БД данными через `админку Django` или `Adminer`.

Для карточек таблицы `услуг` добавить кнопку логического удаления услуги (через статус) с помощью выполнения SQL запроса без ORM.

**Требования к БД**: 

Обязательно наличие 3 таблиц: `услуг`, `заявок` (статус, дата создания, дата формирования, дата завершения и `модератор`), `пользователей`

Обязательно наличие 5 или более статусов `услуг`: введён, в работе, завершён, отменён, удалён. Названия таблиц и их полей должны соответствовать предметной области.

* [Методические указания Django](/tutorials/lab2-py/lab2_tutorial.md)
* [Методические указания Golang](/tutorials/lab2-go/README.md)
* [Курс по основам БД](https://aiintro.docs.iu5edu.ru/docs/db/)

#### Лабораторная 3

- **Цель работы**: создание веб-сервиса в бэкенде для использования его в `SPA`
- **Порядок показа**: выполнить GET списка, сделать POST новой записи, показать новые данные через select. Объяснить модели, сериализаторы, контроллеры, роутеры для методов веб-сервиса
- **Контрольные вопросы**: веб-сервис, микросервисы, REST, RPC
- **Диаграмма классов** с детализацией бэкенда (домены методов по `url` с интерфейсами, модели, таблицы БД) + insomnia/postman
- **Задание**: Создание веб-сервиса со всей итоговой бизнес логикой, но без авторизации, подключение его к БД и тестирование в `insomnia`/`swagger`/`postman`

Создание **веб-сервиса** для получения/редактирования данных из вашей БД. Для изображений `услуг` использовать `Minio` или хранение файлов картинок в бинарном виде в БД.

Требуется разработать все методы для реализации итоговой бизнес логики вашего приложения. Методы и `url` в `API` должны соответствовать `REST`. Для списка `услуг` и `заявок` нужно предусмотреть фильтрацию на бэкенде. Для логических действий в приложении (оплата, подтверждение, завершение) предусмотреть отдельные методы для обновления конкретных полей.

* [Методические указания DRF](/tutorials/lab3-py/lab3_tutorial.md)
* [Методические указания Golang](/tutorials/lab3-go/README.md)

#### Лабораторная 4

- **Цель работы**: Разработка базового SPA на React
- **Порядок показа**: показать две страницы фронтенда в браузере, внести изменения в БД, показать их во фронтенде. Объяснить код компонентов, передаваемые props, вызовы fetch.
- **Контрольные вопросы**: react, props, компонент, элемент, состояние, хуки, жизненный цикл компонента
- **Deployment диаграмма** узлы: фронтенда, веб-сервиса, базы данных, web-сервера со статикой. Узлы соединить протоколами, компоненты фронтенда и бэкенда поместить в узлах, указать API между ними.
- **Задание**: Разработать две страницы фронтенд приложения на `React`, `TS` и подключить его к веб-сервису. Подготовить ТЗ на итоговую систему. 

Разработать базовый интерфейс приложения на `React` для `гостя`, аналогичный двум страницам из лабораторной работы №1 для просмотра `услуг`. Использовать компоненты `React-Bootstrap`. Необходимо развернуть фронтенд на `GitHub Pages`.

В приложении должна быть навигационная панель `navbar` для списка базовых страниц, а также навигационной цепочки `breadcrumbs`, где отображается путь от базовой страницы к текущей. 

Содержимое карточек получать из веб-сервиса лабораторной №3. Ajax-запросы написать самостоятельно через `fetch`. Ограничение с `CORS` решить через проксирование `React`. В методах `fetch` предусмотреть получение данных из коллекции с `mock`-объектами при отсутствии доступа к вашему бэкенду (если он не поддерживает `HTTPS`).

* [Методические указания](/tutorials/lab4/lab4_tutorial.md). Переделать на TS
* [Progressive Web App и адаптивный дизайн](/tutorials/pwa/PWA.md)

**ТЗ** на итоговую систему:
- цель
- назначение - краткое описание для чего, кто работает в системе
- задачи
- методы веб-сервиса таблицей с группировкой по доменам: метод, url, описание, входные, выходные данные
- Описание UI - список окон и какие действия для каких групп пользователей доступны. Указать, какие методы бэкенда при этом вызываются.
- требования к аппаратному обеспечению для сервера и клиента
- требования к программному обеспечению с версиями для серверных компонентов и для клиента

#### Лабораторная 5

Добавление авторизации в веб-сервис. Сразу с Permissions. Показ бизнес-процесса через swagger. +HTTPS?

* [Настройка через WSL](https://github.com/iu5git/Networking/tree/main/kafka_wsl)
* [Методические указания DRF Redis](https://github.com/iu5git/web-2022/blob/main/tutorials/lab7-py/lab7_tutorial.md)
* [Методические указания Golang JWT](https://github.com/iu5git/web-2022/tree/main/tutorials/lab7-go/README.md)

**Sequence диаграмма**: `AJAX` запросы по бизнес-процессу

#### Лабораторная 6

Редакс для смены состояния-авторизации во фронте, корзина (конструктор заявки) и кнопка записи на услуги. Еще одно окно Список заявок (история). Сначала редакс и axios для get услуг. Потом для всего остального через кодогенерацию swagger-типы

* [Методические указания Redux](/tutorials/lab5/lab5_tutorial.md)
* [Методические указания Axios](/tutorials/lab6/lab6_tutorial.md)

**Диаграмма классов** с детализацией бэкенда и фронтенда: все компоненты системы с интерфейсами, выделить сервисы и интерфейсы данных и авторизации

#### Лабораторная 7

Создание нативного простого приложения с подключением API: мобильное или Tauri, Qt для интерфейса гостя без авторизации.

* [Методические указания iOS (Swift)](https://github.com/iu5git/web-2022/blob/main/tutorials/ios_tutorial/ios_tutorial.md)
* [Методические указания Android (Java)](https://github.com/iu5git/web-2022/blob/main/tutorials/android_tutorial/android_tutorial.md)
* [Методические указания React Native + Redux Toolkit](/tutorials/react-native/react_native.md)
* [Методические указания Tauri](/tutorials/tauri/)
* Qt

**Activity диаграмма/BPMN** для итогового бизнес-процесса для ДЗ: описание бизнес-процесса, разделение на дорожки по ролям пользователей, действия соответствуют операциям пользователей в вашей системе.

#### Лабораторная 8

Создание второго простого асинхронного сервиса (на другом языке, кто делал на Django - Go и наоборот) на grpc. Вычисления, моделирование, оплата. У каждого сервиса по 1 gprc методу

#### Домашнее Задание

Интерфейс модератора добавить в основную систему React:
- добавление новых услуг таблицей (обязательные и необязательные поля), редактирование, удаление
- Список заявок с селекторами для смены статуса

**Отчет-РПЗ** по всем лабораторным и ДЗ:
1. **Введение** (актуальность, цель, назначение, требования, задачи)
2. **Бизнес-процесс**. Описание предметной области. Диаграмма прецедентов, диаграмма состояний и деятельности/BPMN
3. **Архитектура**. Диаграммы развертывания, ER с назначением таблиц и диаграмма классов с детализацией бэкенда и фронтенда
4. **Алгоритмы**. Диаграмма последовательности HTTP запросов
5. **Описание интерфейса**. Перечень окон, их назначение и выполняемые пользователями действия
6. **Заключение**
7. **Список использованных источников**  
8. **Приложение. Техническое задание**

#### Дополнительные задания
1. индексы в БД, большое количество `услуг` (> 100000) и пагинация (+4 балла)
2. адаптивность дизайна (+2 балла)
2. swagger и кодогенерация (+2 балла)

### Темы 2023:
1. Система заявок на вычисления: факториал, НОД и тд. `Услуги` - виды вычислений, `заявки` - запрос с входными данными и результатами.
2. Система заявок на моделирование: имитационное/аналитическое моделирование потоков метро и тд. `Услуги` - виды моделирования, `заявки` - запрос с входными данными и результатами.
3. Система заявок для поваров в быстром питании на приготовление. `Услуги` - виды блюд, `заявки` - заявки на приготовление на нужный заказ.
3. Система заявок на производстве
4. Заявки от коллцентра мелкого бизнеса: менеджер-создатель заявки, исполнитель+курьер. `Услуги` - услуги данного бизнеса, `заявки` - заявки от клиентов на услуги.
5. Заявки контроля маршрута беспилотных летательных аппаратов. `Услуги` - районы города, `заявки` - заявки на пролет объекта в данной районе в определенное время.
6. Контроль нарушений ПДД самокатами и др средств индивидуальной мобильности с двигателем. `Услуги` - виды нарушений и штрафы для них, `заявки` - факты нарушения из средств фиксации
7. Заявки на переходы космических аппаратов на различные орбиты. `Услуги` - доступные орбиты, `заявки` - заявки на переход спутников на орбиту.
8. Визовый центр РФ - заявки на визы. `Услуги` - виды виз, `заявки` - заявки на получение нужной визы.
9. Автоматический контроль паспортов на границе. `Услуги` - паспорта, которые заведены в системе, `заявки` - факты пересечения границы по паспорту
10. Заявки на доставку грузов на Марс на Starship. `Услуги` - товары, доставляемы на Марс на Starship, `заявки` - заявки на конкретный объем товаров

11. Отчеты по добыче ресурсов (вода, углекислый газ, гелий и тд) на Луне. `Услуги` - добываемые ресурсы, `заявки` - месячные отчеты об объеме добычи в конкретном месте Луны
12. Трудоустройство женщин в отпуске по уходу за ребенком. `Услуги` - вакансии для женщин с детьми, `заявки` - подача заявок на вакансии от женщин
13. Система трудоустройства для инвалидов. `Услуги` - вакансии для инвалидов, `заявки` - подача заявок на вакансию от инвалидов
14. Система социальной помощи инвалидам - доставка еды, сопровождение на мероприятие и тд. `Услуги` - оказываемые услуги, `заявки` - заявки на них от инвалидов
15. История ВОВ - участники ВОВ и их привязка к архивным документам (личные карточки, наградные, ЖБД итд). `Услуги` - архивные документы, `заявки` - привязка участника с наградой/событием к документу
16. Система археологов - находки и их привязка к раскопкам. `Услуги` - места археологических раскопок, `заявки` - факты находок предметов с группировкой по экспедиции

## Лабораторные 2022

* [Задания 2022 года](2022.md)

## Вопросы к экзамену и РК (примерные)
1. Опишите шаблон MVC, структуру и назначение компонентов.
2. Опишите схему, как реализован шаблон MVC в фреймворке Django.
3. Что такое Django? Его назначение и возможности.
4. Что такое шаблонизация Django? Приведите примеры.
5. Опишите протокол HTTP. Схему работы и основные понятия.
6. Опишите стек протоколов интернета TCP/IP.
7. Перечислите основные составляющие web и опишите их.
8. Что такое HTML, CSS? Приведите примеры.
9. Что такое URI? Опишите элементы URI для HTTP.
10. Виды баз данных. Приведите примеры и отличия.
11. Объясните назначение ORM, ее составляющие. Укажите преимущества и недостатки ORM.
12. Что такое модель и миграция?
13. Укажите группы SQL запросов, их примеры и назначение.
14. Что такое веб-сервис? Отличие от веб-сервера.
15. Что такое Web API? Назначение и применение.
16. Микросервисная архитектура. Отличия от монолитной архитектуры.
17. Перечислите требования REST, опишите их.
18. Что такое RPC? Варианты RPC и их отличия.
19. Что такое Swagger? Назначение и использование.
20. Что такое AJAX? Схема работы и назначение.
21. Назначение JSON и XML. Примеры и отличия.
22. Что такое git? Опишите схему работы с ветками GitHub.
1. Методология разработки Agile. Состав IT команды.
2. Перечислите основные диаграммы UML и их назначение.
3. Что такое Web реального времени? Что такое WebSocket?
4. Укажите отличия XmlHttpRequest и fetch. Приведите примеры.
5. Перечислите отличия Axios от fetch. Приведите примеры.
6. Что такое React? Что такое компонент, его состояния и свойства.
7. Структура React проекта. Назначение Babel и WebPack.
8. Жизненный цикл React компонента.
9. Назначение хуков useState и useEffect.
10. Назначение хуков useContext и useReducer.
11. Опишите схему работы менеджера состояний Redux.
12. Опишите работу Redux на диаграмме последовательности.
13. Какие параметры передаются при создании Store? Их назначение.
14. Что такое Cors? Укажите варианты решения.
15. Что такое Redis? Его назначение и варианты применения.
16. Опишите схему авторизации с помощью JWT.
17. Опишите схему авторизации с помощью сессий.
18. Что такое авторизация и аутентификация? Укажите варианты авторизации и их отличия.
19. Что такое SSO? Схема работы.
20. Протокол OAuth. Схема работы.
21. Отличия мобильных и веб-приложения. Языки и технологии для разработки мобильных приложений.
22. Что такое pwa? Отличия от других вариантов приложений.
23. Плюсы и минусы разработки на React Native.
24. Назначение фреймворков Electron и Tauri. Их отличия.
25. Опишите этапы подхода DevOps. Назначение GitHub Pages.

#### Команда курса выражает благодарность за помощь в подготовке материалов для данного курса
