---
title: Опыт переписывания Slack Desktop
description: Инженеры Slack рассказали про свой опыт обновления приложения
date: 2019-07-24
url: https://slack.engineering/rebuilding-slack-on-the-desktop-308d6fe94ae4
tags:
  - electron
  - performance
  - architecture
layout: layouts/post.njk
---
Недавно инженеры Slack в статье "When a rewrite isn’t: rebuilding Slack on the desktop" поделились опытом обновления своего приложения.

Старая архитектура Slack содержала три основных проблемы: ручное управление DOM, жадную загрузку данных и отдельные процессы для каждого workspace. С первыми двумя проблемами можно было справиться постепенно: для работы с DOM был выбран React, для работы с данными — Redux. Но последняя проблема требовала фундаментального изменения дизайна приложения. Был выработан план: продолжать работать со старой кодовой базой, постепенно её обновляя и используя строгий интерфейс взаимодействия современной и старой части приложения. При этом весь новый код постепенно переносился в современное приложение из старого. Таким образом получилось добиться баланса между доставкой новых фич пользователям и переписыванием приложения. В результате обновлённое приложение стало работать быстрее и потреблять меньше памяти.

Статья очень интересная. Определённо, стоит почитать.

https://slack.engineering/rebuilding-slack-on-the-desktop-308d6fe94ae4
