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

## git push
wysyła obecny lokalny comit do repo na githubie. jeżeli użyłeś komendy git init musisz wcześniej połączyć lokalnego gita ze zdalnym repo na githubie żeby widział gdzie wypychać comity
### git push -u origin master
Upstream dla push. Od tej pory można używać samego git push i git bedzie wiedział żeby wysłać to na origin i master

## git init
Tworzy lokalne repozytorium kontroli wersji. musimy przejść do tego katalogu w którym nie ma jeszcze folderu .git i po stworzeniu tego repo dodajemy pliki, commitujemy i mozemy potem wysłać to do githuba
### git remote add origin git@github.com:filutekartur/to-delete2.git
Łączy origin ze zdalnym repo. W przypadku tworzenia nowego repo na kompie żeby móc potem wysyłąć commity do zdalnego repo to musimy stworzyć najpierw takie repot na githubie i wyciągnąć SSH.

## git checkout master
Przechodzi pomiedzy gałęziami
### git checkout -b branch2
Tworzy gałąź branch2 i do niej przechodzi. jeżeli mamy różnice w jednym pliku w na jednej gałęzi i na drugiej to przchodząc checkoutem plik w którym są te różnice np. README.md bedzie sie zmieniac.
Oznacza to że każda gałąź to tak jakby osobny projekt
### git branch
pokazuje wszystkie dostępne gałęzie

## git diff branch2
Pokazuje różnice pomiędzy ostatnim comitem na obecnej gałęzi i ostatnim comitem gałęzi branch2. Można dopisać drugą nazwę gałęzi żeby sprawdzić dwie konkretne gałęzie a nie tą na której jesteśmy
