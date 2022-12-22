Projekt powstał w trakcie czytania książki "Git i GitHub Kontrola wersji, zarządzanie projektami i zasady pracy zespołówej" autorstwa Mariot Tsitoara. W poniższym pliku zostawiam sobie jako notatkę stany git, komendy oraz inne cenne wskazówki:

1. GIT
1.1. Stany:
1.1.1. Modyfikacja - Katalog roboczy - aktualna migawka, nad która odbywa się praca
1.1.2. Przechowalnia - pliki w stanie, aktualnym gotowe do zapisania w bazie danych (git add z uwzględnieneim wyłaczeń w pliku .gitignore)
1.1.3. Zatwierdzenie - Katalog git - baza danych, migawka całego projektu

1.2. Komendy:
1.2.1. git init - inicjuje kontrolę wersji w folderze i tworzy ukrytą strukture pliku do obsługi gita.
1.2.2. git clone - kopiuje istniejącą baze danych.
1.2.3. git status - sprawdza status lokalnego projektu.
1.2.4. git diff - pokazuje zmiany wprowadzone do projektu od ostatniego commita np. dla jednego pliku git diff todo.txt
1.2.5. git commit - zapisuje stan przechowalni do bazy danych z komentarzem (git commit -m '....' umożliwia komentarz w jednej liniii wiersza poleceń.
1.2.6. git push - kopiuje lokalną baze na zdalny serwer
1.2.7. git pull - kopiuje zdalną baze na lokalny serwer
1.2.8. git log - sprawdza historię projektu (commity) (--graph; -n; --since=2018/11/11; --reverse; --after=2022/12/21; --author=AndrzejKobuszewski; --oneline)
1.2.9.	git branch - wyświetla listę gałęzi, tworzy je lub usuwa
1.2.10. git merge - scala historię dwóch gałęzi
1.2.11. git stash - składuje bieżące zmiany do wykorzystania później
1.2.12. git checkout ...skopiowany z git log numer commita.... - przeniesienie się do wersji z podanego commita
1.2.13. git checkout master - powrót do aktualnej wersji (ostatniego commita)
1.2.14. git config --global user.name "AndrzejKobuszewski" // bez cudzysłowia po prostu zwraca pole user.name
1.2.15. git config --global user.email "AndrzejKobuszewski(At)xxx.xx" // bez cudzysłowia po prostu zwraca pole user.email
1.2.16. git show ...skopiowany z git log numer commita.... - pokazuje zmiany zcommitowane.
1.2.17. git revert ...skopiowany z git log numer commita.... - wprowadza zmiany przeciwne do ostatniego commita. Cofa nowym commitem do poprzedniego stanu.
1.2.18. git commit --amend - modyfikacja ostatniego commita.

1.3. Dobre praktyki
1.3.1. Nazwy commitów: do 50 znaków; z wielkiej litery; w czasie teraźniejszym, bez szczegółów, skonstektualizowane do projektu i jego postępu; bez kropki na końcu. np. Poprawia literówkę w wywołaniu bazy danych, refaktoryzuje funkcję logowania do ponownego użycia.
1.3.2. NIGDY NIE ZMIENIAMY PRZESZŁOŚCI

2. Zdalny GIT
2.1. sudo git remote add origin ...link do utworzonego repo... - dodaje repo
2.2. git remote - nazwa repozystorium oraz git remote -v - wyświetla origin repozytorium git
2.3. git clone, git pull, git checkout master  git merge develop, git branch (nowa gałąź)
2.4. git branch -d - usuwa gałąź
2.5. git remote set-url origin ...link do repo...
2.6. git diff --staged - różnice w przygotowanych plikach
2.7. git rebase master .... nazwa nowej gałęzi.... - uworzenie nowej gałęzi z rodzica z najnowszego commita.



