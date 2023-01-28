---
layout: post
title:  Библиотека Plotly для подготовки результатов моделирования.
date:   2023-01-27 10:00
categories: news
---


## Plotly

При оформлении материалов для статей, дипломов и т.п. для отрисовки графиков и диаграмм рекомендую использовать библиотеку 
[Plotly Open Source Graphing Library for Python](https://plotly.com/python/) вместо любимой всеми matplotlib. Пример использования:

``````
import numpy as np
import plotly.graph_objects as go
import plotly.io as pio
pio.templates.default = 'presentation'

x = np.linspace( -10*np.pi, 10*np.pi, 1000 )
y = np.sin( x )/x
u = np.exp( -0.1*np.square(x) )

fig = go.Figure()
fig.add_trace( go.Scatter( x=x, y=y, name=r'$f(x)=\frac{\sin(x)}{x}$' ) )
fig.add_trace( go.Scatter( x=x, y=u, name=r'$f(x)=e^{-x^2}$' ) )
fig.add_annotation( x=0.0, y=1, 
  text=r'$\text{Разрыв второго рода в функции }f(x)=\frac{\sin(x)}{x}$', 
  font=dict(color='green') )
fig.update_layout( xaxis_title=r'$x$', yaxis_title=r'$f(x)$' )
``````
Результат можно получить в виде html файла с интерактивным содержимым (при просмотре этого файла можно изменять масштаб, сохранять в виде изображения, click по легенде позволяет выключать выборочно графики). Выбор формата html не случаен - флагманский продукт компании Plotly Technologies Inc это [Plotly Dash Enterprise](https://dash.gallery/Portal/) либо (Dash Open Source)[https://dash.plotly.com/], которые можно использовать для быстрой разработки Web приложений.

``````
fig.write_html('sin.html',include_mathjax='cdn')
``````

{% include plotly_example1.html %}



