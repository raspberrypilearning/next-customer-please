## Αγορές

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Το αντικείμενο **πωλητής** πρέπει:
- να ρωτήσει αν ο πελάτης είναι έτοιμος να πληρώσει για τα προϊόντα
- να λάβει την πληρωμή
- να ετοιμαστεί για τον επόμενο πελάτη
</div>
<div>
![](images/step4-image.png){:width="300px"}
</div>
</div>

Όταν ολοκληρώσει την επιλογή των προϊόντων, ο πελάτης θα κάνει κλικ στο αντικείμενο του **πωλητή** για να πληρώσει.

--- task ---

 Πες στον πελάτη πόσο θα κοστίσουν τα προϊόντα του.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds 
```

--- /task ---

--- task ---

Πρόσθεσε έναν ήχο πληρωμής στο αντικείμενο του **πωλητή** σου, ώστε ο πελάτης να γνωρίζει ότι η πληρωμή πραγματοποιείται.

![Το εικονίδιο προσθήκης ήχου](images/add-sound.png)

[[[scratch3-add-sound]]]

Πρόσθεσε το μπλοκ `παίξε τον ήχο μέχρι τέλους`{:class="block3sound"} στο script σου.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
+ play sound [machine v] until done 
```

--- /task ---

--- task ---

Ολοκλήρωσε την πώληση. Όρισε το `σύνολο`{:class="block3variables"} πάλι σε `0` μετά την πληρωμή, `πες`{:class="block3looks"} αντίο και `μετάδωσε`{:class="block3control"} `επόμενος πελάτης`{: class="block3control"}.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
play sound [machine v] until done 
+ set [total v] to (0)
+ say (join [Thanks for shopping at ] (name)) for (2) seconds
+ broadcast (next customer v)
```

--- /task ---

--- task ---

Ίσως θέλεις να δώσεις στον πελάτη την επιλογή να ακυρώσει τις αγορές του.

--- collapse ---
---
title: Ρύθμιση επιλογών πληρωμής και ακύρωσης
---

`Ρώτησε`{:class="block3sensing"} `Θέλετε να πληρώσετε ή να ακυρώσετε;`. Πρόσθεσε ένα μπλοκ `Εάν`{:class="block3control"} για την `απάντηση`{:class="block3sensing"} `=`{:class="block3operators"} `πληρωμή` και βάλε μέσα σε αυτό τα υπάρχοντα μπλοκ πληρωμών.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
+ ask [Would you like to pay or cancel?] and wait
+ if {(answer) = [pay]} then
play sound [machine v] until done 
set [total v] to (0)
say (join [Thanks for shopping at ] (name)) for (2) seconds
broadcast [next customer v]
end
```

