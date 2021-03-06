---
title: Дизайн-документ оптимизации конкатенации строк в v8
description: Возможные пути оптимизации конкатенации строк в v8
date: 2019-03-10
url: https://twitter.com/bmeurer/status/1102452256794906625
tags:
  - js
  - v8
  - performance
layout: layouts/post.njk
---
Бенедикт Мюрер - разработчик v8 - пару дней назад опубликовал дизайн-документ, посвящённый оптимизации конкатенации строк в JS.

Конкатенация строк - одна из основных операций над строками, у которой, как оказывается, есть хороший потенциал для ускорения. Если конкатенация будет оптимизирована, то решения для сервер сайд рендеринга станут ещё быстрее (именно на этом примере Бенедикт показывает важность оптимизации).

В документе также рассказывается про текущий механизм оптимизации строк - "ropes". Приводится пример того, как можно написать один вид конкатенации в двух разных вариантах: оптимизированном и неоптимизированном. Но разработчики v8 предупреждают, чтобы мы не кидались переписывать свой код. Движки будут учиться конкатенировать строки более эффективно самостоятельно, если с этим возникнут проблемы, тогда (возможно) в языке появится новый StringBuilder API.

https://twitter.com/bmeurer/status/1102452256794906625 
