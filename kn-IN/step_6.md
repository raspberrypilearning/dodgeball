## Dodging balls

ನಿಮ್ಮ ಪಾತ್ರವು ಈಗ ಚಲಿಸಬಹುದು ಮತ್ತು ನೆಗೆಯಬಹುದು, ಆದ್ದರಿಂದ ಪಾತ್ರವು ತಪ್ಪಿಸಬೇಕಾದ ಕೆಲವು ಚೆಂಡುಗಳನ್ನು ಸೇರಿಸುವ ಸಮಯ.

--- task ---

ಹೊಸ ಬಾಲ್(ball) sprite ರಚಿಸಿ. ನೀವು ಇಷ್ಟಪಡುವ ಯಾವುದೇ ರೀತಿಯ ಚೆಂಡನ್ನು ನೀವು ಆಯ್ಕೆ ಮಾಡಬಹುದು.

![screenshot](images/dodge-balls.png)

--- /task ---

--- task ---

ಚೆಂಡಿನ sprite ಅನ್ನು ಮರುಗಾತ್ರಗೊಳಿಸಿ ಇದರಿಂದ ಪಾತ್ರವು ಅದರ ಮೇಲೆ ಹಾರಿಹೋಗುತ್ತದೆ. ಚೆಂಡು ಸರಿಯಾದ ಗಾತ್ರವೇ ಎಂದು ಪರೀಕ್ಷಿಸಲು ಪಾತ್ರವು ಚೆಂಡಿನ ಮೇಲೆ ಹಾರಿ ಹೋಗುವಂತೆ ಮಾಡಲು ಪ್ರಯತ್ನಿಸಿ.

![screenshot](images/dodge-ball-resize.png)

--- /task ---

--- task ---

ನಿಮ್ಮ ball sprite ‌ಗೆ ಈ ಕೋಡ್ ಸೇರಿಸಿ:

![ball sprite](images/ball_sprite.png)

```blocks3
when green flag clicked
hide
forever 
  wait (3) seconds
  create clone of (myself v)
end
```

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
delete this clone
```

ಈ ಕೋಡ್ ಪ್ರತಿ ಮೂರು ಸೆಕೆಂಡಿಗೆ ball sprite ‌ನ ಹೊಸ ತದ್ರೂಪಿ ರಚಿಸುತ್ತದೆ. ಪ್ರತಿಯೊಂದು ಹೊಸ ತದ್ರೂಪಿ ಮೇಲಿನ ಪ್ಲಾಟ್ಫಾರ್ಮ್ ನ ಉದ್ದಕ್ಕೂ ಚಲಿಸುತ್ತದೆ ಮತ್ತು ನಂತರ ಇಳಿಯುತ್ತದೆ.

--- /task ---

--- task ---

ಆಟವನ್ನು ಪರೀಕ್ಷಿಸಲು ಧ್ವಜದ ಮೇಲೆ ಕ್ಲಿಕ್ ಮಾಡಿ.

![screenshot](images/dodge-ball-test.png)

--- /task ---

--- task ---

ನಿಮ್ಮ ball sprite ‌ಗೆ ಹೆಚ್ಚಿನ ಕೋಡ್ ಸೇರಿಸಿ ಇದರಿಂದ ಅದರ ತದ್ರೂಪುಗಳು ಎಲ್ಲಾ ಮೂರು ಪ್ಲ್ಯಾಟ್‌ಫಾರ್ಮ್‌ಗಳಲ್ಲಿ ಚಲಿಸುತ್ತವೆ.

![screenshot](images/dodge-ball-more-motion.png)

--- hints ---


--- hint ---

ball sprite ಕ್ಲೋನ್ ಅನ್ನು ಮೊದಲಿನ ಪ್ಲಾಟ್‌ಫಾರ್ಮ್‌ನಾದ್ಯಂತ ಸರಿಸಲು ನೀವು ಬಳಸಿದ ಕೋಡ್ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಪುನರಾವರ್ತಿಸಿ. ನೀವು `x`{:class="block3motion"}, `y`{:class="block3motion"}, ಮತ್ತು `repeat`{:class="block3control"} ಸಂಖ್ಯೆಯನ್ನು ಬದಲಾಯಿಸಬೇಕಾಗಿದೆ ಇದರಿಂದ ತದ್ರೂಪುಗಳು ಪ್ಲ್ಯಾಟ್‌ಫಾರ್ಮ್‌ಗಳನ್ನು ಸರಿಯಾಗಿ ಅನುಸರಿಸುತ್ತವೆ.

--- /hint ---

--- hint ---

ಇವು ನಿಮಗೆ ಅಗತ್ಯವಿರುವ ಬ್ಲಾಕ್ ಗಳು. ನೀವು ಅವುಗಳನ್ನು ಸರಿಯಾದ ಕ್ರಮದಲ್ಲಿ ಸೇರಿಸಿದ್ದೀರಿ ಎಂದು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳಿ.

![ball sprite](images/ball_sprite.png)

```blocks3
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end

repeat (180) 
  change x by (2)
  turn cw (6) degrees
end

repeat (30) 
  change y by (-4)
end
```

--- /hint ---

--- hint ---

ನಿಮ್ಮ ball sprite ತದ್ರೂಪುಗಳ ಕೋಡ್ ಈ ರೀತಿ ಕಾಣಬೇಕು:

![ball sprite](images/ball_sprite.png)

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (180) 
  change x by (2)
  turn cw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
delete this clone
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

ಈಗ ನಿಮ್ಮ ಪಾತ್ರವು ಚೆಂಡಿನಿಂದ ಹೊಡೆದರೆ ಸಂದೇಶವನ್ನು ಪ್ರಸಾರ ಮಾಡಲು (ಕಳುಹಿಸಲು) ಕೆಲವು ಕೋಡ್ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಸೇರಿಸಿ!

ನಿಮ್ಮ ball sprite ‌ಗೆ ಈ ಕೋಡ್ ಸೇರಿಸಿ:

![ball sprite](images/ball_sprite.png)

```blocks3
    when I start as a clone
    forever
        if < touching (Pico walking v)? > then
            broadcast (hit v)
        end
    end
```

--- /task ---

--- task ---

ಅಂತಿಮವಾಗಿ, `hit` ಸಂದೇಶವನ್ನು ಸ್ವೀಕರಿಸುವಾಗ ಅದನ್ನು ನಿಮ್ಮ ಆರಂಭಿಕ ಸ್ಥಾನಕ್ಕೆ ಹಿಂತಿರುಗಿಸಲು ನಿಮ್ಮ sprite ಪಾತ್ರಕ್ಕೆ ಕೋಡ್ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಸೇರಿಸಿ:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

--- /task ---

--- task ---

ನಿಮ್ಮ code ಅನ್ನು ಪರೀಕ್ಷಿಸಿ. ಚೆಂಡನ್ನು ಸ್ಪರ್ಶಿಸಿದ ನಂತರ ಪಾತ್ರವು ಪ್ರಾರಂಭಕ್ಕೆ ಹಿಂತಿರುಗುತ್ತದೆಯೇ ಎಂದು ಪರಿಶೀಲಿಸಿ.

--- /task ---