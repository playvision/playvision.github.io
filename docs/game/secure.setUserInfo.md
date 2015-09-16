---
title: secure.setUserInfo
---
Обновляет данные пользователя в приложениии

### Принимаемые параметры: ###

**user_id**: id пользователя<br>
**project_id**: id вашего проекта<br>
**attribute**: имя атрибута<br>
**value**: значение атрибута<br>
**time**: текущий unix-timestamp<br>
**sig**: сгенерированная подпись см. [генерация подписи](/docs)<br>
**psid** - необязательный параметр. id игрового сервера. Необходимо передавать только в случае если у вашего приложения несколько серверов<br>

Список доступных атрибутов: name.

###Пример запроса###

> http://api.playvision.ru/v1/secure.setUserInfo?project_id=10&user_id=113&attribute=name&value=space_lord&time=1442394880&sig=c950f296873672646da425fd8b5396ca

###Возвращаемые данные:###
В случае успеха:
<pre>
    <code>
        {"status":1,"message":"success"}
    </code>
</pre>
В случае ошибки:
<pre>
    <code>
        {"status":0,"message":Сообщение об ошибке}
    </code>
</pre>
