## Cinematica personajului

Să începem prin crearea unui personaj care să se poată deplasa la stânga și la dreapta, precum și să urce pe scări.

+ Deschideți proiectul "Dodgeball" Scratch online la <a href="http://jumpto.cc/dodge-go" target="_blank"> jumpto.cc/dodge-go </a> sau descărcați din <a href="http://jumpto.cc/dodge-get" target="_blank"> jumpto.cc/dodge-get </a> și apoi deschideți dacă folosiți editorul offline .
    
    Proiectul conține un fundal cu platforme:
    
    ![captură de ecran](images/dodge-background.png)

+ Adăugați un nou caracterj, care va fi personajul tău. Este mai bine dacă alegeți un personaj cu mai multe costume, astfel încât să puteți face să pară ca și cum ar merge.
    
    ![captură de ecran](images/dodge-characters.png)

+ Să folosim tastele săgeți pentru a vă deplasa personajul imprejur. Când jucătorul apasă pe săgeata din dreapta, vrei ca personajul tău să îndrepte spre dreapta, să facă câțiva pași și să se schimbe la costumul următor:
    
    ```blocks
        when flag clicked
        forever
            if <key [right arrow v] pressed? > then
                point in direction (90 v)
                move (3) steps
                next costume
            end
        end
    ```

+ Testați caracterul dvs. făcând clic pe steag și apoi ținând apăsată tasta săgeată dreapta. Personajul dvs. se mișcă spre dreapta? Personajul tău arată ca și cum merge?
    
    ![captură de ecran](images/dodge-walking.png)

+ Pentru a misca personajul tau la stanga va trebui sa adugi un alt bloc `if`{:class="blockcontrol"} in cadrul buclei `forever`{:class="blockcontrol"} care misca personajul tau la stanga.

+ Testați noul cod pentru a vă asigura că funcționează. Personajul tău se răstoarnă când merge la stânga?
    
    ![captură de ecran](images/dodge-upside-down.png)
    
    Daaca sa intampla asa poti sa repari acest bug dand click pe iconul personajului `(i)`{:class="blocksensing"} si apoi dand click pe sageata stanga-dreapra.
    
    ![captură de ecran](images/dodge-left-right.png)
    
    Sau, dacă preferați, puteți adăuga acest bloc la începutul scriptului personajului dvs:
    
    ```scratch
    setati modul de rotatie [left-right v]
    ```

+ Pentru a urca pe o scară roz, caracterul dvs. ar trebui să se miște ușor ori de câte ori săgeata sus este apăsată și atinge culoarea corectă. Adaugand in cadrul buclei pentru personajul dvs. `forever`{:class="blockcontrol"} :
    
    ```blocks
        if < <key [up arrow v] pressed?> and <touching color [#FF69B4]?> > then
            change y by (4)
        end
    ```

+ Testați-vă caracterul - puteți urca scările roz și ajunge la sfârșitul nivelului dvs.?
    
    ![captură de ecran](images/dodge-test-character.png)