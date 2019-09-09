## Wyzwanie: więcej przeszkód

Jeżeli myślisz że Twoja gra wciąż jest zbyt łatwa, możesz do niej dodać więcej przeszkód. Przeszkody mogą być czymkolwiek co lubisz! Oto kilka pomysłów:

+ Groźny motyl
+ Platformy które pojawiając się i znikają
+ Spadające piłeczki tenisowe których musisz unikać

![screenshot](images/dodge-obstacles.png)

Możesz nawet zaprojektować kolejne tło, aby stworzyć kolejny poziom. Następnie dodaj kod, aby gdy Twoja postać dotrze do zielonych drzwi, gra przełączyła się na nowe tło:

![duszek Pico walking](images/pico_walking_sprite.png)

```blocks3
    jeżeli <touching color [#00FF00]?> to
        przełącz tło na (następne tło v)
        idź do x: (-210) y: (-120)
        czekaj (1) sek
    koniec
```