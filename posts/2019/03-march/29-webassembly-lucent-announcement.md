---
title: Lucent - нативный рантайм для WebAssembly от Fastly
description: Анонс создания рантайма и компилятора WebAssembly
date: 2019-03-29
url: https://www.fastly.com/blog/announcing-lucet-fastly-native-webassembly-compiler-runtime 
tags:
  - webassembly
  - wasi
  - lucent
layout: layouts/post.njk
---
Раз уж пошла такая пьянка, давайте продолжим тему WebAssembly, тем более, что сегодня произошло ещё одно интересное событие – компания Fastly открыла исходный код WebAssembly-рантайма с поддрежкой WASI – Lucet.

Lucet разрабатывает компания Fastly – один из игроков в мире edge-computing. Edge-computing подразумевает работу с большим количеством запросов, поэтому здесь очень большую роль играет потребляемые ресурсы. Использование Lucet позволяет инстанциировать WebAssembly-модули менее чем за 50 микросекунд с потреблением памяти в несколько килобайт (для сравнения, v8 – 5 миллисекунд с десятками мегабайт потребляемой памяти). Основа Lucet – генератор кода Cranlift, который разрабатывается Mozilla для поддержки WebAssembly в Firefox. Ребята из Fastly непосредственно участвовуют в проектировании дизайна и разработке Cranlift, поэтому я доверяю цифрам, представленным выше.

Кажется, что мы наблюдаем зарождение чего-то очень интересного.

https://www.fastly.com/blog/announcing-lucet-fastly-native-webassembly-compiler-runtime 
