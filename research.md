---
layout: page
title: Темы
permalink: /research/
---

## Разработка программно-математических средств для распознавания сигналов электромиографии. 

### Что такое электромиография и зачем она нужна
[Распознавание жестов (биотехнические интерфейсы)](https://www.youtube.com/watch?v=mkEL9Fm22J4)

[Распознавание с помощью старого красного носка и NVidia Tegra](https://www.youtube.com/watch?v=OY_BMnhqeok)

[В спорте](https://www.youtube.com/watch?v=Ix561IWFEso)

Вы можете найти кучу аналогичных примеров.

### Книги 
Roberto Merletti Dario Farina    Surface Electromyography : Physiology, Engineering, and Applications. Copyright © 2016 by The Institute of Electricaland Electronics Engineers, Inc.

### Google, Youtube, Yandex и т.п.
Ищите EMG Gesture recognition

### Capacitive EMG (бесконтактная ЭМГ для одежды)
[Parin Dedhia (prd47), Roland Krieger (rk447), Nini Munoz (nlm9) CAPACITIVELY COUPLED EMG ELECTRODES WITH FINGER GESTURE RECOGNITION](https://people.ece.cornell.edu/land/courses/ece5030/FinalProjects/s2013/prd47_nlm9_rk447/Capacitive%20EMG%20electrode/CapacitiveEMGElectrode.html)

### На основе метода опорных векторов
Эта тема самая популярная на нашей кафедре. Но настал момент двигаться дальше. 

### На основе методов глубокого обучения
Цель: Определение структуры нейронной сети для распознавания сигналов ЭМГ. 
В основе данного исследования должна лежать какая-то гипотеза о структуре сигнала ЭМГ или о способе его формирования. 
Полагаясь на эту гипотезу можно предположить сколько необходимо иметь слоев, какие должны быть слои и т.п.
Пример гипотезы: можно обучить сеть на одном человеке и получить универсальный до некоторой степени набор признаков (bottleneck).
Для использования этой сети на другом человеке необходимо лишь переобучить выходной слой - softmax или SVM.
1. [Nils Ackermann Introduction to 1D Convolutional Neural Networks in Keras for Time Sequences (https://blog.goodaudience.com)](https://blog.goodaudience.com/introduction-to-1d-convolutional-neural-networks-in-keras-for-time-sequences-3a7ff801a2cf).
2. [Rita Laezza Deep Neural Networks
for Myoelectric Pattern Recognition](http://publications.lib.chalmers.se/records/fulltext/254980/254980.pdf)

### С использованием автокодирования
Цель: поиск Bottleneck вектора (вектора классификационных признаков) для сигнала ЭМГ. Такой вектор может быть получен путем некоторого преобразования входного сигнала ЭМГ, в данном случае это преобразование выполняет многослойная нейронная сеть. 
1. [Marwa Farouk Ibrahim Ibrahim*
, Adel Ali Al-Jumaily](https://www.astesj.com/publications/ASTESJ_030111.pdf).
2. [Martin Sp¨uler Extracting Muscle Synergy Patterns from EMG
Data Using Autoencoders](https://www.researchgate.net/publication/306081011_Extracting_Muscle_Synergy_Patterns_from_EMG_Data_Using_Autoencoders/download)

### На основе метода Random Forest
1. [Модель Random Forest для классификации, реализация на c#. habr](https://habr.com/post/215453/)
2. [David Rodriguez A Neural Decision Forest Scheme with Application
to EMG Gesture Classification](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7555990)

### Классификация EMG с использованием Ensemble Classifiers
Сейчас нет информации по этому направлению.

### На основе математических моделей EMG сигнала
Определение классификационных признаков на основе математической модели сигнала ЭМГ.
D. Farina ; A. Crosetti ; R. Merletti A model for the generation of synthetic intramuscular EMG signals to test decomposition algorithms. [link](https://ieeexplore.ieee.org/document/900250)

### Мокрая биология
Имеется в виду работа с оборудованием для ЭМГ. На защиту может выноситься только в составе работы, железячников наша кафедра не выпускает!
1. Анализ мышечной усталости. Проведение серии экспериментов во времени по измерению ЭМГ сигнала без перемещения электродов.
Идеальный результат - построение примерной модели которая может объяснять изменения в ЭМГ вследствие нагрузки на мышцу. Еще лучше если удастся это скомпенсировать.
2. Анализ зависимости ЭМГ сигнала от человека. Проведение серии экспериментов на разных людях. необходимо правильно организовать 
эксперимент. Цель -поиск классификационных признаков не зависящих от человека.

### EMG signal processing platform
Здесь вы можете посмотреть на то что уже сделано в этом направлении на кафедре.
[EMG signal processing platform](https://github.com/RF-Lab/emg_platform)

## Обнаружение шумоподобных сигналов на основе методов параметрического спектрального анализа 
Процедура обнаружения сигнала в системах с кодовым разделением доступа (пример- GPS, CDMA) является одной из наиболее затратных составляющих частей современного цифрового приемника. Использование авторегрессионных моделей вместо традиционных алгоритмов на основе метода максимального правдоподобия позволяет существенно снизить вычислительные затраты и продлить время автономной работы мобильных беспроводных устройств.

## Реализация системы передачи данных на базе CMOS сенсора
Takaya Yamazato, Image-Sensor-Based Visible Light Communication for Automotive Applications. - [VISIBLE LIGHT COMMUNICATIONS, IEEE Communications Magazine, July 2014]( http://www.comsoc.org/files/Publications/Tech%20Focus/2015/auto/1.pdf)www.comsoc.org

## Реализация упрощенной системы позиционирования на базе акселерометра
[Implementing Positioning Algorithms Using
Accelerometers, freescale](http://cache.freescale.com/files/sensors/doc/app_note/AN3397.pdf?fsrch=1&sr=2)

