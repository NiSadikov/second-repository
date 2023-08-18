# Работаем с git

Во-первых, необходимо скачать GIT Bash для твоей системы. Будем предполагать, что ты уже освоился с работой командной строки.  
Поэтому для начала работы тебе необходимо будет создать локальный репозиторий. Сделаем это в корневой папке.  

```
cd ~ && mkdir repository $$ git init
```

После этого ты можешь связать свой удалённый репозиторий с локальным репозиторием. Для этого тебе потребуется SSH ссылка на твой локальный репозиторий.  
```
git remote origin git@github.com:NiSadikov/second-repository.git [ссылка]
```
Проверить успешность работы можно следующим образом:  
```
git remote -v 
```
Теперь ты можешь работать в своём локальном репозитории и управлять при этом своим удаленным репозиторием. Давай я покажу это на примере файла README.md  

```
touch REAMDE.md
```
После того, как закончишь его редактировать, необходимо его добавить в отслеживание системой контроля версий
```
git add REAMDE.md
```
Теперь, чтобы создать коммит, то есть сделать фотографию на фотоаппарат, необходимо выполнять следующее:  
```
git commit -m 'Добавлен файл REAMDE.md'
```
Чтобы загрузить свою работу на удаленный репозиторий, необходимо выполнить следующее:  
```
git push
```
Также для тебя могут быть полезны следующие коменды, которые позволяет смотреть текущий статус и свои коммиты:  
```
git status
git log
```