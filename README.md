# lerangit
Tutorials:
-- Deutsch:
---- https://studi.f4.htw-berlin.de/www/help/tutorial/git/

#Start tg tg tg tg tg tg tg tg tg tg tg tg tg tg
#\/ \/ \/ \/ \/ \/ \/ \/ \/ \/ \/ \/ \/ \/ \/ \/ 

https://iis.uibk.ac.at/collab/git :
Branches are used to maintain multiple releases simultaneously while developing new features in the trunk. As long as we will not generally have formal releases, there will be little or no need for branches.

#/\ /\ /\ /\ /\ /\ /\ /\ /\ /\ /\ /\ /\ /\ /\ /\ 
# End  tg tg tg tg tg tg tg tg tg tg tg tg tg tg


Wichtige Befehle:

Vorhandenes Repository mit gleichnamigen auf Github verbinden

1. Remote Git-Repository auf http://github.com/... erzeugen

2. Lokales Git-Repository erzeugen
--> git init

3. Lokales und remote Repository verbinden und testen
--> git remote add origin https://github.com/edvapp/test.git
--> git remote -v

4. Daten von remote nach lokalem Repository holen (Readme usw.)
--> git pull origin master

5. Test ob branch Vorhandenes
--> git branch 
sollte 
* master
anzeigen

6. Prüfen welche Dateien noch nicht im Repository sind
--> git status

7. Dateien in Repository aufnehmen
--> git add .

8. Falls noch nicht erledigt:
--> git config --global user.email "you@example.com"
--> git config --global user.name "Your Name"

10. Änderung commiten
--> git commit -m "first commit"

11. Commit nach remote pushen:
--> git push -u origin master
Achtung -u nur hier nötig

12. Nächsten commit pushen:
--> git push

13. falschen commit rückgängig machen (HEAD um eine commit zurücksetzen):
--> git reset HEAD~1

14: einen evt. zurückgesetzten commit mit Gewalt pushen:
--> git push -f

15: git commit history gut sichtbar machen:
In Datei "homeverzeichnis"/.gitconfig
die Zeile:
[alias]
	hist = log --oneline --decorate --graph --all
einfügen

++++++++++++++++++++++++++++++++++++++++++++++++++++++++


Löschen eines unerwünschten commites git commit -m "unnötiger commit"
--> git reset --hard <sha1-commit-id>

Löschen des letzten unerwünschten commites git commit -m "unnötiger commit"
--> git reset HEAD~1

Löschen eines unerwünschten commites ins Internet gepushed git push
Rücksetzen des Internetrepositories origin auf HEAD
--> git push origin HEAD --force

Einen Branche aus einem Internet - Repository herunter laden:
--> git checkout "Name des Branches"
--> git pull origin "Name des Branches"

Alle Branches aus einem Internet - Repository hinauf laden:
--> git push --all

Eine Datei/ein Verzeichnis aus einem anderen Branch holen:
--> git checkout "Branch, in dem Daten liegen" "Pfad zu den Daten"

