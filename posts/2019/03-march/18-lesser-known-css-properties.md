---
title: Малоизвестные CSS-свойства
description: Обзор малоизвестных CSS-свойств с их визуализацией
date: 2019-03-18
url: https://medium.com/@PavelLaptev/lesser-known-css-properties-in-gifs-966a143497ba
tags:
  - css
  - future
  - visualization
layout: layouts/post.njk
---
Павел Лаптев написал статью "Lesser-known CSS properties in GIFs" про малоизвестные CSS-свойства и функции, которые позволят в некоторых случаях отказаться от JavaScript. Каждое свойство в статье иллюстрируется gif-кой.

C помощью функции `element()` (поддерживается только в Firefox) можно "склонировать" в бэкграунд визуальное представление другого элемента. В Chrome и Safari TP доступны конические градиенты, с помощью которых можно делать красивые эффекты и круговые диаграммы. С помощью `motion-path` можно задать траекторию анимации. Очень полезное свойство, которое поддерживается почти во всех браузерах и которое позволяет делать отзывчивые карусели, `scroll-snap`. Ещё хочется отметить свойство `line-height-step`, с помощью которого можно задать вертикальный ритм текста (доступно в Chrome за флагом).

Некоторые CSS-фичи, перечисленные в статье, например, `element()` доступны уже долгое время. В то время как другие, например, `@media (shape: rect)`, пока существуют на уровне чернового стандарта.

https://medium.com/@PavelLaptev/lesser-known-css-properties-in-gifs-966a143497ba
