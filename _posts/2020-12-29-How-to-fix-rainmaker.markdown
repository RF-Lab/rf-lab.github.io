---
layout: post
title:  Устранение проблем со сборкой ESP RainMaker examples.
date:   2020-12-29 18:30
categories: news
---

# Устранение проблем со сборкой ESP RainMaker examples?

Please ensure that you are using the latest esp-idf master branch and all submodules are in sync. Follow these steps [【How do I fix the compilation errors seen while building the ESP RainMaker examples】](https://rainmaker.espressif.com/docs/faqs.html)
```
$ cd /path/to/esp-idf
$ git checkout master
$ git pull origin master
$ git submodule update --init --recursive
$ cd - # Come back to esp-rainmaker example
$ idf.py build
```

Some issues may also get resolved by clearing the example's build folder and the sdkconfig
```
$ cd /path/to/esp-rainmaker/examples/
$ rm -rf build/ sdkconfig sdkconfig.old
$ idf.py set-target esp32s2
$ idf.py build
```

