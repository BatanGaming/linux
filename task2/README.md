## 1. Каков размер MBR из чего он состоит?
Размер 512 байт. Состоит из кода загрузчика и таблицы разделов.
## 2. Сколько разделов поддерживает MBR
4
## 3. Описать процесс загрузки все этапы на bios и uefi

 - BIOS
	 - Выполняется POST (Power-on self test);
	 - Считывается MBR;
	 - В память загружается первичный загрузчик и запускается;
	 - В память загружается вторичный загрузчик и запускается;
	 - Запускается ОС.
 - UEFI
	 - Фаза SEC (Security) (инициализация процессора);
	 - Фаза PEI (Pre EFI Initialization) (инициализация памяти);
	 - Фаза DXE (Driver Execution Environment) (инициализация драйверов);
	 - Фаза BDS (Boot Device Selection) (загрузка UEFI приложения с устройства загрузки).

## 4. Описать порядок загрузки ОС на sysVinit и systemd

 - sysVinit
	 - Запускается `/etc/init.d/rcS`;
	 - Запускается `/etc/init.d/rc`, которому передается уровень запуска от 0 до 6;
	 - Просматривается каталог `_/etc/rc*.d` (где * - уровень запуска), в котором содержаться ссылки на скрипты запуска системных служб, которые находятся в `/etc/init.d/`;
	 - Ссылки имеют следующий формат: `<S|K><число><имя_службы>`, в котором: **S** - запуск службы, **K** - остановка службы, **<число>** - число, определяющее последовательность запуска служб, **<имя_службы>** -имя запускаемой службы.
 - systemd
	 -   Первым исполняется default.target (символическая ссылка на основной таргет, например, на graphical.target или multi-user.target). Дальше составляется дерево зависимостей юнитов:
			-	если в юнит-файле unit1 используется директива Wants, то юниты, указанные в директиве будут запущены вместе с unit1 (при этом результат запуска этих юнитов не важен).
		   -   если в юнит-файле unit1 используется директива Requires=unit2, то будут запущены оба юнита, но если unit2 не будет успешно запущен, то unit1 будет деактивирован автоматически.
	-	Также можно использовать директивы Before и After, для задания точного порядка запуска юнитов:
	    -   Если unit1 содержит Before=unit2 при одновременной загрузке обоих юнитов, то unit1 будет запущен до момента запуска unit2
	    -   Если unit1 содержит After=unit2, то при запуске обоих юнитов unit2 будет полностью завершен перед запуском unit1

## 5. Показать скриншоты вашего используемого Linux дистрибутива и объяснить на какой системе инициализации он работает
![enter image description here](https://i.imgur.com/gbd1PdM.png)
## 6. Точка монтирования - это?
Каталог или файл, с помощью которого обеспечивается доступ к новой файловой системе, каталогу или файлу 
## 7. Символом "-" обозначается тип файла?
Обычный файл
## 8. Текущее положение в файловой системе можно просмотреть командой?

    $ pwd

## 9. Как сделать рекурсивное копирование каталога?

    $ cp -r source destination

## 10. Какие команды предназначены для создания элементов файловой системы?

    $ mkdir directory_name - создание директории
    $ touch file_name - создание файла

## 11. Домашний каталог суперпользователя находится по адресу?

    /root
