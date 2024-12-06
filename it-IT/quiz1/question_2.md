
--- question ---

---
legend: Domanda 2 di 3
---

In un negozio, il venditore <0></0> ha questo codice nello script di pagamento:

```blocks3
ask [How are you today?] and wait
if <(answer) = [good]> then
say [That's fantastic!] for [2] seconds
else
say [Sorry to hear that.] for [2] seconds
end
```

Quando il codice viene eseguito, l'utente digita la risposta "ottimo". Cosa dirà lo sprite **venditore** ?

![Una casella "chiedi" con la parola "fantastico" digitata.](images/quiz2.png)

--- choices ---

- (x) Il <0>Venditore</0> dirà <1>Mi dispiace sentirlo.</1>

  --- feedback ---

  Sì. Gli esseri umani sanno che "grande" ha lo stesso significato di "bene", ma il simbolo "=" controlla se le lettere sono uguali.

  La condizione **** `risposta`{:class="block3sensing"} = `buona` è 'falsa' quindi il blocco `dire`{:class="block3looks"} nella parte `altrimenti`{:class="block3control"} verrà eseguito.

  --- /feedback ---

- ( ) Il venditore **** dirà `È fantastico!`

  --- feedback ---

No, solo la risposta esatta `bene` farà sì che il venditore **** dica `Fantastico!`. Osserva nuovamente il codice per vedere quale messaggio dirà il venditore **** per tutte le risposte che non sono `buone`.

**Suggerimento:** 'Bene' o 'BENE' corrisponderebbero a 'bene'.

  --- /feedback ---

- ( ) Il venditore **** non dirà nulla.

  --- feedback ---

No, il venditore **** dirà sempre qualcosa. Osserva attentamente il codice per vedere quale sarà il messaggio.

  --- /feedback ---

- ( ) Il venditore **** dirà `ottimo`.

  --- feedback ---

No, il **cliente** ha digitato la risposta "ottimo", ma il **venditore** non dice la risposta. Osserva attentamente il codice per vedere quale sarà il messaggio.

  --- /feedback ---

--- /choices ---

--- /question ---
