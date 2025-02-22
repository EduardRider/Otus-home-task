Домашнее задание к занятию №6 ZFS 

1. Определение алгоритма с наилучшим сжатием

zpool create otus1 mirror /dev/sda /dev/sdb

zpool create otus2 mirror /dev/sdc /dev/sdd

zpool create otus3 mirror /dev/sde /dev/sdf

zpool create otus4 mirror /dev/sdg /dev/sdh


zfs set compression=lzjb otus1

zfs set compression=lz4 otus2

zfs set compression=gzip-9 otus3

zfs set compression=zle otus4


wget -P /otus1 https://gutenberg.org/cache/epub/2600/pg2600.converter.log

wget -P /otus2 https://gutenberg.org/cache/epub/2600/pg2600.converter.log

wget -P /otus3 https://gutenberg.org/cache/epub/2600/pg2600.converter.log

wget -P /otus4 https://gutenberg.org/cache/epub/2600/pg2600.converter.log
  

 Вывод команд zfs list и zfs get all в файле 1-1.png 
 
 
 2. Определение настроек пула
 
вывод команды zpool import -d zpoolexport/ в файле 2_1.png

zpool import -d zpoolexport/ otus

Вывод команд:

zfs get available otus

zfs get readonly otus

zfs get recordsize otus

zfs get compression otus

zfs get checksum otus

в файле файле 2_2.png


3. Работа со снапшотом, поиск сообщения от преподавателя

zfs receive otus/test@today < otus_task2.file

Вывод содержимого файла secret_message в фалей  3_1.png
