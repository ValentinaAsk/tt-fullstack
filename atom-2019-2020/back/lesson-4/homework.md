Дз №4

1. Создать и запустить Django-проект

В том числе настроить директории, чтобы ваш проект выглядел примерно так:

<code>

messenger
    |---- users // директории приложений
    |---- chats
    |---- ...
    …
    |---- templates
    |---- static
    |---- manage.py
    |---- application
          |---- settings.py
          |---- urls.py
          |---- wsgi.py

 </code>


2. Реализовать "заглушки" для всех методов API, используя JsonResponse
	1) Профиль
	2) Список чатов
	3) Страница чата
	4) Список контактов

	5) метод, который должен возвращать html как начальную станицу вашего приложения

Для этого необходимо создать столько приложений, на сколько вы планируете логически разделить ваш проект, предполагаю, что их будет минимум 2
В каждом приложении должен быть файл urls.py с маршрутизацией внутри приложения, а также файл views.py для функций-обработчиков в каждом приложении
Все urls.py приложений должны быть подключены с помощью include в корневой urls.py проекта

3. Обрабатывать только нужные методы (GET/POST/...)

В функциях, прописанных в views.py нужно обрабатывать только http-метод, который соотвествует роли каждой функции.
В случае, если клиент запросил другой метод, нужно возвращать код ответа, обозначающий что метод не разрешен

