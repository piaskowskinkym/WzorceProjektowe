# WzorceProjektowe
# Czym są wzorce projektowe
Wzorce projektowe to uznane przez większość programistów rozwiązania często napotykanych problemów w trakcie porjektowania oprogramowania.Są czymś na krztał gotowych schematów które można dostosować,by naprawić powtarzający się w kodzie problem.


# Podział wzrorców
Wzorce różnią się pomiędzy sobą swoją złożonością, szegółowością i skalą w jakiej da się je zaimplementować.
Z nich wszystkich tworzą się 3 główne grupy według których można skategoryzować wzorce:
* **Wzorce Kreacyjne** które wprowadzają elastyczniejsze mechanizmy tworzenia obiektów i pozwalają na ponowne wykorzystanie istniejącego kodu.
Ważne by powiedzieć że wrzozec nie jest fragmentem kodu lecz ogólną koncepcją pozwalająca rozwiązać dany problem.

* **Wzorce strukturalne** ich celem jest wyjasnianie jak składać obiekty i klasy w większe struktury, zachowując przy tym elastyczność i efektywność struktur

* **Wzorce behawioralne** których zadaniem jest efektywna komunikacja i podział obowiązków pomiędzy obiektami

# Przykłady
**Wrzozec Kreacyjny Singleton**
Wrzozec ten pozwala zapewnić istnienie wyłącznie jednej instancji danej klasy,oraz daje globalny punk dostępowy to tej instancji.
Wszystkie implementacje wzorca Singleton wspołdzielą dwa etapy:
* Ograniczenie dostępu do domyślnego konstrukora przez uczynienie go prywatym - zapobiega to stosowania operatora new względem klasy Singleton
* Utworzenie statycznej metody kreacyjnej któa pełni rolę konsturkotra - metoda ta wywoła prywatny konstruktor aby utworzyć obiekt i umieśic go w polu statycznym klasy.Wszystkie kolejne wywołania tej metody zwrócą już istniejący obiekt

 Kożystamy z Singletów, gdy w  programie ma prawo istnieć wyłącznie jeden ogólnodostępny obiekt danej klasy. Przykładem może być połączenie z bazą danych, którego używa wiele fragmentów programu lub kiedy potrzebujemy ściślejszej kontroli nad zmiennymi globalnymi

---------------------------------------------------------------------------------------------------------------------
**Wrzozec strukturalny Adapter**
Jest on strukturalnym wzorcem projektowym pozwalającym na współdziałanie ze sobą obiektów o niekompatybilnych interfejsach.

Adapter stanowi opakowanie dla obiektu, ukrywając szczegóły konwersji jakie odbywają się poza oczami uzytkownika. Obiekt opakowywany możenie wiedzieć o istnieniu adaptera. Można na przykład opakować obiekt korzystający z jednostek kilometr i metr w adapter konwertujący te dane na jednostki imperialne, takie jak stopy i mile.

Wzorzec Adapter pozwala utworzyć klasę która stanowi warstwę pośredniczącą pomiędzy kodem, a klasą pochodzącą z zewnątrz, lub inną, posiadającą jakiś nietypowy interfejs.

Klasa Adapter może być wykorzystywana kiedy chcemy użyć istniejącej klasy której interfejs nie jest kompatybliny z resztą programu
Można rozszerzyć każdą podklasę i umieścić potrzebną funkcjonalność w nowych klasach pochodnych.

-----------------------------------------------------------------------------------------------------------
**Wrzozec behaworalny Iterator**
Działaniem Iteratora jest sekwencyjne przechodzenie od elementu do elementu jakiegoś zbioru bez konieczności pokazywania jego formy

Główną ideą wzorca Iterator jest ekstrakcja zadań związanych z przechodzeniem przez elementy kolekcji do osobnego obiektu zwanego iteratorem.
Oprócz implementowania samego algorytmu, obiekt iteratora hermetyzuje wszystkie szczegóły sposobu przechodzenia przez kolejne elementy, jak bieżąca pozycja, czy ilość pozostałych elementów. Dzięki temu wiele iteratorów może jednocześnie przeglądać tę samą kolekcję, niezależnie od siebie.

Najczęściej Iterator stosuje się gdy mamy do czynienia z kolekcją ze skomplikowaną strukturą taką jak np. drzewo której nie chcemu pokazać klientowi

Używany jest także  w celu redukcji duplikowania kodu przeglądania elementów zbiorów na przestrzeni całego programu.



