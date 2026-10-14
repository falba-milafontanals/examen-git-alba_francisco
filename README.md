Alba Vilchez, Francisco

\#Ex. 1

* mkdir examen
* cd examen
* mkdir examen-git-alba\_francisco
* cd examen-git-alba\_francisco/
* git init



\#Ex. 2

* notepad README.md
* git add .
* git commit -m "Primer commit"



\#Ex. 3

* git remote add origin git@github.com:falba-milafontanals/examen-git-alba\_francisco.git
* git push -u origin main



\#Ex. 4

* cd ..
* git clone git@github.com:bernatorellana/ExamenGit2627.git



\#Ex. 5

* cd ExamenGit2627/
* git branch -r



origin/HEAD -> origin/main 	

origin/main			Es la branca principal que es fa servir en producció, aquí ja no s'hauria de trobar errors.

origin/develop			Es la branca on es desenvolupen totes les noves funciones sense tocar la branca principal de produccio.

origin/feature/A		Es la branca on s'esta desenvolupant la feature A. Aquesta branca es crea apartir de la branca develop.

origin/feature/B		Es la branca on s'esta desenvolupant la feature B. Aquesta branca es crea apartir de la branca develop. Com es veu, cada nova feature hauria d'anar en una branca separada per a no trobar-se amb posibles conflictes de una altra feature.

origin/hotfix/v2.0.1		Aquesta branca serveix per a solucionar un error que s'ha trobat a produccio, despres s'ha de fusionar amb la branca develop.

origin/support/v2.0		Aquesta branca serveix per a donar suport a una versio antiga del programa, per exemple, arreglant problemes de seguretat o petits errors.



\#Ex. 6

* git diff 0edf191 src/main/java/cat/institut/biblioteca/Biblioteca.java



Aquella versio solament tenia un metode public:
public void afegir(Llibre llibre)



Ara té tots aquests:

public void afegir(Llibre llibre)

public void prestar(String isbn) 

public void retornar(String isbn) 

public boolean estaPrestat(String isbn)



\#Ex 7.

* git checkout v2.0
* git checkout -b alba\_francisco/feature



\#Ex 8.

* mkdir alumnes
* echo "Francisco Javier Alba Vilchez" > alumnes/alba\_francisco.txt
* git add .
* git commit -m "Creat carpeta alumnes per guardar el nom complet de cada alumne. Afegit alumne Alba Francisco."
* notepad docs/TODO.md
* git add .
* git commit -m "S'ha marcat com a fet 'Revisar la documentació'"
* rm docs/notes-antigues.txt
* git add .
* git commit -m "S'ha eliminat l'arxiu notes-antigues.txt"
* git lg1



\#Ex 9. (No ha surtit bé)

* git rebase alba\_francisco/feature  -i
* git rebase --continue
* git lg1



\#Ex 10.

* git tag alba\_francisco/feature\_completed



\#Ex 11.

* git push -u origin alba\_francisco/feature
* git push --tags



\#Ex 12.

* git pull
* git checkout develop
* git merge alba\_francisco/feature --no-ff
* git status
* notepad docs/TODO.md 
* git status
* git add .
* git commit -m "Merged alba\_francisco/feature with develop"
* git push



Aquí he hagut d'arreglar uns conflictes a notepad docs/TODO.md.



\#Ex 13.

* git checkout -b alba\_francisco/release



\#Ex 14.

* notepad pom.xml
* notepad src/main/java/cat/institut/biblioteca/App.java
* git add .
* git commit -m "Canviar numero de versio."



\#Ex 15.

* git tag
* git pull
* git checkout main
* git merge alba\_francisco/release --no-ff
* git tag alba\_francisco/v3.0
* git push



1. Hi ha la versio v1.0 i v2.0.





