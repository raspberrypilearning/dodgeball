## ಗುರುತ್ವಾಕರ್ಷಣೆ ಮತ್ತು ಜಿಗಿತ

ಈಗ ನೀವು ನಿಮ್ಮ ಪಾತ್ರವನ್ನು ಹೆಚ್ಚು ವಾಸ್ತವಿಕವಾಗಿ ಚಲಿಸುವಂತೆ ಮಾಡಲಿದ್ದೀರಿ: ನಿಮ್ಮ ಆಟಕ್ಕೆ ಗುರುತ್ವಾಕರ್ಷಣೆಯನ್ನು ಸೇರಿಸಲು ಮತ್ತು ಪಾತ್ರಕ್ಕೆ ನೆಗೆಯುವ ಸಾಮರ್ಥ್ಯವನ್ನು ನೀಡಲಿದ್ದೀರಿ.

--- task ---

ಆಟದಲ್ಲಿ, ನಿಮ್ಮ ಪಾತ್ರವನ್ನು ಸರಿಸಿ ಇದರಿಂದ ಅದು ಪ್ಲಾಟ್ಫಾರ್ಮ್ ನಿಂದ ಹೊರನಡೆಯುತ್ತದೆ. ಅದು ಖಾಲಿ ಜಾಗಕ್ಕೆ ಕಾಲಿಡಬಹುದೆಂದು ನೀವು ನೋಡುತ್ತೀರಾ?

![screenshot](images/dodge-no-gravity.png)

--- /task ---

--- task ---

ಇದನ್ನು ಸರಿಪಡಿಸಲು, ನಿಮ್ಮ ಆಟಕ್ಕೆ ಗುರುತ್ವಾಕರ್ಷಣೆಯನ್ನು ಸೇರಿಸಿ. ಇದನ್ನು ಮಾಡಲು, `gravity`{:class="block3variables"} ಎಂಬ ಹೊಸ variable ಅನ್ನು ರಚಿಸಿ.

[[[generic-scratch3-add-variable]]]

ನೀವು ಬಯಸಿದರೆ ಈ variable ಅನ್ನು ನಿಮ್ಮ ಹಂತದಿಂದ ಮರೆಮಾಡಬಹುದು.

![screenshot](images/dodge-gravity-annotated.png)

--- /task ---

--- task ---

`gravity` ಅನ್ನು ನಕಾರಾತ್ಮಕ ಸಂಖ್ಯೆಗೆ ಹೊಂದಿಸುವ ಈ ಹೊಸ ಕೋಡ್ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಸೇರಿಸಿ ಮತ್ತು ನಿಮ್ಮ ಪಾತ್ರದ y-coordinate ಅನ್ನು ಪದೇ ಪದೇ ಬದಲಾಯಿಸಲು `gravity` ಮೌಲ್ಯವನ್ನು ಬಳಸಿ:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        change y by (gravity)
    end
```

--- /task ---

--- task ---

ಧ್ವಜವನ್ನು ಕ್ಲಿಕ್ ಮಾಡಿ, ತದನಂತರ ನಿಮ್ಮ ಪಾತ್ರವನ್ನು ಹಂತದ ಮೇಲ್ಭಾಗಕ್ಕೆ ಎಳೆಯಿರಿ. ಏನಾಗುತ್ತದೆ? ನೀವು ನಿರೀಕ್ಷಿಸಿದಂತೆ ಗುರುತ್ವ ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆಯೇ?

![screenshot](images/dodge-gravity-drag.png)

--- /task ---

--- task ---

ಗುರುತ್ವವು sprite ಪಾತ್ರವನ್ನು ವೇದಿಕೆ ಅಥವಾ ಏಣಿಯ ಮೂಲಕ ಚಲಿಸಬಾರದು! ಪಾತ್ರವು ಗಾಳಿಯಲ್ಲಿದ್ದಾಗ ಕೇವಲ ಗುರುತ್ವಾಕರ್ಷಣೆ ಕೆಲಸ ಮಾಡಲು ನಿಮ್ಮ ಕೋಡ್ ಗೆ ಒಂದು `if`{:class="block3control"} ಬ್ಲಾಕ್ ಅನ್ನು ಸೇರಿಸಿ. ಗುರುತ್ವ ಕೋಡ್ ನಂತರ ಈ ರೀತಿ ಇರಬೇಕು:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
            change y by (gravity)
        end
    end
```

--- /task ---

--- task ---

ಗುರುತ್ವವು ಈಗ ಸರಿಯಾಗಿ ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆಯೇ ಎಂದು ನೋಡಲು ಆಟವನ್ನು ಮತ್ತೆ ಪರೀಕ್ಷಿಸಿ. ನಿಮ್ಮ sprite ಪಾತ್ರವು ಪ್ಲಾಟ್‌ಫಾರ್ಮ್ ಅಥವಾ ಏಣಿಯನ್ನು ಮುಟ್ಟಿದಾಗ ಬೀಳುವುದನ್ನು ನಿಲ್ಲಿಸುತ್ತದೆಯೇ? ನೀವು ಪ್ಲ್ಯಾಟ್‌ಫಾರ್ಮ್‌ಗಳ ಅಂಚಿನಿಂದ ಹೊರನಡೆದು ಕೆಳಗಿನ ಮಟ್ಟಕ್ಕೆ ಬೀಳುವಂತೆ ಮಾಡಬಹುದೇ?

