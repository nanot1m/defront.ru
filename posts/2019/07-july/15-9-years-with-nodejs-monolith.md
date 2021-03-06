---
title: 9 лет в монолите на Node.JS
description: Евгений Бондаренко делится опытом перевода Node.js монолита OneTwoTrip на микросервисы
date: 2019-07-15
url: https://habr.com/ru/post/459206/
tags:
  - nodejs
  - architecture
layout: layouts/post.njk
---
Евгений Бондаренко в статье "9 лет в монолите на Node.JS" поделился опытом перевода Node.js монолита OneTwoTrip на микросервисы.

Ребята начали разрабатывать приложение в 2010 году. За это время у них накопился большой опыт. В разделе про недостатки монолита описываются проблемы, которые связаны с масштабированием большого проекта, от сложности обновления зависимостей до поиска новых людей в команду. Из плюсов — простота развёртывания, нет оверхеда на передачу данных, простота отката на предыдущие версии.

Преимущества микросервисов: частые релизы, проще делать независимые тесты, использование разных технологий для наиболее оптимального решения задач. Минусы: необходимость в шине передачи данных и хорошем логировании, у разработчиков появляется слишком много свободы, необходима команда DevOps для управления всеми этими делами.

Автор пишет, что микросервисы не являются серебряной пулей и что погоня за хайпом может быть чревата проблемами. В общем, советую почитать статью, если эта тема вам интересна.

https://habr.com/ru/post/459206/
