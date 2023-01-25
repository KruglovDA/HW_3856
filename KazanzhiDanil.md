# 1. Headlines

1. git global user.name "name"
    
        how to use insertet text?
        Just intend it with several spaces.

1. git global user.email "email@mail.com"

       saving our contact`s for other people
1. git init

1. git add < file >

git commit -m < text > or   
git commit -am < text >

       it`s important to keep order 

1. git status

1. git log

       show all commits

1. git checkout {#hash}

       command to switch between commit`s

## Highlight text

* **Bold**

* *Italic*

* ~~Strikethought~~

* ***Bald italic***

* ~~*__What if we print this?__*~~

## Link`s

1. https://gb.ru/ 
or
2. [gb.ru][https://gb.ru/]

## Quotes

> Let`s make a conflict in this branch
>>You can ask me
>>>How to make it?

>>I`ll answer

>Well, the answer is
>>Type or make something
>>>On the same string in 2 different branches.

[Job`s done](Jobsdone.PNG)

# 2. Branching
1. git branch - show branch list

1. git branch branch_name

1. git checkout branch_name

1. git branch -d branch_name - to delite branch

## Branch merging
1. git merge branch_name

         WARNING!!!
         You must be on "master" or branch you want to push changes from another branch to.
2. git log -graph

       If you want to view visualisation of commits history.

# 3. Work with Github
* git clone "github_name"

       make a copy of remote repository or fork

* git remote add origin "github_name"

       to make chain of local and remote repos

* git push -u origin main

       send status of local repo to remote repo

* git pull

       send status of remote repo to local repo

* git push --set-upstream origin "branch_name"
    
        make a pull request
## Pull requst
1. Делаем (fork) интерегующего нас репозитория.
2. мы делаем git clone для нашей ветки репозитория
3. мы создаем ветку с предлагаемыми изменениями
4. производим все изменения только в этой ветке
5. отправляем эти изменения на свой гитхаб аккаунт
6. в окне в гитхаб появляется возможность создать pull request.

[Github.com](https://github.com/)