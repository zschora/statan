---
## Front matter
lang: ru-RU
title: Лабораторная 3
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

## Актуальность

- - Информационная безопасность - важная часть компетенции в образовательном треке НФИ

## Цели и задачи

- Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.


## Материалы и методы

- Процессор `pandoc` для входного формата Markdown
- Результирующие форматы
  - `pdf`
  - `html`
- Автоматизация процесса создания: `Makefile`
- Компилятор Julia
- OpenModelica

# Результаты

## Циклы

![](image\11.PNG){#fig:001 width=40%}





## Ветвления

![ветвление](image\13.PNG){#fig:002 width=40%}

## Функции

![функции](image\14.PNG){#fig:003 width=40%}

## map

![map](image\15.PNG){#fig:005 width=40%}

## outer

![outer](image\23.PNG){#fig:006 width=40%}

## решение систем

![системы](image\25.PNG){#fig:07 width=40%}



# Вывод

В ходе работы были  освоены применение циклов функций и сторонних для Julia пакетов для решения задач линейной алгебры и работы с матрицами.
