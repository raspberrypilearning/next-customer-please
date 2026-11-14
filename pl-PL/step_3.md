## Przedmioty na sprzedaż

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Twój sklep potrzebuje przedmiotów na sprzedaż. Każdy przedmiot będzie miał cenę, która zostanie dodana do zmiennej `suma`{:class="block3variables"}.
</div>
<div>
![](images/step3-image.png){:width="300px"}
</div>
</div>

Będziesz musiał śledzić, ile pieniędzy wydaje twój klient.

--- task ---

Dodaj nową zmienną o nazwie `suma`{:class="block3variables"} dla wszystkich duszków.

Kliknij na duszka **sprzedawca** i dodaj skrypt do `ustawienia`{:class="block3variables"} `sumy`{:class="block3variables"} na `0`, kiedy projekt się rozpocznie.

[[[scratch3-create-set-variable]]]

--- /task ---

Jakie **produkty** będą kupować Twoi klienci?
+ Jedzenie lub picie
+ Sprzęt sportowy, zabawki, gadżety
+ Różdżki magiczne, mikstury, księgi zaklęć
+ Ubrania lub inne modne przedmioty
+ Your own idea

--- task ---

Dodaj duszka dla pierwszego **przedmiotu** który będziesz sprzedawać w swoim sklepie.

Możesz dodać cenę do kostiumu za pomocą narzędzia tekstowego w edytorze Paint. Możesz też dodać cenę do używanego tła i umieścić przedmiot obok niej.

![Przykłady przedmiotów z napisanymi obok nich cenami.](images/item-amounts.png)

--- /task ---

--- task ---

Dodaj skrypt, aby `zmienić`{:class="block3variables"} `sume`{:class="block3variables"} produktów w koszyku według ceny przedmiotu, który wybrał klient.

--- collapse ---
---
title: Click to add an item
---

```blocks3
when this sprite clicked
start sound (Coin v)
change [total v] by [10]
```

--- /collapse ---

Dobrym pomysłem jest także `odtworzenie dźwięku`{:class="block3sound"}, aby przekazać klientowi informację o dodaniu elementu do koszyka.

![Dodaj ikonkę dźwięku.](images/add-sound.png)

[[[scratch3-add-sound]]]

--- /task ---

--- task ---

**Test:** Kliknij na przedmiot i sprawdź, czy wartość zmiennej `suma`{:class="block3variables"} wzrasta o cenę przedmiotu oraz czy usłyszysz dodany wcześniej efekt dźwiękowy. Spróbuj kliknąć kilka razy, aby zobaczyć czy z każdym kliknięciem suma produktów w koszyku wzrasta.

Kliknij na zieloną flagę, aby rozpocząć projekt i upewnij się, że `suma`{:class="block3variables"} produktów w koszyku zaczyna się od `0`.

--- /task ---

--- task ---

Dodaj kolejne przedmioty do swojego sklepu.

Możesz na przykład:
+ Zduplikować pierwszy przedmiot, a następnie zmienić jego kostium w edytorze Paint
+ Dodać duszka, a następnie przeciągnąć skrypt `po kliknięciu flagi`{:class="block3events"} z pierwszego przedmiotu w twoim sklepie do nowego przedmiotu

Możesz dodać metkę z ceną do użytego kostiumu lub do tła.

--- /task ---

--- task ---

Kliknij swojego nowego duszka **przedmiot** na liście duszków, a następnie kliknij zakładkę **Kod**.

Zmień kwotę, o którą zmienia się `suma`{:class="block3variables"} na cenę nowego przedmiotu.

--- /task ---

--- task ---

**Test:** Kliknij na zieloną flagę, aby rozpocząć projekt i kliknij na przedmioty, aby dodać je do koszyka. Sprawdź, czy suma zwiększa się prawidłowo o wartość każdego nowo dodanego przedmiotu.

Jeśli dodałeś metki z cenami, upewnij się, że odpowiadają one kwocie która zostanie dodana do `sumy`{:class="block3variables"}, w przeciwnym razie Twoi klienci będą zdezorientowani!

--- /task ---

--- task ---

**Debugowanie:** Możesz znaleźć w swoim projekcie pewne błędy, które trzeba naprawić. Tutaj masz kilka przykładów często występujących błędów.

--- collapse ---
---
title: The total doesn't go to 0 when I click the green flag
---

Sprawdź, czy ustawiłeś wartość początkową zmiennej `suma`{:class="block3variables"} w skrypcie `kiedy klikniesz na flagę`{:class="block3events"} na duszku **sprzedawcy**.

--- /collapse ---

--- collapse ---
---
title: The total doesn't increase by the correct amount when I click on an item
---

Sprawdź, czy każdy przedmiot ma skrypt `gdy klikniesz na duszka` {:class="block3events"}, który zmienia `sumę`{:class="block3variables"} na prawidłową kwotę dla tego przedmiotu — mogłeś zmienić cenę dla niewłaściwego duszek.

Sprawdź, czy użyłeś bloku `zmiana`{:class="block3variables"}, a nie bloku `ustaw`{:class="block3variables"}, aby zmienić `sumę`{:class="block3variables"}. Musisz użyć bloku `zmiany`{:class="block3variables"}, aby dodać cenę do sumy. Nie chcesz, aby suma koszyka została przypadkiem ustawiona jako cena produktu, który próbujesz dodać.

--- /collapse ---

--- /task ---

--- save ---
