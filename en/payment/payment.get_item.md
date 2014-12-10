---
title: Getting information about an item
---

This notification is sent when a dialog window is opened for a purchase through an application.

The developer must return current information relevant to the title of the product **item** received in the notification.

The information received about the product is then displayed in a purchase dialog window.

> **Warning!** Since **item** is passed on the client side, this parameter can be changed by the user.


> The Playvision payment system sends the notification to the developer's server using a **POST** query

----------

#### Parameters of notification from Playvision payment system sent to the developer's server

|Name               |Type |Note                                                                                                 |
|-------------------|-----|-----------------------------------------------------------------------------------------------------|
|notification_type |string|equal to "get_item"                                                                                  |
|app_id            |int   |application ID                                                                                       |
|user_id           |int   |ID of user creating order                                                                            |
|item              |String|title of the item passed to the purchase dialog window                                               |
|sig               |String|notification signature (see [Signature generation](/en/main))                                        |



#### Information about an item. A list of parameters for an answer to the Playvision payment system

|Name          |Type  |Note                                                                                                      |
|--------------|------|----------------------------------------------------------------------------------------------------------|
|item_id       |string|ID of item in application                                                                                 |
|item_title    |string|product title                                                                                             |
|item_price    |int   |item cost                                                                                                 |
|item_photo_url|String|item image(Optional parameter.If not set, an image of the project from the Playvision system will be used)|



#### Example of request received from Playvision server

> Parameters: {"notification_type"=>"get_item", "app_id"=>"12", "user_id"=>"100", "item"=>"100", "sig"=>"b4ae2df28b2bbbf5fbd432226c154f9c"}


#### Example answer

> {"item_price": "5", "item_id": "test_12", "item_title": "test"}

[**<- Return to main documentation**](/en/payment/payment.step.html)
