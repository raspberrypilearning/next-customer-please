## Твій магазин

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Придумай ідею магазину. Це може бути щось реалістичне, щось із книги чи фільму, який тобі подобається, або щось абсолютно безглузде.
</div>
<div>
![](images/step2-image.png){:width="300px"}
</div>
</div>

--- task ---

Відкрий [новий проєкт Скретч](http://rpf.io/scratch-new){:target="_blank"} і переглянь варіанти спрайтів і тла, що можна використати. Витрать трохи часу на обмірковування ідеї свого магазину.

--- /task ---

--- task ---

Натисни **Обрати тло** або намалюй своє власне тло.

![](images/choose-backdrop-icon.png)

+ Тло з бібліотеки Скретч чи просте одноколірне тло

--- /task ---

--- task ---

Натисни **Обрати спрайт** та додай або намалюй додаткові спрайти для сцени.

![](images/choose-sprite-icon.png)

--- /task ---

--- task ---

Додай більше декорацій.
+ Стіл, прилавок чи вікно, з якого можна продавати
+ Полиця чи книжкова шафа, на якій можна розмістити товар — це можна намалювати на тлі.

--- /task ---

--- task ---

Додай спрайт, який буде продавцем або продавчинею.

Ти можеш вибрати:
+ Особу чи неігрового персонажа, як-от власницю крамниці, фермера чи бібліотекарку
+ Апарат, як-от торговельний автомат, музичний автомат чи касовий апарат

![](images/choose-sprite-icon.png)

--- /task ---

### Привітай свого першого покупця.

--- task ---

Click on your **seller** sprite and add a `broadcast`{:class="block3events"} block. Створи нове повідомлення під назвою `наступний покупець`.

```blocks3
when flag clicked
+ broadcast (новий покупець v)
```

--- /task ---

--- task ---

Create a new script for your **seller** sprite to `say`{:class="block3looks"} `Next customer please` when they receive the `broadcast`{:class="block3events"} `next customer`{:class="block3events"}.

```blocks3
when I receive [наступний покупець v] 
say [Наступний покупець!] for (2) seconds
```

--- /task ---

--- save ---
