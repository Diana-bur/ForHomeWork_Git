![Тут должен быть логотип](logo.png)

# Инструкция по git

## 1. Установить git

* Скачать установщик git по ссылке https://git-scm.com/downloads

* Установить git и настроить его под себя

## 2. Инициализация репозитория

* Открыть терминал. 

* Ввести комманду "git init"

![введение команды git init](gitinit.jpg)

*Если git запускается в первые также необходима ввести свои данные, иначе неизбежать ошибок!*

*Для этого используем 2 команды:*

* __git config --global user.name__

* __git config --global user.email__

*Так git будет указывать кто ввел изменения*

![фото имени](name.jpg)

## 3. Сохранение изменений в файл

Чтобы сохранить изменение, необходимо ввести команду git add и кнопкой tab выбрать нужный файл

![введение команды git add](gitadd.jpg)

## 4. Запись изменений в репозиторий

* Чтобы ввести коментарий к изменениям в файле, необходимо ввести команду git commit -m "текст комментария"

![введение команды git commit](gitcommit.jpg)

*В дальнейшем можно использовать git commit -am, чтобы не вводить git add каждый раз*

* Чтобы проверить статус изменений, нужно ввести git status

![введение комманды git status](gitstatus.jpg)

## 5. История изменений файлов

Чтобы вывести историю изменений файла, историю комментариев - нужно ввести команду git log

![введение git log](gitlog.jpg)

*Если хотим сделать log "в одну линию" вводим команду git log --oneline*

![фото oneline](oneline.jpg)

*Если есть побочные ветки и нужно их отобразить, используем git log --oneline --graph*

![фото oneline и graph](onelineENDgraph.jpg)

*В случаи, если возникает поле END в конце - нужно нажать q для выхода*

![END](END.jpg)

## 6. Сравнение изменений

Чтобы сравнить изменения происходящие в папке нужно ввести команду git diff

![ввод команды git diff](gitdiff.jpg)

## 7. Перемещение между версиями

 * Чтобы переместиться в другое сохраненное состояние нужно ввести git checkout и первые 4 символа нужной версии. *Названия версий отображаются в git log*

![фото команды git checkout](gitcheckout.jpg)

 * Возможна ошибка - если не было команды git commit (сохранения). В этом случаи программа предупредит что последние изменения не были сохранены.

![фото ошибки](error.jpg)

 * Чтобы вернутся к последней версии, нужно ввести git checkout master
 ![фото команды git checkout master](gitchecM.jpg)

## 8. Работа с ветками

* Чтобы просмотреть ветки необходимо ввести: git branch

![изоброжение branch](branch.jpg)

*Звездочкой и цветом отображается ветка в кторой мы находимся*

* Для создания новой ветки введите команду git branch название_ветки

![изоброжение git branch brancg_name](branch_name.jpg)

* А для перехода на другую ветку используют команду git checkout название_ветки

![фото перехода в другую ветку](check_branch_name.jpg)

*Чтобы проверить в какой ветке сейчас работаем вводим git branch или git status*

![пример git status](status.jpg)

* Чтобы вернутся в главную ветку (в нашем случаи master), используем команду git checkout master

![Фото возвращения на главную ветку](checkoutMaster.jpg)

* Для слияния изменений вводим команду git merge название_ветки 

**Важно! Слияние нужно делать, только находясь в той ветке в которую мы хотим включить изменения**

![фото слияния](merge.jpg)

  * Если происходит конфликт при слиянии, то всплывает окно с вариантами решения

  ![фото конфликта при слиянии](conflict.jpg)

  1. Принять текущее изменение - конфликтующие позиции останутся такими какие были до слияния.

  2. Принять входящее изменение - конфликтующие позиции будут заменены на теже из слияемой ветки (те что были до слияния - удаляются).

  3. Принять оба изменения - сохраняются все конфликтующие позиции, их можно будет отредактировать в ручную.

  4. Сравнить изменения - открывается файл где детально расписаны все конфликтующие строки. 

* Если в ветке нет надобности, удаляем её комбинацией git branch -d название_ветки

![пример удаления ветки](deleteBranch.jpg)

## 9. Работа с github
- Чтобы начать работать с githab, нужно зарегесрировать ся на сайте github.com
- Чтобы выгрузить сою работу нужно ввести в терминале git push и следовать подсказкам git-а
- Чтобы подгрузить изменения из github нужно ввести git pull и следовать подсказкам git-а
- Чтобы скопировать себе работу другого человека, необходимо сделать форк его работы себе на страницу в github. Затем командой git clone ссылка_на_копию выгрузить данные себе на компьютер

*Чтобы перейти на работу с новым репрезеторием вводим: cd название_скопированной_папки*