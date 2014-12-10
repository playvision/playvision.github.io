---
title: wall.post
---
Shows the user a dialog offering to post a message to their wall

### Accepted parameters: ###

**user_id**: the ID of the user to show the dialog to<br>
**project_id**: your project's ID<br>
**token** – a user token passed in the application settings. See [application parameters](/app)<br>
**message** - required parameter. The text of the message presented to the user for posting<br/>
**psid** - optional parameter. A game server ID. Required only if your application uses multiple servers.

###Example request###

> http://api.playvision.ru/v1/wall.post?user_id=131&project_id=1&token=fe4e4e2b3087bf7e22c139f06408d33f
