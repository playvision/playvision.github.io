---
title: friends.getAppUsers
---

This method provides a means to get information about a user's friends who have launched the application

###Accepted parameters###

**user_id**: the user ID to return a friends list for<br/>
**project_id**: application ID

###Example request###

> http://api.playvision.ru/v1/friends.getAppUsers?user_id=111&project_id=1

### Returned data ###
<pre>
<code>
{"response":[103,92293,282314,283346,285935,285969,287598,289780]}
</code>
</pre>