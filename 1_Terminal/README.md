## Terminal

## Linux terminal (GitBash) commands

1) Посмотреть где я   -   <b>pwd</b>
2) Создать папку 	- <b>mkdir qa1</b>
3) Зайти в папку	- <b>cd qa1</b>    
4) Создать 3 папки     -  <b>mkdir f1 f2 f3</b>
5) Зайти в любую папку	- <b>cd f1</b>
6) Создать 5 файлов (3 txt, 2 json)	-  <b>cat >  index.txt</b> создаст один файл и ред.его.
 <b>touch index.txt main.txt name.txt index1.json main1.json</b> 
7) Создать 3 папки - <b>mkdir folder1 folder2 folder3</b>
8) Вывести список содержимого папки  -  <b>ls -la</b>
9) Открыть любой txt файл  -   <b>cat >> index.txt</b>  можно сразу сделать запись в этом файле. Чтобы выйти из редактирования  -  <b>CTRL + C</b>
10) Написать туда что-нибудь, любой текст.     см. пункт выше
11) Сохранить и выйти. см. пункт 9
12) Выйти из папки на уровень выше <b>cd ..</b>      ( cd ../qa2 - сразу в папку qa2)
13) Переместить любые 2 файла, которые вы создали, в любую другую папку<br>
		<b>mv index.txt qa1/index.txt</b> (если уже находишься в папке с файлом index.txt то прописывать адрес этого файла не нужно)

14) Скопировать любые 2 файла, которые вы создали, в любую другую папку<br>
		<b>cp f1/index1.json qa2/index2.json</b>  (f1 можно не указывать )

15) Найти файл по имени  -   <b>find / -name main1.json</b>

16) Просмотреть содержимое в реальном времени (команда grep)   -   <b>tail -f index.txt</b>

<b>cat index.txt</b> - отобразит текст в файле index.txt
<b>grep 1. Name index.txt</b> - найдет текст - > 1. Name (если он есть в файле) <br>
<b>grep -i 1. Name index.txt</b> -   -i  откл. чувствительность к регистру при поиске файлов.
<b>grep -i name index.txt</b>
1. Name<br>
6. NAME

<b>grep -v 1 index.txt</b>	-v покажет все строки где НЕТ "1"<br>
2. Age<br>
3. Email<br>
4. Ciudad<br>                                                               
5. Pais<br>
6. NAME<br>
Посчитать количество строк   -  <b>grep -c Email index.txt</b>
<b>grep -c name index.txt</b><br>
0  - найдено 0 потому что тут не учитывается зависимость от регистра!<br>
<b>grep -ic name index.txt</b><br>
2     <b>-ic</b> исключает зависимость от регистра при поиске.

17) вывести несколько первых строк из текстового файла - <b>head -3 index.txt</b>
18) вывести несколько последних строк из текстового файла - <b>tail -3 index.txt</b>
19) просмотреть содержимое длинного файла (команда less) - <b>less -s index.txt</b>
							(выйти из less, нажмите -  <b>Q</b>)
20) вывести дату и время	-  <b>date</b>
    
=========

Задание *

1) Отправить http запрос на сервер.
http://162.55.220.72:5006/terminal-hw-request <br>
 	<b>cURL "http://162.55.220.72:5005/get_method?name=Aleksei&age=37"</b>

2)Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

vim script.sh
<br>#!/bin/bash
<br>cd qa1
<br>mkdir f1 f2 f3
<br>cd f1
<br>touch index.txt main.txt name.txt index1.json main1.json
<br>mkdir folder1 folder2 folder3
<br>ls
<br>mv index.txt folder1/index.txt
<br>esk:wq

=====================

Удалить файл  -  <b>rm f1/names.txt	rm name.json</b>
<br>Удалить папку и файл (если он есть внутри папки)   -   <b>rm -r f1</b>
<br>Создаст файл users <b>vim users.json</b>
<br>Далее откроется окно и чтобы редактировать в нём нужно нажать <b>I</b>
<br>Чтобы выйти из режима редактирования - <b>esc  :wq</b>
<br>Выгрузит всю историю запросов командной строки -  <b>history >> hist.txt</b>  
<br>Удалить все записи из файла истории bash  -   <b>history -c</b>
