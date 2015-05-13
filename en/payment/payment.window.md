---
title: payment.window
---
Shows the store dialog window to the user

### Accepted parameters: ###

**user_id**: the ID of the user to show the dialog to<br>
**project_id**: application ID<br>
**item**: Title of the item which will be sent in the get_item notification, up to 64 characters. For example: ‘test_item’ <br>
**token** – a user token passed in the application settings (see [application parameters](/en/main/startap.html))

###Example request###

> http://{{domain}}/v1/payment.window?user_id=100&project_id=3&item=test_item&token=68d4dd4dca288a7656b421135dca6ea4

[**<- Return to main documentation**](/en/payment)