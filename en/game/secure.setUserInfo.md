---
title: secure.setUserInfo
---
Updates an user's data in the application

### Accepted parameters: ###

**user_id**: user ID<br>
**project_id**: your project's ID<br>
**attribute**: attribute name<br>
**value**: attribute value<br>
**time**: current unix-timestamp<br>
**sig**: generated signature, see [signature generation](/docs)<br>
**psid** - optional parameter. Game server ID. Required only if your application uses several servers<br>

Available attributes: name.

###Example request###

> http://api.playvision.ru/v1/secure.setUserInfo?project_id=10&user_id=113&attribute=name&value=space_lord&time=1442394880&sig=c950f296873672646da425fd8b5396ca

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
