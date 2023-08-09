# 12-02-hw
Домашнее задание к занятию «Работа с данными (DDL/DML)»   Ярчак Александр

Задание 1

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp.

create user 'sys_temp'@'localhost';

https://github.com/megawebtech/12-02-hw/blob/master/create_user.JPG


1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

select user from mysql.user;

https://github.com/megawebtech/12-02-hw/blob/master/select_user_from.JPG


1.4. Дайте все права для пользователя sys_temp.


grant all privilies on *.* to 'sys_temp'@'localhost';


https://github.com/megawebtech/12-02-hw/blob/master/grant%20all%20privileges.JPG

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

show grants for sys_temp@localhosh;

https://github.com/megawebtech/12-02-hw/blob/master/show%20grants%20for.JPG


1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:

ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

Посмотреть таблицы: 

show tables;

Диаграмма:

https://github.com/megawebtech/12-02-hw/blob/master/%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4.pdf


Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

Задание 2

Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

Название таблицы | Название первичного ключа
customer         | customer_id
