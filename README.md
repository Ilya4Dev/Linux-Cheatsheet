# Шпаргалка по Cli Linux :ru: :pill: :blue_book:
------

## Простые команды

`date` - выводит текущие время и дату

`cal` - по умолчанию выводит календарь текущего месяца

`df` - показывает объем свободного пространства на дисках

`free` - показывает объем свободного пространства в памяти

`exit` - завершение сеанса работы с терминалом

## Навигация

`pwd` - выводит название текущего рабочего каталога

`file` - опредяет тип файла

`cd` - выполняет переход в другой каталог

##### Сокращенные варианты команды `cd`

| Сокращение | Результат	
| :-- 	| :--	
| `cd`	| Сменить рабочий каталог на домашний
| `cd -`	| Сменить рабочий каталог на предыдущий рабочий каталог
| `cd ~ username`	| Сменить рабочий каталог на домашний каталог пользователя username
| `cd .`	| Обозачает рабочий каталог	
| `cd ..`	| Обозачает родительский каталог по отношению к рабочему

`ls` - вывдит список содержимого каталога

##### Наиболее популярные параметры команды `ls`

| Параметр | Длинный параметр | Описание
| :-- 	| :-- | :--	
| `-a` | `--all` | Список всех (all) файлов, даже с именами, начинающимися с точки, скрытые файлы
| `-i` |  | Показывает в первом поле номер индексного узла
| `-d` | `--directory` | Выводит информацию о самом каталоге, а не его содержимое 
| `-F` | `--classify` | Добавляет в конец каждого имени символ-индикатор (например, прямой слеш, если это имя каталога) 
| `-h` | `--human-readable` | Отображает размеры файлов не в байтах, а в величинах с единицами измерения 	
| `-l` | | Выводит результаты с использованием длинного формата 
| `-r` | `--reverse` | Выводит результаты в обратном порядке 
| `-S` | | Сортировать результаты по размеру (size)
| `-t` | | Сортировать результаты по времени (time) последнего изменения

`less` - выводит содержимое файла

##### Команды программы `less`

| Команда | Действие	
| :-- 	| :--	
| Page Up или b | Прокрутка к началу на одну страниц  у
| Pae Down или ПРОБЕЛ | Прокрутка к концу на одну страницу
| СТРЕЛКА ВВЕРХ ↑ | Прокрутка к началу на одну строку 
| СТРЕЛКА ВНИЗ  ↓ | Прокрутка к концу на одну строку 
| G | Переход в конец текстового файла
| 1G или g | Переход в начало текстового файла
| n | Поиск следующего вхождения искомой последовательности символов
| h | Вывод экрана со справкой
| q | Завершение less

## Операции с файлами и каталогами

`cp` - копирует файлы и каталоги

##### Параметры команды `cp`

| Параметр | Длинный параметр | Описание
| :-- 	| :-- | :--	
| `-a` | `--archive` | Скопировать файлы и каталоги со всеми атрибутами, включая идентификаторы владельцев и права доступа. Без этого параметра копии обычно получают значения атрибутов по умочанию, определенных для пользователя, выполняющего копирование 
| `-i` | `--interactive` | Запрашивает у пользователя подтверждение перед перезаписью существующего файла. Если этот параметр отсутствует, команда `cp` просто перезапишет существующие файлы
| `-r` | `--recursive` | Рекурсивно копировать каталоги и их содержимое. Это обязательный параметр (или параметр `-a`) при копировании каталогов    
| `-u` | `--update` | При копировании файлов из одного каталога в другой копиро- вать только файлы, отсутствующие в каталоге назначения или более новые  	
| `-v` | `--verbose` | Выводить информационные сообщения в процессе копирования

`mv`- перемещает/переименовывает файлы и каталоги

##### Параметры команды `mv`

| Параметр | Длинный параметр | Описание
| :-- 	| :-- | :--	
| `-i` | `--interactive` | Запрашивает у пользователя подтверждение перед перезаписью существующего файла. Если этот параметр отсутствует, команда `mv` просто перезапишет существующие файлы
| `-u` | `--update` | При перемещении файлов из одного каталога в другой перемещать только файлы, отсутствующие в каталоге назначения или более новые 	
| `-v` | `--verbose` | Выводить информационные сообщения в процессе перемещения

`mkdir` - создает каталоги

`rm` - удаляет файлы и каталоги

##### Параметры команды `rm`

| Параметр | Длинный параметр | Описание
| :-- 	| :-- | :--	 
| `-i` | `--interactive` | Запрашивать у пользователя подтверждение перед удалением существующего файла. Если этот параметр отсутствует, команда `rm` просто удалит существующие файлы
| `-r` | `--recursive` | Рекурсивно удалить каталоги. То есть вместе с каталогом будут удалены все его подкаталоги. Это обязательный параметр при удалении каталогов   
| `-f` | `--force` | Игнорировать отсутствующие файлы и не запрашивать подтверждения. Этот параметр отменяет действие параметра `--interactive`  	
| `-v` | `--verbose` | Выводить информационные сообщения в процессе удаления 

`ln` - создвет жесткие и символические ссылки

##### Параметры команды `ln`

| Параметр | Длинный параметр | Описание
| :-- 	| :-- | :--	
| `-s` |  | Создает символические ссылки почти так же, как жесткие ссылки 

## Работа с командами

`type` - сообщает, как интерпретируется имя указанной команды

`which` - сообщает, какая программа будет выполнена

`man` - выводит страницу справочного руководства с описанием команды

#####  Организация справочного руководства для команды `man`

