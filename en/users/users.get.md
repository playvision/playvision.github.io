---
title: users.get
---
Returns information about the requested users

### Accepted parameters: ###

**user_ids**: A list of user IDs separated by a comma. Data returns in the format:

###Example request###

> http://{{domain}}/v1/users.get?user_ids=100

### Returned data: ###
<pre>
    <code>
        {"response":[
            {"id":100,
            "first_name":"Няшный",
            "nickname":"sylpheed",
            "last_name":"Котя",
            "sex":2,
            "city":"Underground",
            "country":"Alpha Centauri",
            "photo_50":"http://playvision.ru/uploads/profiles/avatars/15/minimum_e470jjb53f8.png",
            "photo_100":"http://playvision.ru/uploads/profiles/avatars/15/preview_e470jjb53f8.png",
            "photo_200":"http://playvision.ru/uploads/profiles/avatars/15/medium_e470jjb53f8.png"}
        ]}
    </code>

</pre>
