<h2>Работа с git и bash</h2>

<h3>Задача 1:</h3>
<table>
  <tr>
    <th>Задание</th>
    <th>Выполненная команда</th>
  </tr>
  <tr>
    <td>Создать домашнюю директорию через терминал</td>
    <td>$ mkdir homedir</td>
  </tr>
  <tr>
    <td>Открыть домашнюю директорию через терминал</td>
    <td>$ cd homedir</td>
  </tr>
  <tr>
    <td>Определить имя папки, в которой вы находитесь</td>
    <td>$ pwd</td>
  </tr>
  <tr>
    <td>Создать внутри этой папки каталог с именем test1</td>
    <td>$ mkdir test1</td>
  </tr>
  <tr>
    <td>Перейти в папку test1</td>
    <td>$ cd test1</td>
  </tr>
  <tr>
    <td>Создать файл 1,2 и 3 внутри каталога test1</td>
    <td>$ touch file1.txt file2.txt file3.txt</td>
  </tr>
  <tr>
    <td>Проверить содержимое каталога test1</td>
    <td>$ ls 
      <br>file1.txt  file2.txt  file3.txt</td>
  </tr>
  <tr>
    <td>Перейти в домашнюю директорию</td>
    <td>$ cd ..</td>
  </tr>
  <tr>
    <td>Создать папку test2 внутри домашней директории</td>
    <td>$ mkdir test2</td>
  </tr>
  <tr>
    <td>Удалить папку test2</td>
    <td>$ rmdir test2</td>
  </tr>
  <tr>
    <td>Удалить файл 2 из папки test1</td>
    <td>$ rm test1/file2.txt</td>
  </tr>
  <tr>
    <td>Создать папку в домашней директории test3 и добавить в нее два файла</td>
    <td>$ mkdir test3 && touch $_/file4.txt $_/file5.txt</td>
  </tr>
  <tr>
    <td>Удалить папку test3</td>
    <td>$ rm -r test3</td>
  </tr>
  <tr>
    <td>Создать папку test4 в домашней директории</td>
    <td>$ mkdir test4</td>
  </tr>
  <tr>
    <td>Переместить файлы 1 и 3 из папки test1 в папку test4</td>
    <td>$ mv test1/file1.txt test1/file3.txt test4/</td>
  </tr>
  <tr>
    <td>Добавить в файл 1 три строки со словами line</td>
    <td>$ echo -e "line\nline\nline" >> test4/file1.txt</td>
  </tr>
  <tr>
    <td>Посмотреть содержимое файла 1</td>
    <td>$ cat test4/file1.txt</td>
  </tr>
  <tr>
    <td>Добавьте в файл 3 три строки со словами line</td>
    <td>$ echo -e "line\nline\nline" >> test4/file3.txt</td>
  </tr>
  <tr>
    <td>Просмотрите содержимое двух файлов (1 и 3) сразу</td>
    <td>$ cat test4/file1.txt test4/file3.txt</td>
  </tr>
  <tr>
    <td>Используя один из редакторов замените все строки в файле 1</td>
    <td>$ nano test4/file1.txt
    <br>1. ^\ (Нажать сочетание клавиш "Ctrl" + "\")
    <br>2. В поле "Search (to replace)" ввести "line" и нажать клавишу "Enter"
    <br>3. В поле "Replace with" ввести "new line" и нажать клавишу "Enter"
    <br>4. Нажать "A" на клавиатуре</td>
  </tr>
</table>
<hr>
<h3>Задача 2:</h3>
<table>
  <tr>
    <th>Задание</th>
    <th>Выполненная команда</th>
  </tr>
  <tr>
    <td>Создать домашнюю директорию через терминал</td>
    <td>$ mkdir homedir</td>
  </tr>
  <tr>
    <td>Зайти в домашнюю директорию через терминал.</td>
    <td>$ cd homedir</td>
  </tr>
  <tr>
    <td>Создать папку test 3</td>
    <td>$ mkdir test3</td>
  </tr>
  <tr>
    <td>Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4</td>
    <td>$ echo -e "row1\nrow2\nrow3\nrow4" >> test3/file4.txt && echo -e "row1\nrow2\nrow3\nrow4" >> test3/file5.txt && echo -e "row1\nrow2\nrow3\nrow4" >> test3/file6.txt</td>
  </tr>
  <tr>
    <td>Найдите строку row2 в файле 5</td>
    <td>$ cat test3/file5.txt | grep "row2"</td>
  </tr>
  <tr>
    <td>Найдите строку row в папке test3</td>
    <td>$ grep -r 'row' test3</td>
  </tr>
  <tr>
    <td>Посчитайте сколько строк с содержимым row в файле 6</td>
    <td>$ grep -c 'row' test3/file6.txt</td>
  </tr>
  <tr>
    <td>Найдите файл 5 внутри папки test3</td>
    <td>$ find ./test3 -name "*file5*"</td>
  </tr>
  <tr>
    <td>Используя команду find, удалите файл 5</td>
    <td>$ find ./test3 -name "*file5*" -delete</td>
  </tr>
  <tr>
    <td>Используя команду echo, добавьте слово test в файл 4</td>
    <td>$ echo "test" > test3/file4.txt</td>
  </tr>
  <tr>
    <td>Замените слово test в файле 4 на fail</td>
    <td>$ sed "s/test/fail/g" test3/file4.txt -i</td>
  </tr>
  <tr>
    <td>Добавьте в файл 4 слово test так, чтобы сохранилось содержимое</td>
    <td>$ echo "test" >> test3/file4.txt</td>
  </tr>
  <tr>
    <td>Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе</td>
    <td>$ ps aux</td>
  </tr>
  <tr>
    <td>Убейте процесс 666 в консоли</td>
    <td>$ kill 666</td>
  </tr>
  <tr>
    <td>Узнайте доступность ресурса rusau.net, используя ping</td>
    <td>$ ping rusau.net && echo available || echo unavailable</td>
  </tr>
  <tr>
    <td>Отправьте 5 пакетов на сайт rusau.net</td>
    <td>$ ping -c 5 rusau.net</td>
  </tr>
  <tr>
    <td>Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/</td>
    <td>$ curl https://petstore.swagger.io/v2/pet/findByStatus?status=available</td>
  </tr>
  <tr>
    <td>Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/</td>
    <td>$ curl -X POST -H "api_key: special-key" -H "Content-Type: application/json" -d '{"id": 0, "username": "$random", "firstName": "string", "lastName": "string", "email": "string", "password": "string", "phone": "string", "userStatus": 0}' https://petstore.swagger.io/v2/user</td>
  </tr>
</table>
