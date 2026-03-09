University: ITMO University  
Faculty: FTMI  
Course: Intro Web Technologies  
Year: 2025/2026  
Group: U4125  
Author: Diana Pukhova  
Lab: Lab0  
Date of create: 27.02.2026  
Date of finished: 20.03.2026

Description of laboratory work 3. 

---

# Lab 2 Report: CI/CD для Docker приложения

## Цель работы  

Научиться настраивать локальную систему мониторинга, собирать метрики с помощью Prometheus и создавать дашборды в Grafana для визуализации данных.  

---

## Ход работы  

Настройка Prometheus

Создала папку `prometheus` для конфигурации.
![Папка](images/Lab3_0.png)
    
Создала файл `prometheus/prometheus.yml`
![Файл](images/Lab3_1.png)
   
Контейнер Node Exporter запущен и проверен
![Контейнер](images/Lab3_2.png)

Запустила Prometheus: создала том для данных, создала общую сеть для мониторинга, контейнер Prometheus запущен и проверен
![Контейнер](images/Lab3_3.png)

Запустила Grafana: cоздала том для данных, контейнер Grafana запущен и проверен
![Контейнер](images/Lab3_4.png)
![Контейнер](images/Lab3_5.png)
![Контейнер](images/Lab3_6.png)

Настройка Grafana: добавила источник данных Prometheus, создала Dashboard с тремя панелями, графики отображают текущее использование CPU, RAM и диска. Панели обновляются автоматически каждые 15 секунд.
![Контейнер](images/Lab3_7.png)
![Контейнер](images/Lab3_8.png)
![Контейнер](images/Lab3_9.png)
![Контейнер](images/Lab3_10.png)

Проверила контейнеры, все контейнеры запущены: Prometheus, Node Exporter, Grafana.
Проверка метрик:
Prometheus: http://localhost:9090/targets → все цели UP
Node Exporter: http://localhost:9100/metrics → метрики собираются
Grafana: Dashboard с графиками CPU, памяти и диска отображается корректно
![Контейнер](images/Lab3_11.png)

# Вывод
Настроена локальная система мониторинга с использованием Prometheus и Grafana.
Метрики собираются с Node Exporter, визуализируются на Dashboard Grafana.
Созданы панели для CPU, памяти и диска, настроены единицы измерения и графики.
Система мониторинга полностью готова к использованию и тестированию веб-приложений.
