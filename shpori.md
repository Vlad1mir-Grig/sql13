Удалить из таблицы products все товары, которых нет на складе.
-
delete from products where count<1;
-
Удалить из таблицы cars все автомобили начиная с 2010 года и старше
-
delete from cars where year<=2010
-
Измените статус (status) заказа под номером (id) 5 с delivery на success.
-
update orders set status='success' where id=5
-
Увеличьте цену 5 самых дешевых товаров на 5%
-
update products set price=price*1.05 order by price limit 5
-
Теперь самых дорогих:
-
update products set price=price*1.05 order by price desc limit 5
-
У отмененных заказов status равен "cancelled". У новых заказов status равен "new".
-
номер (id) и сумму (sum) заказа.
-
NULL – это особое слово в MySQL и в отличии от "cancelled" или "new", его нужно писать без кавычек. 
А чтобы сравнить значение в поле с NULL, нужно использовать не символы равенства (=) и неравенства (<>), 
а специальное выражение IS NULL или IS NOT NULL.
-
Новые записи в таблицу можно добавить не только с помощью VALUES, но и с помощью SET. 
Следующие два запроса идентичны: 
-
INSERT INTO table (field1, field2) VALUES
(value1, value2); 
-
INSERT INTO table SET field1=value1, field2=value2;
-
Добавьте в таблицу users нового пользователя
-
insert into users SET id=10, first_name='Никита', last_name='Петров'
-
Добавьте в таблицу products новый товар
-
insert into products (id, name, count, price) value
-
INSERT INTO table (column1, column2)
-
VALUES (value1, value2);
-
INSERT INTO table (column1, column2)
-
VALUES (value11, value12),
-
(value21, value22), ..:
-
INSERT INTO table1 (column1, column2)
-
SELECT (col1, col2) FROM table2;
-
UPDATE table1
-
SET column1 = new_value;
-
UPDATE table1
-
SET column1 = new_value
-
column2 = new_value
-
WHERE condition;
-
DELETE FROM table;
-
DELETE FROM table
-
WHERE condition;
-
Типы данных:
-
![image](https://github.com/user-attachments/assets/f69b6183-236a-4591-b79f-23f4e4ae07df)

