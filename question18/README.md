# Билет №18. Полиномиальная и экспоненциальные сложности. Классы P и NP. Полиномиальная сводимость. NP-полные задачи. Примеры.

## Основные термины и обозначения

Параметр $n$ - это некоторое число, от которого зависит работа алгоритма решения задачи (количество городов, количество предметов и т.д.). Время работы алгоритма решения задачи обозначается за $T(n)$.

Полином (многочлен) $P_k(x)$ степени $k$ есть выражение:

$$P_k(x) = c_kx^k + c_{k - 1}x^{k - 1} + … + c_1x + c_0$$

, где $c_j$ - постоянные коэффициенты, $j = 0, …, k$

Будем считать, что $f(x) = O(g(x))$, если существует константа $c > 0$ и $x_0$, что для всех $x > x_0$ выполняется $f(x) \le c \cdot g(x)$. $g(x)$ - оценка сверху функции $f(x)$.

Будем считать, что $f(x) = \Omega(g(x))$, если существует константа $c > 0$ и $x_0$, что для всех $x > x_0$ выполняется $f(x) \ge c \cdot g(x)$. $g(x)$ - оценка снизу функции $f(x)$.

Будем считать, что $f(x) = \Theta(g(x))$, если существует константа $c_1 > 0$, $c_2 > 0$ и $x_0$, что для всех $x > x_0$ выполняется $c_1 \cdot g(x) \ge f(x) \ge c \cdot g(x)$. $g(x)$ - асимптотически точная оценка функции $f(x)$.

## Полиномиальная и экспоненциальные сложности

**Полиномиальный алгоритм** - это алгоритм, время работы $T(n)$ которого, ограничено сверху некоторым полиномом: $T(n) = O(P_k(n))$.

**Экспоненциальный алгоритм** - это алгоритм, время работы $T(n)$ которого, ограничено снизу показательной функцией: $T(n) = \Omega(a^n)$, где $a > 1$.

## Классы P и NP

**Класс P** состоит из задач, для которых существует полиномиальные алгоритмы решения.

**Класс NP** состоит из задач, для которых существует полиномиальные алгоритмы проверки правильности и предъявляемого решения.

Проще говоря, класс P состоит из задач, которые можно быстро решить, а класс NP состоит из задач, которые можно быстро проверить. 

Очевидно включение $P \subset NP$ (для проверки решения задачи класса P достаточно решить ее полиномиальным алгоритмом).

## Примеры

**Задача класса P:**

Требуется определить, есть ли в числовом массиве $A[1, …, n]$ элемент со значением, меньшим, чем $k$. Очевидный алгоритм решения перебирает все элементы массива за время $O(n)$.

**Задача класса NP:**

Задача коммивояжера в постановке задачи разрешимости. Если нам дан некоторый маршрут длиной не более чем $k$, то за время $O(n)$ можно проверить, что он действительно имеет такую длину, тем самым убедиться в его существовании. Для этого необходимо перебрать все $n$, содержащихся в нем переходов между городами и просуммировать их длины. 

# NP-полная задача

**NP-полная задача** - это задача, которая принадлежит классу NP и к ней за полиномиальное время можно свести любую другую задачу этого класса.

Если какая-нибудь NP-полная задача имеет полиномиальный алгоритм решения, то все NP-полные задачи полиномиально разрешимы и, как следствие, $P = NP$ (за полиномиальное время разрешимы все задачи класса NP).

NP-полные задачи являются наиболее трудными в классе NP. Ни для одной из них никому не удавалось построить полиномиальный алгоритм решения. Из чего можно сделать вывод, что $P \neq NP$

## Примеры

1. Выполнимость конъюнкции нескольких дизъюнкций
2. Выполнимость булевой формулы
3. Выполнимость формулы из класса 3-конъюнктивных нормальных форм
4. Задача о клике
5. Задача о вершинном покрытии
6. Задача о суммах подмножеств
7. Задача о гамильтоновом цикле
8. Задача коммивояжера
9. Задача о независимом множестве
10. Задача о раскраске графа

---
## Создатель

Автор расписанного билета: Куусела Демид

Кто проверил: 

## Ресурсы
???
