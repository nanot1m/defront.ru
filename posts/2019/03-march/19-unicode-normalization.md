---
title: Зачем необходимо нормализовывать Unicode-строки
description: Объяснение необходимости нормализации Unicode-строк
date: 2019-03-19
url: https://withblue.ink/2019/03/11/why-you-need-to-normalize-unicode-strings.html
tags:
  - unicode
  - normalization
  - es2015
layout: layouts/post.njk
---
Алессандро Сегала опубликовал небольшой пост про нормализацию Unicode-строк "When 'Zoë' !== 'Zoë'. Or why you need to normalize Unicode strings".

Unicode - очень интересная тема, которая таит в себе много особенностей. Каким образом текст из заголовка статьи не может быть равен самому себе? Дело в том, что символ "ё" в Unicode может быть представлен как одиночным кодпойнтом, так и комбинацией двух кодпойнтов: символа "e" и символа умлаут. Из-за этого сравнение двух одинаковых (по внешнему виду) строк может вернуть `false`. Для решения этой проблемы необходимо воспользоваться Unicode-нормализацией. В стандарт ES2015 для этого был добавлен метод `String.normalize()` с четырьмя формами нормализации: NFC, NFD, NFKC, NFKD.

В конце статьи Алессандро призывает всегда приводить пользовательский ввод к каноничной форме – NFC.

https://withblue.ink/2019/03/11/why-you-need-to-normalize-unicode-strings.html 
