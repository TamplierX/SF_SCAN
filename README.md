# СКАН

Клиентская часть веб-приложения для поиска публикаций о компании в СМИ по ИНН.

## Описание проекта

СКАН - это Single Page Application, разработанное на **React**, которое позволяет пользователям искать публикации о компаниях в средствах массовой информации, используя ИНН организации. Приложение включает систему аутентификации и защищенные маршруты.

## Установка и запуск

1. Установить зависимости:
`npm install`

2. Запустить проект:
`npm run start`

3. Открыть приложение в браузере:
`http://localhost:8080/`

## 🛠️ Технологический стек

- React
- Webpack (сборка проекта)
- React Router (маршрутизация)
- Context Api (управление состоянием)
- Axios (HTTP-клиент)

##  Структура проекта

```
src/
├── assets/      # Статические ресурсы
├── components/  # React компоненты
├── context/     # Хранилище состояния
├── http/        # API интеграции
├── services/    # Сервисные функции
├── styles/      # стили по умолчанию
└── utils/       # Вспомогательные утилиты
```

## Основные страницы

- Главная страница (/)
- Страница авторизации (/login)
- Страница поиска (/search) - защищенный маршрут
- Страница результатов (/results) - защищенный маршрут

Для доступа к защищенным маршутам (/search и /results) необходимо выполнить вход через страницу авторизации.

## 🌐 API Интеграция

Приложение взаимодействует с API по базовому URL: `https://gateway.scan-interfax.ru/api/v1/`

### Основные эндпоинты:

| Эндпоинт                  | Метод | Требует авторизации |
|---------------------------|-------|---------------------|
| /account/login            | POST  | Нет                 |
| /account/info             | GET   | Да                  |
| /objectsearch/histograms  | POST  | Да                  |
| /objectsearch             | POST  | Да                  |
| /documents                | POST  | Да                  |
