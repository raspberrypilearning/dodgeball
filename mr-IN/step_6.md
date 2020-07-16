## चेंडुंना चकवा देणे

Your character can move and jump now, so it's time to add some balls that the character has to avoid.

\--- task \---

नवीन चेंडूची स्प्राइट तयार करा. आपल्या आवडीच्या कोणत्याही प्रकारच्या चेंडूची निवड तुम्ही करू शकता.

![screenshot](images/dodge-balls.png)

\--- /task \---

\--- task \---

चेंडूच्या स्प्राइटचे आकार बदला जेणेकरून पात्र त्यावर उडी मारू शकेल. Try making the character jump over the ball to test whether the ball is the right size.

![screenshot](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

आपल्या चेंडूच्या स्प्राइटमध्ये हा कोड जोडा:

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

हा कोड दर तीन सेकंदाच्या अवधीने चेंडूच्या स्प्राइटचा नवीन क्लोन तयार करतो. प्रत्येक नवीन क्लोन वरच्या फलाटावर फिरतो आणि नंतर पडतो.

\--- /task \---

\--- task \---

खेळाची चाचणी घेण्यासाठी ध्वजावर क्लिक करा.

![screenshot](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Add more code to your ball sprite so that clones of it move across all three platforms.

![screenshot](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Repeat the code blocks you used to move the ball sprite clone across the first platform. You need to change the `x`{:class="block3motion"}, `y`{:class="block3motion"}, and `repeat`{:class="block3control"} numbers so that the clones follow the platforms correctly.

\--- /hint \---

\--- hint \---

आपल्याला आवश्यक असलेले हे ब्लॉकस् आहेत. आपण त्यांना योग्य क्रमाने जोडले असल्याची खात्री करा.

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

\--- /hint \---

\--- hint \---

आपल्या चेंडूच्या स्प्राइट क्लोनसाठी कोड यासारखा दिसावा:

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

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Now add some code blocks to broadcast (send) a message if your character gets hit by a ball!

आपल्या बॉल स्प्राइटमध्ये हा कोड जोडा:

![ball sprite](images/ball_sprite.png)

```blocks3
    when I start as a clone
    forever
        if < touching (Pico walking v)? > then
            broadcast (hit v)
        end
    end
```

\--- /task \---

\--- task \---

Finally, add code blocks to your character sprite to make it move back to its starting position when it receives the `hit` message:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

आपला कोड तपासून पहा. बॉलला स्पर्श केल्यानंतर पात्र परत सुरुवातीकडे जातो की नाही ते तपासा.

\--- /task \---