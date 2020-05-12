---
title: WebGPU и Web Shading Language (WSL) в Safari
description: Статья про статус поддержки WebGPU API в Safari
date: 2019-09-23
url: https://webkit.org/blog/9528/webgpu-and-wsl-in-safari/
tags:
  - webgpu
  - experimental
  - safari
layout: layouts/post.njk
---
В блоге WebKit около двух недель назад появилась статья про статус поддержки WebGPU API в Safari — "WebGPU and WSL in Safari".

Железо и архитектура видеокарт постоянно улучшается. Одновременно с их развитием появляются новые программные API, которые умеют c ними эффективного работать. На сегодняшний день есть Direct3D 12 от Microsoft, Metal от Apple и Vulkan от Khronos Group. Эти API работают на более низком уровне абстракции по сравнению с OpenGL, поэтому они более производительны. Проблема в том, что они не доступны на всех платформах, то есть не могут быть использованы для web'а. Для того чтобы решить эту проблему, разрабатывается новый стандарт для работы с видеокартами — WebGPU.

WebGPU предоставляет набор JavaScript API, с помощью которого рендеринг объектов отделяется от процесса их валидации, тем самым предоставляя разработчикам возможность эффективного управления процессом рендеринга. В статье есть график результатов синтетического бенчмарка. Там видно, что прирост производительность по сравнению с WebGL может увеличиться до семи раз. Есть планы по поддержке WebGPU API из WebAssembly в будущем. В статье ещё немного рассказывается про Web Shading Language (WSL) — новый язык шейдеров, поддержка которого появилась в Safari TP 91. Его основная особенность в том, что он создавался с нуля для поддержки всех платформ и графических API, которые поддерживает WebGPU.

Мне лично непонятно, какая судьба будет у WebGL 2.0. С учётом того, что в разработку WebGPU активно инвестирует Apple, есть риск, что поддержка WebGL 2.0 в Safari так и останется на экспериментальном уровне.

Статью стоит почитать, если вам интересно, как развиваются API для работы с видеокартами.

https://webkit.org/blog/9528/webgpu-and-wsl-in-safari/