---
## Front matter
lang: ru-RU
title: Лабораторная 5
subtitle: 
author:
  - Шалыгин Г. Э.
institute:
  - Российский университет дружбы народов, Москва, Россия
date:

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Докладчик

  * Шалыгин Георгий Эдуардович
  * студент НФИ-02-20
  * Российский университет дружбы народов

# Вводная часть

## Цели и задачи

- Основная цель работы — освоить синтаксис языка Julia для построения графиков.


## Материалы и методы

- Процессор `pandoc` для входного формата Markdown
- Результирующие форматы
  - `pdf`
  - `html`
- Автоматизация процесса создания: `Makefile`
- Компилятор Julia
- OpenModelica

# Результаты

## Графики 2д

![](image\34.PNG){#fig:001 width=40%}



## Параметры графиков

![СЛАУ](image\35.PNG){#fig:002 width=40%}

## Оси

![](image\40.PNG){#fig:003 width=40%}



## Статистические графики

График ошибок

![](image\41.PNG){#fig:005 width=70%}

## Пространственные графики



![](image\43.PNG){#fig:006 width=70%}

## Анимация

Эпициклоида:

![](image\48.PNG){#fig:007 width=70%}



# Вывод

В ходе работы был освоен синтаксис языка Julia для построения графиков
