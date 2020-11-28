---
layout: page
categories: [courses]
title: ЦОС. Лекция 10. Адаптивные линейные фильтры. Общие понятия.
---

### Основные формы представления нерекурсивных фильтров

Линейный фильтр во времени можно представить в виде свертки для одного отсчета выхода:
\begin{equation}
y_k=\sum_{m=0}^{M-1}c_mx_{k-m} \tag{1a}
\end{equation}

Либо в векторно-матричной форме:
\begin{equation}
\mathbf{y}=\mathbf{X}\mathbf{c}=c_1\mathbf{x}_1+c_2\mathbf{x}_2+\ldots +c_M\mathbf{x}_M \tag{1b}
\end{equation}

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


### Градиент

Градиент от (4):
\begin{equation}
\nabla P(\mathbf{c})=\mathbf{A}\mathbf{c}+\mathbf{d} \tag{3}
\end{equation}

### GDA алгоритм

Метод градиентного спуска:
\begin{equation}
\mathbf{c}_{n+1} = \mathbf{c}_n - \mu \nabla P(\mathbf{c}) = \mathbf{c}_n - \left[\mathbf{A}\mathbf{c}+\mathbf{d}\right] \tag{4}
\end{equation}

