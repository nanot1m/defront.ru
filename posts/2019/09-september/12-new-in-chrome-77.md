---
title: Релиз Chrome 77
description: Новинки релиза Chrome 77 — Largest Contentful Paint, Form Participation API, событие formdata и другое
date: 2019-09-12
url: https://www.youtube.com/watch?v=S8aVB3IfOR4 https://www.youtube.com/watch?v=R8KzoMoKhnM
tags:
  - chrome
  - release
layout: layouts/post.njk
---
Два дня назад вышла новая версия Chrome 77. По каким-то причинам в этот раз не было отдельной публикации на официальном сайте, но появилось несколько видео на youtube.

В Chrome 77 появилась поддержка Largest Contentful Paint. Про эту метрику я писал ранее. С её помощью можно отследить время появления основной части контента на странице. Была добавлена поддержка Form Participation API. Благодаря ему можно создавать Custom Elements, которые будут вести себя как полноценные элементы управления стандартных форм. Также в рамках этого api у форм появилось событие `formdata`, на который можно повесить обработчик для модификации отправляемых данных перед `submit`.

В инструментах разработчика тоже есть несколько нововведений. Теперь можно скопировать стили dom-узла (контекстное меню на элементе -> copy -> copy styles). Цветовая тема соответствует настройкам операционной системы. Добавили визуализацию сдвига контента. На вкладке "Network" появилась индикация того, что ресурс был загружен из Prefetch Cache. На вкладке "Application" видны push-сообещния и нотификации от сервис-воркеров. Можно логировать эти события до трёх дней даже при закрытых инструментах разработчика.

https://www.youtube.com/watch?v=S8aVB3IfOR4
https://www.youtube.com/watch?v=R8KzoMoKhnM
