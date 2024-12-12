---
## Front matter
title: "Отчёт по лабораторной работе №10"
subtitle: "Дисциплина: Архитектура компьютера"
author: "Бражко Александра Александровна"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Приобретение навыков написания программ для работы с файлами.

# Задание

1. Выполнение лабораторной работы
2. Выполнение самостоятельной работы

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

Создаём каталог для программ лабораторной работы № 10, переходим в него и создаём файлы lab10-1.asm, readme-1.txt и readme-2.txt (рис. [-@fig:001]).

![Создание каталогов и файлов](image/10.1.png){#fig:001 width=70%}

Вводим в файл lab10-1.asm текст программы из листинга 10.1 (рис. [-@fig:002]).

![Ввод листинга](image/10.2.png){#fig:002 width=70%}

Создаём исполняемый файл и проверяем его работу (рис. [-@fig:003]).

![Создание и проверка](image/10.3.png){#fig:003 width=70%}

С помощью команды chmod изменим права доступа к исполняемому файлу lab10-1,
запретив его выполнение. Выдало отказ в доступе, как и следовало ожидать, так как мы запретили запускать программу для владельца, то есть для себя (рис. [-@fig:004]).

![Изменение прав](image/10.4.png){#fig:004 width=70%}

С помощью команды chmod измените права доступа к файлу lab10-1.asm с исходным
текстом программы, добавив права на исполнение. Программа заработала, 
так как файл был со всеми разрешениями и до этого мы запретили выполняться уже готовой программе, 
а это фактически новая программа которая обладает другими разрешениями, 
поэтому она и запустилась (рис. [-@fig:005]).

![Изменение прав](image/10.5.png){#fig:005 width=70%}

В соответствии с вариантом (у меня вариант 8) в таблице 10.4 предоставим права доступа к файлу readme-1.txt 
представленные в символьном виде. Проверим правильность выполнения с помощью команды ls -l (рис. [-@fig:006]).

![Предоставление прав и проверка](image/10.6.png){#fig:006 width=70%}

Предоставим права доступа к файлу readme-2.txt представленные в двочном виде.
Проверим правильность выполнения с помощью команды ls -l (рис. [-@fig:007]).

![Предоставление прав и проверка](image/10.7.png){#fig:007 width=70%}

# Выполнение самостоятельной работы

Пишем программу, которая запрашивает имя и выводит его в созданном файле. Файл создает сама программа. (рис. [-@fig:008]).

![Написание и выполнение программы](image/10.8.png){#fig:008 width=70%}

# Выводы

Я приобрела навыки написания программ для работы с файлами.

# Список литературы{.unnumbered}

::: {#refs}
:::
