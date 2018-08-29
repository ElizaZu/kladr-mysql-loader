# kladr-mysql-loader

<b><h2>Script for download and import Russian KLADR to MySQL database</h2></b><br>
Tested on ubuntu17.4 and Windows 10 (ubuntu for Windows 10)

<b>How does it work:</b> <br>
1) download the archive with Russian KLADR from official site https://www.gnivc.ru/html/gnivcsoft/KLADR/Base.7z
2) convert dbf files to csv into UTF-8 encoding
3) import csv into MySQL database

<b>To run: </b><br>
1. Run the prerequisites file once. Will be installed (if not installed earlier): MySQL client, p7zip, python3.6, python-pip and python library for working with dbf
2. In the file update_kladr.config configure the connection to the database and, if necessary, tables and columns aliases
  <code>#Database server<br>
  host=127.0.0.1<br><br>
  #Database user<br>
  user=kladruser<br><br>
  #User's password<br>
  password=kladrpassword<br><br>
  #Database name<br>
  database=kladr</code>
3. Run update_kladr. <b>Attention! When you run the import, the previous data from kladr tables in database will be removed. </b><br>

Code of dbf2csv.py taken from https://gist.github.com/bertspaan/8220892
Thank you!

<b><h2>Bash-скрипт для загрузки и экспорта КЛАДР в БД MySQL</h2></b><br>
Проверено на ubuntu17.4 и Windows 10 (ubuntu для Windows 10)

<b>Выполняются следующие дествия:</b><br>
1) загрузку архива с КЛАДР с официального сайта https://www.gnivc.ru/html/gnivcsoft/KLADR/Base.7z
2) конвертация dbf в csv в кодировку UTF-8
3) импорт csv в БД MySQL

<b>Для запуска:</b><br>
1. Один раз запустить prerequisites. Будут установлены, если не были установлены ранее: MySQL client, p7zip, python3.6, python-pip и библиотека питона для работы с dbf
2. В файле update_kladr.config настроить параметры подключения к БД и при необходимости альясы таблиц и столбцов
  #Database server
  host=127.0.0.1
  #Database user
  user=kladruser
  #User's password
  password=kladrpassword
  #Database name
  database=kladr
3. Запустить update_kladr. <b>Внимание! При импорте предыдущие данные из указанных таблиц будут удалены.</b><br>

Код скрипта на питоне для конвертации dbf в csv dbf2csv.py взят отсюда https://gist.github.com/bertspaan/8220892

