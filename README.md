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

### В таблицах хранятся данные:
ФИО сотрудника  

Оклад

Должность

Тип подразделения

Структурное подразделение

Дата найма

Адрес филиала

Проект на который назначен

---

### Какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL:

ФИО сотрудника - строковый (varchar)


Оклад - числовой (decimal/numeric)


Должность - строковый (varchar)


Тип подразделения - строковый (varchar)


Структурное подразделение - строковый (varchar)


Дата найма - дата и время (tinyint)


Адрес филиала - местонахождение филиала (varchar)


Проект на который назначен - строковый (varchar)



---

### Приведите решение к следующему виду:

employees (id_employee, int, not null, auto_increment, primary_key
last_name, varchar(50), not null
first_name, varchar(50), not null
surname, varchar(50)
rank, foreign_key
salary, foreign_key
subdivision, foreign_key
office, foreign_key
project, foreign_key
hired_since, date, not null)


subdivisions (id_subdivision, int, not null, auto_increment, primary_key
subdivision, varchar(100), not null
type_of_subdivision, foreign_key
office, foreign_key)


type_of_subdivision (id_of_type, int, not null, auto_increment, primary_key
type)


offices (id_office, int, not null, auto_increment, primary_key
office, varchar(200), not null)


projects (id_project, int, not null, auto_increment, primary_key
project, varchar(100), not null)
ranks (id_rank, int, not null, auto_increment, primary_key
rank, varchar(100), not null)
salary (id_salary, int, not null, auto_increment, primary_key
salary, real, not null)
