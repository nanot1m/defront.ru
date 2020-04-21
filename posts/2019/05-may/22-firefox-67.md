---
title: Релиз Firefox 67
description: О нововведениях в Firefox 67
date: 2019-05-22
url: https://hacks.mozilla.org/2019/05/firefox-67-dark-mode-css-webrender/
tags:
  - Firefox
  - announcement
layout: layouts/post.njk
---
Вчера вышла новая версия Firefox 67. В блоге Mozilla Hacks по традиции опубликовали пост с самыми интересными нововведениями — "Firefox 67: Dark Mode CSS, WebRender, and more".

В Windows 10 начался процесс постепенной выкатки на всех пользователей с видеокартами NVidia нового WebRender. Это новый движок рендеринга, написанный на Rust и активно использующий GPU для отрисовки элементов страницы.

Появилась поддержка медиа-функции prefers-color-scheme с помощью, которой можно определить, включена ли у пользователя светлая или тёмная тема ОС, и соответствующим образом изменить внешний вид страницы. В JavaScript были добавлены динамические импорты `import()` и `String.prototype.matchAll`. Улучшили инструменты разработчика. Теперь можно ставить брекпойнты на частях одного большого выражения, записанного в одну строку (column breakpoint). Добавлена фича "log point", с помощью которой можно добавлять логирование в ходе процесса отладки, не используя `console.log()`.

Добавили поддержку кодека AV1. Улучшили менеджер паролей. Расширили настройки приватности — теперь браузер может определять криптомайнеры и скрипты, пытающиеся идентифицировать пользователя по цифровому отпечатку.

С каждым релизом Firefox становится лучше, это не может не радовать. Здорово то, что много внимания уделяется инструментам разработчика. WebRender тоже очень крутая фича, очень жду когда она появится под macOS.

https://hacks.mozilla.org/2019/05/firefox-67-dark-mode-css-webrender/