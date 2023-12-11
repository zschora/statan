---
## Front matter
title: "Отчет по лабораторной работе 4"
subtitle: "Линейная алгебра"
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

Основной целью работы является изучение возможностей специализированных пакетов Julia для выполнения и оценки эффективности операций над объектами линейной алгебры.



# Выполнение лабораторной работы

1. Повторим примеры (@fig:001).

   ![Поэлементные операции над многомерными массивами](image\1.PNG){#fig:002 width=70%}

   ![Работа со средними значениями](image\2.PNG){#fig:003 width=70%}

   ![Транспонирование, след, ранг, определитель и инверсия матрицы](image\3.PNG){#fig:004 width=70%}

   ![Вычисление нормы векторов и матриц](image\4.PNG){#fig:005 width=70%}

   ![Углы, повороты, вращения](image\5.PNG){#fig:006 width=70%}

   ![Матричное умножение, единичная матрица, скалярное произведение](image\6.PNG){#fig:007 width=70%}

   ![Решение линейного уравнения](image\7.PNG){#fig:001 width=70%}

   ![LU-факторизация](image\8.PNG){#fig:008 width=70%}

   ![Элементы LU-факторизации](image\9.PNG){#fig:09 width=70%}

   ![Решение СЛАУ через разложение](image\10.PNG){#fig:010 width=70%}
   
   ![QR-факторизация](image\11.PNG){#fig:011 width=70%}
   
   ![Примеры собственной декомпозиции матрицы 𝐴](image\12.PNG){#fig:012 width=70%}
   
   ![Примеры работы с матрицами большой размерности и специальной структуры](image\13.PNG){#fig:013 width=70%}
   
   ![Воспользуемся пакетом BenchmarkTools](image\14.PNG){#fig:014 width=70%}
   
   ![Использование типов Tridiagonal и SymTridiagonal для хранения трёхдиагональных матриц](image\15.PNG){#fig:015 width=70%}
   
   ![Символьное решение СЛАУ с рациональными коэффициентами](image\16.PNG){#fig:016 width=70%}

## Задания для самостоятельного выполнения

1. Задайте вектор v. Умножьте вектор v скалярно сам на себя и сохраните результат в dot_v. Умножьте v матрично на себя (внешнее произведение), присвоив результат переменной outer_v.

   ![Умножение векторов](image\17.PNG){#fig:017 width=70%}

2. Решить СЛАУ с двумя и тремя неизвестными.

   ![Решение СЛАУ с 2-мя неизвестными](image\18.PNG){#fig:018 width=70%}

   ![Решение СЛАУ с 3-мя неизвестными](image\19.PNG){#fig:019 width=70%}

3. Приведите  матрицы к диагональному виду.

   ![Диагонализация](image\20.PNG){#fig:020 width=70%}

4. Вычислите степени от матриц.

   ![Матрицы в степени](image\21.PNG){#fig:021 width=70%}

5. Найдите собственные значения матрицы $A$.

   ![Собственные значения и векторы](image\22.PNG){#fig:022 width=70%}

6. Матрица $A$ называется продуктивной, если решение $x$ системы при любой неотрицательной правой части $y$ имеет только неотрицательные элементы $x_i$ . Используя это определение, проверьте, являются ли матрицы продуктивными.

   ![Проверка продуктивности](image\23.PNG){#fig:023 width=70%}

   Решим уравнения символьно с помощью SymPy. Для двух первых матриц видим, что существуют отрицательные решения. Ниже приведены примеры такие контрпримеры. Для третьей матрицы отрицательных решений нет.

7. Критерий продуктивности: матрица 𝐴 является продуктивной тогда и только тогда, когда все элементы матрица $(E-A)^{-1}$ являются неотрицательными числами. Используя этот критерий, проверьте, являются ли матрицы продуктивными.

   ![Проверка с помощью критерия](image\24.PNG){#fig:024 width=70%}

   Критерием подтверждаются полученные выше результаты: продуктивная только третья матрица.

8. Спектральный критерий продуктивности: матрица $A$ является продуктивной тогда и только тогда, когда все её собственные значения по модулю меньше 1. Используя этот критерий, проверьте, являются ли матрицы продуктивными.

   ![Спектральный критерий](image\25.PNG){#fig:025 width=70%}

   Выводы опять подтвердились, также видим, что четвертая матрица продуктивной является.

   


# Выводы

В ходе работы были  изучены возможности специализированных пакетов Julia для выполнения и оценки эффективности операций над объектами линейной алгебры

# Список литературы{.unnumbered}

::: {#refs}
:::
