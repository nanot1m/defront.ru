---
title: Оптимзиация рендеринга с помощью CSS=свойства contain
description: Рейчел Эндрю написала статью про новое свойство contain, с помощью которого можно подсказывать браузеру, как изменяется элемент, улучшая производительность отрисовки
date: 2019-12-30
url: https://www.smashingmagazine.com/2019/12/browsers-containment-css-contain-property/
tags:
  - css
  - performance
layout: layouts/post.njk
---
Изменение контента страницы может влиять на fps или блокировать работу со страницей из-за большого объёма работы, которую надо выполнить браузеру. Например, изменение свойства `left` у одного элемента может вызвать проверку необходимости изменения положения для каждого элемента в DOM-дереве, что неэффективно. Именно для решения этой проблемы была разработана спецификация CSS Containment. Рейчел Эндрю недавно написала про неё статью — "Helping Browsers Optimize With The CSS Contain Property".

CSS Containment определяет одно свойство — `contain`, которое может содержать значения `layout`, `paint`, `size`, `content` и `strict`. Все эти значения подсказывают браузеру, что изменения внутри элемента, к которому применено свойство, не влияют на другие элементы, поэтому браузер может производить дополнительные оптимизации, сокращая время на рендеринг и лайаут контента. У всех этих значений есть нюансы использования. Например, одни значения влияют на отображение контента, другие создают блочный контекст форматирования и т.п. В статье рекомендуется использовать `contain: content` для web-приложений, построенных на базе компонентного подхода.

CSS Containment стал официальным стандартом месяц назад. Поддержка этой спеки есть в Chrome и Firefox.

https://www.smashingmagazine.com/2019/12/browsers-containment-css-contain-property/
