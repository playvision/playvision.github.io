---
title: sdk.tutorial
---

# Руководство по использованию Javascript SDK

## Подключение SDK

Для подключения SDK нужно добавить в тег `head` страницы

<pre>
  <code>
    &lt;script type="text/javascript" src="http://playvision.ru/api/v1/js/sdk.js"></script>
  </code>
</pre>


## Подписка на события

Формат подписки на событие:

<pre>
    <code>
PLV.addCallback('event_name', function(){
  console.log('event name');
});
    </code>
</pre>

## Список событий

|Название         |Описание                                                            |
|-----------------|--------------------------------------------------------------------|
|game_window.hide | По наступлению этого события игра будет скрыта (например, открыто модальное окно)|
|game_window.show | По наступлению этого события игра будет показана                   |


## Пример

Подписка на событие скрытия игры

<pre><code>
PLV.addCallback('game_window.hide', function(){
  console.log('Игра скрыта');
});
</code></pre>


[**<- Вернуться к основной документации**](/docs/sdk/)
