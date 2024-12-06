## Your shop

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
What is your shop idea? Це може бути щось реалістичне, щось із книги чи фільму, який тобі подобається, або щось абсолютно безглузде.
</div>
<div>
![](images/step2-image.png){:width="300px"}
</div>
</div>

--- task ---

Відкрий [новий проєкт Скретч](http://rpf.io/scratch-new){:target="_blank"} і переглянь варіанти спрайтів і тла, що можна використати. Spend some time thinking about your shop idea.

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
+ Полиця чи книжкова шафа, на якій можна розмістити товар — це можна намалювати на тлі.

--- /task ---

--- task ---

Додай спрайт, який буде продавцем або продавчинею.

You could choose:
+ A person or non-player character such as a shopkeeper, farmer, or librarian
+ A machine such as a vending machine, jukebox, or cash register

![](images/choose-sprite-icon.png)

--- /task ---

### Welcome your first customer.

--- task ---

Натисни на спрайт**продавця** і додай блок `оповістити`{:class="block3control"}. Create a new message called `next customer`.

```blocks3
when flag clicked
+ broadcast (next customer v)
```

--- /task ---

--- task ---

Створи новий скрипт для спрайту **продавця**, щоб він `говорив`{:class="block3looks"} `Прошу, наступний покупець!`, коли отримає `повідомлення`{:class="block3control"} `наступний клієнт`{:class="block3control"}.

```blocks3
when I receive [next customer v] 
say [Next customer please!] for (2) seconds
```

--- /task ---

--- save ---
