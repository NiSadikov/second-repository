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
## Информация про ХЕШ

Хеш - это результат хеширования, т.е получения индетификатора входных данных. Он одинаков для одинаковых исходных данных.  
Использютя цифры от 0 до 9 и латинские буквы от А до F.  

Хеш используют, чтобы индентифировать коммит. Можно посмотреть автора, время и сообщение о коммите.  

## Статусы файлов в GIT

untracked - это файлы, которые не отслеживаются системой.  
staged - это файлы, которые подготовлены к тому, чтобы быть отправлены в коммит, после команды:  
```
git add
```
tracked - это все отслеживаемые файлы, это все файлы, подвергнутые коммиты или добавленные в ослеживание указаной выше командой.  
modified - это состояние, при котором файл был отредактирован. 

## Правило оформления коммитов. 

Все комментарии к коммитам должны быть понятны и информативны. Сообщения не должны быть длиннее 72 символа.  
Должно быть ясно, какое измнение произошло, в каком месте, в чём его суть.  
Все оформления должны быть в едином стиле, например, начинаться с инфинитива: Добавить функцию ввода голосом.  
