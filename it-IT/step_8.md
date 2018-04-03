## Laser!

Rendiamo il gioco un po' più difficile aggiungendo dei laser!

+ Aggiungi un nuovo sprite al tuo gioco, chiamato 'Laser'. Dovrebbe avere 2 costumi, chiamati 'on' e 'off'.

	![screenshot](images/dodge-lasers-costume.png)

+ Posiziona il tuo nuovo laser dove preferisci tra le 2 piattaforme.

	![screenshot](images/dodge-lasers-position.png)

+ Aggiungi un codice al laser per farlo passare da un costumeall'altro.

	```blocks
		quando si clicca sulla bandiera verde
		per sempre
  			passa al costume [accendi v]
  			attendi (2) secondi
  			passa al costume [spegni v]
  			attendi (2) secondi
		end
	```

	Se preferisci, puoi `attendi`{:class="blockcontrol"} un periodo di tempo `a caso`{:class="blockoperators"} tra il cambio da un costume all'altro.

+ Infine, aggiungi un codice al tuo laser, in modo che venga trasmesso il messaggio 'colpito' quando il laser tocca il personaggio. Questo codice sarà molto simile a quello che hai aggiunto allo sprite della palla.

	Non dovrai aggiungere altri codici al tuo personaggio - sa già cosa fare quando viene colpito!

+ Prova il tuo gioco per vedere se riesci a superare il laser. Cambia i tempi di `attendi`{:class="blockcontrol"} nel tuo codice se i laser sono troppo facili o troppo difficili.
