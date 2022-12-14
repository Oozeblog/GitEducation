# Руководство по работе с Git

## <u> Семинар 1 </u>

### Перед началом работы стоит выполнить команды:

* *git --version* - покажет текущую версию git

* *git config --global user.name Name* - установит имя пользователя в git

* *git config --global user.email email* - установит email пользователя в git

### Начало работы с Git:

* *git init* - команда выполняется внутри папки, делает папку репозиторием

* *git status* - показывает текущее состояние репозитория

* *git add* - добавляет файлы к отслеживанию

* *git commit - m 'Message'* - создает коммит и записывает сообщение к нему 

* *git commit* - создает коммит и вызывает ~~страшное~~ окно для его записи. **Лучше пользоваться предыдущей командой: *git commit -m 'Message'* !!!**

### Работа с версиями:

* *git log* - доступ к истории коммитов репозитория <u> **Не растягивать окно - может зависнуть программа!!!** </u> Пользоваться клавишами со стрелками для прокрутки, или нажать 'q' если нет надобности просматривать все изменения.

* *git log --oneline* - доступ к истории коммитов в компактном виде

* *git checkout 'commit number'* - переход на состояние указанного коммита

* *git checkout master* - вернутся к последней сохраненной версии

* *git diff* - показывает разницу между текущей и сохраненной версией файла

## <u> Семинар 2 </u>

### Создание веток

* *git branch < BranchName >* - создать ветку BranchName

* *git branch* - просмотреть список веток имеющихсяся в репозитории

* *git checkout < BranchName >* - переход на ветку BranchName

* *git branch -d < BranchName>* - удалить ветку BranchName

* *git branch -d < BranchName >* - удалить ветку BranchName

 **Перед удалением веток необходимо убедиться, что вся нужная информация слита и сохранена на ветке мастер!**

### Слияние веток

* *git merge < BranchName >* - сливает ветку BranchName в ветку master (при нахождении на ветке master)

* *git log --graph* - история изменений в графическом виде (дерево веток)

#### Виды слияний

1. *Fast-forward* - сливаемая ветка и мастер "шли одним путем". Изменения только на одной ветке. Нет конфликта.

2. *Merge made by the 'ort' strategy* - изменения были на сливаемой ветке и на ветке мастер, но в разных местах. Автоматически записывается коммит о слиянии. Нет конфликта.

3. *Merge conflict. Autumating merge failed* - сливаемая ветка и ветка мастер были изменены в одной и той же зоне. Конфликт - автоматическое слияние невозможно.

### Возникновение и решение конфликтов

Если изменения в сливаемых ветках захватывают общую рабочую зону - это приводит к конфликтам при слиянии. 

Варианты действий:

1. Принять текущие изменения (сохранятся только изменения из ветки мастер)

2. Принять входящие изменения (сохранятся только изменения из сливаемой ветки)

3. Приянять оба изменения (сохранятся изменения обоих веток)

4. Сравнить версии изменений
