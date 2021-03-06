---
title: Svelte 3 - переосмысление реактивности
description: Обзор основных фич Svelte 3
date: 2019-05-04
url: https://svelte.dev/blog/svelte-3-rethinking-reactivity
tags:
  - jsframeworks
  - svelte
  - reactivity
layout: layouts/post.njk
---
Пару недель назад вышла новая версия Svelte. Рич Харрис опубликовал статью с описанием новых возможности — "Svelte 3: Rethinking reactivity".

Самое большое нововведение в новой версии — реактивность переменных в компонентах. Это достигается благодаря тому, что Svelte — это не обычный фреймворк, а компилятор, который преобразует высокоуровневый код приложения в прямые манипуляции DOM-дерева и добавляет всю реактивность в код на выходе.

Вот простой пример компонента, который отображает на кнопке количество нажатий:

```js
<script>
	let count = 0;
	function handleClick() {
		count++
	};
</script>

<button on:click={handleClick}>{count}</button>
```

При компиляции хендлер превращается в такой код:

```js
count++;
$$invalidate('count', count);
```

Таким образом view, которое использует переменную `count`, обновится после вызова `$$invalidate`.

В общем, проект интересный. Взлетит ли он как Vue, пока непонятно. Но можно точно сказать, что выход новой версии ещё сильнее подогрел конкуренцию на рынке js-фреймворков.

https://svelte.dev/blog/svelte-3-rethinking-reactivity
