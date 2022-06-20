## Réflexion

Bravo, tu as utilisé tes compétences pour concevoir et créer une application de boutique !

Tu as utilisé les blocs `Événements`{:class="block3events"}, `Contrôle`{:class="block3control"}, `Capteurs`{:class="block3sensing"}, `Opérateurs`{:class="block3operators"}, `Mouvement`{:class="block3motion"}, `Apparence`{:class="block3looks"}, et `Son`{:class="block3sound"} !

Maintenant, il est temps de réfléchir - la réflexion est une partie importante de l'apprentissage, car elle aide à établir de nouvelles connexions dans ton cerveau.

Réponds aux trois questions ci-dessous pour réfléchir sur ce que tu as appris.

Après chaque question, appuie sur Soumettre. Tu seras guidé vers la bonne réponse. Tu peux faire cette activité autant de fois que tu le souhaites.

Amuse-toi bien !

--- question ---

---
legend: Question 1 sur 3
---

Un projet de boutique utilise une variable `total`{:class="block3variables"} pour stocker le total pour chaque client.

+ Un client ajoute des articles pour un total de `50` et paie
+ Un nouveau client ajoute des articles pour un total de `40`, mais le `total`{:class="block3variables"} est maintenant de `90` pour le deuxième client

Quel bloc dois-tu ajouter au script de paiement pour que le total revienne à `0` lorsque chaque client paie ?

```blocks3
when this sprite clicked
ask [Voulez-vous payer ou annuler ?] and wait
if {(answer) = [payer]} then
say (join [Cela fera ] (total)) for (2) seconds
play sound [coin v] until done 
say (join [Merci d'avoir acheté chez ] (nom)) for (2) seconds
broadcast [client suivant v]
end
```

--- choices ---

- ( )
```blocks3
change [total v] by [0]
```

 --- feedback ---

Pas tout à fait, `total`{:class="block3variables"} devrait être `0` après le paiement d'un client, mais ce n'est pas le bloc `ajouter`{:class="block3variables"} dont tu as besoin.

 --- /feedback ---

- ( )
```blocks3
set [total v] to [40]
```

 --- feedback ---

 Pas tout à fait, cela fonctionnerait pour le deuxième client mais le `total`{:class="block3variables"} serait faux pour les autres clients.

 --- /feedback ---

- (x)

```blocks3
set [total v] to [0]
```

 --- feedback ---

Oui c'est correct. Tu dois `mettre`{:class="block3variables"} le `total`{:class="block3variables"} sur `0` après le paiement de chaque client.

 --- /feedback ---

- ( )

```blocks3
change [total v] by [-50]
```

 --- feedback ---

Cela fonctionnerait pour cet exemple, mais que se passerait-il si le premier client dépensait un montant différent ? Ta solution doit fonctionner lorsque le client précédent dépense des montants différents.

 --- /feedback ---

--- /choices ---

--- /question ---
