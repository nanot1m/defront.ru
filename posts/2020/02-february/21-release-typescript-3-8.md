---
title: Релиз TypeScript 3.8
description: Обзор новых фич TypeScript 3.8 — явный импорт типов, private fields, top-level await и другое
date: 2020-02-21
url: https://devblogs.microsoft.com/typescript/announcing-typescript-3-8/
tags:
  - typescript
  - release
  - announcement
layout: layouts/post.njk
---
Недавно вышла новая версия TypeScript. Дениэл Розенвассер рассказал про новые фичи релиза — "Announcing TypeScript 3.8".

С версии 3.8 можно явно указывать, что импортируется/экспортируется тип, а не значение: `import type { SomeThing } from "./some-module.js";`. Если импортируется только тип, то на этапе транспиляции import удаляется. Иногда из-за этого возникают ошибки в рантайме, например, в Angular.js (1.x) ломалась регистрация сервисов. С появлением более тонкой декларации импортов и новой опции `importsNotUsedAsValues` теперь можно предотвратить подобные ошибки.

Была добавлена поддержка Private Fields из предложения Class field declarations, с помощью которой можно создавать приватные поля класса `#foo = 'bar'`. В TypeScript была возможность создания приватных полей с помощью модификатора `private`, но Private Fields дают настоящую приватность (hard privacy) на уровне цели транспиляции. Также благодаря им решается проблема с перекрытием полей.

Добавили поддержку пропозала top-level await. Эта фича избавляет от необходимости заворачивать в async-функцию код с `await`. Она работает только для модулей, поэтому, если ваш файл ничего экспортиует/импортирует, для того чтобы заработал top-level await надо будет добавить формальный экспорт `export {}`.

Реализовали поддержку ещё одного пропозала будущего стандарта `export * as ns`. Добавили поддержку модификаторов `@public`, `@private`, `@protected` в JSDoc. Очень много изменений было сделано для улучшения вотчинга файлов — теперь в tsconfig.json есть новая группа опций `watchOptions`. Реализовали "неточную и быструю" инкрементальную сборку, которая позволяет ускорить скорость пересборки проекта за счёт снижения строгости проверок. В редакторах появятся новые пункты меню для конвертации конкатенации строк в шаблонные строки и для визуализации иерархии вызовов функций.

https://devblogs.microsoft.com/typescript/announcing-typescript-3-8/
