## Quiz veloce

Rispondi alle tre domande. Alcuni suggerimenti ti aiuteranno a trovare la risposta corretta.

Dopo aver risposto a ciascuna domanda, fai clic su **Controlla la mia risposta**.

Divertiti!

--- question ---

---
legend: Domanda 1 di 3
---

Un progetto di negozio utilizza una variabile `total`{:class="block3variables"} per memorizzare il totale per ciascun cliente.

+ Un cliente aggiunge articoli per un totale di `50` e paga
+ Un nuovo cliente aggiunge articoli per un totale di `40` ma il totale di <0></0>{:class="block3variables"} viene ora visualizzato come <0>90</0> per il secondo cliente

Quale blocco dovresti aggiungere allo script di pagamento per far sì che il totale torni a `0` quando ogni cliente paga?

--- choices ---

- ( )
```blocks3
change [total v] by [0]
```

 --- feedback ---

Non esattamente, `totale`{:class="block3variables"} dovrebbe essere `0` dopo che un cliente paga, ma non è il blocco di modifica ``{:class="block3variables"} di cui hai bisogno.

 --- /feedback ---

- ( )
```blocks3
set [total v] to [40]
```

 --- feedback ---

 Non proprio, questo funzionerebbe per il secondo cliente, ma il `totale`{:class="block3variables"} sarebbe sbagliato per gli altri clienti.

 --- /feedback ---

- (x)

```blocks3
set [total v] to [0]
```

 --- feedback ---

Sì, è corretto. Devi impostare ``{:class="block3variables"} sul totale ``{:class="block3variables"} a `0` dopo che ogni cliente ha pagato.

 --- /feedback ---

- ( )

```blocks3
change [total v] by [-50]
```

 --- feedback ---

Questo potrebbe funzionare per questo esempio, ma cosa succederebbe se il primo cliente spendesse un importo diverso? La soluzione deve funzionare quando il cliente precedente spende importi diversi.

 --- /feedback ---

--- /choices ---

--- /question ---
