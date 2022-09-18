apt install git

git --version

git init

git status

git add

git status

git commit -m

git status

git logs





---

#change file 1.txt

git diff head

git add -A

#we doubt

git diff --staged

#change file 2.txt

git add -A

git reset 2.txt

git status

#restore completely to previous point

git checkout -- 2.txt





--------------------branch 5

git branch br1

git branch

git checkout br1

​		git branch

​		git add -A

​        git commit -m '....'

git merge br1

git log



------------------6

vim 666.txt

git add -A

git commit -m '--------------'

git branch br2

git checkout br2

​    git rm 666.txt 

​    git add -A

​	git commit -m 

​    git checkout master

git merge br2

git branch -d br1





------------------------

git clone https://github.com/jadijadi/titap_mystry.git

#change

git status

#change local

git push origin master  (-u)  #yani ino negah midare az seri bad lazem nist bezanim az origin be master

#change online

git pull origin master



----------------------------- 8

git remote

git status

git remote add origin https://github.com/mortezazahedia/darni.git

git  push origin master

git remote remove origin







-------------------------9 versioning

https://www.youtube.com/watch?v=JCcrdW4Llm0



git show #commit

git tag

git tag -a v2.0 -m '..........'

git tag



git tag -a v1.8 -m ' ......' #commit

git tag -l 'v*'

git show #tag

#tag ha khod be khod push nemishavand va baad be rabveshhae zir push kard

git push origin #tag

git push origin --tags

git checkout v1.8    #(we cant commit and we must create branch)







---------------------10

#pgp(pretty good privacy)

gpg --list-keys

git config

git config --list
git config --global user.name

gpg --list-secret-keys

git config --global user.signingkey

gpg --list-secret-keys --keyid-format LONG

git config --global user.signingkey #newval





----------------------11

git help blame

git blame 1.txt

git blame 1.txt -L1

git blame 1.txt -L1,3





#in project root

git bisect start

git bisect bad

git bisect good #commit id

#repeat

​	git bisect bad

​	git bisect good



---------------------------------------------------------------

type  

```git
#find path

git config --global --edit
git config --system --edit
git config --local --edit
```



```
#configuration

git config --local --list
git config --list
git config --global user.name
git config --global user.name #newname
```



```
#snapshot

"reza " >>name.txt
xxd name.txt


```



```
#diff

touch testdiff.txt
echo "ali reza " >> testdiff.txt
git diff
echo "morteza"  >> testdiff.txt
git diff
git diff --stat
git add .

```





```
#reset

soft
mixed
hard

git reset --soft 30acd0a1279b6c1d2a74a0177c8233ee30d40c36
git reset --soft #lastcommit
git reset --mixed 30acd0a1279b6c1d2a74a0177c8233ee30d40c36
git reset --mixed #lastcommit
git reset --hard 30acd0a1279b6c1d2a74a0177c8233ee30d40c36
git reset --hard #lastcommit
```





```
#on git folder

nano .gitignore

    server[1-5].log
    *.info
    !server.info
    tmp
    
    ,,, dont work
    ,,,logs/temp
	,,,logs/temp/!dir3/!*
```





```'
git log --until=sep--16--2022

git log --until=sep--16--2022
git log --until='Fri Sep 16 20:09:45 2022 +0430'

git log --since=sep--16--2022
git log --since='Fri Sep 16 20:09:45 2022 +0430'

git log  --author=ali 
git log  --author='ali'

git log --grep=s

```





```
#branch

master
develop
features AI


git branch
git branch -r (--remote)
git branch -a (-all)


git branch
git branch -b br2
git checkout -b br2
git checkout master
git branch -c br2 br3
git branch
git branch -contains bde37eb1c6a152c0c0dac7a5b8fc628173a1d8e8
git branch --contains bde37eb1c6a152c0c0dac7a5b8fc628173a1d8e8
git branch -a --contains bde37eb1c6a152c0c0dac7a5b8fc628173a1d8e8
```



```

merge br1            			#without commit (conditional)
merge br1 --no-ff				#with commit
git merge -s octopus br1 br2	#with commit
git merge -s ours br1 br2		#old branch unchanges
git merge br1 --squash			#stage changes

git diff master branch
git merge master br1
nano cc

```



```
#only for modified files
git commit -am '............'  
```



```
#blame

git blame 1.txt
git blame -e 1.txt
git blame -s 1.txt
git blame -L 1,1 1.txt
git blame -L 1,5 1.txt
git blame -l 1.txt
```

```
cherry pick

 cd /c/gitexample/cc
 git init
 touch main
 cd add .
 git add .'\nq\n'
 git status
 git add .
 git commit -m '1st main'
 git branch register
 git branch login
 git checkout register
 echo '<p>reg</p>' >> reg.html
 git add .
 git commit '2st reg.html'
 git checkout login
 touch log1.html
 git add .
 git commit -m '2st log1.html'
 touch reg1.html
 git add .
 git commit -m '3st reg1.html'
 git log
 
 
 
 git checkout register
 git log login
 git cherry-pick #commitid
 
 git checkout login
 touch test >> reg1.html
 git add . 
 git commit -m '2st log1.html'

# for chaning commit message
 git checkout login
 cat reg1.html
 echo 'rrrrrrrrrrrrrrrrr' >> reg1.html
 git commit -am '4st wrong commit'
 git log
 git checkout register
 cat reg1.html
 git log login
 git cherry-pick dadda7159f1eb218c9ef44d6fd82c28180aafe8d
 #edit commit message
 git cherry-pick -e dadda7159f1eb218c9ef44d6fd82c28180aafe8d  
 git log
 cat reg1.html
 
  #staged change
  git cherry-pick -n dadda7159f1eb218c9ef44d6fd82c28180aafe8d #add changes only to repositoy stage
  git diff
  git diff --staged
  git cherry-pick --keep-redundant-commits dadda7159f1eb218c9ef44d6fd82c28180aafe8d #add changes only to repositoy stage
```





```
#change only last commit message
git checkout login
git log
git commit --amend -m '5st this message move to branch register'
git log

```



```
#difference between commit

git checkout dest_branchid
git cherry source_branchid
git cheryy -v branchid #show comment
git show commitid
```







