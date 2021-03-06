## Και τώρα;

Μπράβο, χρησιμοποίησες τις δεξιότητές σου για να σχεδιάσεις και να δημιουργήσεις μια εφαρμογή καταστήματος!

Έχεις χρησιμοποιήσει τα μπλοκ `Συμβάντα`{:class="block3events"}, `Έλεγχος`{:class="block3control"}, `Αισθητήρες`{:class="block3sensing"}, `Τελεστές`{:class="block3operators"}, `Μεταβλητές`{:class="block3motion"}, `Όψεις`{:class="block3looks"} και `Ήχος`{:class="block3sound"}!

Τώρα, ήρθε η ώρα να εξετάσεις τις νέες γνώσεις- ο αναστοχασμός είναι σημαντικό μέρος της μάθησης, επειδή βοηθά στη δημιουργία νέων συνδέσεων στον εγκέφαλό σου.

Απάντησε στις τρεις ερωτήσεις παρακάτω για να διαπιστώσεις τι έμαθες.

Μετά από κάθε ερώτηση, πάτησε Υποβολή. Θα οδηγηθείς στη σωστή απάντηση. Μπορείς να επαναλάβεις αυτήν τη δραστηριότητα όσες φορές θέλεις.

Καλή διασκέδαση!

--- question ---

---
legend: Ερώτηση 1 από 3
---

Ένα έργο καταστήματος χρησιμοποιεί μια μεταβλητή `σύνολο`{:class="block3variables"} για την αποθήκευση του συνόλου για κάθε πελάτη.

+ Ένας πελάτης προσθέτει αντικείμενα που συνολικά κοστίζουν `50` και πληρώνει
+ Ένας νέος πελάτης προσθέτει αντικείμενα που συνολικά κοστίζουν `40`, αλλά το `σύνολο`{:class="block3variables"} εμφανίζεται τώρα ως `90` για τον δεύτερο πελάτη

Ποιο μπλοκ θα πρέπει να προσθέσεις στο script πληρωμής για να επιστρέψει το σύνολο στο `0` όταν πληρώνει κάθε πελάτης;

```blocks3
when this sprite clicked
ask [Θέλεις να πληρώσεις ή να ακυρώσεις;] and wait
if {(answer) = [πληρωμή]} then
say (join [Αυτό θα είναι ] (σύνολο)) for (2) seconds
play sound [coin v] until done 
say (join [Ευχαριστώ για τις αγορές σου στο ] (όνομα)) for (2) seconds
broadcast [επόμενος πελάτης v]
end
```

--- choices ---

- ( )
```blocks3
change [σύνολο v] by [0]
```

 --- feedback ---

Όχι ακριβώς, το `σύνολο`{:class="block3variables"} θα πρέπει να είναι `0` μετά την πληρωμή ενός πελάτη, αλλά δεν είναι το μπλοκ `άλλαξε`{:class="block3variables"} που χρειάζεσαι.

 --- /feedback ---

- ( )
```blocks3
set [σύνολο v] to [40]
```

 --- feedback ---

 Όχι ακριβώς, αυτό θα λειτουργούσε για τον δεύτερο πελάτη, αλλά το `σύνολο`{:class="block3variables"} θα ήταν λάθος για άλλους πελάτες.

 --- /feedback ---

- (x)

```blocks3
set [σύνολο v] to [0]
```

 --- feedback ---

Ναι, αυτό είναι σωστό. Πρέπει να `ορίσεις`{:class="block3variables"} το `σύνολο`{:class="block3variables"} σε `0` μετά την πληρωμή κάθε πελάτη.

 --- /feedback ---

- ( )

```blocks3
change [σύνολο v] by [-50]
```

 --- feedback ---

Αυτό θα λειτουργούσε σε αυτό το παράδειγμα, αλλά τι θα γινόταν αν ο πρώτος πελάτης ξόδευε διαφορετικό ποσό; Η λύση σου πρέπει να λειτουργεί όταν ο προηγούμενος πελάτης ξοδεύει διαφορετικά ποσά.

 --- /feedback ---

--- /choices ---

--- /question ---
