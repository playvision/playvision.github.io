---
title: friends.invite
---

После post-запроса на указанный ниже адрес у пользователя откроется модальное окно со списком его друзей, которые не играют в эту игру, где он сможет выбрать тех, кому хочет отправить приглашение.

###Принимаемые параметры###

**user_id**: id пользователя, который отправляет уведомление<br>
**project_id**: id вашего проекта<br>
**token**: токен пользователя, передаваемый в iframe<br>
**request_ids**: массив id друзей, которых пользователь хочет пригласить в игру

###Пример запроса###

> http://api.playvision.ru/v1/friends.invite?user_id=100&project_id=3&token=3aa6fa7280fd879275c425f10bda9412&request_ids=101,102

###Итог:###
Пользователь увидит модальное окно приглашения друзей, как показано на скриншоте ниже.

![окно приглашения в игру](/images/friends/invite.png "окно приглашения в игру")

Если среди request_ids будут id пользователей, которые уже играют в эту игру, то они не будут отображены в списке.
Если пользователь не указал request_ids, то сможет сам выбрать выбрать друзей, которым он хочет отправить приглашение, а затем нажать на кнопку "Отправить".
После этого выбранные друзья получат уведомление, как на скриншоте:

![уведомление](/images/friends/notification.png "уведомление")

