---
title: Как правильно использовать dns-prefetch и preconnect
description: Для ускорения установки соединения с доменами используют хинты dns-prefetch и preconnect. Дэниэл Александерсен рассказал как их правильно использовать
date: 2019-11-20
url: https://www.ctrl.blog/entry/dns-prefetch-preconnect.html
tags:
  - net
  - performance
layout: layouts/post.njk
---
Для ускорения установки соединения с доменами, на которых находятся загружаемые ресурсы, используют хинты `dns-prefetch` и `preconnect`. Дэниэл Александерсен рассказал как их правильно использовать в статье "What to <link rel=dns-prefetch> and when to use preconnect".

Самая распространённая ошибка при использовании `dns-prefetch` — добавление доменов, ссылки на которые уже есть в html-документе. В этом нет особого смысла, так как браузер будет устанавливать соединение во время парсинга документа. Наибольшую выгоду от использования `dns-prefetch` можно получить, если домен неизвестен на момент парсинга документа, например, когда установка соединения с новым доменом происходит при выполнении загруженного кода. Другой хинт — `preconnect` — не только резолвит доменное имя, но и устанавливает TCP-соединение. Это может быть очень полезно на мобильных устройствах.

Если хотите узнать больше подробностей про использование `dns-prefetch` и `preconnect`, рекомендую почитать статью.

https://www.ctrl.blog/entry/dns-prefetch-preconnect.html