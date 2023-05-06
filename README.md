# GIT Homework 1

### 1. Создать внешний репозиторий c названием TXT.
  Для этого заходим в аккаунт Guthub, нажимаем на "_Repositories_" после на "_New_", называем и создаем.

---

### 2.  Клонировать репозиторий TXT на локальный компьютер.
  Для клонирования репозитория нужно создать папку, после с помощью скопированого URL
```
    git clone https://github.com/Kr0k0d/TXT.git
```
_Вывод_
```
    Cloning into 'TXT'...
    remote: Enumerating objects: 3, done.
    remote: Counting objects: 100% (3/3), done.
    remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    Receiving objects: 100% (3/3), done.

```

---
### 3. Внутри локального TXT создать файл “new.txt”.
```
  touch new.txt
```

---

### 4. Добавить файл под гит.
  Подготавливаем файл: 
  ```
  git add .
  ```
  Проверяем состояние изменений:
  ```
  git status
  ```
  _Вывод_
  ```
   On branch main
   Your branch is up to date with 'origin/main'.
   Changes to be committed:
   (use "git restore --staged <file>..." to unstage)
        new file:   new.txt

  ```

---

### 5. Закоммитить файл. 
  Коммит нужен для фиксации изменений:
  ```
  git commit -m "Create new file"
  ```
  
  _Вывод_
  ```
  [main 19fdd15] Create new file
  1 file changed, 0 insertions(+), 0 deletions(-)
  create mode 100644 new.txt


  ```

---

### 6. Отправить файл на внешний GitHub репозиторий.
  Отправляем коммит и принимает ответ:
  ```
  git push
  ```
  
  _Вывод_
  ```
  Enumerating objects: 4, done.
  Counting objects: 100% (4/4), done.
  Delta compression using up to 4 threads
  Compressing objects: 100% (2/2), done.
  Writing objects: 100% (3/3), 276 bytes | 138.00 KiB/s, done.
  Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  To https://github.com/Kr0k0d/TXT.git
   ef86827..19fdd15  main -> main


  ```

---

### 7. Отредактировать содержание файла “new.txt" - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате TXT.
```
nano new.txt
```
  ```
  Новиков Данилл Дмитриевич
  Возвраст: 19
  Количество домашних животных: 1
  Желаемая зарплата:30000
  ```

---

### 8. Отправить изменения на внешний репозиторий.
Для отправки изменений выполняем теже действия, что и в пунктах 4-6
```
git add .
```
```
git commit -m "File changed"
```
_Вывод_
```
[main c4a9fb8] File changed
 1 file changed, 4 insertions(+)
```
```         
git push
```
_Вывод_
```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 398 bytes | 199.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Kr0k0d/TXT.git
   19fdd15..c4a9fb8  main -> main


```

---

### 9. Создать файл preferences.txt
```
touch preferences.txt
```
  
---

### 10.В файл preferences.txt добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате TXT.

  ```
  nano preferences.txt
  ```
  Открывется менюшка где мы вводим данные
  ```
  Любимый фильм: 1 + 1
  Любимый сериал: Люцифер
  Любимая еда: Стейк
  Страна которую хотел бы посетить: Италия

   ```
   Полсе нажимаем Ctrl+X после Y и enter.
   
---

### 11.  Создать файл sklls.txt добавить информацию о скиллах которые будут изучены на курсе в формате TXT
  Все тоже самое, что и в пункте 10 
  ```
  touch sklls.txt

  nano sklls.txt
  ```
  ```
  Tesring Basics, Manual testing, Automated testing, Security testing,
  Basics of programming, Database basics, Modern testing methods,
  Communication and interpersonal skills,Project manegement,Tools skills(Postman)


  ```
  
---

### 12, 13. Сделать коммит в одну строку; Отправить сразу 2 файла на внешний репозиторий.
  ```
  git add . 
  
  git commit -m "Added information" preferences.txt sklls.txt
  ```
  _Вывод_ 
  ```
  [main e0b999c] Added information
 2 files changed, 8 insertions(+)
 create mode 100644 preferences.txt
 create mode 100644 sklls.txt
  ```
  ```
  git push
  ```
  _Вывод_ 
  ```
  Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 619 bytes | 309.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Kr0k0d/TXT.git
   c4a9fb8..e0b999c  main -> main


  ```
### 14. На веб интерфейсе создать файл bug_report.txt.
Для этого нужно открыть GitHub, перейти в репозиторий,  нажать на кнопку "Add file" и выбрать "Create new file". Добавляем bag report
```
id: 404
Name: Ошибка при загрузке страницы.
Description: При попытке загрузить страницу, браузер выдает ошибку "404 Not Found". Это происходит на всех страницах сайта, не только на одной.
Environment: Windows 10 Chrome.
Reproduction: Открыть любую страницу на сайте и попытаться ее загрузить.
Expected result: Страница должна загрузиться без ошибок.
Current result: Браузер выдал ошибку "404 Not Found".
```

### 15. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
Нажимаем на кнопку "Commit changes".

### 16.На веб интерфейсе модифицировать файл bug_report.txt, добавить баг репорт в формате TXT.
Через GitHub внести изменение в файл bug_report.txt
```
Priority: hight
```
### 17. Сделать Commit changes (сохранить) изменения на веб интерфейсе.

Как и в пункте 14 коммитим изменения

### 18. Синхронизировать внешний и локальный репозиторий TXT

Сохранить изменение на компьютере, помодет команда 

Я до этого уже сохранял изменения, поэтому у меня два вывода
```
git pull
```
_Вывод_
```
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (9/9), 4.35 KiB | 78.00 KiB/s, done.
From https://github.com/Kr0k0d/TXT
   e0b999c..29f5d67  main       -> origin/main
Updating e0b999c..29f5d67
Fast-forward
 README.md      | 206 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 bug_report.txt |   7 ++
 2 files changed, 212 insertions(+), 1 deletion(-)
 create mode 100644 bug_report.txt

```

```
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 676 bytes | 33.00 KiB/s, done.
From https://github.com/Kr0k0d/TXT
   29f5d67..cfa2300  main       -> origin/main
Updating 29f5d67..cfa2300
Fast-forward
 bug_report.txt | 1 +
 1 file changed, 1 insertion(+)
```