| Раздел | Содержит 
| :-- 	| :--  
| 1 | Пользовательские команды 
| 2 | Программные интерфейсы системных вызовов в ядре  
| 3 | Программные интерфейсы в библиотеке C
| 4 | Специальные файлы, такие как узлы устройств и драйверы 
| 5 | Форматы файлов 
| 6 | Игры и развлечения, такие как хранители экрана
| 7 | Прочее 
| 8 | Команды системного администрирования

`apropos` - выводит список подходящих команд

`info` - выводит запись из справочного руководства Info с описанием команды

`whatis` - выводит краткое описание команды

`alias` - создает псевдоним для команды

## Перенаправление

`cat` - объединяет файлы

`sort` - сортирует строки текста

`uniq` - сообщает о повторяющихся строках или удаляет их

`wc` - выводит число символов перевода строки, слов и байтов в каждом указанном файле

`grep` - находит и выводит строки, соответствующие шаблону

`head` - выводит первые строки из файла

`tail` - выводит последние строки из файла

`tee` - читает данные со стандартного ввода и записывает в стандартный вывод  и в файлы

## Команда echo

`echo` - это не системная утилита, у нее нет исполняемого файла. Она существует только внутри интерпретатора Bash

*$ echo опции строка*

#####  Опции для команды `echo`

| Опция | Содержит 
| :-- 	| :--  
| `-n` | Не выводить перевод строки
| `-e` | Включить поддержку вывода Escape последовательностей  
| `-E` | Отключить интерпретацию Escape последовательностей

## Команды перемещения курсора

| Клавиша | Действие 
| :-- 	| :--  
| `CTRL+A` | Перемещает курсор в начало строки
| `CTRL+E` | Перемещает курсор в конец строки 
| `CTRL+L` | Очищает экран и устанавливает курсор в левый верхний угол. То же самое делает команда clear
| `CTRL+K` | Удаляет символы от позиции курсора до конца строки
| `CTRL+U` | Удаляет символы от позиции курсора до начала строки
| `CTRL+C` | Прерывает/завершает выполнение программы

## Привилегии

`id` - выводит информацию об идентичности пользователя

`chmod` - изменяет режим доступа к файлу

##### Режимы доступа к файлу в двоичном и восьмеричном представлениях

| Восьмеричное |  Двоичное | Режим доступа
| :-- 	| :-- | :--	 
| 0 | 000 | ---
| 1 | 001 | --x   
| 2 | 010 | -w-
| 3 | 010 | -wx
| 4 | 100 | r--
| 5 | 101 | r-x
| 6 | 110 | rw-
| 7 | 111 | rwx

##### Символическая форма записи аргументов команды `chmod`

| Символ | Значение 
| :-- 	| :--  
| `u` | Сокращенно от *user* (пользователь), означает владельца файла или каталога
| `g` | Группа
| `o` | Сокращенно от *other* (другие, остальные), означает весь остальной мир
| `a` | Сокращенно от *all* (все); комбинация из всех трех символов: u, g и o

`umask` - определяет разрешения доступа к файлам по умолчанию

`su` - запускает командную оболочку от имени другого пользователя

`sudo` - выполняет команду от имени другого пользователя

`chown` - изменяет владельца файла

*$ chown name picture.jpg*

`chgrp` - изменяет группу файла

`passwd` - изменяет пароль пользователя

## Процессы

`ps` - выводит список процессов, выполняющихся в текущий момент

`top` - выводит задачи

`jobs` - выводит список активных заданий 

`bg` - переводит задание в фоновый режим работы

`fg` - переводит задание в режим работы на переднем плане 

`kill` - посылает сигнал процессу 

##### Часто используемые сигналы

|  Номер | Имя | Значение
| :-- 	| :-- | :--	 
| 1 | HUP | Этот сигнал используется, чтобы подсказать программе, что потеряна связь с управляющим терминалом. Действие этого сигнала можно продемонстрировать, закрыв окно терминала. Программа переднего плана, запущенная в терминале, получит сигнал и завершится
| 2 | INT | Прервать. Выполняет ту же функцию, что и нажатие комбинации CTRL+C в терминале. Обычно приводит к завершению программы
| 3 | QUIT | Выйти  
| 9 | KILL | Уничтожить. Ядро немедленно завершает указанный процесс
| 11 | SEGV | Ошибка сегментации. Этот сигнал посылается программе, предпринявшей попытку недопустимого обращения к памяти, то есть попытку выполнить запись в память, доступ к которой запрещен 
| 15 | TERM | Завершить. Это сигнал по умолчанию, посылаемый командой `kill`. Если программа достаточно «живая», чтобы принять этот сигнал, она завершится
| 18 | CONT | Продолжить. Этот сигнал восстанавливает нормальную работу процесса после сигнала STOP
| 19 | STOP | Приостановить. Этот сигнал заставляет процесс приостановиться, не завершаясь. Подобно сигналу `kill`, он не передается целевому процессу и потому не может быть проигнорирован им
| 20 | TSTP | Сигнал «стоп» с клавиатуры. Этот сигнал посылается терминалом после нажатия комбинации CTRL+Z. В отличие от сигнала STOP, TSTP передается программе, и программа может решить игнорировать его
| 28 | WINCH | Изменение окна. Этот сигнал посылается системой при изменении размеров окна терминала. Некоторые программы, такие как top и less, реагируют на этот сигнал, обновляя свой вывод в соответствии с новыми размерами окна терминала

`killall` - останавливает процессы по именам

`shutdown` - останавливает или перезагружает систему

  