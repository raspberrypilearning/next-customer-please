
--- question ---

---
legend: Question 2 sur 3
---

Dans une boutique, le **vendeur** a ce code dans le script de paiement :

```blocks3
ask [How are you today?] and wait
if <(answer) = [good]> then
say [That's fantastic!] for [2] seconds
else
say [Sorry to hear that.] for [2] seconds
end
```

Lorsque le code s'exécute, l'utilisateur tape la réponse « super ». Que dira le sprite **vendeur** ?

![Une case "demander" avec le mot "super" tapé.](images/quiz2.png)

--- choices ---

- (x) Le **vendeur** dira `Je suis désolé.`

  --- feedback ---

  Oui. Les humains savent que « super » signifie la même chose que « bien », mais le « = » vérifie si les lettres sont les mêmes.

  La **condition** `réponse`{:class="block3sensing"} = `bien` est « faux » donc le bloc `dire`{:class="block3looks"} dans la partie `sinon`{:class="block3control"} s'exécutera.

  --- /feedback ---

- ( ) Le **vendeur** dira `C'est fantastique !`

  --- feedback ---

Non, seule la réponse exacte `bien` fera dire au **vendeur** `C'est fantastique !`. Regarde à nouveau le code pour voir quel message le **vendeur** dira pour toutes les réponses qui ne sont pas `bien`.

**Astuce :** « Bien » ou « BIEN » correspondrait à « bien ».

  --- /feedback ---

- ( ) Le **vendeur** ne dira rien.

  --- feedback ---

Non, le **vendeur** dira toujours quelque chose. Regarde attentivement le code pour voir quel sera le message.

  --- /feedback ---

- ( ) Le **vendeur** dira `super`.

  --- feedback ---

Non, le **client** a tapé la réponse « super » mais le **vendeur** ne dit pas la réponse. Regarde attentivement le code pour voir quel sera le message.

  --- /feedback ---

--- /choices ---

--- /question ---
