## Grawitacja i skakanie

Uczyńmy ruchy Twojej postaci bardziej realistycznymi, przez dodanie grawitacji i pozwalając jej skakać.

+ Być może zauważyłeś że Twoja postać może zejść z platformy i chodzić w powietrzu. Spróbuj zejść z platformy i zobacz co się stanie.
    
    ![screenshot](images/dodge-no-gravity.png)

+ By to naprawić, dodajmy grawitację do Twojej gry. Stwórz nową zmienną o nazwie `gravity`{:class="blockdata"}. Możesz ukryć tą zmienną ze sceny jeśli chcesz.
    
    ![screenshot](images/dodge-gravity.png)

+ Dodaj nowy blok kodu, który ustawia grawitację jako ujemną liczbę i używa jej ciągle zmieniając koordynaty Twojej postaci.
    
    ```blocks
        kiedy kliknięto flagę
        ustaw [gravity v] na [-4]
        zawsze
            zmień y o (gravity)
        end
    ```

+ Kliknij flagę, i przesuń Twoją postać na szczyt sceny. What happens? Czy grawitacja działa tak jak się spodziewałeś?
    
    ![screenshot](images/dodge-gravity-drag.png)

+ Grawitacja nie powinna poruszać Twoją postacią poprzez platformy lub drabiny! Dodaj blok `jeżeli`{:class="blockcontrol"} do Twojego kocu, tak by grawitacja działała tylko gdy Twoja postać jest w powietrzu. Kod grawitacji powinien wyglądać teraz w ten sposób:
    
    ```blocks
        kiedy kliknięto flagę
            ustaw [gravity v] na [-4]
            zawsze
                jeżeli < nie < < dotyka koloru [#0000FF]?> or < dotyka koloru [#Ff69B4]?>>> to
                    zmień y o (gravity)
                end
            end
    ```

+ Przetestuj grawitację znowu. Czy Twoja postać zatrzyma się gdy będzie na platformie lub drabinie? Czy możesz zejść z krawędzi platformy na poziom poniżej?
    
    ![screenshot](images/dodge-gravity-test.png)

+ Zróbmy tak, by Twoja postać skakała gdy gracz naciśnie klawisz spacji. Jedna, bardzo prosta możliwość by to zrobić, to poruszyć Twoją postać do góry, kilka razy używając tego kodu:
    
    ```blocks
        kiedy klawisz [spacja v] naciśnięty
            powtórz (10) razy
                zmień y o (4)
            end
    ```
    
    Grawitacja ciągle popycha Twoją postać w dół o 4 pixele, potrzebujesz wybrać liczbę większą niż 4 w Twoim bloku `zmień y o (4)`{:class="blockmotion"}. Zmień tą liczbę aż będziesz zadowolony z wysokości skoków Twojej postaci.

+ Jeśli przetestujesz ten kod, zauważysz że działa, ale ruch nie jest zbyt płynny. By uczynić skakanie bardziej płynnym, potrzebujesz przesunąć Twoją postać o mniejszą i mniejszą liczbę, dopóki nie będzie więcej skakać.

+ By to zrobić, utwórz następną zmienną o nazwie `jump height`{:class="blockdata"}. Ponownie, jeśli chcesz możesz ukryć tę zmienną.

+ Usuń kod skoków który dodałeś do Twojej postaci i zamień go z tym kodem:
    
    ```blocks
        kiedy klawisz [spacja v] naciśnięty
            ustaw [jump height v] na [8]
            powtarzaj aż < (jump height) = [0] >
                zmień y o (jumpu height)
                zmień [jump height v] o (-0,5)
            end
    ```
    
    Ten kod porusza Twoją postać do góry o 8 pixeli, następnie o 7,5 pixeli, następnie i 7 pixeli, i tak dalej, dopóki Twoja postać nie zakończy skakać. To uczyni wygląd skoków bardziej płynnym.

+ Zmień początkową wartość Twojej zmiennej `jump height`{:class="blockdata"} i testuj zmiany aż będziesz zadowolony z wysokości skoków Twojej postaci.