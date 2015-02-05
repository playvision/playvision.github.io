---
title: Test mode
---

With the test mode you can test functionality of PlayGold transfer in application without actual PlayGold transfer.

You shall use the test mode till your application is checked by the Site Administration. Actual payments are made immediately after the application is successfully checked.

For payments in the test mode, add all users with test payments into a special list in application settings Management(Roles).

![Test payments](/images/payment/testers.jpg "Test payments")

In test mode, notification_type is added with "_test" suffix. Thus, notifications will be shown as '[get_item_test](/docs/payment/payment.get_item.html)', '[order_status_change_test](/docs/payment/payment.server.html)' respectively.

And order IDs in the test mode — order_id parameters of notifications — can overlap with order IDs in standard mode.


[**<- Return to main documentation**](/en/payment/)
