
--- question ---

---
legend: Question 2 sur 3
---

Dans une boutique, le/la **vendeur·euse** a ce code dans le script de paiement :

```blocks3
ask [How are you today?] and wait
if <(answer) = [good]> then
say [That's fantastic!] for [2] seconds
else
say [Sorry to hear that.] for [2] seconds
end
```

Lorsque le code s'exécute, l'utilisateur tape la réponse « super ». Que dira le sprite **vendeur·euse** ?

![Une case "demander" avec le mot "super" tapé.](images/quiz2.png)

--- choices ---

- (x) Le/la **vendeur·euse** dira `Je suis désolé·e.`

  --- feedback ---

  Oui. Les humains savent que « super » signifie la même chose que « bien », mais le « = » vérifie si les lettres sont les mêmes.

  La **condition** `réponse`{:class="block3sensing"} = `bien` est « faux » donc le bloc `dire`{:class="block3looks"} dans la partie `sinon`{:class="block3control"} s'exécutera.

  --- /feedback ---

- ( ) Le/la **vendeur·euse** dira `C'est fantastique !`

  --- feedback ---

Non, seule la réponse exacte `bien` fera dire au **vendeur·euse** `C'est fantastique !`. Regarde à nouveau le code pour voir quel message le/la **vendeur·euse** dira pour toutes les réponses qui ne sont pas `bien`.

**Astuce :** « Bien » ou « BIEN » correspondrait à « bien ».

  --- /feedback ---

- ( ) Le/la **vendeur·euse** ne dira rien.

  --- feedback ---

Non, le/la **vendeur·euse** dira toujours quelque chose. Regarde attentivement le code pour voir quel sera le message.

  --- /feedback ---

- ( ) Le/la **vendeur·euse** dira `super`.

  --- feedback ---

Non, le/la **client·e** a tapé la réponse « super » mais le/la **vendeur·euse** ne dit pas la réponse. Regarde attentivement le code pour voir quel sera le message.

  --- /feedback ---

--- /choices ---

--- /question ---
