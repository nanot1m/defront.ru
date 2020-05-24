---
title: Улучшение загрузки Next.js и Gatsby
description: Хуссейн Джирде написал статью про улучшение разделения на чанки Next.js и Gatsby
date: 2020-05-02
url: https://web.dev/granular-chunking-nextjs/
tags:
  - webpack
  - performance
layout: layouts/post.njk
---
Команда разработчиков Chrome активно контрибьютит в инструменты js-экосистемы и фреймворки. Хуссейн Джирде написал статью про один из таких кейсов сотрудничества — "Improved Next.js and Gatsby page load performance with granular chunking".

В Next.js и Gatsby в бандл `commons` попадал код, который использовался более чем на 50% страниц. Такая настройка была не очень эффективна, так как общий код оставшихся 50% страниц не разделялся между чанками. Для решения этой проблемы была адаптирована стратегия, в которой с помощью `SplitChunksPlugin`:
— все модули больше 160kb выносятся в индивидуальные чанки;
— создаётся отдельный чанк `frameworks` с кодом, который используется на всех страницах ( `react`, `react-dom` и т.п.);
— создаётся столько общих чанков, сколько webpack посчитает нужным создать, но не более 25.

Такие настройки позволяют улучшить скорость загрузки и улучшить утилизацию кеша при переходе между страницами. При переходе на новую стратегию разделения чанков общий размер генерируемого js-кода на production-сайтах уменьшился в среднем на 20%.

Рекомендую почитать статью, если интересуетесь темой производительности.

https://web.dev/granular-chunking-nextjs/