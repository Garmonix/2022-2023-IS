---
## Front matter
title: "Лабораторная работа  №2"
subtitle: "Шифры перестановки"
author: "Якушевич Артём Юрьевич"

## Generic options
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

Ознакомиться с шифрами перестановки и обучиться их программной реализации.

# Задание

- Реализовать шифрование столбцовой перестановки;
- Реализовать таблицу виженера.

# Теоретическое введение

При подготовке использовалась методичка со страницы курса в ТУИС.[@tuis:ru]

Шифрование столбцовой перестановки. Криптограмма получается выписыванием букв из таблицы в соответствии с некоторым маршрутом.
Ключом такой криптограммы является марштур и числа m и n. Внизу таблицы приписывается слово из n неповторющихся букв и столбцы
нумеруются по алфавитному порядку букв пароля.

Шифрование столбцовой перестановки (рис. [-@fig:001]):

![Шифрование столбцовой перестановки](image/1.png){ #fig:001 width=70% }

Таблица Виженера. Его принцип в том, что каждая буква в исходном шифруемом тексте сдвигается по алфавиту не на фиксированное,
а переменное количество символов. Величина сдвига каждой буквы задается ключом (паролем) - секретным словом или фразой, 
которая используется для шифрования и расшифровки. (рис. [-@fig:002]):

![Таблица Виженера](image/2.png){ #fig:002 width=70% }

# Выполнение лабораторной работы

Работа была выполнена на языке программирования Python.

Сначала реализуем шифрование столбцовой перестановки (рис. [-@fig:003]):

![шифрование столбцовой перестановки](image/3.png){ #fig:003 width=70% }

Сначала реализуем шифрование столбцовой перестановки (рис. [-@fig:004]):

![шифрование столбцовой перестановки](image/4.png){ #fig:004 width=70% }

Вывод программы (рис. [-@fig:005]):

![Вывод программы](image/5.png){ #fig:005 width=70% }

Реализация таблицы Виженера (рис. [-@fig:006]):

![таблица Виженера](image/6.png){ #fig:006 width=70% }

Вывод программы (рис. [-@fig:007]):

![Вывод программы](image/7.png){ #fig:007 width=70% }

# Выводы

Ознакомился с шифрами перестановки и обучился их программной реализации.

# Список литературы{.unnumbered}

::: {#refs}
:::
