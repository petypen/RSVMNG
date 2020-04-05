# SRVMNG (Services managing)  
## Скрипт для запуска и остановки сервисов srv1cv83 и postgresql в WSL

## Задача  
В сиcтеме Linux, которая работает в WSL автоматизировать запуск и остановку серверов 1С:Предприятие 8 (srv1cv83) и PostgresQL (postgresql). Лог работы скрипта сохраняется в файл srvmng.log

## Зависимости и разрешения  
Используются библиотеки 
* [1commands](https://github.com/oscript-library/1commands)
* [logos](https://github.com/oscript-library/logos)

Требуются разрешения:
* Для корректного сохранения файла лога требуется разрешение на запись в папку, где распологается скрипт.

## Параметры  
-sp pass (--SudoPassword pass) : (обязательно) пароль пользователя для выполнения операций с повышенными привилегиями

-a action (--action action) : (обязательно) действие, которое должен выполнить скрипт. Доступные варианты действия: start|stop|restart

-v (--verbosity) : (необязательно) содержимое лога выводить еще и в окно терминала, логирование в файл при этом не отключается

## Примеры использования  
Остановить сервисы srv1cv83 и postgresql, где 1111 пароль пользователя, для выполнения операций с повышенными привилегиями (sudo). Лог дополнительно выводить в окно терминала.  
`oscript srvmng.os -sp 1111 -a stop -v`

Запустить сервисы srv1cv83 и postgres, где 1111 пароль пользователя. Лог в окно терминала не выводить.  
`oscript srvmng.os -sp 1111 -a start`