## Défi

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Tu peux ajouter de nombreuses fonctionnalités pour améliorer l'expérience d'achat de tes client·e·s. Tu n'as pas besoin de tout ajouter. Ajoute simplement les améliorations que tu juges importantes.
</div>
<div>
![](images/customer-count.png){:width="300px"}
</div>
</div>

--- task ---

Ajoute plus d'articles à vendre.

--- /task ---

--- task ---

Ajoute plus d'effets graphiques et sonores.

--- /task ---

--- task ---

Peins tes propres décors et autres costumes.

--- /task ---

--- task ---

Crée un autre commerce et autorise les joueurs à les visiter tous les deux.

--- /task ---

Chaque exemple de projet dans l'[introduction](.) a un lien « voir à l'intérieur » pour que tu puisses ouvrir le projet dans Scratch et regarder le code pour avoir des idées et voir comment ils fonctionnent. Tu peux « voir à l'intérieur » des exemples de projets pour voir comment ils fonctionnent.

Exemples de projets : 
**Fruits frais de l'espace** : [voir à l'intérieur](https://scratch.mit.edu/projects/707260567/editor){:target="_blank"}
**T-shirts cool**: [voir à l'intérieur](https://scratch.mit.edu/projects/707260366/editor){:target="_blank"}
**Glacier** : [voir à l'intérieur](https://scratch.mit.edu/projects/707260702/editor){:target="_blank"}
**Distributeur automatique** : [voir à l'intérieur](https://scratch.mit.edu/projects/707260825/editor){:target="_blank"}

**Astuce :** si tu es connecté à un compte Scratch, tu peux utiliser le **Sac à dos** pour copier des scripts ou des sprites dans ton projet.

[[[scratch-backpack]]]

### Caisse bavarde !

Ton caissier ou caissière (ou la machine) pourrait demander si le service était bon, ou si le/la client·e passe une bonne journée.

--- task ---

Ajoute des blocs `demander`{:class="block3sensing"} au script de ton/ta **vendeur·euse** `quand ce sprite est cliqué`{:class="block3events"} et `dire`{:class="block3looks"} différentes choses en fonction de la réponse du client ou de la cliente.

--- collapse ---

---
title: Poser des questions et y répondre
---

```blocks3
ask [Avez-vous trouvé tout ce que vous vouliez aujourd'hui ?] and wait
if <(answer) = [oui]> then
say [C'est fantastique !] for [2] seconds
else
say [Peut-être que je devrais ajouter plus d'articles à ma boutique] for [2] seconds
end
```

**Débogage :** vérifie que tu as correctement orthographié les options dans ton code et dans ta réponse. Ce n'est pas grave si tu utilises des majuscules, donc « Oui » et « OUI » correspondront à « oui ».

Ajoute plusieurs questions pour créer un chatbot ou un personnage non-joueur avec qui tu peux parler.

--- /collapse ---

--- /task ---

### Mettre les articles dans un sac

--- task ---

Le projet T-shirts cool propose des t-shirts qui se glissent facilement dans un sac.

--- collapse ---

---
title: Faire glisser les articles dans un conteneur
---

Ajoute un sprite **Conteneur**. Tu peux utiliser un sprite existant comme le sprite **Cadeau** ou **À emporter**, ou peindre le tien avec des formes simples.

Ajoute un script pour que le **Conteneur** apparaisse toujours à l'avant plan :

```blocks3
when flag clicked
forever
go to [avant v] layer
end
```

Ensuite, tu devras ajouter un code à chaque **article** en vente pour les faire glisser vers le conteneur lorsqu'ils sont cliqués :

```blocks3
when this sprite clicked
+go to [avant v] layer
+glide [1] secs to (Bag v) // utiliser le nom du sprite du conteneur
+hide
change [total v] by [12]
+go to x: [-180] y: [68] // position de départ
+show
```

Si tu ne veux pas que le conteneur soit présent en permanence, tu peux ajouter des scripts pour qu'il s'affiche et se cache au bon moment :

```blocks3
when I receive [client suivant v]
hide // le client précédent prend le sac
wait [1] seconds
show
```

**Test :** essaie ton projet et assure-toi que les articles glissent vers le conteneur et se cachent.

**Debogage :** vérfie iattentivementment tes scripts et assure-toi d'avoir mis à jour tous tes sprites **Article**. Tu peux consulter le projet [T-shirts cool](https://scratch.mit.edu/projects/707260366/editor){:target="_blank"} si tu as besoin de voir un exemple fonctionnel.

--- /collapse ---

--- /task ---

###  Arrêter d'ajouter des articles lorsque le/la client·e est à la caisse

--- task ---

Ajoute une variable `boutique`{:class="block3variables"} et utilise-la pour contrôler quand des articles peuvent être ajoutés.

--- collapse ---

---
title: Autoriser les achats lorsque le/la client·e n'est pas à la caisse
---

Ajoute une `variable`{:class="block3variables"} appelée `boutique` pour tous les sprites. Tu la mettras sur `vrai` lorsque le/la client·e est dans la boutique et `faux` lorsqu'il/elle est à la caisse.

Sélectionne ton sprite **vendeur·euse**. Mets à jour le script `quand le drapeau est cliqué`{:class="block3events"} pour autoriser les achats au démarrage de ton projet :

```blocks3
+set [boutique v] to [true]
```

Ajoute maintenant un bloc pour changer la `boutique`{:class="block3variables"} sur `faux` au début du script de ton/ta **vendeur·euse** `quand ce sprite est cliqué`{:class="block3events"} :

```blocks3 
+set [boutique v] to [false]
```

Et un bloc pour remettre la variable `boutique`{:class="block3variables"} sur `vrai` à la fin du même script :

```blocks3 
+set [boutique v] to [true]
```

Tu dois maintenant mettre à jour les articles que tu vends pour vérifier la variable `boutique`{:class="block3variables"} :

```blocks3
when this sprite clicked
+if <(boutique) = [true]> then
start sound (Coin v)
change [total v] by [10]
end
```
Tu devras le faire pour chaque article que tu vends dans ta boutique.

**Test :** clique sur le drapeau vert puis essaie de faire des achats. Vérifie que tu peux toujours ajouter des articles et payer, mais tu ne peux pas ajouter d'articles une fois que tu as commencé à payer.

**Débogage :** si tu obtiens une erreur, vérifie ton code très attentivement. Tu peux consulter le projet [Fruits de l'espace](https://scratch.mit.edu/projects/528696418/editor){:target="_blank"} si tu as besoin de voir un exemple fonctionnel.

--- /collapse ---

--- /task ---

--- task ---

### Donne au client ou à la cliente la possibilité d'annuler ses achats.

--- collapse ---

---
title: Configurer les options de paiement et d'annulation
---

`Demander`{:class="block3sensing"} `Voulez-vous payer ou annuler ?`. Ajoute un bloc `si`{:class="block3control"} pour `réponse`{:class="block3sensing"} `=`{:class="block3operators"} `payer` et mets-y tes blocs de paiement existants.

```blocks3
when this sprite clicked
say (join [Cela fera ] (total)) for (2) seconds
+ ask [Voulez-vous payer ou annuler ?] and wait
+ if {(answer) = [payer]} then
play sound [machine v] until done 
set [total v] to (0)
say (join [Merci d'avoir acheté chez ] (nom)) for (2) seconds
broadcast [client suivant v]
end
```

Ajoute un deuxième bloc `si`{:class="block3control"} pour `réponse`{:class="block3sensing"} `=`{:class="block3operators"} `annuler` et ajoute à l'intérieur le code pour annuler la commande.

```blocks3
when this sprite clicked
say (join [Cela fera ] (total)) for (2) seconds
ask [Voulez-vous payer ou annuler ?] and wait
if {(answer) = [payer]} then
play sound [machine v] until done 
set [total v] to (0)
say (join [Merci d'avoir acheté chez ] (nom)) for (2) seconds
broadcast [client suivant v]
end
+ if {(answer) = [annuler]} then
set [total v] to (0)
say [D'accord. Pas de problème] for (2) seconds
broadcast [client suivant v]
end
```

--- /collapse ---

--- /task ---

Jette un œil à notre studio Scratch [« Intergalactic shopping market »](https://scratch.mit.edu/studios/707260567){:target="_blank"} pour voir les projets créés par les membres de la communauté.

--- save ---
