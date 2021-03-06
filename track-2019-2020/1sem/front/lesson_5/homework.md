# Домашнее задание 5

## Задание:
- Закрепить знания [React.js](https://reactjs.org/docs/getting-started.html)
  - Вспомнить, как мы разворачивали свое окружение для разработки [тут](https://github.com/track-mail-ru/lesson-5-samples) (но не использовать это при выполнении ДЗ, мы будем использовать `Create React App` для скорости)
  - Пройти [Tutorial](https://reactjs.org/tutorial/tutorial.html)
  - Изучить [Docs](https://reactjs.org/docs/hello-world.html)
  - [Скринкаст ч.1](https://cloud.mail.ru/public/aZA1/4B5U2JkYs)
  - [Скринкаст ч.2](https://cloud.mail.ru/public/5uoU/29Nosa19E)
- Изучить [Create React App](https://github.com/facebook/create-react-app)
- Обновить генератор **Инструкция к этому пункту находится ниже** <details>
  <summary>Как обновить генератор</summary>

  **Все последующие команды выполняем из-под `bash`.**
  1. Заходим в терминале в папку вашего проекта

  2. Обновляем глобально установленный генератор. Если ругается на недостаточные права, то выполнить с `sudo`:

  ```bash
  npm i -g generator-track-mail
  ```
  3. Проверяем версию установленного генератора. Должно получиться так (версия 0.4.3):
  ```
  $ npm list -g --depth 0 | grep track-mail
  ├── generator-track-mail@0.4.3
  ```

</details>

- Сгенерировать проект при помощи `generator-track-mail` **Инструкция к этому пункту находится ниже** <details>
  <summary>Как сгенерировать и обновить свой проект</summary>

  Ниже мы будем повторно проходить пункт из 1 ДЗ по генерации проекта.
  Генератор обновился, ваш базовый реактовый проект тоже должен получить эти изменения.
  1. Заходим в терминале в папку вашего проекта
  2. Выполняем генерацию проекта еще раз
  ```bash
  yo track-mail
  ```
  Будет тот же самый интерактивный режим, где вам будут задаваться вопросы. За одним исключением, там будут запросы на разрешение перезаписи файлов, нужно будет нажать `y` и нажать `enter`. Далее все как обычно. Процесс может занять некоторое время, но в итоге вы получите последние обновления проекта.

  3. Удаляем конфиг jest `rm jest.config.js`
  4. Удаляем из package.json скрипт `test:unit` и его запуск (`npm run test:unit`)

  **Если вы столкнулись с какой-то проблемой, генератор не работает или что-либо другое:**
  1. Создайте новую отдельную папку. Перейдите в нее
  2. Выполните шаги предыдущей инструкции с 1 по 2
  3. Вручную скопируйте все полученное содержимое в свой проект, соглашаясь на перезапись файлов
  4. Если генератор отказывается работать, у вас нет `bash` или существует какая-то другая проблема, которая не позволяет выполнить эти шаги, то нужно скачать [этот репозиторий](https://github.com/track-mail-ru/2019-2-Track-Frontend-M-Komitsky) и вручную скопировать его содержимое в свой проект. Обращаем внимание на изменения в `package.json`, нужно оставить свои старые контактные данные (поля `author`, `repository`, `homepage` и `description`). Если вы сдадите `PR` с моим именем, будет плохо :)

</details>

- Переписать компоненты на `React`
- Восстановить стили для всех компонентов
- Восстановить функциональность всех компонентов
- Приложение должно продолжать деплоиться, но теперь из корня

## Рекомендации к архитектуре вашего приложения
* То приложение, которое уже у вас получено при помощи генератора можно использовать как пример. Ненужные части нужно удалить
* Мы будем использовать для стилей `CSS Modules`. При особом желании используйте `Styled Components`, но разбираться придется самим
* Старайтесь везде использовать функциональные компоненты и `hooks api`, а не классовые
* Самый большой родительский компонент должен быть классовым (`extends React.Component`). В нем вы будете хранить глобальное состояние всего приложения
* ...

## Срок: 11 ноября

При сдаче ДЗ необходимо убедиться, что у вас без ошибок выполняется команда `npm run test`.
После создания пулл реквеста у вас проходит сборка проекта в трэвисе.
