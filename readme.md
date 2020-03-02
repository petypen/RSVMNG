# SRVMNG (Services managing)  
## Скрипт для запуска и остановки сервисов srv1cv83 и postgresql в WSL

## Задача  
В сиcтеме Linux, которая работает в WSL автоматизировать запуск и остановку серверов 1С:Предприятие 8 (srv1cv83) и PostgresQL (postgresql)

## Зависимости  
Используется библиотека [1commands](https://github.com/oscript-library/1commands)

## Параметры  
-stop : остановить работающие сервисы  
-sp pass : (обязательно) пароль пользователя для выполнения операций с повышенными привилегиями

## Примеры использования  
Остановить сервисы srv1cv83 и postgresql, где 1111 пароль пользователя, для выполнения операций с повышенными привилегиями (sudo)  
`oscript srvmng.os -stop -sp 1111`

Запустить сервисы srv1cv83 и postgres, где 1111 пароль пользователя  
`oscript srvmng.os -sp 1111`