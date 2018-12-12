<img alt="Logo" src="http://coderslab.pl/svg/logo-coderslab.svg" width="400">

# JavaScript &ndash; egzamin poprawkowy

## Wytyczne

1. Stwórz [*fork*](https://guides.github.com/activities/forking/) repozytorium z zadaniami.
2. Sklonuj repozytorium na swój komputer. Użyj do tego komendy `git clone adres_repozytorium`
Adres repozytorium możesz znaleźć na stronie repozytorium po naciśnięciu w guzik "Clone or download".
3. Rozwiąż zadania i skomituj zmiany do swojego repozytorium. Użyj do tego komend `git add nazwa_pliku`.
Jeżeli chcesz dodać wszystkie zmienione pliki użyj `git add .` 
Pamiętaj że kropka na końcu jest ważna!
Następnie skommituj zmiany komendą `git commit -m "nazwa_commita"`
4. Wypchnij zmiany do swojego repozytorium na GitHubie.  Użyj do tego komendy `git push origin master`
5. Stwórz [*pull request*](https://help.github.com/articles/creating-a-pull-request) do oryginalnego repozytorium, gdy skończysz wszystkie zadania.

## Uwagi

* Zadania te są testowane za pomocą specjalnych testów automatycznych. Jeśli więc w zadaniu jest wspomniane, aby funkcja zwracała wynik to powinna zwracać (wyświetlanie w konsoli pomaga w sprawdzeniu jednak nie zwraca wartości). Jeśli w treści zadania jest wspomniane, aby taki konkretny tekst został wypisany/zwrócony, to powinien być wypisany/zwrócony dokładnie taki sam tekst jak w treści zadania.

* Odpowiedzi do zadań 1&ndash;2 wpisz w pliku **zadanie01_02.txt**.
Resztę zadań rozwiąż w odpowiednich plikach **js**.
Nie zmieniaj nic w plikach HTML.

* Zawsze sprawdź, czy Twoje rozwiązanie działa.


### Pamiętaj, że zadanie jest __niezaliczone__ jeżeli:
- nie zastosujesz się do poleceń! :bomb: :bomb: :bomb:
- plik JavaScript zawiera błędy na poziomie kompilacji.

---------------------------------------------------------------------

## Zadanie 1

(1.5pkt)

Opisz własnymi słowami różnicę między ```&&```, ```||``` i ```!```.

## Zadanie 2

(1.5pkt)

Opisz różnicę między ```null``` i ```undefined```.

## Zadanie 3

(3pkt)

Napisz funkcję ```checkPalindrom(myString)```, która sprawdza czy ciąg znaków przekazany jako parametr jest palindromem. Jeśli jest, zwróć wartosć logiczną ```true```, w przeciwnym wypadku zwróć ```false```. Zadbaj o to, aby wielkość znaków w ciągu znaków przekazanych jako parametr nie była brana pod uwagę podczas sprawdzania czy ciąg jest palindromem.

Np:
  ```
  checkPalindrom("Kajak") // => true
  checkPalindrom("Czarne kropki") // => false
  ```

## Zadanie 4

(5 pkt)

 - Nie używaj eventu DOMContentLoaded. Skrypt jest wczytany do pliku html przed końcem body.
 - Do każdego podpunktu stwórz odpowiednią funkcję o nazwie podanej w treści zadania.
 - Każda funkcja niech **zwraca** tablicę wypełnioną odpowiednimi elementami. ( Pamiętasz, że zwracanie, a wyświetlanie to różnica? )


 Wykonaj następujące polecenia:

* **1. Szukanie nazw tagów:**
   - znajdź wszystkie elementy o **klasie** ```sample_class```,
   - stwórz funkcję ```getTagsOfElements(elements)``` do której przekaż jako argument znalezione elementy,
   - stwórz w funkcji tablicę i wypełnij ją pobranymi nazwami tagów. Pobierz je z elementów przekazanych jako argument.
   - zwróć tablicę.


* **2. Dodawanie klasy:**
  - Znajdź element o **id** ```sample_id_2```.
  - stwórz funkcję ```getClassesOfElement(element)``` do której przekaż jako argument znaleziony element.
  - stwórz w funkcji tablicę i wypełnij ją nazwami klas. Pobierz klasy z przekazanego jako argument elementu.
  - zwróć tablicę.


* **3. Szukanie tekstu:**
  - Znajdź wszystkie elementy **listy**, której klasa to ```funny_text```,
  - stwórz funkcję ```getInnerTextsOfElements(elements)```, do której przekaż jako argument znalezione elementy.
  - stwórz w funkcji tablicę i wypełnij ją tekstami pobranymi z elementów przekazanych jako argument.
  - zwróć tablicę.


* **4. Szukanie adresów linków:**
  - Znajdź wszystkie linki,
  - stwórz funkcję ```getAddressesOfElements(elements)```, do której przekaż jako argument znalezione elementy.
  - stwórz w funkcji tablicę i wypełnij ją adresami pobranymi z elementów przekazanych jako argument.
  - jeśli atrybut **href** elementu jest pusty, nie dodawaj tej wartości do nowej tablicy.
  - zwróć tablicę.


* **5. Szukanie tagów dzieci:**
  - Znajdź wszystkie dzieci elementu o **id** ```super_form```,
  - do funkcji, która wyszukuje tagi elementów, przekaż jako argument, znalezione dzieci.


## Zadanie 5

(3pkt) 

Używając JavaScript dopisz do wszystkich divów o klasie ```color``` nasłuchiwanie zdarzeń, które po najechaniu na element sprawi, że kolor diva zmieni się na losowy, a na divie pokaże się tekst trzymany w ```data-text```. Zjechanie z diva powinno usuwać tekst, ale div powinien zostać pokolorowany. Ponowne najechanie powinno zmienić kolor tła i znowu wyświetlić tekst.

**Hint**:
Żeby uzyskać losowy kolor użyj poniższego kodu:
```JavaScript
var randomColor = "#" + Math.floor(Math.random()*16777215).toString(16);
```
## Zadanie 6
(6pkt)

Używając JavaScript dopisz odpowiednie nasłuchiwanie zdarzeń do formularza. Nasłuchiwanie ma reagować na wysłanie formularza. Po wciśnięciu przycisku **submit**, funkcja nasuchiwania powinna:

  1. Zapobiegać przeładowaniu strony,
  2. Sprawdzić czy wartość pola **Numer domu** jest liczbą. Jeżeli warunek nie jest spełniony, to do **diva** o **klasie** ```error_message``` wstaw paragraf z wiadomością **Niepoprawny numer domu**,
  3. Sprawdzić czy wartość pola **Kod pocztowy** składa się z dokładnie 6 znaków. Jeżeli warunek nie jest spełniony, to do **diva** o **klasie** ```error_message``` wstaw paragraf z wiadomością **Zły kod pocztowy**,
  4. Sprawdzić czy zaznaczony jest checkbox **"Akceptuję warunki"**. Jeżeli warunek nie jest spełniony, to do **diva** o **klasie** ```error_message``` wstaw paragraf z wiadomością **Zaakceptuj warunki**.
  5. Jeżeli wszystkie warunki są spełnione, wyświetl w konsoli wszystkie informacje z formularza, a w **divie** o **klasie**  ```success_message``` wstaw tekst **Udana rejestracja**.

Pamiętaj: jeśli wszystkie warunki nie są spełnione, **div** o klasie ```error_message``` powinien mieć trzy paragrafy z odpowiednimi komunikatami.
