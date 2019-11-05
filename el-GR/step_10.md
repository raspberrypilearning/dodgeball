## Πρόκληση: βελτιωμένη βαρύτητα

Υπάρχει ένα ακόμη μικρό σφάλμα στο παιχνίδι σας: η βαρύτητα δεν τραβάει το αντικείμενο χαρακτήρα προς τα κάτω αν ** οποιοδήποτε ** ένα τμήμα του αντικείμενου αγγίζει μια μπλε πλατφόρμα. Έτσι, ακόμη και αν το κεφάλι των χαρακτήρας αγγίζει μια πλατφόρμα, ο χαρακτήρας δεν πέφτει! Μπορείτε να δοκιμάσετε τον εαυτό σας: να κάνετε τον χαρακτήρα σας να ανέβει κατά το μεγαλύτερο μέρος του επάνω σε μια σκάλα και στη συνέχεια να μετακινήσετε τον χαρακτήρα πλάγια κάτω από μια πλατφόρμα:

![screenshot](images/dodge-gravity-bug.png)

Για να διορθώσετε το σφάλμα, πρέπει πρώτα να δώσετε στο αντικείμενο σας ένα νέο παντελόνι που έχει διαφορετικό χρώμα (σε ** όλα ** ενδημασία).

![screenshot](images/dodge-trousers.png)

Στη συνέχεια αντικαταστήστε αυτό το μπλοκ:

```blocks3
    εάν < touching color [#0000FF]; >
```

με αυτό το μπλοκ:

```blocks3
    < χρώμα [# 00FF00] αγγίζει [# 0000FF]; >
```

Για να βεβαιωθείτε ότι έχετε διορθώσει το σφάλμα, δοκιμάστε το παιχνίδι αφού έχετε κάνει αυτές τις αλλαγές!