---
layout: page
categories: [courses]
title: ЦОС. Лекция 10. Адаптивные линейные фильтры. Общие понятия.
---

# Основные формы представления нерекурсивных фильтров

Линейный фильтр во времени можно представить в виде свертки для одного отсчета выхода:
\begin{equation}
y_k=\sum_{m=0}^{M-1}c_mx_{k-m} \tag{1a}
\end{equation}

Либо в векторно-матричной форме:
\begin{equation}
\mathbf{y}=\mathbf{X}\mathbf{c}=c_1\mathbf{x}_1+c_2\mathbf{x}_2+\ldots +c_M\mathbf{x}_M \tag{1b}
\end{equation}

