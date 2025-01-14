# GR_4406

# Инструкция по работе с Git 

!["Hey, it's Git!"](pic.png)

Системы контроля версий, одной из которых является Git, используются при работе с
самыми разными проектами, начиная от программных проектов и заканчивая написанием книги или статьи.

Git позволяет работать с __разными версиями одного и того же документа__, не создавая при этом избыточного количества файлов.

## Быстрая настройка Git

>Нам будет достаточно только задать имя и email командами. Например: 
*    git config ­­global user.name "Oleg Yasnev" 
*  git config ­­global user.email oyasnev@gmail.com

## Базовые команды 

Базовые команды – самые часто используемые, нужные для фиксации изменений и добавления комментариев к ним. 

### Добавление новых файлов в репозиторий 

* Чтобы «запустить» Git в папке и заставить его отслеживать изменения в ее файлах, используйте команду **git init**

* Чтобы добавить файл, создайте файл и после этого используйте команду **git add «file name»**

### Сохранение изменений файлов 

* Чтобы проверить редактируемый файл на наличие изменений, используйте команду **git status**. Она помогает понять, есть ли у вас какие-либо изменения, которые требуется сохранить. 

* Чтобы сохранить изменения, используйте комбинированную команду **git commit -a -m "текст сообщения"**. 

>Она позволит вам избежать повторного использования команды **git add** перед каждым коммитом и также позволит добавлять сообщения (-m) к каждому сохранению. 

## Переключение между версиями 

* Чтобы просмотреть все версии одного документа, используйте команду **git log**

* Чтобы переключиться на конкретную версию, используйте команду **git checkout «первые 4-5 цифр из названия версии»**

## Создание ветвей и операции с ними 

!["It's branches"](gitbranches.png)

Ветви нужны для лучшей классификации версий документа и для возможности одновременно курировать как черновые, так и чистовые варианты одного и того же документа. 

>Или – для упорядоченной совместной работы над разными версиями документа с коллегами. 

* Чтобы просмотреть, на какой ветви вы сейчас находитесь, используйте команду **git branch**

* Чтобы создать новую ветвь, используйте команду **git branch «имя новой ветви»**

* Чтобы переместиться на нужную ветвь, используйте команду **git checkout «имя ветви»** 

* Чтобы слить ветви вместе _(внимание, эту команду надо отдавать из ветви, в которую вы планируете перемещать информацию из второй ветви – не наоборот)_, используйте команду **git merge «имя ветви, информацию _из_ которой вы хотите слить»**

* Чтобы удалить ветвь, используйте команду **git branch -d «имя ветви»**

## Работа с удаленными репозиториями

* Сначала вам надо зарегистрироваться на GitHub – это сервис, позволяющий размещать удаленный репозиторий в сети, видеть удаленные репозитории других людей и работать с ними. 

* После регистрации и создания собственного репозитория, вы можете выгрузить файлы, отслеживаемые Git, с вашего компьютера в сеть. Для этого вам надо воспользоваться рядом команд, **которые GitHub предоставит вам после создания первого нового репозитория.** 

* После этого вы сможете «пушить» изменения, вносимые в файлы на компьютере, в сеть – и наоборот, вытягивать изменения, вносимые напрямую в репозиторий онлайн в ваш компьютер. 
1. **git push**
2. **git pull**

>Чтобы скопировать себе чей-либо репозиторий и работать с ним со своего компьютера, вы можете воспользоваться командой **git clone «ссылка на нужный репозиторий»**.

### Что означает «форкнуть» проект? 

>Форкнуть – значит создать полную копию проекта с чужого репозитория в вашем репозитории. Это позволит вам внести какие угодно изменения, а после – вы сможете предложить их хозяину проекта в качестве проделанной работы или помощи. 
