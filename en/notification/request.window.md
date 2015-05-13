---
title: request.window
---
Shows the user a window for sending a notification to another user in his name.

### Accepted parameters: ###

**user_id**: the ID of the user to show the dialog to<br>
**project_id**: your project's ID<br>
**token** – user token passed in the application settings. See [application parameters](/app)<br>
**request_user_id** - required parameter. The ID of the user who will be sent a message from the name of the user indicated in the 
**request_key** - optional extra parameter which will be passed during application launch.<br>
**message** - the parameter containing the message text.

###Example request###

> http://**domain**/v1/request.window?user_id=100&project_id=1&token=fe4e4e2b3087bf7e22c139f06408d33f&request_user_id=119&request_key=some_string&message=test

[**<- Return to main documentation**](/en/notification)