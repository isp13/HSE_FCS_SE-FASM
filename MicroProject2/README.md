# Микропроэкт №2

## Казанцев Никита БПИ191 ВАР 16

Задача о клумбе. На клумбе растет 40 цветов, за ними непрерывно
следят два садовника и поливают увядшие цветы, при этом оба садовника
очень боятся полить один и тот же цветок. Создать многопоточное
приложение, моделирующее состояния клумбы и действия садовников. Для
изменения состояния цветов создать отдельный поток.

## Программа

Имеется три потока. Первый поток ответственен за генерацию грядок, которые
нужно полить. Параллельно с первым потоком два других потока,
символизирующих садовников, ходят по этим грядкам и ищут грядку для того,
чтобы полить. Только один садовник может полить конкретную не политую грядку.
Для выполнения данного условия применяются мьютексы. Мьютексные семафоры
(мьютексы) являются упрощённой реализацией семафоров, аналогичной двоичным
семафорам с тем отличием, что мьютексы должны отпускаться тем же процессом
или потоком, который осуществляет их захват, однако в зависимости от типа и
реализации попытка освобождения другим потоком может как освободить
мьютекс, так и вернуть ошибку.


Отработка программы на нормальном вводе. Вводятся 1 число - кол-во событий генерации не политой грядки. Выводится результат в виде комментирования действий всех трех потоков.
- **Результат работы**</br>
  ![](https://github.com/isp13/HSE_FCS_SE-FASM/blob/master/MicroProject2/res1.PNG)
  ![](https://github.com/isp13/HSE_FCS_SE-FASM/blob/master/MicroProject2/res2.PNG)
 

### Отработка программы на некорректном/ нестандартном вводе
- **Результат работы**</br>
  ввод отрицательного значения</br>
![](https://github.com/isp13/HSE_FCS_SE-FASM/blob/master/MicroProject2/res3.PNG)


## Использованная литература/ интернет источники
a. Статья "Такие удивительные семафоры" https://habr.com/ru/post/261273/
[интернет ресурс] \n
b. Алгоритмы параллельных вычислений и
программирование http://window.edu.ru/catalog/pdf2txt/971/67971/41350?p_page=
20 [интернет ресурс]