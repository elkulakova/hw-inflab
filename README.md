# Лабораторная работа 4: Работа с grep

## Введение:

Команда `grep` — одна из самых полезных утилит в Linux для поиска текста в файлах и потоках данных. В рамках этой лабораторной работы мы будем использовать `grep` для поиска различных шаблонов в текстовых файлах и оптимизируем запросы с помощью регулярных выражений.

## Пример работы с `grep` **(не включать в отчет!)**:

Создадим текстовый файл с системными логами и используем `grep` для поиска.
```
cat > example_log.txt <<EOL
System: Boot completed
User: Admin login successful
System: Disk check passed
Error: Unable to mount drive
Warning: High CPU usage
User: Logout detected
System: Update available
ERROR: Network connection lost
WARNING: Low disk space
EOL
```

1. Поиск всех строк, содержащих слово "System":
```
grep "System" example_log.txt
```

2. Поиск всех строк, заканчивающихся на "successful":
```
grep "successful$" example_log.txt
```

3. Подсчет всех строк, содержащих "User":
```
grep -c "User" example_log.txt
```

## Задание:

Создайте текстовый файл `logfile.txt` с произвольными строками текста (не менее 10 строк). Вставьте в него строки, содержащие слова "error", "warning" и "info" в разном регистре (например, ERROR, Warning, Info).

Используя команду `grep`, выполните следующие задачи:

- Найдите все строки с ошибками ("error") независимо от регистра.

- Выведите строки, содержащие только слово "warning" в начале строки.

- Найдите строки, содержащие "info" в конце строки.

- Подсчитайте количество строк с "error".

- Сохраните результат каждой команды в отдельные файлы (error_output.txt, warning_output.txt, info_output.txt).

## Рекомендации по оформлению отчета:

Создайте публичный репозиторий на GitHub.
Оформите отчет, описав все шаги работы (создание файла, выполнение команд, сохранение результатов).
Приложите скриншоты терминала с результатами работы.

## Темы, которые нужно знать для защиты работы:

Синтаксис и флаги команды grep.
Основы регулярных выражений.
Работа с текстовыми файлами и потоками ввода-вывода.

## Полезные источники:

[Официальная документация grep (GNU)](https://www.gnu.org/software/grep/manual/)

[Linux man pages (grep)](https://man7.org/linux/man-pages/man1/grep.1.html)

[Tutorialspoint: grep command](https://www.tutorialspoint.com/unix_commands/grep.htm)

[RegExr – сайт для тестирования регулярных выражений](https://regexr.com/)
