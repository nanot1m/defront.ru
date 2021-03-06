---
title: Эффективность Brotli в реальном мире
description: Гарри Робертс поделился своими мыслями по поводу влияния Brotli на производительность сайтов
date: 2020-04-25
url: https://csswizardry.com/2020/04/real-world-effectiveness-of-brotli/
tags:
  - compression
  - performance
  - brotli
layout: layouts/post.njk
---
Гарри Робертс поделился своими мыслями по поводу влияния Brotli на производительность сайтов — "Real-World Effectiveness of Brotli".

Brotli — это алгоритм сжатия, который был представлен Google в 2013 году. На данный момент он поддерживается во всех актуальных браузерах. Использование Brotli вместо Gzip позволяет уменьшить объём передаваемых ресурсов до ~30%.

Внедрение Brotli иногда может быть гораздо сложнее, чем включение опции в панели CDN. Гарри провёл эксперимент, чтобы понять, стоит ли вкладывать в этом случае много сил для его поддержки, или можно обойтись обычным Gzip. Как оказалось, уменьшение объёма ресурсов на 30% не гарантирует, что на 30% улучшатся другие метрики. При сравнении работы разных сайтов переход с Gzip на Brotli не дал большого прироста производительности: общий объём передаваемых ресурсов снизился на 5.8%, а метрика First contentful paint (FCP) улучшилась всего лишь на 3.5%.

В конце статьи Гарри подводит итог. Если у вас есть возможность включить Brotli, этим стоит воспользоваться. Если же внедрение Brotli влечёт за собой недели разработки, то имеет смысл продолжать использовать Gzip.

https://csswizardry.com/2020/04/real-world-effectiveness-of-brotli/
