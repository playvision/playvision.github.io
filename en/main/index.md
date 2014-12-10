---
title: API requests
---

To call a Playvision API method, you must perform a POST or GET request to this URL:

> http://api.playvision.ru/v1/**method_name**?**parameters**

**method_name** – the name of a method from the API's list of functions <br>
**parameters** – the parameters of the corresponding API method

Example link:

> http://api.playvision.ru/v1/wall.post?user_id=131&project_id=1&token=fe4e4e2b3087bf7e22c139f06408d33f

##Signature generation##

To execute requests from the server, you must add the **sig** parameter.
The **sig** parameter is equal to an MD5 hash of the following lines concatenated:

1. the **parameter_name=parameter_value** pairs in ascending order by parameter name (alphabetical order).<br>
2. the application's **api_secret** parameter (you can change the secret when editing the application's page).

<pre>
    <code>
        sig = md5(name1=value1name2=value2api_secret)
    </code>
</pre>

An example request to update a level

> http://api.playvision.ru/v1/secure.setUserLevel?project_id=1&user_id=131&level=16&time=1409581492&sig=81555196e23f9950c0d2780ce2274fc7

**sig** is equal to md5("level=16project_id=1time=1409581492user_id=131api_secret") i.e. 81555196e23f9950c0d2780ce2274fc7
