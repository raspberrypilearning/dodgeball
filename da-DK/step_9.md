## Udfordring: flere forhindringer

Hvis du tror at dit spil stadigvæk er for let, kan du tilføje flere forhindringer til det. Du kan frit bestemme hvad forhindringerne skal være! Her er nogle ideer:

+ En farlig sommerfugl
+ Platforme, som dukker op og forsvinder
+ Tennisbolde som falder ned og skal undviges

![screenshot](images/dodge-obstacles.png)

Du kunne endda skabe det næste niveau ved at designe en anden baggrund med platforme. For at tilgå det næste niveau, skal du tilføje kode der gør, at når din figur rører den grønne dør, så skifter spillet til den næste baggrund:

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
	if <touching color [#00FF00]?> then
		switch backdrop to (next backdrop v)
		go to x: (-210) y: (-120)
		wait (1) seconds
	end
```
