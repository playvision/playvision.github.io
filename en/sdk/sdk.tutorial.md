---
title: sdk.tutorial
---

# Javascript SDK tutorial

## SDK integration

Add this snippet to the `head` tag of page

<pre>
  <code>
    &lt;script type="text/javascript" src="http://playvision.ru/api/v1/js/sdk.js"></script>
  </code>
</pre>


## Event subscription

Event subscription format:

<pre>
    <code>
PLV.addCallback('event_name', function(){
  console.log('event name');
});
    </code>
</pre>

## Event list

|Name         |Description                                                             |
|-----------------|--------------------------------------------------------------------|
|game_window.hide | The game iframe would be hidden on this event                      |
|game_window.show | The game iframe would be shown on this event                       |


## Example

Hide game window event subscription

<pre><code>
PLV.addCallback('game_window.hide', function(){
  console.log('The game is hidden');
});
</code></pre>


[**<- Back**](/docs/sdk/)
