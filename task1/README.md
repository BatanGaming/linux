
## 1.    Основные принципы Unix-way
- Одна задача - одна программа
- Есть множество путей решения
- Все есть файл

------------

## 2.  Линус Торвальдс является разработчиком чего

Ядра Linux

------------

## 3.    Как посмотреть  название ядра системы из консоли?

```uname -s```

------------

## 4.    Промежутки измерения загрузки системы для команды uptime следующие

1, 5, 15 минут

------------

## 5.    Какой командой узнать сколько занято на HDD

```df -H``` (флаг H - человеческий вывод)

------------

## 6.    Какие разделы содержит вывод команды vmstat
- procs (количество процессов)
- memory (память)
- swap
- io (загрузка ввода-вывода)
- cpu (загрузка процессора)

------------

## 7.    Описать работу своего Linux дистрибутива: какое ядро, архитектура, размеры hdd, объеме ОЗУ, загрузке процессора и т.д.
1. Ядро, архитектура:

```uname -a```

Linux ubuntu 4.15.0-117-generic #118~16.04.1-Ubuntu SMP Sat Sep 5 23:35:06 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux

2. Размер HDD

```df -H```
```
Filesystem      Size  Used Avail Use% Mounted on
udev            1.1G     0  1.1G   0% /dev
tmpfs           207M  6.5M  201M   4% /run
/dev/sda1        20G  5.2G   14G  28% /
tmpfs           1.1G  218k  1.1G   1% /dev/shm
tmpfs           5.3M  4.1k  5.3M   1% /run/lock
tmpfs           1.1G     0  1.1G   0% /sys/fs/cgroup
tmpfs           207M   78k  207M   1% /run/user/1000
```

4. Объем ОЗУ

```free -h```
```
              total        used        free      shared  buff/cache   available
Mem:           1.9G        732M        189M         16M        1.0G        1.0G
Swap:          974M          0B        974M
```
5. Загрузка процессора

```uptime```
```23:13:34 up 10 min,  1 user,  load average: 0.13, 0.41, 0.41```

------------

## 8. Установить Linux

![linux](https://i.imgur.com/XMdkzrV.png)
