---
layout: page
categories: [courses]
title: ЦОС. Лекция 11. Устойчивость алгоритма градиентного спуска.
---

### Критерий оптимизации линейного фильтра

Ошибку на выходе линейного фильтра можно представить в виде:
\begin{equation}
\pmb{\varepsilon}=\mathbf{y}-\mathbf{X}\mathbf{c} \tag{1}
\end{equation}
Здесь 
* $\mathbf{y}$ - желаемый (заданный) выход фильтра (вектор-столбец, размера $N$).
* $\mathbf{X}$ - матрица входного процесса ($N\times M$).
* $\mathbf{c}$ - вектор коэффициентов (вектор-столбец, размера $N$).

Квадратичный критерий (сумма квадратов ошибок):
\begin{equation}
P=\pmb{\varepsilon}^2=\left(\mathbf{y}-\mathbf{X}\mathbf{c}\right)^T\left(\mathbf{y}-\mathbf{X}\mathbf{c}\right) \tag{2}
\end{equation}

Раскрывая скобки, получим:
\begin{equation}
P=\left(\mathbf{y}^T-\mathbf{c}^T\mathbf{X}^T\right)\left(\mathbf{y}-\mathbf{X}\mathbf{c}\right) = \\
\mathbf{y}^T\mathbf{y} - \mathbf{y}^T\mathbf{X}\mathbf{c} -\mathbf{c}^T\mathbf{X}^T\mathbf{y} + \mathbf{c}^T\mathbf{X}^T\mathbf{X}\mathbf{c}= \\ 
\mathbf{c}^T\mathbf{X}^T\mathbf{X}\mathbf{c} - 2\mathbf{y}^T\mathbf{X}\mathbf{c} + \mathbf{y}^T\mathbf{y}
\tag{3}
\end{equation}

Введем обозначения:
\begin{equation}
\frac{1}{2}\mathbf{A}=\mathbf{X}^T\mathbf{X}
\end{equation}
\begin{equation}
\mathbf{d} = -2\mathbf{X}^T\mathbf{y}
\end{equation}
\begin{equation}
h = \mathbf{y}^T\mathbf{y}
\end{equation}

Тогда выражение (3) можно представить в виде:
\begin{equation}
P=\pmb{\varepsilon}^2=\frac{1}{2}\mathbf{c}^T\mathbf{A}\mathbf{c}+\mathbf{d}^T\mathbf{c}+h \tag{4}
\end{equation}

### Градиент

Градиент от (4):
\begin{equation}
\nabla P(\mathbf{c})=\mathbf{A}\mathbf{c}+\mathbf{d} \tag{5}
\end{equation}

### GDA алгоритм

Метод градиентного спуска:
\begin{equation}
\mathbf{c}_{n+1} = \mathbf{c}_n - \mu \nabla P(\mathbf{c}) = \mathbf{c}_n - \left[\mathbf{A}\mathbf{c}+\mathbf{d}\right] \tag{6}
\end{equation}

Или:
\begin{equation}
\mathbf{c}_{n+1} = \left[\mathbf{E}-\mu \mathbf{A}\right]\mathbf{c}_n - \mu\mathbf{d}  \tag{7*}
\end{equation}

### Предельная скорость GDA

Выражение (7*) определяет рекурсивный фильтр. Здесь $\left[\mathbf{E}-\mu \mathbf{A}\right]$ - матрица динамики фильтра. 
Известно, что такая система будет устойчивой, если все собственные числа матрицы $\left[\mathbf{E}-\mu \mathbf{A}\right]$ по модулю меньше единицы (лежат внутри единичной окружности).

### Собственные числа матрицы

Вспомним, что вектор $\mathbf{x}$ называется собственным вектором матрицы $\mathbf{F}$, если существует скаляр $\lambda$, т.ч.
\begin{equation}
\mathbf{F}\mathbf{x} = \lambda \mathbf{x} \tag{e1}
\end{equation}

Или 
\begin{equation}
\mathbf{F}\mathbf{x} - \lambda \mathbf{x} = 0 \tag{e2}
\end{equation}

\begin{equation}
\left[\mathbf{F}-\mathbf{E}\lambda\right]\mathbf{x} = 0 \tag{e3}
\end{equation}

Случай $\mathbf{x}=0$ - тривиальный, не представляет интереса.

Уравнение (e3) разрешимо для ненулевого $\mathbf{x}$, только тогда, когда матрица $\mathbf{F}$ вырождена (почему?).

Тогда для определения собственных значений необходимо найти корни уравнения:
\begin{equation}
det\left[\mathbf{F}-\mathbf{E}\lambda\right] = 0 \tag{e4}
\end{equation}

Пример:
\begin{equation}
F=
\begin{array}{cc}
3 & 1 \\
1 & 3
\end{array}
\end{equation}

