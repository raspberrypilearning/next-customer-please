## Your shop

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
What is your shop idea? Podría ser algo realista, algo de un libro o una película que te guste, o algo completamente absurdo.
</div>
<div>
![](images/step2-image.png){:width="300px"}
</div>
</div>

--- task ---

Abre un [nuevo proyecto de Scratch](http://rpf.io/scratch-new){:target="_blank"} y observa la variedad de objetos y fondos que puedes usar. Spend some time thinking about your shop idea.

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
+ Un estante o una librería para poner artículos; podrías pintar esto en el fondo

--- /task ---

--- task ---

Agrega un objeto para representar al vendedor.

You could choose:
+ A person or non-player character such as a shopkeeper, farmer, or librarian
+ A machine such as a vending machine, jukebox, or cash register

![](images/choose-sprite-icon.png)

--- /task ---

### Welcome your first customer.

--- task ---

Haz clic en tu objeto **vendedor** y agrega un bloque `broadcast`{:class="block3control"}. Create a new message called `next customer`.

```blocks3
when flag clicked
+ broadcast (next customer v)
```

--- /task ---

--- task ---

Crea un nuevo script para tu objeto **vendedor** para `decir`{:class="block3looks"} `Siguiente cliente, por favor` cuando reciba la `transmisión`{:class="block3control"} `siguiente cliente`{:class= "bloque3control"}.

```blocks3
when I receive [next customer v] 
say [Next customer please!] for (2) seconds
```

--- /task ---

--- save ---
