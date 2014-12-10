---
title: Processing payment notifications
---

The payment system server sends the notifications to the Return request address indicated in the application's settings. They are sent using the HTTP or HTTPS protocol depending on the protocol of the return request address, by the POST method in UTF-8 format.

To eliminate the possibility of falsifying the notification, it is signed with a secret key known only to the owners of the application and the payment system


The application developer must implement notification processing and return either the process result if successful, 
or an error description if unsuccessful (see Answer format when processing fails). 
The answer must also be sent within 10 seconds, 
otherwise the connection will be lost and the error text will be recorded to the transaction log.

> **Warning!** The answer must be in **JSON** format and must be **UTF-8** encoded

#### General notification parameters

The parameters indicated below are sent in the notification to the application server with each request.

|Name             |Type  |Note                                                         |
|-----------------|------|-------------------------------------------------------------|
|notification_type|String|equal to "order_status_change"                               |
|user_id          |Int   |ID of user in Playvision system                              |
|sid              |Int   |Game server ID if multiple servers are being used            |
|transaction_id   |Int   |Order ID                                                     |
|sum              |Int   |Amount of game currency                                      |
|item_id          |Int   |ID of item in application                                    |
|time             |Int   |Time in the timestamp format                                 |
|sig              |String|notification signature (see [Signature generation](/en/main))|

#### Verifying notification signature

The sig parameter is equal to an md5 hash of the parameter=value pairs concatenated in ascending order by parameter name (alphabetical order) and the project's secret key indicated in your application's settings.

![project's secret key](/images/payment/scr1.jpg "project's secret key")

If the signatures do not match, an error must be given in response.

Example of formulating signature with the secret key SeOkPegfgFDS2:

> sig = md5("name1=value1name2=valueSeOkPegfgFDS2")


#### Payment result notification from Playvision platform

After processing the information about the funds transfer to the user, 
a notification must be sent to the Playvision platform about the execution result. 
The response must be in the json format and it must contain the following fields:

|Name   |Type  |Note                                                                                         |
|-------|------|---------------------------------------------------------------------------------------------|
|status |Int   |Order fulfillment status. Successful - 1, Unsuccessful - other numbers                       |
|message|String|Error string if payment is unsuccessful. Will be displayed in transaction log(“Result” field)|



**Example response**

Successful payment:

> {"status": "1"}

Unsuccessful payment:

> {"status": "-1", "message": "Invalid signature"}

[**<- Return to main documentation**](/en/payment/payment.step.html)
