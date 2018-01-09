# Git Basics
* Git init
* Git status
* Git add &nbsp;( save to git )
* Git add . &nbsp; ( track all )
* Git reset HEAD filename &nbsp; ( untrack some )
* .gitignore &nbsp; ( liste ignored files or folder/ inside )
* Git rm --cached &nbsp; ( remove from git )
* Git commit
* Git commit -m ' '
* Git commit -a -m ' ' &nbsp; ( -a add mettre * files en zone staged)

# Git Checkout
* Git log &nbsp; ( q -> logout )
* Git log --oneline &nbsp; ( liste commit en 1 ligne )
* q &nbsp; ( quit )
* Git checkout &nbsp; ( commit | master ) <br>
ls ( to see from wich file commit come )
* Git reset --hard commitID &nbsp; ( efface après selected commit )
* Git diff commitID_1  commitID_2  &nbsp; ( difference entre 2 commits )
* Git diff commitID_2 &nbsp; ( compare difference commitID_1 actuel avec autre commit )

Head &nbsp; 0 -> 0 -> 0 -> 0 &nbsp;Master
               
# Git Branch
* Git branch contact &nbsp; ( pour créer page contact.html ) 
* Git branch &nbsp; ( affichage des différentes branch ) <br>
-> contact <br>
-> master
* Git checkout contact &nbsp; ( switch vers la branch contact )
* Git merge contact &nbsp; ( depuis master FUSIONNE branch contact )
* Git branch -D contact &nbsp; ( Delete contact branch )<br><br>
* PS : pour créer une branch et directement checkout dessus : <br>
-> Git checkout -b contact &nbsp; ( -b &nbsp; === &nbsp; branch )<br>
-> Git add -i (interactif)<br>
-> Git add -p ( )


# Git Flow ( easy tool )

 4 branchs -> feature | develop | release  | master <br>

 feature -> quand feature finish then merge with develop<br>
 develop -> fusionne régulièrement entre master et release<br>
 release -> derniers correctifs de l'ensemble avant master<br>
 master -> finalité tout doit fonctionner

 5ème branche -> HOTFIX

Git init

* Git flow init

Git branch <br>
  -> develop * <br>
  -> master

* Git flow feature start MYFEATURE

Git branch <br>
  -> develop <br>
  -> master <br>
	-> feature/MYFEATURE *

PS : instead &nbsp; CTRL+V &nbsp; -> &nbsp; CTRL+SHIFT+INSERT

inside feature/index <br>
touch index.html
git add index.html
git commit -m 'creation fichier index.html'

* Git flow feature finish MYFEATURE &nbsp; ( merge with develop )

can add how many features u want<br>
when one is fully checked : 

* Git flow release start index

ici sert surtout tagger la version :

* Git tag 1.0

git tag <br>
-> 1.0 <br>

now can be publish online :

* Git flow release finish MYFEATURE 
* Git push --tags

ensuite si malgrès tout un beug online :

* Git flow hotfix start VERSION master
* Git flow hotflix finish VERSION

qui corrigera aussi dans develop

# Git-Hub

* $ git remote add origin https://repository_link
* $ git push origin master