![screenshot](images/dodge-gravity-test.png)

--- /task ---

--- task ---

ಆಟಗಾರನು <kbd>space</kbd> ಕೀಲಿಯನ್ನು ಒತ್ತಿದಾಗಲೆಲ್ಲಾ ನಿಮ್ಮ ಪಾತ್ರವನ್ನು ಜಿಗಿಯುವಂತೆ ಮಾಡಲು ಕೋಡ್ ಸೇರಿಸಿ. ಇದನ್ನು ಮಾಡಲು ಬಹಳ ಸುಲಭವಾದ ಮಾರ್ಗವೆಂದರೆ ನಿಮ್ಮ ಪಾತ್ರವನ್ನು ಕೆಲವು ಬಾರಿ ಸರಿಸುವುದು:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    repeat (10)
        change y by (4)
    end
```

ಗುರುತ್ವ ನಿರಂತರವಾಗಿ 4 pixel ಗಳಿಂದ ನಿಮ್ಮ ಪಾತ್ರವನ್ನು ಕೆಳಗೆ ತಳ್ಳುತ್ತದೆ, ನೀವು ನಿಮ್ಮ `change y by (4)`{:class="block3motion"} block ನಲ್ಲಿ `4` ಕಿಂತ ಹೆಚ್ಚಿನ ಸಂಖ್ಯೆಯನ್ನು ಆಯ್ಕೆ ಮಾಡಬೇಕಾಗುತ್ತದೆ. ಪಾತ್ರ ಜಿಗಿತದ ಎತ್ತರದಿಂದ ನೀವು ಸಂತೋಷವಾಗುವವರೆಗೆ ಸಂಖ್ಯೆಯನ್ನು ಬದಲಾಯಿಸಿ.

--- /task ---

--- task ---

ನಿಮ್ಮ code ಅನ್ನು ಪರೀಕ್ಷಿಸಿ. ಜಿಗಿತದ ಚಲನೆ ತುಂಬಾ ಸುಗಮವಾಗಿಲ್ಲ ಎಂಬುದನ್ನು ಗಮನಿಸಿ. ಜಿಗಿತವನ್ನು ಸುಗಮವಾಗಿ ಕಾಣುವಂತೆ ಮಾಡಲು, ಅದು ಯಾವುದೇ ಎತ್ತರಕ್ಕೆ ಏರದಿರುವವರೆಗೆ, ನಿಮ್ಮ sprite ಪಾತ್ರವನ್ನು ಕಡಿಮೆ ಪ್ರಮಾಣದಲ್ಲಿ ಸರಿಸಬೇಕು.

--- /task ---

--- task ---

ಇದನ್ನು ಮಾಡಲು, `jump height`{:class="block3variables"} ಎಂಬ ಹೊಸ variable ಅನ್ನು ರಚಿಸಿ. ಮತ್ತೆ, ನೀವು ಬಯಸಿದಲ್ಲಿ ಈ variable ಅನ್ನು ನೀವು ಮರೆಮಾಡಬಹುದು.

--- /task ---

--- task ---

ನಿಮ್ಮ sprite ಪಾತ್ರಕ್ಕೆ ನೀವು ಸೇರಿಸಿದ ಜಂಪಿಂಗ್ ಕೋಡ್(jumping code ) ಅನ್ನು ಅಳಿಸಿ, ಮತ್ತು ಬದಲಿಗೆ ಈ ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಿ:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    set [jump height v] to [8]
    repeat until < (jump height) = [0] >
        change y by (jump height)
        change [jump height v] by (-0.5)
    end
```

ಈ ಕೋಡ್ ನಿಮ್ಮ ಪಾತ್ರವು ಮೇಲೆ ಏರಿಕೆಯಾಗದಿರುವವರೆಗೂ 8 pixel, ನಂತರ 7.5 pixel, ನಂತರ 7 pixel ಮತ್ತು ಹೀಗೆ ಮುಂದುವರೆಯುತ್ತದೆ. ಇದು ಜಿಗಿತವನ್ನು ಹೆಚ್ಚು ಸುಗಮವಾಗಿ ಕಾಣುವಂತೆ ಮಾಡುತ್ತದೆ.

--- /task ---

--- task ---

`repeat`{:class="block3control"} ಪ್ರಾರಂಭವಾಗುವ ಮೊದಲು ದೃಢೀಕರಿಸಿದ `jump height`{:class="block3variables"} variable ನ ಮೌಲ್ಯವನ್ನು ಬದಲಾಯಿಸಿ. ನಂತರ ನಿಮ್ಮ ಆಟವನ್ನು ಪರೀಕ್ಷಿಸಿ.

ಪಾತ್ರವು ಎಷ್ಟು ಎತ್ತರಕ್ಕೆ ಜಿಗಿಯುತ್ತದೆ ಎಂದು ನಿಮಗೆ ಸಂತೋಷವಾಗುವವರೆಗೆ ಈ ಎರಡು ಹಂತಗಳನ್ನು ಪುನರಾವರ್ತಿಸಿ.

--- /task ---