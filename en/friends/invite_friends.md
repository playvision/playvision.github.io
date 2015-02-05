---
title: invite_friends
---

After sending post-request to the address below, a modal window opens  at client side with list of users friends, where will be ability to choose those friends, who user wants to send an invitation.
###Parameters###

**uid**: id of user who will invites his friends<br>
**token**: token of user that is send in iframe

###Example###

> http://api.playvision.ru/v1/invite_friends?uid=100&token=some_token

###Result:###
The user will see a modal window with ability to invite friends, as shown in the screenshot below.
![invitation window](/images/friends/invite.png "Invitation window")

The user can select friends, he wants to send the invitation, and then click on the "Send" button.

After that, selected friends will be notified, as in the screenshot below:

![notify](/images/friends/invite.png "notify")
