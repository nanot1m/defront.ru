---
title: Как был создан новый facebook.com с помощью React Relay и GraphQL
description: Доклад про внутреннее устройство обновленной версии facebook.com
date: 2019-05-02
tags:
  - relay
  - codesplitting
  - facebook
layout: layouts/post.njk
---
Два дня назад на конференции F8 была представлена новая версия facebook.com. Команда разработчиков рассказала о технологиях, которые лежат в основе новой версии социальной сети.

Новый сайт — это полноценное SPA-приложение. За данные отвечают GraphQL и Relay, которые позволяют получать только те данные, которые нужны компонентам на текущей странице. Такой подход помог избавиться от загрузки избыточных данных и сделал возможным загрузку данных параллельно коду. Очень много внимания уделили Code-Splitting'у. С помощью Relay был достигнут Data-Driven Code-Splitting — вместе с данными указываются компоненты, которые нужны для отрисовки кода. Ещё реализовали пару дополнительных функций для разделения кода в зависимости от фаз отрисовки страницы: показ начальной страницы загрузки, отрисовка страницы, добавление интерактивности.

Также рассказали про изменения в CSS. Теперь за каждое правило отвечает отдельный класс (Atomic Stylesheets), что позволило снизить общее количество скачиваемых стилей. Используют React.Suspense, для того чтобы улучшить UX. Рассказали про свою работу над Chromium: скоро зарелизят новое  браузерное API `isInputPending`. С помощью этого API станет возможным прерывать работу JS, если известно, что пользователю результат выполнения кода не нужен. Например, если код на первой странице приложения ещё не отработал, а пользователь уже попытался перейти на следующую страницу.

Информации очень много, рекомендую посмотреть.

https://developers.facebook.com/videos/2019/building-the-new-facebookcom-with-react-graphql-and-relay/