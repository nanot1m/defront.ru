---
title: Создание тёмной темы с помощью mix-blend-mode
description: Подход к созданию тёмной темы с использованием mix-blend-mode
date: 2019-06-02
url: https://dev.wgao19.cc/2019-05-04__sun-moon-blending-mode/
tags:
  - css
  - colors
layout: layouts/post.njk
---
Вей Гао опубликовала статью про то, как она добавила поддержку тёмной темы у себя в блоге — "Night Mode with Mix Blend Mode: Difference".

При подготовке своего доклада "This World Mixed and Blended" к Вей пришла идея сделать тёмную тему с помощью CSS-свойства `mix-blend-mode: difference`. `Difference` — режим смешивания, который доступен почти во всех современных браузерах кроме IE11. Этот режим можно выразить формулой: `difference(A, B ) = |A - B|`. То есть абсолютное значение разницы двух цветов.

Для реализации тёмной темы Вей сделала дополнительный div, который перекрывает контент. У этого элемента установлены `background: white` и `mix-blend-mode: difference;`. Благодаря этому светлый фон становится тёмным, а тёмный текст — светлым. Для исключения изображений из режима смешивания используется свойство `isolation: isolate`.

В статье очень подробно рассматривается работа `difference`. Но этот подход может вызывать проблемы с производительностью, поэтому Вей не рекомендует делать сложные анимации, если используются режимы смешивания.

https://dev.wgao19.cc/2019-05-04__sun-moon-blending-mode/
