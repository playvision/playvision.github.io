---
title: friends.get
---

This method provides a means to get information about a user's friends.

###Accepted parameters###

**user_id**: the user ID to return a friends list for

###Example request###

> http://**domain**/v1/friends.get?user_id=100

### Returned data: ###
<pre>
<code>
{
    "response": {
        "count": 4,
        "items": [
            {
                "id": 119,
                "first_name": "Дмитрий",
                "nickname": "Diks",
                "last_name": "Столяров",
                "sex": 2,
                "city": "Санкт-Петербург",
                "country": "Россия",
                "photo_50": "http://playvision.ru/uploads/profiles/avatars/34/minimum_313cf2c.png",
                "photo_100": "http://playvision.ru/uploads/profiles/avatars/34/preview_313cf2c.png",
                "photo_200": "http://playvision.ru/uploads/profiles/avatars/34/medium_313cf2c.png"
            },
            {
                "id": 100,
                "first_name": "Няшный",
                "nickname": "sylpheed",
                "last_name": "Котя",
                "sex": 2,
                "city": "Underground",
                "country": "Alpha Centauri",
                "photo_50": "http://playvision.ru/uploads/profiles/avatars/15/minimum_0b53f8.png",
                "photo_100": "http://playvision.ru/uploads/profiles/avatars/15/preview_0b53f8.png",
                "photo_200": "http://playvision.ru/uploads/profiles/avatars/15/medium_0b53f8.png"
            },
            {
                "id": 27233,
                "first_name": "Виктория",
                "nickname": "Severinsday",
                "last_name": "",
                "sex": 1,
                "city": "St.Petersburg",
                "country": "Russia",
                "photo_50": "http://playvision.ru/uploads/profiles/avatars/27148/minimum_30ed85.jpg",
                "photo_100": "http://playvision.ru/uploads/profiles/avatars/27148/preview_30ed85.jpg",
                "photo_200": "http://playvision.ru/uploads/profiles/avatars/27148/medium_30ed85.jpg"
            },
            {
                "id": 85311,
                "first_name": "Кристина",
                "nickname": "Kristinya",
                "last_name": "Forever",
                "sex": 1,
                "city": "Малоархангельск",
                "country": "Россия",
                "photo_50": "http://playvision.ru/uploads/profiles/avatars/85222/minimum_a84d29d.jpg",
                "photo_100": "http://playvision.ru/uploads/profiles/avatars/85222/preview_a84d29d.jpg",
                "photo_200": "http://playvision.ru/uploads/profiles/avatars/85222/medium_a84d29d.jpg"
            }
        ]
    }
}
</code>
</pre>