---
title: Релевантен ли GraphQL в мире HTTP2
description: Марк-Андрэ Жиру написал пост в защиту GraphQL
date: 2019-10-16
url: https://medium.com/@__xuorig__/is-graphql-still-relevant-in-an-http2-world-64964f207b8
tags:
  - http
  - graphql
layout: layouts/post.njk
---
На этой неделе в сообществе web-разработчиков развернулся спор "HTTP/2 vs GraphQL". Марк-Андрэ Жиру встал на защиту GraphQL со статьёй "Is GraphQL Still Relevant in an HTTP2 World?"

В статье говорится о том, что HTTP/2 может помочь в снижении количества запросов к серверу и в более быстрой доставке ресурсов клиенту. Но тем не менее он не решает проблему поддержки большого количества эндпойнтов, с которым хорошо справляется GraphQL. Марк ещё пишет о том, что GraphQL очень удобен при разработке приложений, построенных на базе компонентов. GraphQL предоставляет много разных возможностей из коробки (интроспекция, типизированная схема и т.п.). Поддержка GraphQL существует во многих языках. В статье ещё есть раздел про сетевые ограничения, которые сказываются на дизайне API, построенных на базе HTTP/2, но мне он показался неубедительным.

В общем, рекомендую прочитать статью, если интересно узнать позицию всех сторон спора.

https://medium.com/@__xuorig__/is-graphql-still-relevant-in-an-http2-world-64964f207b8
