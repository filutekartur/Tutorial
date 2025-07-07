# This is header
This is not header

Git to kontrola wersji lokalnie na komputerze
Github to zdalny system kontroli wersji. Możemy posiadać wiele repo
Repozytoria/Projekty możemy pushować do githuba lub pullować/clonować do lokalnego gita

README.md plik strony głównej na githubie. opisuje repo

Przy comicie na githubie i tak samo na gicie podajemy opis tego konkretnego comita i jego description. Potem wiemy co zmienił konkretny commit

## Dodawanie lokalnego klucza ssh do githuba
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
Dodawanie lokalnego klucza do gituba autoryzuje nas i pozwala nam modyfikować kod na zdalnym repozytorium pushami itd

ssh-keygen -t ed25519 -C "your_email@example.com"
Ta komenda stworzy klucz prywatny id_ed25519 i publiczny id_ed25519.pub w C:\Users\S\.ssh. Zawartośc plublicznego dodajemy w githubie w ustawieniach.
Musimy potem jescze ten klucz dodac do ssh agenta ale to wszystko jest opisane w linku powyżej

W C:\Users\S\.gitconfig znajduje sie nazwa i email lokalnego commitera. Każdy lokalny comit bedzie podpisywany tym userem.


## git clone git@github.com:filutekartur/Tutorial.git
klonuje całe repo z githuba do miejsca w którym jest obecnie terminal
Bedac w jakimś repo na githubie możemy kliknąć code>SSH i tam mamy link : git@github.com:filutekartur/Tutorial.git

## git status
pokazuje status repozytorium tj. ktore pliki zostały zmodyfikowane, a które zostały dodane całkowicie nowe itp.


## git add .
Rozpoczyna śledzenie plików. Można dodać pojedyncze pliki, całe katalogi lub . która dodaje całą zawartość

## git commit -m "Title" -m "Description"
zapisuje zmiany w śledzonych plikach (add) zmiany zostaną zapisane w lokalnym Git 


## git init
Tworzy lokalne repozytorium kontroli wersji. musimy przejść do tego katalogu w którym nie ma jeszcze folderu .git i po stworzeniu tego repo dodajemy pliki, commitujemy i mozemy potem wysłać to do githuba

