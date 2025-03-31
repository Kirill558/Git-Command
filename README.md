# Добавляем в индекс один файл
git add file_name
# Добавляем в индекс несколько файлов 
git add file_name_1 file_name_2 file_name_3
# Добавляем в индекс все изменённые файлы 
git add .
# Вызвать справку
git help command_name


git status   # Запрашиваем текущее состояние репозитория
# Видим файлы, которые находятся в индексе и подготовлены для коммита
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html
        modified:   styles.css
# Видим неотслеживаемые файлы, которые только попали в проект
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        script.js   # Файл script.js не отслеживается Git
# Видим изменённые файлы репозитория, которые ещё не добавлены в индекс 
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        README.md   # Файл README.md был изменён, но не добавлен в индекс

# Добавление файлов в репозиторий
git commit -m "Commit message"

 git log   # Запрос на просмотр журнала коммитов

# Информация о третьем сделанном коммите
commit 3f6f9e1f58e30e0d3a0d0ab764c0b30a5b621d4a   # Хеш первого коммита
Author: John Doe <johndoe@example.com>   # Автор первого коммита
Date:   Thu Apr 21 10:26:52 2024 +0300   # Дата первого коммита
    Update README.md   # Сообщение первого коммита

# Информация о втором сделанном коммите
commit acd1e81729dc2ee2dc107ba345fa1ab7e6cfbff9
Author: Jane Smith <janesmith@example.com>
Date:   Wed Apr 20 16:45:39 2024 +0300
    Add new feature

# Информация о первом сделанном коммите
commit 7df1e8c33b0a617b3a72c785a67e45d0d932a180
Author: John Doe <johndoe@example.com>
Date:   Mon Apr 18 09:12:21 2024 +0300
    Initial commit

# Смотрим разницу между последним коммитом и текущим состоянием репозитория
git diff

# Разница между последним коммитом и текущим состоянием файла 
git diff file_name

# Разница между последним коммитом и коммитом с указанным хешем 
git diff commit_hash

# Разница между последним коммитом и отслеживаемым состоянием репозитория 
git diff --staged