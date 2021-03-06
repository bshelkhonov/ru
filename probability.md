# Ликбез по теорверу

Эта статья представляет собой выжимку самых интересных фактов и «больших идей» теорвера, которые обычно рассказывают на курсах статистики, машинного обучения и теории информации.

```python
import numpy as np

import matplotlib as plt
%matplotlib inline

import seaborn as sns
sns.set()
```
## Плотность распределения

Пусть есть некоторая случайная величина $X$. *Плотностью распределения* $X$ называется функция $p(x)$, отражающая относительную вероятность наступления события $X=x$ (то есть относительно всех остальных возможных событий). Например, для случайной величины с конечным множеством элементарных исходов $\Omega$ $p(x)=P(X=x)$ (где $P(A)$ - вероятность наступления события $A$). Обычно функция плотности вероятности предполагается нормированной на единицу (то есть площадь под графиком равна 1). *Функцией распределения* случайной численной величины $F(x)$ называется вероятность попадания $X$ в луч $(-\infty;\,x]$ (или $\int_{-\infty}^{x}p(x)\,dx$). 

## Матожидание

Предположим, у нас есть случайная численная величина $X$ с функцией плотности $p(x)$. Тогда математическое ожидание случайной величины равно сумме $P(A) \cdot A$ для всех возможных исходов $A$. TODO

## Дисперсия

Какие два числа лучше всего описывают распределение?

## Нормальное распределение

Центральная предельная теорема названа так пафосно вполне обоснованно.

Она говорит, что нам достаточно про каждое слагаемое знать всего два числа — ожидание и дисперсию.

$$ f(x) = \frac{1}{2\sqrt{\pi}} e^{-\frac{(x-\mu)^2}{\sigma^2}} $$

Доказать это очень трудно. Даже со ссылками на мощные теоремы оно займёт не одну страницу. Обычно доказательство рассказывают в середине второго курса.

Трудно даже доказать, что это распределение, т. е. что.

## Применения

Пусть в некоторой стране есть два кандидата в президенты, назовём их Путин и Навальный.

Мы спросили у 1000 случайных избирателей бинарный вопрос, и 510 из них сказали, что будут голосовать за Путина. С какой вероятностью он победит? Теорема говорит, что число голосов, как 

## Линейные рекурренты

Чтобы решать следующие задачи, нам нужно будет использовать следующий факт:

...

Доказательство мы не приведем.

В частности, таким образом получается формула для чисел Фибоначчи.

$$ f_n = \ldots $$

Кто бы мог подумать, что все эти иррациональности и степени сократятся и вообще дадут целое число?..

## Классика

Парадокс дней рождения.

Это на самом деле очень часто используемый результат. Так можно считать вероятность коллизии хэшей, а также он используется во многих теоретико-числовых алгоритмах, в которых используется предположения (весьма справедливые) о распределении простых чисел.

Пьяница. Человек стоит на краю обрава и идёт в его сторону с вероятностью p. С какой вероятностью он когда-либо в него упадёт?

TODO: история про эстетическое удовольствие, азарт и смысл посещения казино.
Казино. Мы приходим в казино с 1000\$ и следующим образом проводим там время: ставим по 1\$, пока не обанкротимся или не выиграем 1100\$. Какая вероятность того, что мы уйдём с деньгами?

## Принцип максимального правдоподобия

## Энтропия

Энтропией называется минимальное число бит, которым теоретически возможно сжать сообщение. Эта величина важна, потому что на практике если её можно посчитать, то сжатие с соответствующей кратностью реально достижимо.

Шумный канал.

Пусть у вас есть 1тб данных и два китайских терабайтника, на каждый из которых можно записать столько данных, но каждый бит имеет вероятность 10% записаться на противоположный. Требуется сохранить данные с первого раза без потерь. Совсем без потерь.

Причём это делается почти впритык.
