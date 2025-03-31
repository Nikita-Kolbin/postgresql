#### Установил постгрес на виртуалку и залил тестовую базу данных. При выполненни тяжелого запроса получил сложность 328127 "попугаев"
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_7/images/img1.png?raw=true)

#### Время выполнения запроса 1.5 секунды
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_7/images/img2.png?raw=true)

#### Навесил индексы на поля внешних ключей
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_7/images/img3.png?raw=true)

#### Получил результат даже немного хуже, чем без индексов - 328193, по времени так же около 1.5 секунд. Предполагаю, что это происходит по тому, что нам в любом случае надо пройти по всем внешним ключам, а в таблице, которую мы присоединяем, мы берем записи по id, которые уже имеют индекс. По этому индексы на внешние ключи не дают прироста производительности. 
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_7/images/img4.png?raw=true)
