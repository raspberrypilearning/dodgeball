## Bewegung der Spielfigur

Lass uns damit starten, dass wir eine Spielfugur erstllen, die sich sowohl nach rechts und links bewegen, als auch springen und Mäste hochklettern kann.

+ Starte ein neues Projekt und lösche die bestehende Figur, so dass Dein Projekt leer ist. Du kannst das Online-Bearbeitungstool hier finden: <a href="http://jumpto.cc/scratch-new">jumpto.cc/scratch-new</a>.

+ Für dieses Projekt solltest Du einen 'Project Resources'Órdner hqbenm yelcher dqs Hintergrundbild enthält, das Du benötigst. Stelle sicher, dass Du diesen Ordner hast und farage Deinen Club-Leiter, falls Du diesen nicht finden kannst.

	![screenshot](images/dodge-resources.png)

+ Füge das Bild 'background.png' als Bühne hinzu oder zeiche Deinen eigenen Hintergrund! Wenn Du Dein eigenes Level erstellst, solltest Du nur sicherstellen, dass die Mäste und Böden andere Farben haben und dass es eine Tür (oder etwas Ähnliches) gibt, die Dein Spieler erreichen muss. So sollte Dein Projekt aussehen:

	![screenshot](images/dodge-background.png)

+ Füge eine neue Figur hinzu, die Dein Spielcharakter sein wird. Es ist besser, wenn Du eine Figur mit mehreren Kostümen aussuchst, so dass Du es so aussehen lassen kannst, als ob es tatsächlich geht.

	![screenshot](images/dodge-characters.png)

+ Lass uns die Pfeile benutzeb, um Deinen Charakter umherzubewegen. Wenn der Spieler der rechten Pfeil anklickt, sollte sich Dein Charekter nach rechts drehen, einige Schritte gehen und zum nächsten Kostüm wechseln:

	```blocks
		Wenn die grüne Flagge angeklickt
		wiederhole fortlaufend
		   falls <Taste [Pfeil nach rechts v] gedrückt?> dann
		      setze Richtung auf (90 v)
		      gehe (3) er-Schritt
		      nächstes Kostüm
		   Ende
		Ende
	```

+ Teste Deinen Charakter indem Du auf die Fahne klickst und den Rechtspfeil gedrückt hältst. Bewegt sich Deine Spielfigur nach rechts? Sieht Deine Figur so aus, als ob sie wirklich geht?

	![screenshot](images/dodge-walking.png)

+ Um Deine Figur nach links zu bewegen, musst Du einen weiteren `wenn`{:class="blockcontrol"}-Block in Deine `forever`{:class="blockcontrol"}-Schliefe einbauen. Vergiss nicht Deinen Code zu testen, um sicherzustellen, dass er funktioniert!

+ Um einen Mast hochklettern zu können, sollte sich Deine Spielfigur leicht nach oben bewegen, sobald der Hoch-Pfeil gedrückt wird und die Figur die richtige Farbe berührt wird. Füge diesen Code in die `forever`{:class="blockcontrol"}´Schleife der Spielfigur hinzu:

	```blocks
		falls <<Taste [Pfeil nach oben v] gedrückt?> und <wird Farbe [#FFFF00] berührt?>> dann
		   ändere y um (4)
		Ende
	```

+ Teste Deine Spielfigur. Kann es die gelben Masten hochklettern und so das Ende des Levels erreichen?

	![screenshot](images/dodge-test-character.png)
