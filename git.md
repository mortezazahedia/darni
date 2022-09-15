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

signing pgp(pretty good privacy)



