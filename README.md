# Terminal_linux
1) Посмотреть где я <br>
   `pwd`
2) Создать папку<br>
    `mkdir p1`
3) Зайти в папку<br>
    `cd p1`
4) Создать 3 папки<br>
    `mkdir p2 p3 p4`
5) Зайти в любоую папку<br>
    `cd p2`
6) Создать 5 файлов (3 txt, 2 json)<br>
    `touch t1.txt t2.txt t3.txt j1.json j2.json
7) Создать 3 папки<br>
    `mkdir p5 p6 p7
8) Вывести список содержимого папки<br>
    `ls -la
9) + Открыть любой txt файл<br>
    `vim t1.txt
10) + написать туда что-нибудь, любой текст.<br>
    `режим редактирования нажатием i<br>
    
    123 <br>
    456<br>
    789<br>`
 
 11) сохранить и выйти.<br>
   ` нажатием Esc : w q Enter`

12) Выйти из папки на уровень выше<br>
    `cd ..`
13) переместить любые 2 файла, которые вы создали, в любую другую папку.<br>
    `mv /c/Users/user/QA/p1/p2/{t1.txt,t2.txt} /c/Users/user/QA/p1/p3`<br>
или<br>

    `mv p2/{t1.txt,t2.txt} p3`<br>
или<br>

    `mv t1.txt t2.txt p3 <br>
14) скопировать любые 2 файла, которые вы создали, в любую другую папку.<br>
   ` cp /c/Users/user/QA/p1/p3/{t2.txt,t1.txt} /c/Users/user/QA/p1/p4`<br>
или<br>

    cp p3/{t2.txt,t1.txt} p4<br>
или

    cp t2.txt t1 txt p4<br>
15) Найти файл по имени<br>
    `find . -name t1.txt
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.<br>
    `tail -f p4/t1.txt |grep 'err'
отслеживание только строк с 'err', выход по Ctrl+C
17) вывести несколько первых строк из текстового файла<br>
    `head -n 3 p4/t1.txt
18) вывести несколько последних строк из текстового файла<br>
    `tail -n 3 p4/t1.txt
19) просмотреть содержимое длинного файла (команда less) изучите как она работает.<br>
     `less p4/t1.txt
выход Q
19) просмотреть содержимое длинного файла (команда less) изучите как она работает.<br>
    `less p4/t1.txt
выход Q

20) вывести дату и время<br>
    `date +%x" "%X`<br>
или<br>

    `date +"%D %R"`<br>
<hr>
<h4>Задание *</h4>
1) Отправить http запрос на сервер. http://162.55.220.72:5005/terminal-hw-request<br>
    `curl ‘http://162.55.220.72:5005/terminal-hw-request’<br>`
После получения ответа сервера, отправить повторный запрос<br>

    curl ‘http://162.55.220.72:5005/get_method?name=Natali&age=37’<br>

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13<br>
1.Создать файл:<br>
   ` touch script.sh<br>`
2.Изменить содержимое файла:<br>
    `cat >script.sh <br>
    #!/bin/sh <br>
    cd foldername<br>
    mkdir foldername1 foldername2  foldername3<br>
    cd foldername1<br>
    touch 1.txt 2.txt 3.txt 4.json 5.json<br>
    mkdir foldername4  foldername5  foldername7<br>
    ls -la<br>
    mv 1.txt 2.txt foldername4/ <br>`

3.Сохранить изменения и выйти из режима редактирования:<br>
выйти из режима редактирования нажатием Ctrl+C<br>

4.Сделать файл "скриптом" исполняемым:<br>
    `chmod +x ./script.sh <br>`
5.Запустить скрипт<br>
   ` ./script.sh<br>`
