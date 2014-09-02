---
title: Запросы к API
---

Для того чтобы вызвать метод API Playvision, Вам необходимо осуществить POST или GET запрос на указанный URL:

> http://playvision.ru/api/v1/**method_name**?**parameters**

**method_name** – название метода из списка функций API <br>
**parameters** – параметры соответствующего метода API

Пример ссылки:

> http://playvision.ru/api/v1/wall.post?user_id=131&project_id=1&token=fe4e4e2b3087bf7e22c139f06408d33f

##Генерация подписи##

Для совершения запросов с сервера к параметрам запроса должен быть добавлен параметр **sig**.
Параметр **sig** равен md5 от конкатенации следующих строк:

1. пар **parameter_name=parameter_value**, расположенных в порядке возрастания имени параметра (по алфавиту).<br>
2. секрета приложения **api_secret** (секрет Вы можете менять при редактировании страницы приложения).

<pre>
    <code>
        sig = md5(name1=value1name2=value2api_secret)
    </code>
</pre>
К примеру при запросе на обновление уровня

> http://playvision.ru/api/v1/secure.setUserLevel?project_id=1&user_id=131&level=16&time=1409581492&sig=81555196e23f9950c0d2780ce2274fc7

**sig** равен md5("level=16project_id=1time=1409581492user_id=131api_secret") то есть 81555196e23f9950c0d2780ce2274fc7
