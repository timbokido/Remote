![Logo](Git-Logo-1788C.png)
# Работа с Git и Github
## 1. Проверка наличия Установленного Git
В терминале выполнить команду `git version`. Если Git Установлен, появится сообщение о версии программы, иначе будет сообщение об ошибке.
## 2. Установка Git
Загружаем последнюю версию Git с сайта [Установка Git](https://git-scx.com/downloads).
Устанавливаем с настройками по умолчанию.
## 3. Настройка Git
 При первом использовании Git необходимо представляться.
 Для этого нужно ввести в терминале 2 команды:
 ```

 git config -- global user.name <<Ваше имя английскими буквами>>
 git config --global user.email ваша почта@example.com
 ```

 ## 4. Инициализация репозитория
 В терминале переходим к папке, в которой хотим создать репозиторий. Выполняем команду:
 ```

 git init
 ```

 ## 5. Запись изменений в репозиторий
 Для записи изменений нужно сохранить файл, добавить его в отслеживание командой:

```

git add FileName
```
Чтобы записать изменение, нужно воспользоваться командой:

```

git commit -m "комментарий к сохранению"
```

 ## 6. Просмотр истории коммитов
 Команда:
 ```

git log
 ```

 Чтобы посмотреть список логов в формате графа нужно воспользоваться командой:

 ```

 git log --graph 
 ```
 Для вывода логов в одну строку:

 ```

git log --oneline
 ```
 ## 7. Перемещение между сохранениями
 Для перемещения между сохранениями нужно воспользоваться командой:

 ```

git checkout SaveID
 ```
 ## 8. Игнорирование файлов
 Для того, чтобы исключить из отслеживания в репозитории определенные файлы или папки, необходимо создать файл ***.gitignore*** и записать в него их названия или шаблоны, соответствующие таким файлам или папкам.

 ## 9. Создание веток в Git
 По умолчанию имя основной ветки в Git - *master*.
 Создать ветку можно командой:
 ```

 git branch BranchName
 ```

 ## 10. Слияние веток и разрешение конфликтов
 Для слияния выбранной ветки с текущей нужно выполнить команду:
 ```

 git merge <Название выбранной ветки>
 ```
Если была изменена одна и та же часть файла в обеих ветках, то может возникнуть конфликт, который потребует участия пользователя. VSCode предлагает варианты решения.
Чтобы разрешить конфликт, нужно выбрать один из вариантов, либо объединить содержимое по-своему.

## 11. Удаление веток

Для удаления ветки нужно использовать комманду:
```

git branch -d <<BranchName>>
```
# **Работа с удаленными репозиториями **
1. Создать аккаунт на GitHub
2. Создать локальный репозиторий
3. Создать удаленный репозиторий
4. Связать удаленный репозиторий с локальным
   
Добавить удаленный репозиторий к проекту:
```

git remote add <имя репозитория><url-адрес репозитория в сети>
```
Для получения и слияния изменений из удаленного репозитория используется команда `git pull`

Для создания pull request нужно форкнуть чужой проект, клонировать свой форкнутый проект на локальный репозиторий, внести нужные изменения в новой ветке, загрузить измененный проект на гитхаб и сделать пул реквест