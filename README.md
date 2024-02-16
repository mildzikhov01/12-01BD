# Домашнее задание к занятию "Базы данных" - `Мильдзихов Сергей`


### Легенда

Заказчик передал вам файл в формате Excel, в котором сформирован отчёт. На основе этого отчёта нужно выполнить следующие задания.
   
---

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

какие данные хранятся в этих таблицах;
какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Приведите решение к следующему виду: Сотрудники (

идентификатор, первичный ключ, serial,
фамилия varchar(50),
...
идентификатор структурного подразделения, внешний ключ, integer).


### Ответ

1. Сотрудники (

Идентификатор, первичный ключ, serial,
Фамилия, varchar(50),
Имя, varchar(50),
Отчество, varchar(50),
Дата найма (Date),
Оклад, идентификатор оклада, внешний ключ, integer,
Должность, идентификатор должности, внешний ключ, integer,
Структурное подразделение, идентификатор кода структурного поразделения, внешний ключ, integer)

2. Должность (

Идентификатор, первичный ключ, serial,
Должность, varchar(50)

3. Оклад (

Идентификатор, первичный ключ, serial,
Идентификатор должности, внешний ключ, integer,
Размер оклада, decimal)

4. Структурное подразделение (

Идентификатор, первичный ключ, serial,
Полное наименование структурного подразделения, varchar(255),
Идентификатор типа подразделения, внешний ключ, integer,
Идентификатор адреса филиала, внешний ключ, integer)

5. Тип подразделения (

Идентификатор, первичный ключ, serial,
Тип подразделения, enum)

6. Адрес филиала (

Идентификатор, первичный ключ, serial,
Полный адрес филиала, varchar(255) )

7. Проект (

Идентификатор, первичный ключ, serial,
Название проекта, varchar(100) )

8. Назначение на проект (

- Идентификатор проекта, внешний ключ, integer,
- Идентификатор сотрудника, внешний ключ, integer)
