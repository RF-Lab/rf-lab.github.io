---
layout: page
categories: [courses]
title: ЦОС. Лекция 11. Устойчивость алгоритма градиентного спуска.
---

# Критерий оптимизации линейного фильтра

Ошибку на выходе линейного фильтра можно представить в виде:
\begin{equation}
\mathbf{\varepsilon}=\mathbf{y}-\mathbf{X}\mathbf{c} \tag{1}
\end{equation}
Здесь 
* $\mathbf{y}$ - желаемый (заданный) выход фильтра (вектор-столбец, размера $N$).
* $\mathbf{X}$ - матрица входного процесса ($N\times M$).
* $\mathbf{c}$ - вектор коэффициентов (вектор-столбец, размера $N$).

Квадритичный критерий (сумма квадратов ошибок):
\begin{equation}
P=\pbm{\varepsilon}^2=\left(\mathbf{y}-\mathbf{X}\mathbf{c}\right)^T\left(\mathbf{y}-\mathbf{X}\mathbf{c}\right) \tag{2}
\end{equation}
