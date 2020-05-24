---
title: Система межпроцессорного взаимодействия Chromium
description: Гюёнг Ким в блоге Igalia рассказал про новую систему межпроцессорного взаимодействия Chromium
date: 2020-05-12
url: https://blogs.igalia.com/gyuyoung/2020/05/11/how-chromium-got-its-mojo/
tags:
  - internals
  - chromium
layout: layouts/post.njk
---
Гюёнг Ким в блоге Igalia рассказал про новую систему межпроцессорного взаимодействия Chromium — "How Chromium Got its Mojo?".

Chromium использует мультипроцессорную архитектуру для безопасности и устойчивости к сбоям. Внутри него работают разные процессы: renderer process, browser process, GPU process, utility process и т.п. Для общения между процессами используется IPC (Inter-process Communication). Команда Chromium решила отказаться от IPC и разбить браузер на большое количество маленьких сервисов. Для этого был разработан Mojo.

Mojo — это фреймворк для взаимодействия между процессами внутри браузера. Он отвечает за доставку сообщений между процессами и позволяет интегрировать большое количество компонентов без необходимости их линковки, сокращая время сборки и упрощая работу с частями кода, написанными на C++, Java, JavaScript. На данный момент идёт активная работа над миграцией кода, использующего Chromium IPC, на Mojo.

Если интересуетесь техническими деталями работы браузеров, то очень рекомендую заглянуть в статью.

https://blogs.igalia.com/gyuyoung/2020/05/11/how-chromium-got-its-mojo/