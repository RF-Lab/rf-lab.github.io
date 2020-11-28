---
layout: page
categories: [courses]
title: ЦОС. Лекция 10. Адаптивные линейные фильтры. Общие определения.
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

### Зачем нам нужны адаптивные фильтры?!
Рассмотрим пример использования адаптивного фильтра в системе компенсации дальнего эхо-сигнала (сотовая связь, skype, Discord,...).
![EchoCompensationScheme](https://drive.google.com/uc?export=view&id=1JUDjNms5voS-LshRlNdYck4sScOl6Aqf)

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
\nabla P(\mathbf{c})=\left(\frac{\partial P}{\partial c_1},\frac{\partial P}{\partial c_2},\ldots,\frac{\partial P}{\partial c_M}\right) \tag{3}
\end{equation}

### GDA алгоритм

Метод градиентного спуска:
\begin{equation}
\mathbf{c}_{n+1} = \mathbf{c}_n - \mu \nabla P(\mathbf{c}) \tag{4}
\end{equation}

### Основные алгоритмы адаптации коэффициентов
* Метод наименьших квадратов - LS - требует обращения корреляционной матрицы.
* Метод градиентного спуска (метод наискорейшего спуска) - GDA(Gradient Descent Algorithm). - На практике редко применяется ввиду большой вычислительной сложности.
* Метод стохастического градиента - LMS(least mean squares). Bernard Widrow, Ted Hoff. 1960, Stanford University.
* Рекурсивный алгоритм наименьших квадратов - RLS - (Matrix Inversion Lemma). - Оригинальная работа Гаусса(1821), повторно исследован R. L. PLACKETT SOME THEOREMS IN LEAST SQUARES - University of Liverpool.
* Фильтр Калмана - A New Approach to Linear Filtering and Prediction Problems. 1960. Research Institute for Advanced Study,2 Baltimore, Md.

