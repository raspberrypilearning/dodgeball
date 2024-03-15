## Κίνηση χαρακτήρων

Ξεκίνα δημιουργώντας έναν χαρακτήρα που μπορεί να κινηθεί αριστερά και δεξιά και μπορεί να ανέβει πάνω σε σκάλες.

\--- task \---

Άνοιξε το αρχικό έργο Scratch 'Dodgeball'.

**Online:** open the starter project at [rpf.io/dodgeball-on](https://rpf.io/dodgeball-on){:target="_blank"}.

Αν έχεις λογαριασμό Scratch μπορείς να δημιουργήσεις ένα αντίγραφο, κάνοντας κλικ στο κουμπί **Ανάμειξη**.

**Offline:** download the starter project from [rpf.io/p/en/dodgeball-get](https://rpf.io/p/en/dodgeball-get) and then open it using the offline editor.

\--- /task \---

Το έργο περιέχει ένα σκηνικό με πλατφόρμες:

![φόντο έργου 'Dodgeball'](images/dodge-background.png)

\--- task \---

Επέλεξε μία νέα κινούμενη εικόνα για τον χαρακτήρα που θα ελέγχει ο παίκτης και πρόσθεσέ την στο έργο σου. Καλύτερα να επιλέξεις μία κινούμενη εικόνα με πολλές ενδυμασίες για να μπορείς να την κάνεις να μοιάζει σαν να περπατάει.

![διάλεξε μία κινούμενη εικόνα](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Πρόσθεσε τουβλάκια κώδικα στην εικόνα του χαρακτήρα σου, για να μπορεί ο παίκτης να χρησιμοποιήσει τα βελάκια για να τον μετακινήσει. Όταν ο παίκτης πατήσει το δεξιό βέλος, ο χαρακτήρας θα πρέπει να κοιτάξει δεξιά, να κάνει μερικά βήματα και να αλλάξει την επόμενη ενδυμασία:

![κινούμενη εικόνα pico](images/pico_walking_sprite.png)

```blocks3
when flag clicked
forever
    if <key (right arrow v) pressed; > then
        point in direction (90 v)
        move (3) steps
        next costume
    end
end
```

\--- /task \---

\--- task \---

Εάν η εικόνα σου δεν χωράει, προσάρμοσε το μέγεθός της.

![όρισε το μέγεθος της εικόνας για να χωράει](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

Δοκίμασε το χαρακτήρα σου κάνοντας κλικ στη σημαία και στη συνέχεια κρατώντας πατημένο το δεξί πλήκτρο βέλους. Ο χαρακτήρας σου κινείται προς τα δεξιά; Ο χαρακτήρας σου μοιάζει σα να περπατάει;

![στιγμιότυπο οθόνης](images/dodge-walking.png)

\--- /task \---

\--- task \---

Πρόσθεσε τουβλάκια κώδικα στο `forever` {: class = "block3control"} της εικόνας του χαρακτήρα, για να περπατήσει αριστερά αν πατηθεί το αριστερό πλήκτρο βέλους.

\--- hints \---

\--- hint \---

Για να μετακινηθεί ο χαρακτήρας σου προς τα αριστερά, θα πρέπει να προσθέσεις άλλο ένα `if` {: class = "block3control"} τουβλάκι μέσα στο `forever` {: class = "block3control"}. Σε αυτό το νέο `if` {block: block3control} τουβλάκι, πρόσθεσε τον κώδικα για να κάνεις την εικόνα του χαρακτήρα σου να `μετακινηθεί` {: class = "block3motion"} προς τα αριστερά.

\--- /hint \---

\--- hint \---

Αντέγραψε τον κώδικα που δημιούργησες για να κάνεις τον χαρακτήρα να περπατήσει προς τα δεξιά. Στη συνέχεια, όρισε το `key pressed` {: class = "block3sensing"} στο `left arrow` {: class = "block3sensing"}, και αλλάξτε το `direction` {: class = "block3motion"} σε `-90`.

```blocks3
if <key (right arrow v) pressed; > then
    point in direction (90 v)
    move (3) steps
    next costume
end
```

\--- /hint \---

\--- hint \---

Ο κώδικάς σου θα πρέπει τώρα να μοιάζει κάπως έτσι:

![κινούμενη εικόνα pico](images/pico_walking_sprite.png)

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

Δοκίμασε το νέο σου κώδικα για να βεβαιωθείς ότι λειτουργεί. Γυρίζει ο χαρακτήρας σου ανάποδα, όταν περπατάει προς τα αριστερά;

![στιγμιότυπο οθόνης](images/dodge-upside-down.png)

Αν ναι, τότε μπορείς να το διορθώσεις κάνοντας κλικ στην **κατεύθυνση** της εικόνας του χαρακτήρα σου και στη συνέχεια κάνοντας κλικ στο αριστερό-δεξί βέλος.

![στιγμιότυπο οθόνης](images/dodge-left-right-annotated.png)

Ή αν προτιμάς, μπορείς επίσης να διορθώσεις το πρόβλημα, προσθέτοντας αυτό το τουβλάκι στην αρχή του κώδικα του χαρακτήρα σου:

```blocks3
set rotation style [left-right v]
```

\--- /task \---

\--- task \---

Για να ανεβείς σε μια ροζ σκάλα, ο χαρακτήρας σου θα πρέπει να μετακινείται μερικά βήματα προς τα πάνω στο Επίπεδο, κάθε φορά που πατιέται το βέλος προς τα πάνω **και** ο χαρακτήρας αγγίζει το σωστό χρώμα.

Πρόσθεσε κώδικα στο βρόχο του χαρακτήρα σου `για πάντα`{:class="block3control"} ώστε να `αλλάξει`{:class="block3motion"} την (κάθετη) θέση `y` του χαρακτήρα `εάν`{:class="block3control"} το `πάνω βέλος είναι πατημένο`{:class="block3sensing"} και ο χαρακτήρας `αγγίζει το ροζ χρώμα`{:class="block3sensing"}.

![κινούμενη εικόνα pico](images/pico_walking_sprite.png)

```blocks3
    if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
        change y by (4)
    end
```

\--- /task \---

\--- task \---

Δοκίμασε τον κώδικά σου. Μπορείς να κάνεις το χαρακτήρα να ανέβει τις ροζ σκάλες και να φτάσει στο τέλος του επιπέδου;

![στιγμιότυπο οθόνης](images/dodge-test-character.png)

\--- /task \---