---
title: request.window
---
Показывает пользователю окно для отправки уведомления другому пользователю от его имени.

### Принимаемые параметры: ###

**user_id**: id пользователя которому будет показан диалог<br>
**project_id**: id вашего проекта<br>
**token** – токен пользователя, переданный в параметрах приложения. См. [параметры приложения](/app)<br>
**request_user_id** - обязательный параметр. ID пользователя, которому будет отправлено сообщение от имени пользователя указанного у параметре **user_id**<br/>
**request_key** - произвольный дополнительный параметр который будет передан при открытии приложения.<br>
**message** - параметр, в котором будет содержаться текст сообщения.

###Пример запроса###

> http://api.playvision.ru/v1/request.window?user_id=100&project_id=1&token=fe4e4e2b3087bf7e22c139f06408d33f&request_user_id=119&request_key=some_string&message=test

[**<- Вернуться к основной документации**](/docs/notification)