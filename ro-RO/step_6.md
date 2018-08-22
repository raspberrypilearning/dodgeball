## Evita mingea

Acum, că ați făcut personajul să se miște, să adăugăm niște mingi pentru ca personajul tău sa le poata evita.

+ Creați un nou model de minge. Puteți alege orice tip de minge care vă place.
    
    ![screenshot](images/dodge-balls.png)

+ Redimensionați-vă mingea, astfel încât personajul dvs. să poată sări peste ea. Încercați să sariti peste minge pentru a o testa.
    
    ![screenshot](images/dodge-ball-resize.png)

+ Adăugați acest cod la mingea dumneavoastra:
    
    ![screenshot](images/dodge-ball-motion.png)
    
    Acest cod creează o nouă clona a mingii la fiecare 3 secunde. Fiecare nouă clonă se mișcă de-a lungul platformei de sus.

+ Faceți clic pe steag pentru a testa acest lucru.
    
    ![screenshot](images/dodge-ball-test.png)

+ Adăugați linii de cod astfel că mingile se deplasează pe toate cele 3 platforme.
    
    ![screenshot](images/dodge-ball-more-motion.png)

+ În cele din urmă, veți avea nevoie de linii de cod pentru momentul în care personajul dvs. este lovit de o minge! Adăugați aceste linii de cod la modelul dvs. de minge:
    
    ```blocks
        when I start as a clone
        forever
            if < touching [Pico walking v]? > then
                broadcast [hit v]
            end
        end
    ```

+ Va trebui, de asemenea, să adăugați un linii de cod personajului dvs., pentru a vă deplasa înapoi la început atunci când este lovit:
    
    ```blocks
        when I receive [hit v]
        point in direction (90 v)
        go to x: (-210) y: (-120)
    ```

+ Testați-vă programul și vedeți dacă personajul se întorce la început când au fost loviți de o minge.