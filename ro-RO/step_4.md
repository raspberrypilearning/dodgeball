## Gravitatie si sarituri

Să facem ca personajul tău să se miște mai realist, adăugând gravitate și permițându-i să sară.

+ S-ar putea să fi observat că personajul tău poate se poate deplasa pe o platformă plutind în mijlocul aerului. Încercați să ieșiți de pe o platformă și să vedeți ce se întâmplă.
    
    ![captură de ecran](images/dodge-no-gravity.png)

+ Pentru a rezolva acest lucru, să adăugăm gravitate in jocul tău. Creați o nouă variabilă numită `gravitate`{:class="blockdata"}. Puteți să ascundeți această variabilă din stadiul dvs. dacă doriți.
    
    ![captură de ecran](images/dodge-gravity.png)

+ Adăugați acest nou bloc de cod, care stabilește gravitatea la un număr negativ, și apoi folosește aceasta pentru a modifica în mod repetat coordonatele y ale personajului.
    
    ```blocks
        when flag clicked
        set [gravitate v] to [-4]
        forever
            change y by (gravitate)
        end
    ```

+ Faceți clic pe pavilion, apoi trageți caracterul dvs. în partea de sus a scenei. Ce se itampla? Gravitatea functioneaza asa cum va asteptati?
    
    ![captură de ecran](images/dodge-gravity-drag.png)

+ Gravitatea nu ar trebui să vă miște caracterul printr-o platformă sau o scară! Adăugați un bloc `if`{:class="blockcontrol"} programului dvs., astfel încât gravitatea să funcționeze numai atunci când personajul dvs. este plasat în mijlocul aerului. Segventa de codul gravitate ar trebui să arate astfel:
    
    ```blocks
        when flag clicked
        set [gravitate v] to [-4]
        forever
            if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
                change y by (gravitate)
            end
        end
    ```

+ Testați din nou gravitatea. Caracterul tău se oprește când sestepe o platformă sau pe o scară? Poți să te duci de la marginea platformelor la nivelul de mai jos?
    
    ![captură de ecran](images/dodge-gravity-test.png)

+ Să programam și saltul personajului când jucătorul apasă bara de spațiu. O modalitate foarte ușoară de a face acest lucru este să vă mutați caracterul de câteva ori, folosind acesta secventa de cod:
    
    ```blocks
        when [space v] key pressed
        repeat (10)
            change y by (4)
        end
    ```
    
    Deoarece gravitația vă împinge în mod constant caracterul cu 4 pixeli, trebuie să alegeți un număr mai mare de 4 în blocul `schimba y cu (4)`{:class="blockmotion"}. Modificați acest număr până când sunteți mulțumit de înălțimea pe care personajul dvs. o sare.

+ Dacă testați acest cod, veți observa că funcționează, dar mișcarea nu este foarte buna. Pentru a face săriturile să arate mai bine, va trebui să mișcați personajul în distante mai mici și mai mici, până când nu mai poate sară.

+ Pentru aceasta, creați o altă variabilă numită `înălțime salt`{:class = "blockdata"}. Din nou, puteți ascunde această variabilă dacă preferați.

+ Ștergeți segventa de codul pentru sarituri pe care ați adăugat-o personajului dvs. și îl înlocuiți cu acesta segventa de cod:
    
    ```blocks
        when [space v] key pressed
        set [inaltime salt v] to [8]
        repeat until < (inaltime salt) = [0] >
            change y by (inaltime salt)
            change [inaltime salt v] by (-0.5)
        end
    ```
    
    Acesta secventa de cod mișcă personajul tău cu 8 pixeli, apoi cu 7,5 pixeli, apoi cu 7 pixeli și așa mai departe, până când personajul tău nu mai poate sări. Acest lucru face ca sariturile sa arate mult mai real.

+ Modificați valoarea de pornire a variabilei ` înălțime salt ` {:class="blockdata"} și testați-o până când sunteți mulțumit de înălțimea pe care personajul dvs. o atinge.