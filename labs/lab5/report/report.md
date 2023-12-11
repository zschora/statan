---
## Front matter
title: "Отчет по лабораторной работе 5"
subtitle: "Построение графиков"
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

Основная цель работы — освоить синтаксис языка Julia для построения графиков.



# Выполнение лабораторной работы

1. Повторим примеры.

   ![Кривая](image\1.PNG){#fig:001 width=70%}

   ![Кривая с плотли](image\2.PNG){#fig:002 width=70%}

   ![Синус](image\3.PNG){#fig:003 width=70%}

   ![Два графика на одном](image\4.PNG){#fig:004 width=70%}

   ![Задание параметров графика](image\5.PNG){#fig:005 width=70%}

   ![Сохранение](image\6.PNG){#fig:006 width=70%}

   ![Точечный график](image\7.PNG){#fig:007 width=70%}

   ![Изменение размера вершин](image\8.PNG){#fig:008 width=70%}

   ![Пространственный график](image\9.PNG){#fig:009 width=70%}

   ![Зашумленные данные](image\10.PNG){#fig:010 width=70%}
   
   ![QR-факторизация](image\11.PNG){#fig:011 width=70%}
   
   ![Регрессия данных](image\12.PNG){#fig:012 width=70%}
   
   ![Случайный график](image\13.PNG){#fig:013 width=70%}
   
   ![Вторые оси добавить не получилось](image\14.PNG){#fig:014 width=70%}
   
   ![Полярные координаты](image\15.PNG){#fig:015 width=70%}
   
   ![Параметрический график](image\16.PNG){#fig:016 width=70%}
   
   ![Параметрический график в 3д](image\17.PNG){#fig:017 width=70%}
   
   ![Поверхность](image\18.PNG){#fig:018 width=70%}
   
   ![Поверхность](image\19.PNG){#fig:019 width=70%}
   
   ![Линии уровня](image\21.PNG){#fig:021 width=70%}
   
   ![Поверхность](image\22.PNG){#fig:02 width=70%}
   
   ![Анимация](image\23.PNG){#fig:023 width=70%}
   
   ![Гипоциклоида](image\24.PNG){#fig:024 width=70%}
   
   
   
   ![График ошибок](image\25.PNG){#fig:025 width=70%}
   
   ![График ошибок 2 вид](image\26.PNG){#fig:026 width=70%}
   
   ![Ошибки по осям](image\27.PNG){#fig:027 width=70%}
   
   ![Гистограмма](image\28.PNG){#fig:028 width=70%}
   
   ![Множественная гистограмма](image\29.PNG){#fig:029 width=70%}
   
   ![Несколько графиков](image\30.PNG){#fig:030 width=70%}
   
   ![Несколько графиков 2 вид](image\31.PNG){#fig:031 width=70%}
   
   ![Несколько графиков 3 вид](image\32.PNG){#fig:032 width=70%}
   
   ![Несколько графиков с макросом](image\33.PNG){#fig:033 width=70%}
   
   
   
   

## Задания для самостоятельного выполнения

1. Постройте все возможные типы графиков (простые, точечные, гистограммы и т.д.) функции $sin(X), x \in (0..2\pi)$. Отобразите все графики в одном графическом окне.

   ![Sinus](image\34.PNG){#fig:034 width=70%}

2. Постройте графики функции $sin(X), x \in (0..2\pi)$ со всеми возможными (сколько сможете вспомнить) типами оформления линий графика. Отобразите все графики в одном графическом окне.

   ![Кастом графика синуса](image\35.PNG){#fig:035 width=70%}

   

3. Постройте график функции $y = \pi x^2 \ln(x)$ назовите оси соответственно. Пусть цвет рамки будет зелёным, а цвет самого графика — красным. Задайте расстояние между надписями и осями так, чтобы надписи полностью умещались в графическом окне. Задайте шрифт надписей. Задайте частоту отметок на осях координат.

   ![График функции](image\36.PNG){#fig:036 width=70%}

   ![График функции](image\37.PNG){#fig:037 width=70%}

4. Задайте вектор x = (−2, −1, 0, 1, 2). В одном графическом окне (в 4-х подокнах) изобразите графически по точкам 𝑥 значения функции $x^3-3x$ в виде: – точек, – линий, – линий и точек, – кривой. Сохраните полученные изображения в файле figure_familiya.png, где вместо familiya укажите вашу фамилию..

   ![4 вида графика](image\38.PNG){#fig:038 width=70%}

5. Задайте вектор x = (3, 3.1, 3.2, … , 6). Постройте графики функций $y_1=\pi x$ и $y_2 = exp(x)cos(x)$ в указанном диапазоне значений аргумента 𝑥 следующим образом: – постройте оба графика разного цвета на одном рисунке, добавьте легенду и сетку для каждого графика; укажите недостатки у данного построения; – постройте аналогичный график с двумя осями ординат.![На одном графике](image\39.PNG){#fig:039 width=70%}

   ![Разные оси](image\40.PNG){#fig:040 width=70%}

   Здесь, очевидно, удобнее две оси из-за разных масштабов. В первом случае график просто становится линией.

6. Постройте график некоторых экспериментальных данных (придумайте сами), учитывая ошибку измерения.

   ![График ошибок](image\41.PNG){#fig:041 width=70%}

   

7. Постройте точечный график случайных данных. Подпишите оси, легенду, название графика.

   ![Случайные точки трех кластеров](image\42.PNG){#fig:042 width=70%}

   

8. . Постройте 3-мерный точечный график случайных данных. Подпишите оси, легенду, название графика.

   ![Трехмерный случайный график](image\43.PNG){#fig:043 width=70%}

9. Создайте анимацию с построением синусоиды. То есть вы строите последовательность графиков синусоиды, постепенно увеличивая значение аргумента. После соедините их в анимацию. 

   ![Анимация синуса](image\44.PNG){#fig:044 width=70%}

10. Постройте анимированную гипоциклоиду для 2 целых значений модуля к и 2 рациональных значений модуля к.

    ![Целое значение](image\45.PNG){#fig:045 width=70%}

    ![Нецелое значение](image\46.PNG){#fig:046 width=70%}

    В итоге для всех нецелых значений циклоида расходилась, а для целых возвращалась в исходную точку.

11. Постройте анимированную эпициклоиду для 2 целых значений модуля к и 2 рациональных значений модуля к.

    ![Целое значение](image\48.PNG){#fig:047 width=70%}

    ![Целое значение](image\49.PNG){#fig:048 width=70%}

    ![Нецелое значение](image\50.PNG){#fig:049 width=70%}

    Аналогично, циклоида замыкалась для целых значений.

    


# Выводы

В ходе работы был освоен синтаксис языка Julia для построения графиков

# Список литературы{.unnumbered}

::: {#refs}
:::
