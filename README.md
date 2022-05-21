# Terminal_linux
1) Посмотреть где я
    pwd
2) Создать папку
    mkdir p1
3) Зайти в папку
    cd p1
4) Создать 3 папки
    mkdir p2 p3 p4
5) Зайти в любоую папку
    cd p2
6) Создать 5 файлов (3 txt, 2 json)
    touch t1.txt t2.txt t3.txt j1.json j2.json
7) Создать 3 папки
    mkdir p5 p6 p7
8) Вывести список содержимого папки
    ls -la
9) + Открыть любой txt файл
    vim t1.txt
10) + написать туда что-нибудь, любой текст.
    режим редактирования нажатием i
    
    123 
    456
    789
 
 11) + сохранить и выйти.
    нажатием Esc : w q Enter

12) Выйти из папки на уровень выше
    cd ..
13) переместить любые 2 файла, которые вы создали, в любую другую папку.
    mv /c/Users/user/QA/p1/p2/{t1.txt,t2.txt} /c/Users/user/QA/p1/p3
или

    mv p2/{t1.txt,t2.txt} p3
или

    mv t1.txt t2.txt p3 
14) скопировать любые 2 файла, которые вы создали, в любую другую папку.
    cp /c/Users/user/QA/p1/p3/{t2.txt,t1.txt} /c/Users/user/QA/p1/p4
или

    cp p3/{t2.txt,t1.txt} p4
или

    cp t2.txt t1 txt p4
15) Найти файл по имени
    find . -name t1.txt
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.
    tail -f p4/t1.txt |grep 'err'
отслеживание только строк с 'err', выход по Ctrl+C

17) вывести несколько первых строк из текстового файла
    head -n 3 p4/t1.txt
18) вывести несколько последних строк из текстового файла
    tail -n 3 p4/t1.txt
19) просмотреть содержимое длинного файла (команда less) изучите как она работает.
    less p4/t1.txt
выход Q

20) вывести дату и время
    date +%x" "%X
или

    date +"%D %R"
Задание *
1) Отправить http запрос на сервер. http://162.55.220.72:5005/terminal-hw-request
curl ‘http://162.55.220.72:5005/terminal-hw-request’
После получения ответа сервера, отправить повторный запрос

curl ‘http://162.55.220.72:5005/get_method?name=Marg0shik&age=34’
2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
1.Создать файл:
    touch script.sh
2.Изменить содержимое файла:
    cat >script.sh 
    #!/bin/sh 
    cd foldername
    mkdir foldername1 foldername2  foldername3
    cd foldername1
    touch 1.txt 2.txt 3.txt 4.json 5.json
    mkdir foldername4  foldername5  foldername7
    ls -la
    mv 1.txt 2.txt foldername4/ 

3.Сохранить изменения и выйти из режима редактирования:
выйти из режима редактирования нажатием Ctrl+C

4.Сделать файл "скриптом" исполняемым:
    chmod +x ./script.sh 
5.Запустить скрипт
    ./script.sh
