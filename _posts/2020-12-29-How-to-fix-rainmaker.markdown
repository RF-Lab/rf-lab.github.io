---
layout: post
title:  How do I fix the compilation errors seen while building the ESP RainMaker examples.
date:   2020-12-29 18:30
categories: news
---

# How do I fix the compilation errors seen while building the ESP RainMaker examples?

Please ensure that you are using the latest esp-idf master branch and all submodules are in sync. Follow these steps [【Ссылка Espressif】](https://rainmaker.espressif.com/docs/faqs.html)
```
$ cd /path/to/esp-idf
$ git checkout master
$ git pull origin master
$ git submodule update --init --recursive
$ cd - # Come back to esp-rainmaker example
$ idf.py build
```
