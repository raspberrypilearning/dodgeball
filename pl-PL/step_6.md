## Unikając piłek

Teraz masz poruszającą się postać, dodajmy kilka piłek których Twoja postać musi unikać.

+ Utwórz nowego duszka piłkę. Możesz wybrać każdy typ piłki który chcesz.
    
    ![screenshot](images/dodge-balls.png)

+ Zmień rozmiar piłki, tak by Twoja postać mogła ją przeskoczyć. By to przetestować, spróbuj przeskoczyć piłkę.
    
    ![screenshot](images/dodge-ball-resize.png)

+ Dodaj ten kod do Twojej piłki:
    
    ![screenshot](images/dodge-ball-motion.png)
    
    Ten kod tworzy nowy klon piłki co 3 sekundy. Każdy nowy klon porusza się wzdłuż górnej platformy.

+ Kliknij flagę by to przetestować.
    
    ![screenshot](images/dodge-ball-test.png)

+ Dodaj więcej kody do duszka piłki, tak by te poruszały się po wszystkich trzech platformach.
    
    ![screenshot](images/dodge-ball-more-motion.png)

+ Ostatecznie, będziesz potrzebować kod gdy w Twoją postać trafi piłka! Dodaj poniższy kod do duszka piłki:
    
    ```blocks
        when I start as a clone
        forever
            if < touching [Pico walking v]? > then
                broadcast [hit v]
            end
        end
    ```

+ You'll also need to add code to your character, to move back to the start when they're hit:
    
    ```blocks
        when I receive [hit v]
        point in direction (90 v)
        go to x: (-210) y: (-120)
    ```

+ Test out your character and see if they go back to the start when they've been hit by a ball.