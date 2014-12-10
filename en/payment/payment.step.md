---
title: Step-by-step guide
---

**Payments API** provides the opportunity to transfer PlayGold from users to application accounts based on the exchange rate indicated in the application.

This guide will go through each step of connecting the payment interface to your application:

1. Preparing the server side for operation with the payment system
2. Configuring payments in the application
3. Calling the payment dialog window
4. Submitting an application for verification

----------

#### 1. Preparing the server side for operation with the payment system

Firstly, you need to implement processing for Playvision payment system notifications on your application's server.

- [Receiving information about an item](/en/payment/payment.get_item.html). Playvision requests information about an item to display it in the purchase dialog.
- [Processing payment notifications](payment.server.html).

The Playvision platform adds a sig parameter to each request. This provides a guarantee that the user did not falsify or alter the request.

> More information about [Signature generation](/en/main)

----------

#### 2. Configuring payments in the application

You must indicate the address of a return call script in the application's options

The data is filled in on the **Options** page in the **Payment link** parameter

![Link for accepting payments](/images/payment/scr1.jpg "Link for accepting payments")

If your application has not yet undergone verification, only test payments will work.


----------

#### 3. Calling the payment dialog window

You must place an icon in your application which users can press to open a Playvision dialog window with a description of the purchase cost.

The user can either confirm or cancel the purchase

![Store 1](/images/shop/choose-type.jpg "Store 1")

If there is an insufficient amount of PlayGold in the user's balance, an offer will be made to add funds to the balance using one of several methods.

![Store 2](/images/shop/choose-payment.jpg "Store 2")

To open the window, you must call the [payment.window](payment.window.html) API method.

> This does not cause the game to reload

----------

#### 4. Submitting an application for verification

If your application has not yet been verified and made part of the general application catalog, now is the time to get this done. 
Otherwise, users will be unable to use payment functionality in your application.<br>

[**<- Return to main documentation**](/en/payment/)
