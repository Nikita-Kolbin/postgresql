#### Настроил pgbouncer и запустил бенч с 120 клиентами в дефолтном режиме (pool_mode = session)
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_5/images/img1.png?raw=true)

#### Потом установил режим pool_mode = transaction
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_5/images/img2.png?raw=true)

#### Результат бенча в режиме transaction
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_5/images/img3.png?raw=true)

#### И третий режим pool_mode = statement
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_5/images/img4.png?raw=true)

#### Результат бенча в режиме statement
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_5/images/img5.png?raw=true)

#### Вывод: Как и ожидалось, самый медленный тип соединений на сессию, соединение на транзакцию заметно быстрее. А вот режим соединения на операцию незначительно быстрее транзакции. 