# otus-bash

Написать скрипт для крона, который раз в час присылает на заданную почту:

1. X IP адресов (с наибольшим кол-вом запросов) с указанием кол-ва запросов c момента последнего запуска скрипта;
2. Y запрашиваемых адресов (с наибольшим кол-вом запросов) с указанием кол-ва запросов c момента последнего запуска скрипта;
все ошибки c момента последнего запуска;
3. Список всех кодов возврата с указанием их кол-ва с момента последнего запуска.

В письме должен быть прописан обрабатываемый временной диапазон и должна быть реализована защита от мультизапуска.

Для проверки ДЗ отредактировать Vagrantfile. В строке 

    echo "0 * * * * /vagrant/web-cron.sh your@email.addr" > cronfile

заменить **your@email.addr** на почту, куда должны прилететь письма(прямиком в спам). После запустить

    vagrant up

и подождать. Либо руками тригернуть выполнение скрипта внутри виртуальной машины.
