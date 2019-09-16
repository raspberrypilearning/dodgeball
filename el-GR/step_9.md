## Challenge: περισσότερα εμπόδια

If you think your game is still too easy, you can add more obstacles to it. The obstacles can be anything you like! Here are some ideas:

+ A dangerous butterfly
+ Platforms that appear and disappear
+ Falling tennis balls that must be avoided

![screenshot](images/dodge-obstacles.png)

Θα μπορούσατε ακόμη να σχεδιάσετε ένα άλλο σκηνικό για να δημιουργήσετε το επόμενο επίπεδο. Στη συνέχεια, προσθέστε τον κώδικα έτσι ώστε, όταν ο χαρακτήρας σας φτάσει στην πράσινη πόρτα, το παιχνίδι μεταβαίνει στο νέο φόντο:

![χαρακτηρας περπάτηματος pico](images/pico_walking_sprite.png)

```blocks3
    if <touching color [#00FF00]?> then
        switch backdrop to (next backdrop v)
        go to x: (-210) y: (-120)
        wait (1) seconds
    end
```