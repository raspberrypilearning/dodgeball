## Lasers!

ನಿಮ್ಮ ಆಟವನ್ನು ಕಷ್ಟದಿಂದ ಪೂರ್ಣಗೊಳಿಸಲು, ನೀವು ಲೇಸರ್‌(laser)ಗಳನ್ನು ಸೇರಿಸಲು ಹೊರಟಿದ್ದೀರಿ!

\--- task \---

ನಿಮ್ಮ ಆಟಕ್ಕೆ ಹೊಸ sprite ಸೇರಿಸಿ ಮತ್ತು ಅದನ್ನು `laser` ಎಂದು ಕರೆಯಿರಿ. ಇದು ಎರಡು ವೇಷಭೂಷಣಗಳನ್ನು ಹೊಂದಿರಬೇಕು: ಒಂದು 'on' ಮತ್ತೊಂದು 'ಆಫ್' ಎಂದು ಕರೆಯಲ್ಪಡುತ್ತದೆ.

![screenshot](images/dodge-lasers-costume1.png)

![screenshot](images/dodge-lasers-costume2.png)

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಹೊಸ laser sprite ಅನ್ನು ಎರಡು ಪ್ಲಾಟ್‌ಫಾರ್ಮ್‌ಗಳ ನಡುವೆ ಇರಿಸಿ.

![screenshot](images/dodge-lasers-position.png)

\--- /task \---

\--- task \---

ಎರಡು ವೇಷಭೂಷಣಗಳ ನಡುವೆ ಬದಲಾಯಿಸಲು ನಿಮ್ಮlaser sprite ಗೆ ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಿ.

![laser sprite](images/laser_sprite.png)

```blocks3
    when flag clicked
    forever
        switch costume to (on v)
        wait (2) seconds
        switch costume to (off v)
        wait (2) seconds
    end
```

ನೀವು ಬಯಸಿದಲ್ಲಿ, ನೀವು ಮೇಲೆ ತೋರಿಸಿರುವ ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಬಹುದು ಇದರಿಂದ sprite `random`{:class="block3operators"} ಅವಧಿಯವರೆಗೆ `waits`{:class="block3control"} ಮಾಡುತ್ತದೆ.

\--- /task \---

\--- task \---

ಅಂತಿಮವಾಗಿ, ನಿಮ್ಮ laser sprite ಗೆ ಕೋಡ್ ಸೇರಿಸಿ ಇದರಿಂದ laser sprite ಅದರ ಪಾತ್ರವನ್ನು ಮುಟ್ಟಿದಾಗ 'hit' ಸಂದೇಶವನ್ನು ಪ್ರಸಾರ ಮಾಡುತ್ತದೆ.

\--- hints \---

\--- hint \---

ಈ ಕೋಡ್ ನಿಮ್ಮ ball sprite ಗೆ ಸೇರಿಸಿರುವ ಕೋಡ್ ಅನ್ನು ಹೋಲುವಂತೆ ಇರಬೇಕು.

\--- /hint \---

\--- hint \---

`touching your character`{:class="block3sensing"} ಸ್ಪರ್ಶಿಸಿದಾಗ `broadcast 'hit'`{:class="block3control"} ಮಾಡಲು ball sprite ಗೆ ಸೇರಿಸುವ ಕೋಡ್ ಅನ್ನು ನಕಲಿಸಿ.

\--- /hint \---

\--- hint \---

ನೀವು ಈ ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಬೇಕು:

![laser sprite](images/laser_sprite.png)

```blocks3
when green flag clicked
forever 
  if <touching (Pico walking v) ?> then 
    broadcast (hit v)
  end
end
```

\--- /hint \---

\--- /hints \---

ನಿಮ್ಮ sprite ಪಾತ್ರಕ್ಕೆ ನೀವು ಯಾವುದೇ ಹೆಚ್ಚುವರಿ ಕೋಡ್ ಅನ್ನು ಸೇರಿಸುವ ಅಗತ್ಯವಿಲ್ಲ, ಏಕೆಂದರೆ `broadcast 'hit'`{:class="block3control"} ಅನ್ನು ಪಡೆದಾಗ ಏನು ಮಾಡಬೇಕೆಂದು sprite ಪಾತ್ರಕ್ಕೆ ಈಗಾಗಲೇ ತಿಳಿದಿದೆ!

\--- /task \---

\--- task \---

ನೀವು ಪಾತ್ರವನ್ನು laser ನ ಹಿಂದೆ ಸರಿಸಬಹುದೇ ಎಂದು ನೋಡಲು ನಿಮ್ಮ ಆಟವನ್ನು ಪರೀಕ್ಷಿಸಿ. Laser ತುಂಬಾ ಸುಲಭ ಅಥವಾ ತಪ್ಪಿಸಲು ತುಂಬಾ ಕಷ್ಟವಾಗಿದ್ದರೆ, laser sprite ಗಾಗಿ ಕೋಡ್‌ನಲ್ಲಿ `wait`{:class="block3control"} ಸಮಯವನ್ನ ಬದಲಾಯಿಸಿ.

\--- /task \---