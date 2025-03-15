#### 1-3) Открыл 2 консоли и зашел в psql
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img1.png?raw=true)

#### 4) В первой сессии создал новую таблицу и заполнил ее данными
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img2.png?raw=true)

#### 5) Текущий уровень изоляции - read committed
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img3.png?raw=true)

#### 6-7) В обеих сессиях начал транзакцию, в первой добавил новую запись, но пока не коммитил
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img4.png?raw=true)

#### 8) Во второй сессии сделал запрос на получение всех записей (первый до инсерта в первой сессии, второй после)
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img5.png?raw=true)

#### 9) Новую запись не видно, так как дефолтный уровень изоляции read committed не подразумевает "грязное" чтение

#### 10-11) В первой сессии закомитил тарнзакцию и опять получил все записи во второй сессии
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img6.png?raw=true)

#### 12) Да, новая запись появилась, так как это теперь неповторяющееся чтение, которое разрешено на уровне read committed

#### 13-15) В обеих сессиях начал транзакцию на уровне repeatable read и в первой добавил новую запись
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img7.png?raw=true)

#### 16) Получил все записи во второй сессии
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img8.png?raw=true)

#### 17) Нет, новую запись не видно, так как уровень изоляции repeatable read как и read committed не подразумевает "грязное" чтение

#### 18-19) Завершил транзакцию в первой сессии и получил все записи во второй
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_2/images/img9.png?raw=true)

#### 20) Новая запись не появилась, так как в отличаи от read committed, repeatable read уровень не подразумевает неповторяющееся чтение

