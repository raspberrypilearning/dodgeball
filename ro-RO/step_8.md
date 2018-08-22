## Lasere!

Să facem jocul mai dificil de finalizat, prin adăugarea de lasere!

+ Adăugați un nou personaj la jocul dvs., numit "Laser". Ar trebui să aibă 2 costume, numite "on" și "off".
    
    ![captura de ecran ](images/dodge-lasers-costume.png)

+ Plasați noul dvs. laser oriunde doriți, între 2 platforme.
    
    ![captura de ecran](images/dodge-lasers-position.png)

+ Adăugați linii de cod la laser, pentru a comuta între cele două costume.
    
    ```blocks
        when flag clicked
        forever
            switch costume to [on v]
            wait (2) secs
            switch costume to [off v]
            wait (2) secs
        end
    ```
    
    Daca preferati, puteti `wait`{:class="blockcontrol"} a `random`{:class="blockoperators"} durata de timp intre schimbarile de costum.

+ În cele din urmă, adăugați linii de cod la laser, astfel încât mesajul "lovit" să fie difuzat când laserul atinge caracterul tău. Acest cod va fi foarte similar cu liniile de codul pe care l-ați folosit in cazul in care mingea a atins personajul.
    
    Nu aveți nevoie să adăugați nici un alt cod cpersonajului dvs. - el știe deja ce să facă atunci când este lovit!

+ Testați-vă jocul pentru a vedea dacă puteți trece de laser. Modificați în cod `wait`{:class="blockcontrol"} în cazul în care laserele sunt prea ușor sau prea greu de evitat.