---
layout: page
categories: [courses]
usemathjax: true
title: ЦОС. Лекция 10. Адаптивные линейные фильтры. Общие понятия.
---

# Основные формы представления нерекурсивных фильтров

Линейный фильтр во времени можно представить в виде свертки для одного отсчета выхода:
$$
\begin{equation}
y_k=\sum_{m=0}^{M-1}c_mx_{k-m}\tag{1}
\end{equation}
$$

Либо в векторно-матричной форме:
$$
\begin{equation}
\boldsymbol{y}=\boldsymbol{X}\boldsymbol{c}\tag{a}
\end{equation}
$$