Πρόσθεσε ένα δεύτερο μπλοκ `Εάν`{:class="block3control"} για την `απάντηση`{:class="block3sensing"} `=`{:class="block3operators"} `ακύρωση` και πρόσθεσε μέσα σε αυτό τον κώδικα για να ακυρώσεις την παραγγελία.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
ask [Would you like to pay or cancel?] and wait
if {(answer) = [pay]} then
play sound [machine v] until done 
set [total v] to (0)
say (join [Thanks for shopping at ] (name)) for (2) seconds
broadcast [next customer v]
end
+ if {(answer) = [cancel]} then
set [total v] to (0)
say [Ok. No problem] for (2) seconds
broadcast [next customer v]
end
```

--- /collapse ---

--- /task ---

--- task ---

Για να βεβαιωθείς ότι ο πελάτης σου έχει προϊόντα στο καλάθι του προτού πληρώσει, μπορείς να εισαγάγεις ένα μπλοκ `εάν...αλλιώς`{:class="block3control"}.

--- collapse ---
---
title: Έλεγξε το συνολικό ποσό
---

`Εάν`{:class="block3control"} `σύνολο`{:class="block3variables"} `>`{:class="block3operators"} `0` τότε τοποθέτησε το υπάρχον script σου.

`Αλλιώς`{:class="block3control"} `πες`{:class="block3looks"} ένα χρήσιμο μήνυμα.

```blocks3
when this sprite clicked
+ if <(total) > [0]>then
say (join [That will be ] (total)) for (2) seconds
ask [Would you like to pay or cancel?] and wait
if {(answer) = [pay]} then
play sound [machine v] until done 
set [total v] to (0)
say (join [Thanks for shopping at ] (name)) for (2) seconds
broadcast [next customer v]
end
if {(answer) = [cancel]} then
set [total v] to (0)
say [Ok. No problem] for (2) seconds
broadcast [next customer v]
end
else
say [Click on the items you'd like] for (2) seconds
end
```

--- /collapse ---

--- /task ---

--- task ---

**Δοκιμή:** Δοκίμασε το έργο σου και βεβαιώσου:
- Ο πελάτης μπορεί να πληρώσει με τα σωστά ηχητικά εφέ
- Το `σύνολο`{:class="block3variables"} επανέρχεται σε `0` αφού ένας πελάτης πληρώσει ή ακυρώσει.

--- /task ---


--- task ---

**Εντοπισμός σφαλμάτων:** Ενδέχεται να βρεις κάποια σφάλματα στο έργο σου που πρέπει να διορθώσεις.

Εδώ είναι μερικά συνηθισμένα σφάλματα:

--- collapse ---
---
title: Ο πωλητής δεν κάνει τίποτα όταν κάνω κλικ πάνω του
---

Έχεις πολλά αντικείμενα στο έργο σου. Βεβαιώσου ότι το script `όταν γίνει κλικ σε αυτό το αντικείμενο`{: class = "block3events"} βρίσκεται στο αντικείμενό σου **πωλητής**.

**Συμβουλή:** Εάν το έχεις προσθέσει σε λάθος αντικείμενο, μπορείς να σύρεις τον κώδικα στο αντικείμενο **πωλητής** και μετά να το διαγράψεις από το άλλο αντικείμενο.

--- /collapse ---

--- collapse ---
---
title: Ο πωλητής λέει "σύνολο" όχι το συνολικό ποσό
---

Βεβαιώσου ότι το μπλοκ `πες`{:class="block3looks"} έχει το μπλοκ μεταβλητής `σύνολο`{:class="block3variables"} και όχι τη λέξη `σύνολο`.

```blocks3
 when this sprite clicked
 say {join [That will be ](total)} for (2) seconds 
 ```

--- /collapse ---

--- collapse ---
---
title: Οι λέξεις στα μπλοκ "πες" συγχωνεύονται μεταξύ τους
---

Όταν `ενώνεις`{:class="block3operators"} δύο κείμενα μαζί, πρέπει να προσθέτεις ένα κενό στο τέλος του πρώτου σου κειμένου ή στην αρχή του δεύτερου κειμένου.

Αυτά έχουν ένα κενό στο τέλος του πρώτου μέρους της ένωσης:

```blocks3
say {join [That will be ](total)} for (2) seconds

say {join [Thanks for shopping at ](name)} for (2) seconds
```

--- /collapse ---

--- collapse ---
---
title: Το σύνολο δεν επανέρχεται στην αρχική τιμή μετά την πώληση
---

Έλεγξε ότι έχεις χρησιμοποιήσει:

```blocks3
set [total v] to (0)
```

**όχι**:

```blocks3
change [total v] by (0)
```

--- /collapse ---

--- collapse ---
---
title: Ο πωλητής δεν ανταποκρίνεται
---

Βεβαιώσου ότι ο `τελεστής`{:class="block3operators"} στη συνθήκη `εάν`{:class="block3control"} είναι το σύμβολο μεγαλύτερο από `>`{:class="block3operators"}.

```blocks3
if <(total) > [0]> then
```

--- /collapse ---

**Συμβουλή:** Σύγκρινε τον κώδικά σου με τα παραδείγματα κώδικα. Υπάρχουν διαφορές που δεν θα έπρεπε να υπάρχουν;

--- /task ---

--- save ---
