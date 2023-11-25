---
## Front matter
title: "Отчет по лабораторной работе 3"
subtitle: "Управляющие структуры"
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

Основная цель работы — освоить применение циклов функций и сторонних для Julia пакетов для решения задач линейной алгебры и работы с матрицами.



# Выполнение лабораторной работы

1. Повторим примеры (@fig:001).

   ![while](image\1.PNG){#fig:002 width=70%}

   ![for](image\2.PNG){#fig:003 width=70%}

   ![двойной for](image\3.PNG){#fig:004 width=70%}

   ![if-else](image\4.PNG){#fig:005 width=70%}

   ![функции](image\5.PNG){#fig:006 width=70%}

   ![способы задания функций](image\6.PNG){#fig:007 width=70%}

   ![операции inplace](image\7.PNG){#fig:001 width=70%}

   ![map, broadcast](image\8.PNG){#fig:008 width=70%}

   ![broadcast](image\9.PNG){#fig:09 width=70%}

   ![установка пакета](image\10.PNG){#fig:010 width=70%}


## Задания для самостоятельного выполнения



1. Используя циклы while и for: 

   – выведите на экран целые числа от 1 до 100 и напечатайте их квадраты;

   ![1](image\11.PNG){#fig:011 width=70%}

2. создайте словарь squares, который будет содержать целые числа в качестве ключей и квадраты в качестве их пар-значений; 

   – создайте массив squares_arr, содержащий квадраты всех чисел от 1 до 100

   ![2](image\12.PNG){#fig:012 width=70%}

3. Напишите условный оператор, который печатает число, если число чётное, и строку «нечётное», если число нечётное. Перепишите код, используя тернарный оператор

   ![3](image\13.PNG){#fig:013 width=70%}

4. Напишите функцию add_one, которая добавляет 1 к своему входу

   ![4](image\14.PNG){#fig:014 width=70%}

5. Используйте map() или broadcast() для задания матрицы 𝐴, каждый элемент которой увеличивается на единицу по сравнению с предыдущим.

   ![5](image\15.PNG){#fig:015 width=70%}

6. Задайте матрицу 𝐴  . – Найдите $𝐴^3$ . – Замените третий столбец матрицы 𝐴 на сумму второго и третьего столбцов

   ![6](image\16.PNG){#fig:016 width=70%}

7. Создайте матрицу 𝐵 с элементами $𝐵𝑖1 = 10, 𝐵𝑖2 = −10, 𝐵𝑖3 = 10, 𝑖 = 1, 2, … , 15. Вычислите матрицу 𝐶 = 𝐵^𝑇𝐵.

   ![7](image\17.PNG){#fig:017 width=70%}

8. Создайте матрицу 𝑍 размерности 6 × 6, все элементы которой равны нулю, и матрицу 𝐸, все элементы которой равны 1. Используя цикл while или for и закономерности расположения элементов, создайте следующие матрицы размерности 6 × 6:

   ![8](image\18.PNG){#fig:018 width=70%}

   ![9](image\19.PNG){#fig:019 width=70%}

   ![10](image\20.PNG){#fig:020 width=70%}

   ![21](image\21.PNG){#fig:021 width=70%}

9. Напишите свою функцию, аналогичную функции outer() языка R

   ![22](image\23.PNG){#fig:022 width=70%}

10. Используя написанную вами функцию outer(), создайте матрицы следующей структуры:

    ![23](image\24.PNG){#fig:023 width=70%}

11. Решите следующую систему линейных уравнений с 5 неизвестными:

    ![24](image\25.PNG){#fig:024 width=70%}

12. Создайте матрицу 𝑀 размерности 6 × 10, элементами которой являются целые числа, выбранные случайным образом с повторениями из совокупности 1, 2, … , 10. – Найдите число элементов в каждой строке матрицы 𝑀, которые больше числа 𝑁 (например, 𝑁 = 4). – Определите, в каких строках матрицы𝑀число𝑀(например,𝑀 = 7) встречается ровно 2 раза? – Определите все пары столбцов матрицы 𝑀, сумма элементов которых больше 𝐾 (например, 𝐾 = 75).

    ![25](image\26.PNG){#fig:025 width=70%}

    


# Выводы

В ходе работы были  освоены применение циклов функций и сторонних для Julia пакетов для решения задач линейной алгебры и работы с матрицами.

# Список литературы{.unnumbered}

::: {#refs}
:::
