---
title: Main application startup options
---
The following parameters are passed to the request string when the application is displayed

**api_id**  – the launched application's ID <br>
**viewer_id** – the ID of the user who launched the application <br>
**psid** – the game server's internal ID (set automatically when the server is created) <br>
**sid** – the game server's external ID (set by you when the game server is created) <br>
**nickname** – the player's nickname <br>
**auth_key** – a generated key for user authentication. The generation algorithm is described below <br>
**token** – a unique user token <br>
**auth_key** is calculated on the Playvision server using the following method:
<pre><code>auth_key = md5(api_id + '_' + viewer_id + '_' + secret_key)</code></pre>
where **secret_key** – is your application's secret key. You can set this in the [administrative](http://dev.playvision.ru) section of your application

The request's hash (the data after the # in the address) is also passed in the **hash** parameter<br>