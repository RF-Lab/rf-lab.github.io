---
layout: post
title:  Новости EMG8xR2
date:   2020-10-11 22:02
categories: news
---
### Закончил правки схемы для EMG8xR2

Revision 2 будет полностью сделан на opensource'e. Схема и разводка платы будет выполнена в [KiCAD](https://kicad-pcb.org/).

Пока закончил схему. Все не быстро, но надеюсь дальше наверстать. Старые ошибки исправил, добавил новые фичи:
* Полностью дифференциальный интерфейс с раздельными входными фильтрами (как в [EEG Front-End Performance Demonstration Kit](https://www.ti.com/lit/ug/slau443b/slau443b.pdf?ts=1602258946892&ref_url=https%253A%252F%252Fwww.ti.com%252Ftool%252FADS1299EEGFE-PDK))
* Полностью дифференциальный интерфейс с общим фильтром (как в [Datasheet ADS1299](https://www.ti.com/lit/ds/symlink/ads1299.pdf?ts=1602417721400))
* Третий электрод теперь можно завести на GNDA, на сигнал смещения или на общий электрод.
* Интерфейс с одним общим электродом (меньше проводов).
* Питание от двух аккумуляторов Li-Ion 18650.

Главное теперь не добавить новых ошибок.

![Схема (KiCAD Eeschema)](https://drive.google.com/uc?export=view&id=18xvGgrcY3SdtwbyLzkZvpchL3RI9LBVP)
