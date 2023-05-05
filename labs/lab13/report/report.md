---
## Front matter
title: "Лабораторная работа №13"
subtitle: "Средства, применяемые при
разработке программного обеспечения в ОС типа UNIX/Linux"
author: "Салькова Кристина Михайловна"

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

Приобрести простейшие навыки разработки, анализа, тестирования и отладки при-
ложений в ОС типа UNIX/Linux на примере создания на языке программирования
С калькулятора с простейшими функциями.

# Задание

1. В домашнем каталоге создайте подкаталог ~/work/os/lab_prog.
2. Создайте в нём файлы: calculate.h, calculate.c, main.c.
Это будет примитивнейший калькулятор, способный складывать, вычитать, умножать
и делить, возводить число в степень, брать квадратный корень, вычислять sin, cos, tan.
При запуске он будет запрашивать первое число, операцию, второе число. После этого
программа выведет результат и остановится.
- Реализация функций калькулятора в файле calculate.c
- Интерфейсный файл calculate.h, описывающий формат вызова функции-
калькулятора
- Основной файл main.c, реализующий интерфейс пользователя к калькулятору
3. Выполните компиляцию программы посредством gcc
4. При необходимости исправьте синтаксические ошибки.
5. Создайте Makefile со следующим содержанием
6. С помощью gdb выполните отладку программы calcul (перед использованием gdb
исправьте Makefile):
- Запустите отладчик GDB, загрузив в него программу для отладки
# Теоретическое введение

# Выполнение лабораторной работы

1. В домашнем каталоге создадим подкаталог ~/work/os/lab_prog.

![создание подкаталога](image/1.png){#fig:001 width=50%}

2. Создайте в нём файлы: calculate.h, calculate.c, main.c.

![создание файлов](image/2.png){#fig:001 width=50%}

- Реализация функций калькулятора в файле calculate.c

![реализация calculate.c(1)](image/3.png){#fig:001 width=50%}

![реализация calculate.c(2)](image/4.png){#fig:001 width=50%}

- Интерфейсный файл calculate.h, описывающий формат вызова функции-
калькулятора

![ calculate.h](image/5.png){#fig:001 width=50%}

- Основной файл main.c, реализующий интерфейс пользователя к калькулятору

![main.c](image/6.png){#fig:001 width=50%}

3. Выполните компиляцию программы посредством gcc

![выполнение компиляции](image/7.png){#fig:001 width=50%}

4. Видим, что существуют некоторые ошибки и исправляем их

5. Создадим Makefile

![создание makefile](image/11.png){#fig:001 width=50%}

6. Исправление makefile

![исправление makefile](image/9.png){#fig:001 width=50%}

7. С помощью gdb выполним отладку программы calcul 

- Запустите отладчик GDB, загрузив в него программу для отладки

![запустим gdb](image/10.png){#fig:001 width=50%}


# Выводы

Мы приобрели простейшие навыки разработки, анализа, тестирования и отладки при-
ложений в ОС типа UNIX/Linux на примере создания на языке программирования
С калькулятора с простейшими функциями.

# Список литературы{.unnumbered}

::: {#refs}
:::
