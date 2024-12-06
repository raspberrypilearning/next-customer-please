## Your shop

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
What is your shop idea? Gallai fod yn rhywbeth realistig, fel rhywbeth o lyfr neu ffilm rwyt ti'n ei hoffi, neu'n rhywbeth hollol wirion.
</div>
<div>
![](images/step2-image.png){:width="300px"}
</div>
</div>

--- task ---

Agora [brosiect Scratch newydd](http://rpf.io/scratch-new){:target="_blank"} a tharo golwg ar yr amrywiaeth o gorluniau a chefnlenni y galli di eu defnyddio. Spend some time thinking about your shop idea.

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
+ Silff neu gwpwrdd llyfrau i roi eitemau arno - fe allech chi Beintio hwn ar y gefnlen

--- /task ---

--- task ---

Ychwanega gorlun i gynrychioli'r gwerthwr.

You could choose:
+ A person or non-player character such as a shopkeeper, farmer, or librarian
+ A machine such as a vending machine, jukebox, or cash register

![](images/choose-sprite-icon.png)

--- /task ---

### Welcome your first customer.

--- task ---

Clicia ar dy gorlun **gwerthwr** ac ychwanega floc `darlledu`{:class="block3control"}. Create a new message called `next customer`.

```blocks3
when flag clicked
+ broadcast (next customer v)
```

--- /task ---

--- task ---

Crea sgript newydd ar gyfer dy gorlun **gwerthwr** i `ddweud`{:class="block3looks"} `Cwsmer nesaf plîs` pan fyddan nhw'n derbyn y `darllediad`{:class="block3control"} `cwsmer nesaf`{:class= "block3control"}.

```blocks3
when I receive [next customer v] 
say [Next customer please!] for (2) seconds
```

--- /task ---

--- cadw ---
