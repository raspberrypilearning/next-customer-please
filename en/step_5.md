## Additional features

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
There are lots of features you could add to improve your customers' shopping experience. You don't need to add everything. Just add improvements that you think are important.

</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

--- task ---
Do you want something else to happen when you add an item? 

The Cool Shirts project has the shirts gliding into a bag.

--- collapse ---

---
title: Make items glide into a container
---

Add a container sprite. You could use an existing sprite like the 'Gift' or 'Take out' or paint your own with simple shapes.

Add a script to make the **Container** always appear at the front:

```blocks3
when flag clicked
forever
go to [front v] layer
end
```

Then you'll need to add code to each **Item** you have for sale to make them glide to the container when they are clicked:

```blocks3
when this sprite clicked
if <(shop) = [true]> then
+go to [front v] layer
+glide [1] secs to (Bag v)
+hide
change [total v] by [12]
+go to x: [-180] y: [68] // start position
+show
end
```

If you don't want the container there all the time you can add scripts to make it show and hide at the right time:

```blocks3
when I receive [next customer v]
hide // previous customer takes the bag
wait [1] seconds
show

when I receive [cancel v]
hide
```

**Test:** Try your project and make sure items glide to the container and hide.

**Debug:** Check your scripts carefully and make sure you have updated all of your **Item** sprites. You can look at [Cool Shirts](https://scratch.mit.edu/projects/528697069/editor){:target="_blank"} if you need to see a working example.

--- /collapse ---

--- /task ---

--- task ---

Have you noticed that your customer can add items after they have started to check out?

If you want to fix this you can add a `shop`{:class="block3variables"} variable and use it to control when items can be added.

--- collapse ---

---
title: Only allow buying when the customer isn't at the checkout 
---

Add a `variable`{:class="block3variables"} called `shop` for all sprites. You will set this to `true` when the customer is in the shop and `false` when they are at the checkout.

Select your **Seller** sprite. Update the `when flag clicked`{:class="block3events"} script to allow shopping when your project starts:

```blocks3
+set [shop v] to [true]
```

Now add a blocks to change the `shop`{:class="block3variables"} to `false` at the beginning of your **Seller**'s `when this sprite clicked`{:class="block3events"} script:

```blocks3 
+set [shop v] to [false]
```

And a block to set the `shop`{:class="block3variables"} variable back to `true` at the end of the same script:

```blocks3 
+set [shop v] to [true]
```

Now you need to update the items you sell to check the `shop`{:class="block3variables"} variable:

```blocks3
when this sprite clicked
+if <(shop) = [true]> then
start sound (Coin v)
change [total v] by [10]
end
```

You will need to do this for every item you sell in your shop.

**Test:** Try shopping and check that you can still add items and checkout, but you can't add items once you have started checking out. 

**Debug:** Check your code really carefully. You can look at the [Space fruit](https://scratch.mit.edu/projects/528696418/editor){:target="_blank"} project if you need to see a working example.

--- /collapse ---


--- collapse ---

---
title: Customize and show a sprite
---



--- /collapse ---




--- /task ---

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