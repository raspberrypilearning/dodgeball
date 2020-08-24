## বল ডজিং

আপনার character টি এখন সরতে এবং লাফাতে পারে, তাই character টি এড়িয়ে চলবে এমন কয়েকটি বল যুক্ত করার সময় এসেছে ।.

\--- task \---

একটি নতুন বল/ball sprite তৈরি করুন।. আপনি যে কোনও ধরণের বল পছন্দ করতে পারেন।.

![screenshot](images/dodge-balls.png)

\--- /task \---

\--- task \---

বল sprite কে resize করুন যাতে character টি তার উপরে লাফিয়ে উঠতে পারে।. Try making the character jump over the ball to test whether the ball is the right size.

![screenshot](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

আপনার ball sprite এ এই কোড যুক্ত করুন:

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

এই কোড প্রতি তিন সেকেন্ডে বল sprite এর একটি নতুন ক্লোন তৈরি করে।. প্রতিটি নতুন ক্লোন উপরের প্ল্যাটফর্মের সাথে সরতে পারে এবং তারপরে পড়ে যায়।.

\--- /task \---

\--- task \---

গেমটি পরীক্ষা করতে পতাকাতে ক্লিক করুন।.

![screenshot](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

আপনার বল sprite এ আরও কোড যুক্ত করুন যাতে এর ক্লোনগুলি তিনটি প্ল্যাটফর্ম জুড়ে চলতে পারে।.

![screenshot](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

আপনি প্রথম প্ল্যাটফর্ম জুড়ে বল sprite ক্লোন সরানোর জন্য যে কোড ব্লকগুলি ব্যবহার করেছিলেন সেগুলি পুনরাবৃত্তি করুন।. `x`{:class="block3motion"}, `y`{:class="block3motion"}, এবং `repeat`{:class="block3control"} নম্বরগুলি পরিবর্তন করতে হবে যাতে ক্লোনগুলি প্লাটফর্মকে সঠিক ভাবে অনুসরণ করে.

\--- /hint \---

\--- hint \---

আপনার প্রয়োজনীয় কোডগুলি এখানে রইল. আপনি এগুলি সঠিক ক্রমে যুক্ত করেছেন তা নিশ্চিত করুন।.

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

আপনার বল sprite ক্লোনগুলির কোডটি দেখতে এমন হওয়া উচিত:

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

আপনার character টি যদি কোনও বল দ্বারা আঘাতের শিকার হয় তবে একটি বার্তা সম্প্রচার (broadcast) করতে করতে কয়েকটি কোড ব্লক যুক্ত করুন!

আপনার ball sprite এ এই কোডটি যুক্ত করুন:

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

Test out your code. Check whether the character moves back to the start after touching a ball.

\--- /task \---