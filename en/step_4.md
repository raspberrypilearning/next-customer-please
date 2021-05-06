## Currency

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you'll decide whether your customer needs money or some other form of currency to buy items. Currency could be money, gems, coins, gold, stars, or anything else that makes sense for your project. 

Can you think of games you play with currency?
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

**Choose:** Will your customer start with `0` currency or have some already. 

--- task ---

Create a `variable`{:class="block3variables"} named after your currency.

`When flag clicked`{:class="block3events"} set your currency `variable`{:class="block3variables"} to zero or another starting amount. 

```blocks3
when flag clicked
set [gold v] to [200]
```

--- /task ---

**Choose:** Will your customer have a set amount to spend or will they be able to earn more currency during the project?

--- task ---

To earn currency by collecting it, add a currency sprite to your project.

--- collapse ---

---
title: Find and collect currency
---

Add a `when flag clicked`{:class="block3events"} script to your currency sprite to `go to front layer`{:class="block3looks"} and `show`{:class="block3looks"}. 

```blocks3
when flag clicked
go to [front v] layer
show
```

Create a second script, add a `when this sprite clicked`{:class="block3events"} block and `change`{:class="block3variables"} your currency by `1`. 

To move your currency to a new place, add a `hide`{:class="block3looks"} block then `go to random postion`{:class="block3motion"} and `show`{:class="block3looks"}. Add a `go to front layer`{:class="block3looks"} block so the currency is always visible.

```blocks3
when this sprite clicked
change [stars v] by [1] 
start sound (collect v) // you could add a sound
hide
go to (random position v)
show
go to [front v] layer 
```

--- /collapse ---

--- /task ---

Sellers put prices on their items to earn currency. They only sell their items to customers that have enough currency to buy the item. 

--- task ---

If you only have one item sprite, or your items all cost the same amount, add code to your seller sprite so that they only sell to the customer when they have enough currency.

--- collapse ---

---
title: Check customer has enough currency
---

```blocks3
block // comment
```

--- /collapse ---

If you have more than one item sprite and they cost different amounts you will need to create a `variable`{:class="block3variables"} named `cost` to store the cost of the item the customer is currently buying.

--- /task ---


Reduce the amount when buying.
Check and add a message if the customer doesnt have enough. 


Or, you might add one sprite and change it for each customer like the Laptop or the ice-cream. Or may-be a go-cart that you get a short ride on, or a car to be washed.

--- task ---



--- /task ---

--- task ---

--- /task ---

--- task ---

--- /task ---

--- task ---

**Debug:** You might find some bugs in your project that you need to fix. Here are some common bugs.


// currency not reseting to right level or not starting at zero

--- collapse ---

---
title: 
---



--- /collapse ---

--- /task ---

--- save ---