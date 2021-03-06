# Разбалловка Backend - 1 семестр

## 1. Вводное занятие - *11 баллов*

- Завести репозиторий на github - 1
- Создать стурктуру проекта - 1
- Установить новые версии NodeJS (8.*) и Python (3.*) - 2
- Создать виртуальное окружение для Python - 2
- Описать зависимости в requirements.txt и package.json - 1
- Создать простой Hello-World скрипт на Python - 2
- Создать правильный .gitignore файл - 1
- Оформить изменения в виде отдельных осмысленных коммитов - 1

## 2. Интенсив по Python - *12 баллов*

- Реализовать класс DoubleLinkedList на Python - 5
- Написать тесты (pytest) для класса - 4
- Проверить граничные условия в тестах - 1
- Проверить корректность и стиль кода с помощью pylint или flake8 - 2

## 3. Протокол HTTP - *12 баллов*

- Установить Nginx и Gunicorn - 1
- Настроить Nginx для отдачу статический файлов из public/ - 2
- Создать простейшее WSGI приложение и запустить его с помощью Gunicorn - 3
- Настроить проксирование запросов на Nginx - 2
- Измерить производительность Nginx и Gunicorn c помощью ab или wrk - 2
- Выполнить HTTP запрос с помощью curl и сохранить результат - 1
- Выполнить HTTP запрос с помощью telnet и сохранить результат - 1

## 4. Application Server - *11 баллов*

- Создать и запустить Flask проект - 3
- Реализовать "заглушки" для всех методов API, используя jsonify - 4
- Обрабтывать только нужные методы (GET/POST) - 1
- Написать тесты проверяющие работу (достаточно проверить) - 3

## 5. Работа с базой данных - *12 баллов*

- Установить Postgres и настроить доступ - 1
- Спроектировать базу данных проекта, сохранить в виде SQL скрипта - 3
- Написать модуль для работы с базой используя psycopg2 - 4
- Реализовать методы и тесты для: - 4
    - поиска пользователей
    - создание персонального чата
    - получение списка чатов

## 6. Реализация API - *10 баллов*

- Переработать API с использованием Flask-JSONRPC - 3
- Реализовать методы и тесты для: - 4
    - отправка сообщения
    - получение списка сообщений чата
    - прочтение сообщение
- Валидировать входные параметры API - 3

## 7. Авторизация в Web приложениях - *11 баллов*

- Реализовать обработчик для OAuth авторизации (используя authlib flask client) - 4
- Реальзовать декоратор проверяющий авторизацию при вызовах API - 4
- Изменить запросы и код API так что бы учитывался текущий пользователь - 3

## 8. Работа с файлами - *11 баллов*

- Реализовать метод API для загрузки файла в чат (использовать base64) - 3
- Использовать для хранения файла облачное S3 хранилище - 3
- Создать localtion в Nginx для раздачи загруженных файлов - 3
- Реализовать обработчик в приложении для проверки прав доступа к файлу - 2

## 9. Real-Time сообщения - *10 баллов*

- Установить Centrifugo - 2
- Настроить подключение к Centrifugo из Python используя requests - 4
- При добавлении сообщения в чат отправлять его всем участникам - 4
