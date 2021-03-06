---
title: Нативная ленивая загрузка изображений для веба
description: Описание работы нового атрибута loading у изображений и iframe'ов
date: 2019-04-07
url: https://addyosmani.com/blog/lazy-loading/
tags:
  - html
  - lazy
  - future
  - chrome
layout: layouts/post.njk
---
Вчера Эдди Османи из Google написал в своём блоге про новый экспериментальный атрибут для ленивой загрузки изображений и iframe'ов – loading.

Новый атрибут позволяет отложить загрузку элемента до того момента, как он будет готов попасть во viewport. Это очень критично для мобильных устройств, так как изображения и фреймы, которые находятся на странице, отъедают память устройства и потребляют траффик, но при этом пользователь может до них просто не доскроллить.

Раньше задачу отложенной загрузки можно было решить только с помощью JavaScript, например, используя библиотеку lazysizes. Сейчас в Chrome 73 с помощью флага можно включить поддержку нового атрибута loading. У атрибута есть три возможных значения: lazy (ленивая загрузка), eager (загрузка изображения сразу же), auto (будет ли изображение загружаться лениво, решает браузер):

```
<img src="img1.jpg" loading="lazy" />
<img src="img2.jpg" loading="eager" />
<img src="img3.jpg" loading="auto" />
```

Loading – это экспериментальный атрибут, стандарт которого находится на стадии черновика. Поддержка loading без флага должна появиться в Chrome 75.

https://addyosmani.com/blog/lazy-loading/ 
