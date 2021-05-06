## Buying things

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will let your customer(s) make purchases. You don't need to worry about money or other currency yet. Everything is free, yay! You'll get the chance to fix this in the next step if you want your business to make money.
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Open a [new Scratch project](http://rpf.io/scratch-new){:target="_blank"}. Scratch will open in another browser tab.

[[[working-offline]]]

--- /task ---

How will a new customer use your business? 

In the Tech Repair Cafe you can click on the **Technician** or on the desk to `broadcast`{:class="block3events"} a `next customer`{:class="block3events"} message. When the laptop receives the `next customer`{:class="block3events"} message it switches to a new `size`{:class="block3looks"} and `color`{:class="block3looks"} and `shows`{:class="block3looks"} to turn into the laptop for the next customer and the **Technician** greets the customer and `asks`{:class="block3sensing"} what the problem is.

In the Vending machine, you click on one of the numbers on the machine to select an item and this `broadcasts`{:class="block3events"} a message to say that a purchase has been started.

--- task ---

--- collapse ---

---
title: Click on a sprite to start serving a customer
---

Add a script to the sprite or sprites that can be clicked on to start a sale:

```blocks3
when this sprite clicked
broadcast (next customer v)
```

--- /collapse ---

--- /task ---

A new customer has arrived, how will your business serve them?

You might need to greet them and/or ask a question to get their order.

--- task ---

**Choose:** What happens when a new customer has arrived at your business?

Add a script to the sprite or sprites that need to do something to serve a customer. When you have all the information about the sale you can `broadcast`{:class="block3events"} a message to let other sprites know that a sale has been made.

--- collapse ---

---
title: Greet the customer
---

```blocks3
when I receive [next customer v]
say (join [Welcome to ] (name)) for [2] seconds
```

--- /collapse ---

--- collapse ---

---
title: Ask a question, check and use the answer
---

Check that a number is allowed:

```blocks3
ask [1, 2, or 3 scoops] and wait
if <(answer) < [4]> then
set [scoops v] to (answer)
say [Here you go] for [2] seconds
broadcast (sale v)
else
say [That's to many!] for [2] seconds
end
```

Turn numbers into words:

```blocks3
ask [How can I help?] and wait 
set [problem v] to [unknown]
if <(answer) = [1]> then
set [problem v] to [screen]
end
if <(answer) = [2]> then
set [problem v] to [keyboard]
end
if <(answer) = [3]> then
set [problem v] to [battery]
end
if <(problem) = [unknown]> then
say [Sorry, I can't fix everything!] for [2] seconds
else
say (join [I can fix the ] (problem)) for [2] seconds
broadcast (problem v) and wait
end
```

Do something different for different answers:

```blocks3
if <(answer) = [wand] ?> then 
say [Here you go] for [2] seconds
broadcast (wand v)
end
if <(answer) = [wand] ?> then 
say [Here you go] for [2] seconds
broadcast (wand v)
end
```

--- /collapse ---

--- /task ---

What happens when a sale takes place?

--- task ---

Add a script to sprites that need to do something when they recieve a message about a sale:

--- collapse ---

---
title: Move a sprite
---

```blocks3
when I receive [wand v]
go to x: [171] y: [28]
start sound (Magic Spell v)
```

You might also need to get the sprite back to its starting position:

```blocks3
when flag clicked
go to x: [-73] y: [9]
```

--- /collapse ---


--- collapse ---

---
title: Customize and show a sprite
---



--- /collapse ---




--- /task ---


--- task ---

Step content
Can use
**Test:**
**Choose:**
**Tip:**

--- /task ---

--- task ---

**Debug:** You might find some bugs in your project that you need to fix. Here are some common bugs.

--- collapse ---

---
title: 
---



--- /collapse ---

--- /task ---

--- save ---