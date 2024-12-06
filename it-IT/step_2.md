## Your shop

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
What is your shop idea? Potrebbe essere qualcosa di realistico, qualcosa tratto da un libro o da un film che ti piace, o qualcosa di completamente sciocco.
</div>
<div>
![](images/step2-image.png){:width="300px"}
</div>
</div>

--- task ---

Apri un [nuovo progetto Scratch](http://rpf.io/scratch-new){:target="_blank"} e guarda la gamma di sprite e sfondi che puoi utilizzare. Spend some time thinking about your shop idea.

--- /task ---

--- task ---

**Choose a Backdrop** or paint your own backdrop.

![](images/choose-backdrop-icon.png)

+ A backdrop from the Scratch library, or a plain coloured backdrop

--- /task ---

--- task ---

**Choose a Sprite** and add or paint extra scenery sprites.

![](images/choose-sprite-icon.png)

--- /task ---

--- task ---

Add more scenery.
+ A desk, counter, or window to sell from
+ Uno scaffale o una libreria su cui appoggiare gli oggetti - potresti dipingerlo sullo sfondo

--- /task ---

--- task ---

Aggiungi uno sprite per rappresentare il venditore.

You could choose:
+ A person or non-player character such as a shopkeeper, farmer, or librarian
+ A machine such as a vending machine, jukebox, or cash register

![](images/choose-sprite-icon.png)

--- /task ---

### Welcome your first customer.

--- task ---

Fai clic sul tuo sprite venditore **** e aggiungi un blocco di trasmissione ``{:class="block3control"}. Create a new message called `next customer`.

```blocks3
when flag clicked
+ broadcast (next customer v)
```

--- /task ---

--- task ---

Crea un nuovo script per il tuo sprite **venditore** per `dire`{:class="block3looks"} `Prossimo cliente per favore` quando riceve la `trasmissione`{:class="block3control"} `prossimo cliente`{:class="block3control"}.

```blocks3
when I receive [next customer v] 
say [Next customer please!] for (2) seconds
```

--- /task ---

--- save ---
