#### 1) Создал таблицу и добавил в нее 2 записи
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_4/images/img1.png?raw=true)

#### 2) Из двух транзакций попытался изменить обе записи и получил сообщение о дедлоке, при этом вторая транзакция улетела в ошибку
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_4/images/img2.png?raw=true)

#### 3) Посмотрел файл логов, информация о дедлоке туда попала
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_4/images/img3.png?raw=true)
