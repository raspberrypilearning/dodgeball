## पात्राची हालचाल

Start by creating a character that can move left and right, and can climb up ladders.

\--- task \---

'डॉजबॉल' स्क्रॅच स्टार्टर प्रकल्प उघडा.

**Online:** open the starter project at [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){:target="_blank"}.

आपल्याकडे स्क्रॅच खाते असल्यास आपण **Remix** वर क्लिक करून प्रत तयार करू शकता.

**Offline:** download the starter project from [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get) and then open it using the offline editor.

\--- /task \---

The project contains a backdrop with platforms:

![dodgeball project background](images/dodge-background.png)

\--- task \---

Choose a new sprite as the character the player will control, and add it to your project. It's best if you choose a sprite with multiple costumes, so that you can make it look as though it's walking.

![pick a sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Add code blocks to your character sprite so that the player can use the arrow keys to move the character around. When the player presses the right arrow, the character should point right, move a few steps, and change to the next costume:

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

\--- /task \---

\--- task \---

If your sprite doesn't fit, adjust its size.

![set sprite size so it fits](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

Test out your character by clicking the flag and then holding down the right arrow key. आपले पात्र उजवीकडे सरकत आहे का? आपले पात्र चालत असल्यासारखे दिसते आहे का?

![screenshot](images/dodge-walking.png)

\--- /task \---

\--- task \---

Add code blocks to the character sprite's `forever`{:class="block3control"} loop so that it walks left if the left arrow key is pressed.

\--- hints \---

\--- hint \---

So that your character can move to the left, you'll need to add another `if`{:class="block3control"} block inside the `forever`{:class="block3control"} loop. In this new `if`{:class="block3control"} block, add code to make your character sprite `move`{:class="block3motion"} to the left.

\--- /hint \---

\--- hint \---

पात्र उजवीकडे चालवण्यासाठी आपण तयार केलेला कोड कॉपी करा. Then set the `key pressed`{:class="block3sensing"} to the `left arrow`{:class="block3sensing"}, and change the `direction`{:class="block3motion"} to `-90`.

```blocks3
if <key (right arrow v) pressed? > then
    point in direction (90 v)
    move (3) steps
    next costume
end
```

\--- /hint \---

\--- hint \---

आपला कोड आता यासारखा दिसला पाहिजे:

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

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

आपला नवीन कोड ठीक चालतोय हे पाहण्यासाठी त्याला चालवून पहा. डावीकडे चालत असताना आपले पात्र उलटे होते?

![screenshot](images/dodge-upside-down.png)

If so, you can fix this by clicking on the **direction** of your character sprite, and then clicking on the left-right arrow.

![screenshot](images/dodge-left-right-annotated.png)

Or if you prefer, you can also fix the problem by adding this block to the start of your character's script:

```blocks3
set rotation style [left-right v]
```

\--- /task \---

\--- task \---

To climb a pink ladder, your character sprite should move a few steps upwards on the Stage whenever the up arrow is pressed **and** the character is touching the correct colour.

Add inside your character's `forever`{:class="block3control"} loop to `change`{:class="block3motion"} the character's `y` (vertical) position `if`{:class="block3control"} the `up arrow is pressed`{:class="block3sensing"} and the character is `touching the colour pink`{:class="block3sensing"}.

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
        change y by (4)
    end
```

\--- /task \---

\--- task \---

आपल्या कोडची पुन्हा चाचणी घ्या. आपण पात्राला गुलाबी शिडी चढायला लावून पातळीच्या शेवटाला पोहचवू शकता का?

![screenshot](images/dodge-test-character.png)

\--- /task \---