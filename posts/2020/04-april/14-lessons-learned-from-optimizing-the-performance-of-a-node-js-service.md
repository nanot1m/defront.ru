---
title: Опыт оптимизации Node.js-сервиса
description: Итамар Бен Закен поделился опытом оптимизации Node.js-сервиса
date: 2020-04-14
url: https://engineering.klarna.com/6-lessons-learned-from-optimizing-the-performance-of-a-node-js-service-f163cac20473
tags:
  - performance
  - nodejs
layout: layouts/post.njk
---
Итамар Бен Закен поделился опытом оптимизации Node.js-сервиса — "6 Lessons learned from optimizing the performance of a Node.js service".

Итамар разрабатывал сервис для A/B-тестирования. Такие сервисы должны работать очень стабильно, поэтому много внимания было уделено оптимизации. Вот некоторые мысли из статьи.

Нагрузочное тестирование — полезный инструмент. Оно даёт гарантии, что новые фичи не будут ломать производительность сервиса. Некоторые проблемы могут вскрываться только на больших промежутках времени, поэтому стоит увеличить время прогона тестов. Если каждый запрос должен быть обработан внешним сервисом, то при большом траффике это может создать проблемы. В статье разбирался кейс с Kafka — при её интеграции возникала большая задержка при отправке запросов. Чтобы решить эту проблему, была изменена логика обработки запросов. Их стали собирать в батчи и отправлять на обработку каждую секунду.

Довольно неплохая статья. Рекомендую почитать всем, кто разрабатывает сервисы на Node.js.

https://engineering.klarna.com/6-lessons-learned-from-optimizing-the-performance-of-a-node-js-service-f163cac20473