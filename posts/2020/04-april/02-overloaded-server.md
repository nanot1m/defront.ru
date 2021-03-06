---
title: Решение проблем, вызванных большим траффиком
description: Кэти Хемпениус на сайте web.dev опубликовала гид по решению проблем, возникающих из-за большого траффика 
date: 2020-04-02
url: https://web.dev/overloaded-server/
tags:
  - performance
  - backend
layout: layouts/post.njk
---
Кэти Хемпениус на сайте web.dev опубликовала гид по решению проблем, возникающих из-за большого траффика — "Fix an overloaded server".

Если на сайт внезапно пришло большое количество пользователей, и он перестал осиливать нагрузку, то надо предпринять четыре шага:
1. Оценка — поиск причин отказов: CPU, IO, память, сеть.
2. Стабилизация — быстрые фиксы, которые позволят вернуть сайт к жизни: rate limiting, кэширование, отключение фич, которые особо сильно не влияют на бизнес-метрики, но которые потребляют ресурсы.
3. Улучшение — использование CDN и балансеров, добавление железа, использования сжатия ресурсов
4. Мониторинг — использование средств мониторинга показателей по перцентилям, чтобы средние значения не могли скрыть проблемы, которые возникают не у всех пользователей.

Статья полезная, рекомендую почитать.

https://web.dev/overloaded-server/
