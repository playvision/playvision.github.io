---
title: friends.invite
---

After sending post-request to the address below, a modal window opens at client side with list of user's friends available for invitation to the game. That is, those people who do not play this game.
###Parameters###

**user_id**: id of user who will invites his friends<br>
**project_id**: your project's ID<br>
**token**: token of user that is send in iframe<br>
**request_ids**: (optional) array of friends ids, which user wants to invite to the game

###Example###

> http://**domain**/v1/friends.invite?user_id=100&project_id=3&token=3aa6fa7280fd879275c425f10bda9412&request_ids=101,102

###Result:###
If request_ids are not specified, user will be able to choose from a list of friends, then click on the "Send" button. As shown in the screenshot below.
![invitation window](/images/friends/invite.png "Invitation window")

If request_ids are specified, these users will automatically be added to the list of candidates. The user has to press the "Send" button.

![invitation window](/images/friends/invite_request_ids.png "Invitation window")

After that, selected friends will be notified, as in the screenshot below:

![notify](/images/friends/notification.png "notify")

When entering the game via invitation the option referrer_id will be sent to the iframe. This is the id of the user who sent the invitation. Checking referrer_id remains on the side of the game.
