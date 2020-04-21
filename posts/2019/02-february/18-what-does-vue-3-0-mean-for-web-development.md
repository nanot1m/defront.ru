---
title: Что ожидать в Vue 3.0?
description: Обзор нововведений в будущей версии Vue 3.0
date: 2019-02-18
tags:
  - vue
  - js
  - jsframeworks
layout: layouts/post.njk
---
Давайте поговорим про js-фреймворки, а именно про будущий Vue 3.0. Кажется, что прошло совсем немного времени с момента релиза второй версии, но разработчики уже готовы выпустить следующий мажорный релиз. Статья "What Does Vue 3.0 Mean for Web Development?" рассказывает о том, чего нам ждать в будущем.

Основной упор был сделан на оптимизации производительности. Движок отслеживания изменений был переписан на ES2015 Proxy. Это позволило ускорить начальную инициализацию компонентов в 2 раза и снизить потребление памяти. Также разработчики разбили фреймворк на ещё большее количество модулей, что позволило уменьшить ядро до 10Кб (в gzip). Во второй версии были эксперименты с использованием Vue на нативных платформах аля React Native. В третей версии поддержка нативных платформ заявлена как основная фича. Под шумок разработчики переписывают код с Flow на TypeScript, мотивируя это тем, что пользователей TS гораздо больше. Очень много внимания уделили Developer Experience.

Ну что сказать, звучит это всё более чем любопытно. Очень интересно наблюдать за тем, как Vue стремительно развивается, не имея за спиной поддержки в лице больших корпораций. И кто знает, какую долю займёт Vue через несколько лет.

https://medium.com/@mattmaribojoc/what-does-vue-3-0-mean-for-web-development-851052fc0138 