## Your shop

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
What is your shop idea? Het zou iets realistisch kunnen zijn, iets uit een boek of film die je leuk vindt, of iets heel geks.
</div>
<div>
![](images/step2-image.png){:width="300px"}
</div>
</div>

--- task ---

Open een [nieuw Scratch project](http://rpf.io/scratch-new){:target="_blank"} en kijk naar de sprites en achtergronden die je kunt gebruiken. Spend some time thinking about your shop idea.

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
+ Een plank of boekenkast om producten op te zetten; je zou dit op de achtergrond kunnen tekenen

--- /task ---

--- task ---

Voeg een sprite toe voor de verkoper.

You could choose:
+ A person or non-player character such as a shopkeeper, farmer, or librarian
+ A machine such as a vending machine, jukebox, or cash register

![](images/choose-sprite-icon.png)

--- /task ---

### Welcome your first customer.

--- task ---

Klik op je **verkoper** sprite en voeg een `uitzending`{:class="block3control"} blok toe. Create a new message called `next customer`.

```blocks3
when flag clicked
+ broadcast (next customer v)
```

--- /task ---

--- task ---

Maak een nieuw script voor je **verkoper** sprite om `te zeggen`{:class="block3looks"} `volgende klant asljeblieft` wanneer deze het `bericht`{:class="block3control"} `volgende klant`{:class="block3control"} ontvangt.

```blocks3
when I receive [next customer v] 
say [Next customer please!] for (2) seconds
```

--- /task ---

--- save ---
