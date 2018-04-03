--- challenge ---
## Sfida: Altri ostacoli 
Se credi che il gioco sia troppo facile, puoi aggiungere altri ostacoli al tuo livello. Puoi aggiungere quello che vuoi, ma ecco qualche idea:

+ Una farfalla assassina;
+ Piattaforme che appaiono e scompaiono;
+ Palline da tennis cadenti che devono essere evitate.

![screenshot](images/dodge-obstacles.png)

Puoi perfino creare più di uno scenario, e avanzare al livello seguente quando il personaggio raggiunge la porta verde:

```blocks
	se <sta toccando il colore [#00FF00]> allora
  		passa allo sfondo [prossimo scenario v]
  		vai a x: (-210) y: (-120)
  		attendi (1) secondi
	end
```




--- /challenge ---