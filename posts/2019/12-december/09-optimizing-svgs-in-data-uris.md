---
title: Оптимизация svg в data uri
description: Объяснение принципа кодирования svg c помощью svg-url-loader
date: 2019-12-09
url: https://codepen.io/tigt/post/optimizing-svgs-in-data-uris
tags:
  - performance
  - svg
  - webpack
layout: layouts/post.njk
---
Последние дни занимался настройкой webpack. Сегодня прикручивал загрузчик для SVG. Пока не стал заморачиваться со спрайтами, воспользовался `svg-url-loader`. Этот загрузчик в отличии от `url-loader` при инлайне изображений не кодирует их в base64, а использует url-encoded XML. Стало интересно, какими принципами следует лоадер — нашёл статью Тейлора Ханта "Optimizing SVGs in data URIs", в которой объясняется самая лучшая стратегия для инлайна.

Простого преобразования с помощью `encodeURIComponent` недостаточно, так как в результате обычно получается закодированный текст, который длиннее исходного текста SVG. Поэтому SVG кодируется "точечно", так чтобы закодированное сообщение содержало как можно меньше закодированных "unsafe URL" символов. Наибольший эффект получается от замены двойных кавычек апострофом, так как он попадает в категорию "safe URL" символов. Благодаря этому вместо трёх байтов для кодирования двойной кавычки используется один байт. Если кодируется сложный SVG с большим количеством атрибутов, это легко может сократить сотню байт.

У вас может возникнуть вполне резонный комментарий, что получившаяся экономия совсем ни о чём. Но в некоторых случаях, она может помочь избавиться от пары запросов к серверу (при использовании `limit` в `svg-url-loader` ), ускоряя отображение SVG в браузере.

https://codepen.io/tigt/post/optimizing-svgs-in-data-uris
https://github.com/bhovhannes/svg-url-loader