# GamesPortal
Program o nazwie 'GamesPortal' to projekt zaliczeniowy napisany w Django. 


Charakterystyka projektu.
   
Program 'GamesPortal' jest inspirowany fanowskimi stronami internetowymi o tematyce gier komputerowych. Posiada własną bazę danych. Dane pochodzą ze strony: https://www.gry-online.pl/ . Baza została przygotowana w taki sposób, aby dawała możliwość tworzenia relacji między poszczególnymi grupami informacji. Na zbiór danych składają się kolejno kolumny:
- game_id (nie wykorzystywane w Django),
- title,
- cycle,
- release_date,
- depiction,
- vote_average,
- vote_count,
- country,
- producer,
- genres


Instalacja i uruchomienie projektu:
   
1. Projetk dostępny jest pod adressem: https://github.com/Izabela13/GamesPortal
   CODE --> Download ZIP
2. plik ZIP będzie nazywał się 'GamesPortal-main', a wewnątrz niego będzie znajdował się plik docelowy 'GamesPortal'.
3. Projekt (program) można przenieść do odpowiedniego folderu/ miejsca na projekty w PyCharmie. Można go również otworzyć z innego miejsca przy użyciu PyCharm.
4. Po otwarciu może pojawić się problem z interpreterem. Można spróbować go ustawić. Powinno zazdziałać zamknięcie PyCharma i uruchomienie go ponownie. Jeśli i to nie zadziała można utworzyć projekt Djnago w PyCharmie o nazwie 'GamesPortal' i przenieść do niego wszystkie pobrane pliki.
5. Po uruchomieniu aplikacji i wpisaniu w przeglądarce 'localhost:8000' powinna pokazać się strona startowa oraz możliwość wejścia w poszczególne przyciski. Zawartość poszczególnych stron powinna być kompletna. Jeśli jednak zawartość dostępna pod przyciskiem "gry", "znajdź" i "topka" będzie pusta, należy uruchomić 'magane.py' i dokonać migracji ("makemigrations" i "migrate").


Wygląd na stronie.
   
Po uruchomieniu projektu i wejściu w przeglądarce na stronę 'localhost:8000' pojawi się strona startowa 'home'. Z tej strony możemy nawigować się w panelu bocznym. Poza 'HOME' możemy użyć trzech innych przycisków: 'GRY', 'ZNAJDŹ' i "TOPKA". Mamy również dostępny panel górny, który odpowiada za rejestrację i logowanie.

Przycisk 'GRY': 
przenosi użytkownika do tabeli z grami, w której znajdują się informacje o tytule gry, cyklu, średniej ocenie, a także możliwość dynamiczneog przejścia do szczegółów. Ponieważ tabela posiada 46 pozycji, została podzielona na strony. 

Wejście w szczegóły danej gry pozwala na sprawdzenie (poza cyklem i średnią oceną) datę premiery światowej, producenta, kraj powstania oraz gatunki. Dodatkowo poniżej informacji znajduje się krótki opis (charakterystyka) danej gry. Poniżej ustawione są średnia oraz liczba ocen. Ze szczegółów danej gry można przemieszczać się do szczegółów innych gier. Szczegóły gry nie będą widoczne w kolejności alfabetycznej, ale w kolejności "id" danej gry. Widać to w pasku przeglądarki (np. http://localhost:8000/24?page=1). 
a) jeśli znajdujemy się na początku listy gier, na dole pojawi się link "następna"
b) jeśli znajdujemy się dalej niż na początku i nie na końcu listy gier będziemy widzieć linki "poprzednia" i "następna".
c) jeśli znajdujemy się na końcu listy gier, mamy możliwość wrócenia się, czyli zobaczymy tylko link "poprzednia. 
Jeśli spróbujemy wpisać w adresie przeglądarki id, którego nie ma (np. http://localhost:8000/100?page=1), zobaczymy błąd: NIE ODNALEZIONO ZAWARTOŚCI.
Będąc w szczegółach możemy wrócić do wszystkich gier klikając na link "przejdź do wszystkich gier".

Przycisk 'ZNAJDŹ':
jest to miejsce, w któym można przeszukiwać zawartość w celu odnalezienia tytułu. Wyszukiwać można na 2 sposoby:
1) wprowadzając jeden znak.
2) wprowadzając więcej niż jeden znak.
W pierwszym przypadku pojawią się tytuły gier zaczynające się od podanego znaku. Jeśli nie ma tytułu zaczynającego się od podanego znaku, wówczas dostaniemy stosowną ifnormację.
W drugim przypadku program przeszukuje tytuły pod kątem wystąpienia danego 'zlepka znaków'. Jeśli wprowadzony ciąg znaków nie wystąpił w żadnym tytule, wówczas dostaniemy ifnromację o braku wystąpień.
Jeśli po wprowadzeniu znaku lub znaków zostanie nam zwrócona lista gier, będzie można wejść wich szczegóły. 

Przycisk 'TOPKA':
W topce znajduje się 10 najwyżej ocenionych gier. Pierwsze trzy miejsca są zaznaczone odpowiednio jako złote, srebrne i brązowe miejsce. W tym widoku zobaczymy miejsce, jakie zajmuje dana gra, jej tytuł, średnią ocenę i liczbę głosów. Dodatkowo możemy wejdź w 'SPRAWDŹ SZCZEGÓŁY', które przeniesie nas do szczegółów gier. 

Rejestracja i logowanie.
Do portalu można się zalogować, ale wcześniej trzeba być zarejestrowanym. W projekcie dostępni są trzej użytkownicy: Ellie, Ethan i Mia. Wszyscy troje mają to samo hasło, które brzmi "Giereczkowanie". Można zalogować się na któregoś z użytkowników, aby zobaczyć, że po zalogowaniu w panelu górnym pojawi się nazwa użytkownika oraz opcja 'Wyloguj'. 


Bibliografia
   
Projekt nie powstałby bez pomocy naukowo-dydaktycznych. W projekcie wykorzytsano:
1. Filmiki z zajęć z tematyki Django i notatki dzięki temu utworzone.
2. Książki:
   - Django : tworzenie nowoczesnych aplikacji internetowych w Pythonie / Ben Shaw, Saurabh Badhwar, Andrew Bird, Bharath Chandra K S, Chris Guest ; przekład: Joanna Zatorska. - Gliwice : Helion, copyright 2022.
   - Django 3 : praktyczne tworzenie aplikacji sieciowych / Antonio Melé ; przekład: Radosław Meryk, Robert Górczyński. - Gliwice : Helion, copyright 2021.
   - Nowoczesne Django / Sylwester Walczak. - Gliwice : Helion, copyright 2022.
4. Dokumemntację Django: https://docs.djangoproject.com/pl/4.2/
5. Wpisy z rozwiązaniami problemów z różnych blogów i forów.

W projekcie wykorzystano również darmowe obrazki dostępne na stronie https://pl.freepik.com/darmowe-zdjecie-wektory/gry
