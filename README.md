#Чтобы создать новый проект на основе этого шаблона с помощью degit
Используйте команды

```bash
npx degit datletik/app datletik-app
cd datletik-app
```

*Обратите внимание, что вам нужно установить Node.js.*


## Установка Node.js


```bash
cd datletik-app
npm install
```

...Для разработчиков::

```bash
npm run dev
```

Перейдите на localhost:8080. Вы должны увидеть работающее приложение. Отредактируйте файл компонента в src, сохраните его и перезагрузите страницу, чтобы увидеть изменения.

По умолчанию сервер будет отвечать только на запросы с localhost. Чтобы разрешить подключения с других компьютеров, отредактируйте команды sirv в package.json и добавьте опцию --host 0.0.0.0.

Если вы используете Visual Studio Code, мы рекомендуем установить официальное расширение datletik для VS Code. Если вы используете другие редакторы, вам может потребоваться установить плагин, чтобы получить подсветку синтаксиса и интеллисенс.

## Сборка и запуск в режиме продакшн
Чтобы создать оптимизированную версию приложения::

```bash
npm run build
```

Вы можете запустить только что созданное приложение с помощью npm run start. Это использует sirv, который включен в зависимости вашего package.json, чтобы приложение работало при развертывании на платформах, таких как Heroku.


## Режим одностраничного приложения


По умолчанию sirv будет отвечать только на запросы, которые соответствуют файлам в public. Это для максимальной совместимости со статическими файловыми серверами, позволяющими развернуть ваше приложение где угодно.

Если вы создаете одностраничное приложение (SPA) с несколькими маршрутами, sirv должен быть способен отвечать на запросы для любого пути. Вы можете это сделать, отредактировав команду "start" в package.json:

"start": "sirv public --single"
Использование TypeScript
