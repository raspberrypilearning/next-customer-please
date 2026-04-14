## Achats

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">

Le sprite **vendeur·euse** doit :
- demander si le client est prêt à payer les articles
- accepter le paiement
- se préparer pour le/la client·e suivant·e
</div>
<div>
![](images/step4-image.png){:width="300px"}
</div>
</div>

Lorsqu'il/elle aura fini de choisir les articles, le/la client·e cliquera sur le sprite **vendeur·euse** pour payer.

--- task ---

 Dis au clientou à la cliente combien coûteront ses articles.

```blocks3
when this sprite clicked
say (join [Cela fera ] (total)) for (2) seconds 
```

--- /task ---

--- task ---

Ajoute un son de paiement à ton sprite **vendeur·euse** pour que le/la client·e sache que le paiement est en cours.

![L'icône ajouter un son](images/add-sound.png)

[[[scratch3-add-sound]]]

Ajoute le bloc `jouer le son jusqu'au bout`{:class="block3sound"} à ton script.

```blocks3
when this sprite clicked
say (join [Cela fera ] (total)) for (2) seconds
+ play sound [machine v] until done 
```

--- /task ---

--- task ---

Termine la vente. Mets `total`{:class="block3variables"} à `0` après le paiement, `dire`{:class="block3looks"} au revoir et `envoyer à tous`{:class="block3control"} `client suivant`{:class="block3control"}.

```blocks3
when this sprite clicked
say (join [Cela fera ] (total)) for (2) seconds
play sound [machine v] until done 
+ set [total v] to (0)
+ say (join [Merci d'avoir acheté chez ] (nom)) for (2) seconds
+ broadcast (client suivant v)
```

--- /task ---

--- task ---

**Test :** teste ton projet et assure-toi que :
- Le/la client·e peut acheter avec les effets sonores corrects
- Le `total`{:class="block3variables"} est remis à `0` après qu'un·e client·e a payé ou annulé.

--- /task ---


--- task ---

**Débogage :** Il est possible que tu trouves des bogues dans ton projet que tu dois corriger.

Voici quelques bogues assez courants :

--- collapse ---
---
title: Le/la vendeur·euse ne fait rien lorsque je clique dessus
---

Tu as pas mal de sprites dans ton projet. Assure-toi que le script `quand ce sprite est cliqué`{:class="block3events"} est sur ton sprite **vendeur·euse**.

**Astuce :** si tu l'as ajouté au mauvais sprite, tu peux faire glisser le code vers le sprite **vendeur·euse**, puis le supprimer de l'autre sprite.

--- /collapse ---

--- collapse ---
---
title: Les mots contenus dans les blocs « dire » fusionnent
---

Lorsque tu `regroupes`{:class="block3operators"} deux morceaux ensemble, tu dois ajouter un espace à la fin de ton premier morceau de texte ou au début du deuxième.

Ceux-ci ont un espace à la fin de la première partie de la jointure :

```blocks3
say {join [Cela fera ](total)} for (2) seconds

say {join [Merci d'avoir acheté chez ](nom)} for (2) seconds
```

--- /collapse ---

--- collapse ---
---
title: Le total ne se réinitialise pas après une vente
---

Vérifie que tu as utilisé :

```blocks3
set [total v] to (0)
```

**et pas** :

```blocks3
change [total v] by (0)
```

--- /collapse ---

--- collapse ---
---
title: Le/la vendeur·euse ne répond pas
---

Assure-toi que l'`opérateur`{:class="block3operators"} dans la condition `si`{:class="block3control"} est supérieur au symbole `>`{:class="block3operators"}.

```blocks3
if <(total) > [0]> then
```

--- /collapse ---

**Astuce :** compare ton code avec les exemples de code. Y a-t-il des différences qui ne devraient pas exister ?

--- /task ---

--- save ---
