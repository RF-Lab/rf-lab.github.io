---
layout: page
categories: [courses]
title: ЦОС. Лекция 11. Устойчивость алгоритма градиентного спуска.
---

# Критерий оптимизации линейного фильтра

Ошибку на выходе линейного фильтра можно представить в виде:
\begin{equation}
\pmb{\varepsilon}=\mathbf{y}-\mathbf{X}\mathbf{c} \tag{1}
\end{equation}
Здесь 
* $\mathbf{y}$ - желаемый (заданный) выход фильтра (вектор-столбец, размера $N$).
* $\mathbf{X}$ - матрица входного процесса ($N\times M$).
* $\mathbf{c}$ - вектор коэффициентов (вектор-столбец, размера $N$).

Квадритичный критерий (сумма квадратов ошибок):
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

Градиент от (4):
\begin{equation}
\nabla P(\mathbf{c})=\mathbf{A}\mathbf{c}+\mathbf{d} \tag{4}
\end{equation}

