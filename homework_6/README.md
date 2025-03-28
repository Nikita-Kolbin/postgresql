#### В яндекс облаке создал 2 машины в одной сети и установил на них постгрес и настроил репликацию. Провел бенчмарк на запись и на чтение до включения асинхронной реплики. Получилось 2731 tps на запись и 46219 на чтение
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_6/images/img1.png?raw=true)

#### Далее поднимаю реплику
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_6/images/img2.png?raw=true)

#### И повторяю замеры, tps уменьшились и при записи и при чтении, но незначительно, в рамках погрешности, 2640 и 45461 соответственно
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_6/images/img3.png?raw=true)

#### Ну и протестировал реплику на чтение, получил результаты немного хуже, чем на мастере - 42937
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_6/images/img4.png?raw=true)
