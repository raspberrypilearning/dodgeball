## Unikanie piłek

Teraz masz poruszającą się postać, dodajmy kilka piłek których musi unikać.

+ Utwórz nowego duszka piłkę. Możesz wybrać dowolny typ piłki który chcesz.
    
    ![screenshot](images/dodge-balls.png)

+ Zmień rozmiar piłki, tak by Twoja postać mogła ją przeskoczyć. By to przetestować, spróbuj przeskoczyć piłkę.
    
    ![screenshot](images/dodge-ball-resize.png)

+ Dodaj ten kod do Twojej piłki:
    
    ![screenshot](images/dodge-ball-motion.png)
    
    Ten kod tworzy nowy klon piłki co 3 sekundy. Każdy nowy klon porusza się wzdłuż górnej platformy.

+ Kliknij flagę by to przetestować.
    
    ![screenshot](images/dodge-ball-test.png)

+ Dodaj więcej kodu do duszków piłek, tak by te poruszały się po wszystkich trzech platformach.
    
    ![screenshot](images/dodge-ball-more-motion.png)

+ Ostatecznie, będziesz potrzebować kodu gdy w Twoją postać zostanie trafiona piłką! Dodaj poniższy kod do duszka piłki:
    
    ```blocks
        kiedy zaczynam jako klon
            zawsze
                jeżeli < dotyka [Pico v]? > to? > to
                nadaj [trafienie v]
            end
        end
    ```

+ Będziesz również potrzebował dodać kod do Twojej postaci, aby wracała na start gdy zostanie trafiona:
    
    ```blocks
        kiedy otrzymam [trafienie v]
    ustaw kierunek na (9 0v)
    idź do x: (-210) y: (-120)
    ```

+ Przetestuj Twoją postać i zobacz czy powraca na start kiedy zostanie trafiona przez piłkę.