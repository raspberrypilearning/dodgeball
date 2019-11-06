## Grawitacja i skakanie

Teraz sprawisz, że Twoja postać będzie poruszać się bardziej realistycznie: dodasz grawitację do swojej gry i dasz postaci umiejętność skakania.

--- task ---

W grze poruszaj swoją postacią tak, aby zeszła z platformy. Czy widzisz, że może wejść w puste miejsce?

![zrzut ekranu](images/dodge-no-gravity.png)

--- /task ---

--- task ---

Aby to naprawić, dodaj grawitację do swojej gry. Żeby to zrobić, utwórz nową zmienną o nazwie `grawitacja`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Możesz ukryć tą zmienną na scenie jeśli chcesz.

![zrzut ekranu](images/dodge-gravity-annotated.png)

--- /task ---

--- task ---

Dodaj te nowe bloki kodu, które ustawiają `grawitację` na liczbę ujemną i użyj wartości zmiennej `grawitacja` aby wielokrotnie zmieniać współrzędną y twojej postaci:

![duszek Pico walking](images/pico_walking_sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw [grawitacja v] na [-4]
    zawsze
        zmień y o (grawitacja)
    end
```

--- /task ---

--- task ---

Kliknij flagę, a następnie przesuń Twoją postać na szczyt sceny. Co się wtedy stanie? Czy grawitacja działa tak jak się spodziewałaś?

![zrzut ekranu](images/dodge-gravity-drag.png)

--- /task ---

--- task ---

Grawitacja nie powinna pozwalać na przesuwanie Twojej postaci przez platformy lub drabinę! Dodaj blok `jeżeli`{:class="block3control"} do swojego kodu, aby grawitacja działała tylko wtedy, gdy postać jest w powietrzu. Kod odpowiedzialny za grawitację powinien wyglądać teraz w ten sposób:

![duszek Pico walking](images/pico_walking_sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
        ustaw [grawitacja v] na [-4]
        zawsze
            jeżeli < nie < <dotyka koloru [#FF69B4]?> lub <dotyka koloru [#0000FF]?> > > to
                zmień y o (grawitacja)
            end
        end
```

--- /task ---

--- task ---

Przetestuj grę ponownie, aby sprawdzić, czy grawitacja działa teraz poprawnie. Czy duszek Twojej postaci przestaje spadać, gdy dotknie platformy lub drabiny? Czy potrafisz sprawić, że postać zejdzie z krawędzi platform i spadnie na niższy poziom?

![zrzut ekranu](images/dodge-gravity-test.png)

--- /task ---

--- task ---

Teraz dodaj kod, aby twoja postać podskakiwała za każdym razem, gdy gracz naciśnie klawisz <kbd>spacja</kbd>. Jednym z bardzo łatwych sposobów jest przesunięcie swojej postaci kilka razy w górę:

![duszek Pico walking](images/pico_walking_sprite.png)

```blocks3
kiedy klawisz [spacja v] naciśnięty
powtarzaj (10) 
  zmień y o (4)
end
```

Ponieważ grawitacja nieustannie przesuwa twoją postać w dół o 4 piksele, musisz wybrać liczbę większą niż `4` w bloku `zmień y o (4)`{:class="block3motion"}. Zmieniaj liczbę, aż będziesz zadowolona z wysokości, na jaką skacze Twoja postać.

--- /task ---

--- task ---

Przetestuj swój kod. Zauważ, że ruch skakania nie jest zbyt płynny. Aby skakanie wyglądało płynniej, musisz przesuwać duszka postaci o coraz mniejsze wartości, dopóki postać nie będzie podnosiła się.

--- /task ---

--- task ---

Żeby to zrobić, utwórz nową zmienną o nazwie `wysokość skoku`{:class="block3variables"}. Ponownie, jeśli chcesz możesz ukryć tę zmienną.

--- /task ---

--- task ---

Usuń kod odpowiedzialny za skoki który dodałaś do Twojej postaci i dodaj ten kod:

![duszek Pico walking](images/pico_walking_sprite.png)

```blocks3
kiedy klawisz [spacja v] naciśnięty
ustaw [wysokość skoku v] na [8]
powtarzaj aż <(wysokość skoku) = [0]> 
  zmień y o (wysokość skoku)
  zmień [wysokość skoku v] o (-0.5)
koniec
```

Ten kod przesuwa twoją postać w górę o 8 pikseli, następnie 7.5 pikseli, następnie 7 pikseli i tak dalej, aż postać nie podniesie się. To uczyni wygląd skoków bardziej płynnym.

--- /task ---

--- task ---

Zmień wartość zmiennej `wysokość skoku`{:class="block3variables"}, ustawionej przed rozpoczęciem pętli `powtarzaj`{:class="block3control"}. Następnie przetestuj swoją grę.

Powtarzaj te dwa kroki, aż będziesz zadowolona z wysokości skoku Twojej postaci.

--- /task ---