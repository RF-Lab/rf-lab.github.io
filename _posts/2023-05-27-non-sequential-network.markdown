---
layout: post
title:  Создание сети с произвольной структурой в keras.
date:   2023-05-26 15:00
categories: news
---

Для примера создадим сеть с двумы входами и одним выходом. Первй вход будет скалярным второй векторным. Векторный вход будет обрабатываться с помощью сверточной многослойной сети
а скалярный вход будет пробрасываться на выходной полносвязный слой минуя сверточные слои.

# 1. Наследуем собственный класс от класса keras.model

``````
class MyModel(tf.keras.Model):
  def __init__(self):
    super(MyModel, self).__init__()
    self.conv1 = tf.keras.layers.Conv1d(50, 50, activation=tf.nn.relu)
    self.dense = tf.keras.layers.Dense(1)

  def call(self, inputs):
    x = self.conv1(inputs[:,:-1]) # сигнал
    a = inputs[:,-1:] # скаляр
    x = self.dense(tf.concat([x,a],axis=1))
    return x
``````
