---
title: JavaScript Proxy — инструкция к применению
description: Чем может быть полезен объект Proxy на практике
date: 2019-07-02
url: https://blog.bitsrc.io/a-practical-guide-to-es6-proxy-229079c3c2f0
tags:
  - es2015
  - js
layout: layouts/post.njk
---
Proxy появился в ES2015, но до сих пор остаётся эзотерической фичей JavaScript. Про то чем он может быть полезен, рассказывает Томас Баррассо в статье "A practical guide to Javascript Proxy".

Proxy можно использовать для задания дефолтного значения, отличного от undefined, при обращении к несуществующему свойству объекта. С помощью него можно сделать python-like обращение к последнему элементу массива — `arr[-1]`, скрытие свойств и инавалидирование свойств объекта, что может быть полезно при кешировании. Но больше всего мне понравился пример с перегрузкой оператора `in`, который позволяет реализовать проверку вхождения числа в заданный диапазон как в python `2 in range(1, 100) // true`:

```js
const range = (min, max) => new Proxy(Object.create(null), {
  has: (_, prop) => (+prop >= min && +prop <= max)
})
```

Это, конечно, не всё, на что способен Proxy. В статье упоминается, что он лежит в основе новой системы реактивности Vue 3. Ещё там есть ссылки на другие способы использования. В общем, статья хорошая, почитать стоит.

https://blog.bitsrc.io/a-practical-guide-to-es6-proxy-229079c3c2f0