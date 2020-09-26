Установка и конфигурация
------------

1) Устанавливаем систему виртуализации <a href="https://hub.docker.com/editions/community/docker-ce-desktop-windows/" target="_blank">DOCKER</a>
2) Клонируем проект с репозитория
3) Используя либо IDE,либо git bash заходим в корень проекта
4) Выполняем команду docker-compose up. Дожидаемся сборки проекта
5) Далее заходим в dashboard docker. В трее(нижний правый угол экрана) находим иконку docker и жмем правйо кнопкой мыши. Выбириаем "Dashboard"
6) Выбираем наш контейнер находим контейнер с базой данных *****_db_1 и нажимаем синюю кнопку CLI.
7) Попадаем в консоль где теперь работает mysql. " По умолчанию user=root password=pass ". Они уже прописаны в конфиге который просят создать по ДЗ.
8) Далее переходим в домашнюю директорию " cd /home ". Здесь видим директорию lesson02 в которой лежат два sql файла необходимых по ДЗ. Извдекаем их с помощью команд:
<br />
<br />
mysql < create.sql
<br />
mysql < createtable.sql

9) Выполняем команду:
<br />
mysqldump > /home/lesson02/dump.sql
<br />
Для создания дампа.

10) Выполняем команду:
<br />
mysqldump > /home/lesson02/dump.sql
<br />
Для создания дампа.

11) Выполняем команду:
<br />
mysql sample < /home/lesson02/dump.sql
<br />
Для залива бекапа в базу.

12). Для создания бекапа опредленной табицы базы с 100 строками лимита, нужно использоват команду mysqldump с параметром opt и where
<br />
<br />
mysqldump --opt --where="1 limit 100" mysql help_keyword  > /home/lesson02/dumptest.sql
<br />
<br />
После указания базы указывается таблица которую нужно выбрать.

