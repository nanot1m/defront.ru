---
title: Миграция 300 тысяч строк кода с Flow на TypeScript
description: Опыт миграции большого приложения Quizlet с Flow на TypeScript
date: 2019-07-25
url: https://medium.com/tech-quizlet/now-or-never-migrating-300k-loc-from-flow-to-typescript-at-quizlet-d3bae5830a1
tags:
  - flow
  - typescript
layout: layouts/post.njk
---
Попалась на глаза статья, в которой ребята из Quizlet рассказывают про опыт перевода кодовой базы c Flow на TypeScript — "Now or Never: Migrating 300k LOC from Flow to TypeScript at Quizlet".

Было несколько причин, которые заставили задуматься о миграции на TypeScript: медленная работа тайп-чекера, проблемы в определениях типов используемых библиотек, не такая качественная поддержка в редакторах кода как с TypeScript и т.п.

Общая кодовая база на момент переноса состояла из 300 тысяч строк. Рассматривался вариант с инкрементальным переносом проекта на TypeScript, но это усложнило бы поддержку кода, поэтому было решено мигрировать весь код сразу. Для автоматической конвертации использовался babel-плагин `babel-plugin-flow-to-typescript`. После переноса появилось 6000 ошибок в типах. Как написано в статье это не было проблемой, так как Flow всё равно их не отлавливал, поэтому они были заигнорированы. После внедрения TypeScript покрытие кода типами увеличилось на 20%. Также стали отслеживаются те ошибки, которые были проблемой для Flow.

Последнее время стало появляться больше случаев, когда большие проекты переходят c Flow на TypeScript. Не знаю, что теперь надо сделать команде Flow, чтобы удержать своих немногих пользователей... Статью стоит почитать, если перед вами стоит задача переноса кодовой базы с Flow на TypeScript.

https://medium.com/tech-quizlet/now-or-never-migrating-300k-loc-from-flow-to-typescript-at-quizlet-d3bae5830a1