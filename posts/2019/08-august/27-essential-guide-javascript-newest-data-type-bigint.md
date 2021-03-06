---
title: BigInt — новый тип данных JavaScript
description: Руководство по использованию BigInt — нового типа данных в JavaScript
date: 2019-08-27
url: https://www.smashingmagazine.com/2019/07/essential-guide-javascript-newest-data-type-bigint/
tags:
  - js
  - proposal
layout: layouts/post.njk
---
Фараз Келини написал хорошую статью про BigInt — предложение добавления в стандарт JavaScript — "The Essential Guide To JavaScript’s Newest Data Type: BigInt".

`BigInt` — новый тип в языке. Его планируют добавить в стандарт из-за того, что размерности `Number` недостаточно, если необходимо работать с большими числами. Если `Number` выходит за пределы `Number.MAX_SAFE_INTEGER` и `Number.MIN_SAFE_INTEGER`, то число округляется, приводя к багам в программе. Например, `9007199254740992 === 9007199254740993` будет `true`.

BigInt-числа выглядят как обычные, но с суффиксом `n` в конце — `10000n`. В арифметических выражениях `BigInt` и `Number`, нельзя смешивать между собой (будет `TypeError` ), так как возникает дихотомия в интерпретации результата. Если хочется использовать разные типы в одном выражении, то их надо привести явно к одному типу: `1000n + BigInt(1)`. При сравнении чисел `BigInt` и `Number` нельзя использовать строгое сравнение, так как это разные типы ( `10n === 10 // false` ), но можно использовать нестрогое.

На данный момент пропозал BigInt находится на stage 3. Его поддержка есть в Chrome, Firefox и последней версии Edge. Создать полноценный полифилл для BigInt невозможно, поэтому в статье предлагается использовать библиотеку JSBI для поддержки старых версий браузеров.

В общем, рекомендую почитать статью. Скорее всего `BigInt` попадёт в следующую версию стандарта.

https://www.smashingmagazine.com/2019/07/essential-guide-javascript-newest-data-type-bigint/
