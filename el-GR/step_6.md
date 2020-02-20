## Αποφεύγοντας τις μπάλες

Ο χαρακτήρας σου μπορεί πλέον να κινηθεί και να πηδήξει, οπότε ήρθε η ώρα να προσθέσουμε μερικές μπάλες τις οποίες ο χαρακτήρας πρέπει να αποφύγει.

\--- task \---

Δημιούργησε μία κινούμενη εικόνα μπάλας. Μπορείς να επιλέξεις οποιοδήποτε τύπο μπάλας θέλεις.

![στιγμιότυπο οθόνης](images/dodge-balls.png)

\--- /task \---

\--- task --

Άλλαξε το μέγεθος της εικόνας της μπάλας, έτσι ώστε ο χαρακτήρας να μπορεί να πηδήξει από πάνω της. Δοκίμασε να κάνεις το χαρακτήρα να πηδήξει πάνω από την μπάλα για να ελέγξεις αν η μπάλα είναι στο σωστό μέγεθος.

![στιγμιότυπο οθόνης](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Πρόσθεσε αυτόν τον κώδικα στην εικόνα της μπάλας:

![κινούμενη εικόνα μπάλας](images/ball_sprite.png)

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

Αυτός ο κώδικας δημιουργεί ένα νέο κλώνο της μπάλας κάθε τρία δευτερόλεπτα. Κάθε νέος κλώνος κινείται κατά μήκος της επάνω πλατφόρμας και έπειτα πέφτει.

\--- /task \---

\--- task \---

Κάνε κλικ στη σημαία για να δοκιμάσεις το παιχνίδι.

![στιγμιότυπο οθόνης](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Πρόσθεσε περισσότερο κώδικα στην εικόνα της μπάλας, έτσι ώστε οι κλώνοι της να κινούνται και στις τρεις πλατφόρμες.

![στιγμιότυπο οθόνης](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Επανέλαβε τα τουβλάκια κώδικα που χρησιμοποίησες για να μετακινήσεις τον κλώνο της μπάλας στην πρώτη πλατφόρμα. Πρέπει να αλλάξεις το `x` {: class = "block3motion"}, το `y` {: class = "block3motion"}, και τον αριθμό `επανάληψης` {: class = "block3control"}, ώστε οι κλώνοι να ακολουθούν σωστά τις πλατφόρμες.

\--- /hint \---

\--- hint \---

Αυτά είναι τα τουβλάκια που χρειάζεσαι. Βεβαιώσου ότι θα τα προσθέσεις με τη σωστή σειρά.

![κινούμενη εικόνα μπάλας](images/ball_sprite.png)

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

Ο κώδικας των κλώνων της μπάλας θα πρέπει να έχει την εξής μορφή:

![κινούμενη εικόνα μπάλας](images/ball_sprite.png)

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

Τώρα πρόσθεσε μερικά τουβλάκια κώδικα για να μεταδώσεις (στείλεις) ένα μήνυμα, αν ο χαρακτήρας σου χτυπηθεί από μια μπάλα!

Πρόσθεσε αυτόν τον κώδικα στην εικόνα της μπάλας:

![κινούμενη εικόνα μπάλας](images/ball_sprite.png)

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

Τέλος, πρόσθεσε τουβλάκια κώδικα στην εικόνα του χαρακτήρα σου για να τον κάνεις να επιστρέψει στην αρχική του θέση, όταν λάβει ένα μήνυμα`χτυπήματος`:

![κινούμενη εικόνα pico](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Δοκίμασε τον κώδικά σου. Έλεγξε εάν ο χαρακτήρας μετακινείται πίσω στην αρχή μετά από το άγγιγμα μιας μπάλας.

\--- /task \---