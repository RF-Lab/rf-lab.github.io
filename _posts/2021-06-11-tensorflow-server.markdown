---
layout: post
title:  Выполнение графа TensorFlow на сервере
date:   2021-06-11 14:20
categories: news
---
## TensorFlow Server

Если локальная машина, на которой создается код TensorFlow, не обладает достаточными вычислительными ресурсами, но есть сервер с большими мощностями, то можно делать так:

На сервере устанавливаем Python и TensorFlow. Создаем и запускаем следующий скрипт на питоне:

```
import tensorflow as tf

cluster_spec = tf.train.ClusterSpec({
    "worker": [
        "remotehost:2222"
        ],
    "ps": [
        "remotehost:2221"
        ]
    })


ps = tf.distribute.Server(cluster_spec, job_name="ps", task_index=0)
worker = tf.distribute.Server(cluster_spec, job_name="worker", task_index=0)

ps.join()
worker.join()
```

remotehost меняем на IP-адрес сервера. 

На клиенте присоединяемся к серверу с помощью вызова:

```
tf.config.experimental_connect_to_host(remote_host='remotehost:2222', job_name='worker')
with tf.device(remote resource):
```

remote resource можно выбрать из списка ресурсов на сервере. Они выводятся при запуске серверной части в окне терминала.

[Ссылка на электронный ресурс.](https://stackoverflow.com/questions/64067606/train-a-model-using-keras-and-remote-tesorflow)
