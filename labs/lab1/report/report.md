---
## Front matter
title: "Лабораторная работа No 1.  Julia. Установка и настройка. Основные принципы."
author: "Шалыгин Георгий Эдуардович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Основная цель работы — подготовить рабочее пространство и инструментарий для работы с языком программирования Julia, на простейших примерах познакомиться с основами синтаксиса Julia.

# Выполнение лабораторной работы

## Примеры

1. Первый пример использует ф-цию println для вывода строки на экран и вывода из буфера.

   ![Вывод текста](./image/1.png){#fig:001 width=70%}

2. Получение типа выражения функцией typeof, вывод диапазонов типов, приведение типов с помощью.

   ![Работа с типами](./image/2.png){#fig:002 width=70%}

3. Работа с функциями.

   ![Задание функции](./image/3.png){#fig:003 width=70%}

4. Работа с векторами и матрицами.

   ![Работа с векторами и матрицами](./image/4.png){#fig:004 width=70%}

   

## Задания для самостоятельной работы

1. Использование функции read для чтения строк из файлов разными способами и из буфера.

   ![read](./image/5.png){#fig:005 width=70%}

2. Использование функции readdlm для чтения значений из файла, разделенных символом. В данном случае табуляция и перевод каретки.![readdlm](./image/6.png){#fig:006 width=70%}

3. Функция show выводит значение в окружении. Здесь кавычки.

   ![shpw](./image/7.png){#fig:007 width=70%}

4. Парсинг строки с приведением к значению определённого типа. Для целых значений указывается основание системы счисления.

   ![parse](./image/8.png){#fig:008 width=70%}

5. Арифметические операции, можно выполнять с рациональными дробями.

   ![Арифметика](./image/9.png){#fig:009 width=70%}

6. Алгебраические операции с векторами и матрицами, столбец и срока матрицы – векторы.

   ![Алгебра](./image/10.png){#fig:010 width=70%}



# Выводы

В ходе выполнения работы подготовлено рабочее пространство и инструментарий для работы с языком программирования Julia, разобраны простейшие примеры синтаксиса Julia.
