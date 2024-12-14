## Sfida

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Sono tante le funzionalità che potresti aggiungere per migliorare l'esperienza di acquisto dei tuoi clienti. Non è necessario aggiungere tutto. Aggiungi semplicemente i miglioramenti che ritieni importanti.
</div>
<div>
![](images/customer-count.png){:width="300px"}
</div>
</div>

--- task ---

Aggiungi altri articoli da vendere.

--- /task ---

--- task ---

Aggiungi musica ed effetti sonori.

--- /task ---

--- task ---

Dipingi il tuo scenario e altri costumi.

--- /task ---

--- task ---

Crea un'altra attività e consenti ai giocatori di visitarle entrambe.

--- /task ---

Ogni progetto di esempio nell'Introduzione [](https://scratch. mit. edu/studios/29662180) ha un collegamento "Guarda all'interno" che ti consente di aprire il progetto in Scratch e di guardare il codice per prendere spunto e vedere come funziona. Puoi "Guardare all'interno" dei progetti di esempio per vedere come funzionano.

Progetti di esempio: **Frutta fresca spaziale**: [Guarda all'interno](https://scratch.mit.edu/projects/528696418/editor){:target="_blank"}
**Magliette fantastiche**: [Guarda all'interno](https://scratch.mit.edu/projects/528697069/editor){:target="_blank"}
**Gelateria**: [Guarda all'interno](https://scratch.mit.edu/projects/525972748/editor){:target="_blank"}
**Distributore automatico**: [Guarda all'interno](https://scratch.mit.edu/projects/526051796/editor){:target="_blank"}

**Suggerimento:** se hai effettuato l'accesso a un account Scratch, puoi usare il **Backpack** per copiare script o sprite nel tuo progetto.

[[[scratch-backpack]]]

### Paga, chiacchierone!

Il cassiere (o la cassa automatica) potrebbe chiedere se il servizio è stato buono o se il cliente sta avendo una bella giornata.

--- task ---

Puoi aggiungere blocchi `chiedi`{:class="block3sensing"} allo script del tuo **venditore** `quando si clicca questo sprite`{:class="block3events"} e `dire`{:class="block3looks"} cose diverse a seconda della risposta del cliente.

--- collapse ---

---

title: Fai e rispondi alle domande

---

```blocks3
ask [Did you find everything you wanted today?] and wait
if <(answer) = [yes]> then
say [That's fantastic!] for [2] seconds
else
say [Maybe I should add more items to my shop] for [2] seconds
end
```

**Debug:** controlla di aver scritto correttamente le opzioni nel tuo codice e nella tua risposta. Va bene anche usare le lettere maiuscole, quindi "Yes" e "YES" corrisponderanno a "yes".

Aggiungi più domande per creare un chatbot o un personaggio non giocante con cui puoi parlare.

--- /collapse ---

--- /task ---

### Metti gli oggetti in un sacchetto

--- task ---

Il progetto "Magliette fantastiche" propone magliette che scivolano in una borsa.

--- collapse ---

---

title: Fai scivolare gli oggetti in un contenitore

---

Aggiungere uno sprite **Contenitore**. Potresti usare uno sprite esistente come **Gift** o **Take out**, oppure colorarne uno tuo con forme semplici.

Aggiungi uno script per far sì che il contenitore **** appaia sempre in primo piano:

```blocks3
when flag clicked
forever
go to [front v] layer
end
```

Quindi dovrai aggiungere del codice a ciascun **oggetto** in vendita per farli scivolare verso il contenitore quando vengono cliccati:

```blocks3
when this sprite clicked
+go to [front v] layer
+glide [1] secs to (Bag v) // use the name of your Container sprite
+hide
change [total v] by [12]
+go to x: [-180] y: [68] // start position
+show
```

Se non vuoi che il contenitore sia sempre presente, puoi aggiungere degli script per visualizzarlo e nasconderlo al momento giusto:

```blocks3
when I receive [next customer v]
hide // previous customer takes the bag
wait [1] seconds
show
```

**Test:** Prova il tuo progetto e assicurati che gli oggetti scivolino verso il contenitore e si nascondano.

**Debug:** Controlla attentamente i tuoi script e assicurati di aver aggiornato tutti i tuoi **sprite degli oggetti**. Se hai bisogno di un esempio funzionante, puoi dare un'occhiata a [Magliette fantastiche](https://scratch.mit.edu/projects/528697069/editor){:target="_blank"}.

--- /collapse ---

--- /task ---

###  Interrompi l'aggiunta di articoli quando il cliente è alla cassa

--- task ---

Aggiungi una variabile `shop`{:class="block3variables"} e usala per controllare quando possono essere aggiunti gli articoli.

--- collapse ---

---
title: Consenti gli acquisti solo quando il cliente non è alla cassa

---

Aggiungi una `variabile`{:class="block3variables"} chiamata `shop` per tutti gli sprite. Imposterai questo valore su **true** quando il cliente è nel negozio e su <0>false</0> quando è alla cassa.

Seleziona il tuo sprite **venditore**. Aggiorna lo script `quando si fa clic sulla bandiera`{:class="block3events"} per consentire lo shopping all'avvio del progetto:

```blocks3
+set [shop v] to [true]
```

Ora aggiungi un blocco per modificare il negozio ``{:class="block3variables"} in `falso` all'inizio dello script del tuo **venditore** `quando si clicca sprite`{:class="block3events"}:

```blocks3 
+set [shop v] to [false]
```

E un blocco per impostare la variabile `shop`{:class="block3variables"} di nuovo su `true` alla fine dello stesso script:

```blocks3 
+set [shop v] to [true]
```

Ora devi aggiornare gli oggetti che vendi per controllare la variabile del negozio ``{:class="block3variables"}:

```blocks3
when this sprite clicked
+if <(shop) = [true]> then
start sound (Coin v)
change [total v] by [10]
end
```
Dovrai fare questa operazione per ogni articolo che vendi nel tuo negozio.

**Test:** Fai clic sulla bandiera verde, quindi prova a fare acquisti. Verifica che sia ancora possibile aggiungere articoli e procedere al pagamento, ma che non sia possibile aggiungere articoli una volta avviato il pagamento.

**Debug:** Controlla il tuo codice molto attentamente. Se hai bisogno di vedere un esempio funzionante, puoi dare un'occhiata al progetto [Frutta fresca spaziale](https://scratch.mit.edu/projects/528696418/editor){:target="_blank"}.

--- /collapse ---

--- /task ---

--- task ---

### Potresti dare al cliente la possibilità di annullare l'acquisto.

--- collapse ---
---
title: Imposta le opzioni di pagamento e annullamento
---

`Chiedi`{:class="block3sensing"} `Vuoi pagare o annullare?`. Aggiungi un blocco `Se`{:class="block3control"} per `rispondi`{:class="block3sensing"} `=`{:class="block3operators"} `paga` e al suo interno inserisci i tuoi blocchi di pagamento esistenti.

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

Aggiungi un secondo blocco `Se`{:class="block3control"} per `rispondi`{:class="block3sensing"} `=`{:class="block3operators"} `annulla` e al suo interno aggiungi il codice per annullare l'ordine.

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

Dai un'occhiata al nostro ['Mercato dello shopping intergalattico'](https://scratch.mit.edu/studios/29662180){:target="_blank"} studio Scratch per vedere i progetti creati dai membri della community.

--- save ---
