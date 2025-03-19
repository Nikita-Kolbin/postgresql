#### 1) Создал таблицу и заполнил ее миллионом случайных строк
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_3/images/img1.png?raw=true)

#### 2) Размер таблицы получился 65мб
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_3/images/img2.png?raw=true)

#### 3-4) 5 раз обновил записи и посмотрел сколько мервых строчек, их оказалось чуть меньше миллиона (у меня строки обнновлялись довольно долго и за время, пока я обновлял 5 раз автовакуум приходил и чистил часть мертвых строк)
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_3/images/img3.png?raw=true)

#### 5) Через некоторое время посмотрел еще раз и их стало 0, автовакуум пришел и почистил оставшиеся мертвые строчки
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_3/images/img4.png?raw=true)

#### 6-7) Еще раз обновил строки, тут я поймал момент, когда мервых 3 миллиона. Размер таблицы 391мб (после первого обновления строк было столько же)
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_3/images/img5.png?raw=true)

#### 8-10) Выключил автовакуум и 10 раз изменил все строки, размер таблицы получился 856мб
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_3/images/img6.png?raw=true)

#### 10.5) На данный момент в таблице 10 миллионов мертвых строк, я решил вызвать вакуум вручную, он отчистил мертвые строки, но при этом не освободил память, а вот вакуум фулл уже освободил память и таблица стала весить 81мб
![картинка](https://github.com/Nikita-Kolbin/postgresql/blob/main/homework_3/images/img7.png?raw=true)

#### 11) При выключении автовакуума мертвые строки не чистятся и занимают память, также влиюяют на производительность так как постгрес при запросах обрабатывает их тоже. 
