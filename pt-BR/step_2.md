## Your shop

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
What is your shop idea? Pode ser algo realista, algo de um livro ou filme que você goste, ou algo completamente bobo.
</div>
<div>
![](images/step2-image.png){:width="300px"}
</div>
</div>

--- task ---

Abra um [novo projeto Scratch](http://rpf.io/scratch-new){: target = "_ blank"} e observe a gama de atores e cenários que você pode usar. Spend some time thinking about your shop idea.

--- /task ---

--- task ---

**Choose a Backdrop** or paint your own backdrop.

![](images/choose-backdrop-icon.png)

+ Um cenário da biblioteca Scratch ou um cenário de cor básica

--- /task ---

--- task ---

**Choose a Sprite** and add or paint extra scenery sprites.

![](images/choose-sprite-icon.png)

--- /task ---

--- task ---

Add more scenery.
+ Uma mesa, balcão ou janela para as vendas
+ Uma prateleira ou estante para colocar itens – você pode pintar no cenário

--- /task ---

--- task ---

Adicione um sprite para representar o vendedor.

Você pode escolher:
+ Uma pessoa ou personagem não jogável, como lojista, fazendeiro ou bibliotecário
+ Uma máquina como uma máquina de venda automática, jukebox ou caixa registradora

![](images/choose-sprite-icon.png)

--- /task ---

### Welcome your first customer.

--- task ---

Click on your **seller** sprite and add a `broadcast`{:class="block3events"} block. Create a new message called `next customer`.

```blocks3
when flag clicked
+ broadcast (next customer v)
```

--- /task ---

--- task ---

Create a new script for your **seller** sprite to `say`{:class="block3looks"} `Next customer please` when they receive the `broadcast`{:class="block3events"} `next customer`{:class="block3events"}.

```blocks3
when I receive [next customer v] 
say [Next customer please!] for (2) seconds
```

--- /task ---

--- save ---
