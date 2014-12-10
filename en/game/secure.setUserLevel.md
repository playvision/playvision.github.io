---
title: secure.setUserLevel
---
Sets a user's level in the application

### Accepted parameters: ###

**user_id**: the ID of the user to update the level of<br>
**project_id**: your project's ID<br>
**level**: level value<br>
**time**: current unix-timestamp<br>
**sig**: generated signature, see [signature generation](/docs)<br>
**psid** - optional parameter. Game server ID. Required only if your application uses several servers<br>

###Example request###

> http://api.playvision.ru/v1/secure.setUserLevel?project_id=1&user_id=131&level=16&time=1409581492&sig=8955855380da9d1e3a9acf5a3cc1c9ce

###Returned data:###
If successful:
<pre>
    <code>
        {"status":1,"message":"success"}
    </code>
</pre>
If an error occurs:
<pre>
    <code>
        {"status":0,"message": "Error message"}
    </code>
</pre>