---
## Front matter
title: "Отчет по лабораторной работе 2"
subtitle: "Структуры данных"
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

Основная цель работы — изучить несколько структур данных, реализованных в Julia, научиться применять их и операции над ними для решения задач.



# Выполнение лабораторной работы

1. Повторим примеры кода работы с кортежами (@fig:001)

   ![Кортежи](image\1.PNG){#fig:001 width=70%}

2. Примеры код работы со словарями (fig:002)

   ![Словари](image\2.PNG){#fig:002 width=70%}

3. Работа с множествами (@fig:003). 

   ![Множества](image\3.PNG){#fig:003 width=70%}

4. Создание массивов (@fig:004). 

   ![Массивы](image\4.PNG){#fig:004 width=70%}

5. Генераторы массивов (@fig:005). 

   ![Массивы](image\5.PNG){#fig:005 width=70%}

6. Заполнение массивов (@fig:006).

   ![Массивы](image\6.PNG){#fig:006 width=70%}

7. Примеры срезов, функции сортировки и логическая индексация (@fig:007). 

   ![Создание файла](image\7.PNG){#fig:007 width=70%}

8. Задания для самостоятельного выполнения. 1 задание

   ![Множества](image\8.1.PNG){#fig:008 width=70%}

9. Задания для самостоятельного выполнения. 2 задание

   ![Множества разного типа](image\8.2.PNG){#fig:009 width=70%}

10. Создание массивов.

    ![Создание массивов](image\8.14.PNG){#fig:010 width=70%}

11. Создание массивов с помощью функций fill, repeat

    ![Создание массивов](image\8.3.PNG){#fig:011 width=70%}

12. Создание массивов с помощью генераторов и условий, поиск цифры 6 в значениях массива. Здесь она встречается 2 раза.

    ![Создание массивов](image\8.4.PNG){#fig:012 width=70%}

13. Создание массивов с помощью генераторов.

    ![Создание массивов](image\8.5.PNG){#fig:013 width=70%}

14. Создание массивов с помощью генераторов, создание массива строк с параметром.

    ![Создание массивов](image\8.6.PNG){#fig:014 width=70%}

15. Создание массивов с помощью генераторов на основе существующих. Подсчет суммы с помощью генератора массива.

    ![Создание массивов](image\8.7.PNG){#fig:015 width=70%}

16. Поиск элементов в массиве по условию, логическая индексация для двух массивов. подсчет элементов, удовлетворяющих условию с помощью логической индексации. Сумма здесь равно количеству значений true, 59.

    ![Логическая индексация](image\8.8.PNG){#fig:016 width=70%}

17. Подсчет элементов по условию с помощью функции count(условие, массив). Функция sortperm возвращает индексы, отсортированные по значениями элементов, то есть x[sortperm(y)] отсортирует х в порядке сортировки для у.

    ![Работа с элементами массива](image\8.9.PNG){#fig:017 width=70%}

18. Создадим массив квадратов.

    ![Создание массива](image\8.10.PNG){#fig:018 width=70%}

19. Скачаем и подключим пакет Primes.

    ![Подключение Primes](image\8.11.PNG){#fig:019 width=70%}

20. Функцией primes(1000) получим простые числа, меньше 1000, и возьмем первые 168, они отсортированы по возрастанию.

    ![Получение простых чисел](image\8.12.PNG){#fig:020 width=70%}

21. С помощью массивов, полученных генераторами, вычислим следующие выражения.

    ![Вычисление сумм](image\8.13.PNG){#fig:021 width=70%}

# Выводы

В ходе работы были изучены несколько структур данных, реализованных в Julia, научились применять их и операции над ними для решения задач.

