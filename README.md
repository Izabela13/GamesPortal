# GamesPortal
GamesPortal – opis projektu, technikalia i bibliografia

1. Charakterystyka projektu.
   
Program GamesPortal jest inspirowany fanowskimi stronami internetowymi o tematyce gier komputerowych. Posiada własną bazę danych. Dane pochodzą ze strony:
https://www.gry-online.pl/
Baza została przygotowana w taki sposób, aby dawała możliwość tworzenia relacji między poszczególnymi grupami informacji. Na zbiór danych składają się kolejno kolumny:
• game_id (nie wykorzystywane w Django),
• title,
• cycle,
• release_date,
• depiction,
• vote_average,
• vote_count,
• country,
• producer,
• genres


2. Instalacja i uruchomienie projektu:
   
Projekt dostępny jest pod adresem:
https://github.com/Izabela13/GamesPortal
CODE --> Download ZIP

Pobrany plik ZIP będzie domyślnie nazywał się 'GamesPortal-main', a wewnątrz niego będzie znajdował się plik docelowy 'GamesPortal'.

Projekt (program) można przenieść do odpowiedniego folderu/ miejsca na projekty w PyCharmie. Można go również otworzyć z innego miejsca przy użyciu PyCharm.
Po otwarciu może pojawić się problem z interpreterem. Można spróbować go ustawić, jeśli to nie zadziała, powinno pomóc zamknięcie PyCharma i uruchomienie go ponownie. Jeśli i to nie zadziała można utworzyć projekt Djnago w PyCharmie o nazwie 'GamesPortal' i przenieść do niego wszystkie pobrane pliki.

Po uruchomieniu aplikacji i wpisaniu w przeglądarce:
http://localhost:8000/
powinna pokazać się strona startowa oraz możliwość wejścia w poszczególne przyciski. Zawartość poszczególnych stron powinna być kompletna. Jeśli jednak zawartość dostępna pod przyciskiem "GRY", "ZNAJDŹ" i "TOPKA" będzie pusta, należy uruchomić 'magane.py' i dokonać migracji ("makemigrations" i "migrate").


3. Wygląd na stronie.
   
Po uruchomieniu projektu i wejściu w przeglądarce na stronę:
http://localhost:8000/
pojawi się strona startowa dostępna pod przyciskiem 'HOME'. Z tej strony możemy nawigować się w panelu bocznym. Poza 'HOME' możemy użyć trzech innych przycisków: 'GRY', 'ZNAJDŹ' i "TOPKA". Mamy również dostępny panel górny, który odpowiada za rejestrację i logowanie.

3.1. Przycisk 'GRY' 

Przycisk ‘GRY’ przenosi użytkownika do tabeli z grami, w której znajdują się informacje o tytule gry, cyklu, średniej ocenie, a także możliwość dynamicznego przejścia do szczegółów. Ponieważ tabela posiada 46 pozycji, została podzielona na strony.

Wejście w szczegóły danej gry pozwala na sprawdzenie (poza cyklem i średnią oceną) datę premiery światowej, producenta, kraj powstania oraz gatunki. Dodatkowo poniżej informacji znajduje się krótki opis (charakterystyka) danej gry.

Ze szczegółów danej gry można przemieszczać się do szczegółów innych gier. Szczegóły gry nie będą widoczne w kolejności alfabetycznej, ale w kolejności "id" danej gry. Widać to w pasku przeglądarki, np.
http://localhost:8000/24?page=1
a) jeśli znajdujemy się na początku listy gier, na dole pojawi się link "następna"
b) jeśli znajdujemy się dalej niż na początku i nie na końcu listy gier, będziemy widzieć linki "poprzednia" i "następna"
c) jeśli znajdujemy się na końcu listy gier, mamy możliwość wrócenia się, czyli zobaczymy tylko link "poprzednia.
Będąc w szczegółach możemy wrócić do wszystkich gier klikając na link "przejdź do wszystkich gier". Jeśli spróbujemy wpisać w adresie przeglądarki id, którego nie ma np.
http://localhost:8000/100?page=1
zobaczymy błąd: NIE ODNALEZIONO ZAWARTOŚCI.

3.2. Przycisk 'ZNAJDŹ'

Jest to miejsce, w którym można przeszukiwać zawartość tabeli z grami w celu odnalezienia tytułu. Wyszukiwać można na 2 sposoby:
a) wprowadzając jeden znak.
b) wprowadzając więcej niż jeden znak.
W pierwszym przypadku pojawią się tytuły gier zaczynające się od podanego znaku. Jeśli nie ma tytułu zaczynającego się od podanego znaku, wówczas dostaniemy stosowną informację. W drugim przypadku program przeszukuje tytuły pod kątem wystąpienia danego 'zlepka znaków'. Jeśli wprowadzony ciąg znaków nie wystąpił w żadnym tytule, wówczas dostaniemy informację o braku wystąpień. Jeśli po wprowadzeniu znaku lub znaków zostanie nam zwrócona lista gier, będzie można wejść w ich szczegóły.

3.3. Przycisk 'TOPKA'

W topce znajduje się 10 najwyżej ocenionych gier. Pierwsze trzy miejsca są zaznaczone odpowiednio jako złote, srebrne i brązowe miejsce. W tym widoku zobaczymy miejsce, jakie zajmuje dana gra, jej tytuł, średnią ocenę i liczbę głosów. Dodatkowo możemy wejść w 'SPRAWDŹ SZCZEGÓŁY', które przeniesie nas do szczegółów gier.

3.4. Rejestracja i logowanie.

Do portalu można się zalogować, ale wcześniej trzeba być zarejestrowanym. W projekcie dostępni są trzej użytkownicy: Ellie, Ethan i Mia. Wszyscy troje mają to samo hasło, które brzmi: "Gierkowanie". Można zalogować się na któregoś z użytkowników, aby zobaczyć, że po zalogowaniu w panelu górnym pojawi się nazwa użytkownika oraz opcja 'Wyloguj'. Można również samemu się zarejestrować i zalogować.


4. Bibliografia

Projekt nie powstałby bez pomocy naukowo-dydaktycznych. W projekcie wykorzystano:
• filmiki z zajęć z tematyki Django i notatki dzięki temu utworzone.
• Książki:
o Django : tworzenie nowoczesnych aplikacji internetowych w Pythonie / Ben Shaw, Saurabh Badhwar, Andrew Bird, Bharath Chandra K S, Chris Guest ; przekład: Joanna Zatorska. - Gliwice : Helion, copyright 2022.
o Django 3 : praktyczne tworzenie aplikacji sieciowych / Antonio Melé ; przekład: Radosław Meryk, Robert Górczyński. - Gliwice : Helion, copyright 2021.
o Nowoczesne Django / Sylwester Walczak. - Gliwice : Helion, copyright 2022.
• Dokumemntację Django: https://docs.djangoproject.com/pl/4.2/
• Wpisy z rozwiązaniami problemów z różnych blogów i forów.
W projekcie wykorzystano również darmowe obrazki dostępne na stronie:
https://pl.freepik.com/darmowe-zdjecie-wektory/gry
