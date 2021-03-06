---
title: Следующее поколоение 3D-графики в Web'е
description: Доклад про текущее состояние WebGL и про новое API WebGPU
date: 2019-05-12
url: https://www.youtube.com/watch?v=K2JzIUIHIhc
tags:
  - talk
  - webgl
  - webgpu
layout: layouts/post.njk
---
Посмотрел доклад с прошедшего Google I/O'19 "Next-Generation 3D Graphics on the Web" про настоящее и будущее 3D-графики в Web'е.

Из первой части доклада запомнилось использование веб-компонентов для снижения сложности кода при использовании WebGL-фич. Вот так выглядит пример вставки просмотрщика 3D-моделей на страницу:

```js
// импорт библиотеки
<script type="module" src="model-viewer.js"></script>
// добавление просмотрщика на страницу
<model-viewer src="astronaut.glb"></model-viewer>
```

Вторая часть доклада для меня была самой интересной. Она была посвящена новому API — WebGPU. Показали демо, где на сцене рендерилось 10000 объектов. Всё работало довольно производительно (~40fps). WebGPU способен отправить в три раза больше команд на отрисовку относительно WebGL.

Рассказали про то, что с помощью WebGPU теперь можно эффективнее работать с фильтрами пост-процессинга и алгоритмами машинного обучения, так как WebGPU гораздо гибче чем WebGL — он позволяет работать с разделяемой памятью GPU. Это также открывает возможность вынесения симуляции жидкости, скиннинга, параллельной сортировки и других алгоритмов с CPU на GPU.

Новое API доступно пока в Chrome Canary на macOS в экспериментальном режиме. API включается с помощью флага `chrome://flags/#enable-unsafe-webgpu`. Над новой спецификацией работают производители всех браузеров.

https://www.youtube.com/watch?v=K2JzIUIHIhc
