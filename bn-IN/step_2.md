## Character এর চলন

এমন একটি character তৈরি করে শুরু করুন যা বাম এবং ডানদিকে যেতে পারে এবং মই দিয়ে উঠতে পারে।.

--- task ---

'Dodgeball' Scratch starter project খুলুন।.

**Online:** starter প্রকল্প এখানে খুলুন [rpf.io/dodgeball-on](https://rpf.io/dodgeball-on){:target="_blank"}.

আপনার যদি scratch অ্যাকাউন্ট থাকে তবে আপনি **Remix** ক্লিক করে এটির একটি অনুলিপি তৈরি করতে পারেন ।.

**Offline:** প্রজেক্ট টি [rpf.io/p/bn-IN/dodgeball-get](https://rpf.io/p/bn-IN/dodgeball-get) থেকে ডাউনলোড করুন এবং সেটি অফলাইন এডিটর ব্যবহার করে খুলুন.

--- /task ---

প্রকল্পটিতে প্ল্যাটফর্মগুলির সাথে একটি ব্যাকড্রপ রয়েছে:

![dodgeball project background](images/dodge-background.png)

--- task ---

প্লেয়ারটি যে characterটি নিয়ন্ত্রণ করবে তার একটি নতুন sprite চয়ন করুন এবং এটি আপনার প্রকল্পে যুক্ত করুন।. আপনি একাধিক costume এর সাথে একটি sprite বেছে নিলে এটি সর্বোত্তম হয়, যাতে এটিকে হাঁটাচলা করার মতো দেখায়।.

![pick a sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

আপনার character sprite এ কোড ব্লক যুক্ত করুন যাতে প্লেয়ার character টিকে চারপাশে সরানোর জন্য তীরযুক্ত কী বা arrow keys গুলো ব্যবহার করতে পারে।. প্লেয়ার যখন right arrow চাপছে, character টিকে ডানদিকে নির্দেশ করা উচিত, কয়েক ধাপ সরিয়ে নিয়ে, পরবর্তী costume পরিবর্তন করা উচিত:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
when flag clicked
forever
    if <key (right arrow v) pressed? > then
        point in direction (90 v)
        move (3) steps
        next costume
    end
end
```

--- /task ---

--- task ---

যদি আপনার sprite ফিট না করে তবে এর আকারটি সামঞ্জস্য করুন।.

![set sprite size so it fits](images/dodge-sprite-size-annotated.png)

--- /task ---

--- task ---

পতাকাটিতে ক্লিক করে এবং তারপরে right arrow key ধরে রেখে আপনার character টি পরীক্ষা করে দেখুন।. আপনার character কি ডানে যায়? Character দেখে মনে হয় এটি হাঁটছে?

![screenshot](images/dodge-walking.png)

--- /task ---

--- task ---

Character sprite এর লুপে এই কোড ব্লক যোগ করুন `forever`{:class="block3control"} যাতে এটি বাম দিকে যায় left arrow key চাপলে.

--- hints ---


--- hint ---

যাতে character টি বাম দিকে যেতে পারে, আপনাকে `if`{:class="block3control"} এই ব্লক যোগ করতে হবে `forever`{:class="block3control"} loop এর মধ্যে।. এই নতুন `if`{:class="block3control"} ব্লক এর মধ্যে, character sprite কোড যুক্ত করুন `move`{:class="block3motion"} যাতে এটি বাম দিকে যায়.

--- /hint ---

--- hint ---

Character টি ডানদিকে হাঁটতে আপনি তৈরি কোডটি অনুলিপি করুন।. `key pressed`{:class="block3sensing"} এটিকে `left arrow`{:class="block3sensing"} এটিতে পরিবর্তন করুন, এবং `direction`{:class="block3motion"} এটিকে বদলে করুন `-90` তে.

```blocks3
if <key (right arrow v) pressed? > then
    point in direction (90 v)
    move (3) steps
    next costume
end
```

--- /hint ---

--- hint ---

আপনার কোডটি দেখতে এমন হওয়া উচিত:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
when green flag clicked
forever 
  if <key (right arrow v) pressed?> then 
    point in direction (90 v)
    move (3) steps
    next costume
  end
  if <key (left arrow v) pressed?> then 
    point in direction (-90 v)
    move (3) steps
    next costume
  end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

আপনার নতুন কোডটি কাজ করে তা নিশ্চিত করার জন্য পরীক্ষা করুন।. বাম দিকে হাঁটার সময় আপনার character টি কি উল্টো দিকে ঘুরছে?

![screenshot](images/dodge-upside-down.png)

যদি তা হয় তবে **direction** ক্লিক করে আপনি এটি ঠিক করতে পারেন এবং তারপরে বাম-ডান তীর বা left-right arrow ক্লিক করুন।.

![screenshot](images/dodge-left-right-annotated.png)

অথবা আপনি যদি মনে করেন তবে আপনার character script এর শুরুতে এই ব্লকটি যুক্ত করে সমস্যাটি ঠিক করতে পারেন:

```blocks3
set rotation style [left-right v]
```

--- /task ---

--- task ---

গোলাপী মইয়ের উপরে উঠতে, যখনই উপরের তীরটি চাপা হয় তখন আপনার character sprite টি স্টেজের উপরে কয়েক ধাপ উপরে যাবে **and** character টি সঠিক রঙ স্পর্শ করবে ।.

Add inside your character's `forever`{:class="block3control"} loop to `change`{:class="block3motion"} the character's `y` (vertical) position `if`{:class="block3control"} the `up arrow is pressed`{:class="block3sensing"} and the character is `touching the colour pink`{:class="block3sensing"}.

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
        change y by (4)
    end
```

--- /task ---

--- task ---

আপনার কোড পরীক্ষা করুন।. আপনি কি character টিকে গোলাপী মইয়ের উপরে তুলে স্তরটির শেষে যেতে পারেন?

![screenshot](images/dodge-test-character.png)

--- /task ---
