## Additional features

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
There are lots of features you could add to improve your customers' shopping experience. You don't need to add everything. Just add improvements that you think are important.

</div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>


You can 'See Inside' the example projects if you want to see how they work. If you are logged in to a Scratch account then you can use the **Backpack** to copy scripts or sprites to your project and then change them to work with your project.

Example projects:
**Fresh Space Fruit**: [See inside](https://scratch.mit.edu/projects/528696418/editor){:target="_blank"}
**Cool Shirts**: [See inside](https://scratch.mit.edu/projects/528697069/editor){:target="_blank"}
**Ice cream shop**: [See inside](https://scratch.mit.edu/projects/525972748/editor){:target="_blank"}
**Vending machine**: [See inside](https://scratch.mit.edu/projects/526051796/editor){:target="_blank"}

[[[scratch-backpack]]]

--- task ---

Do you think your checkout person (or machine!) should ask more questions? 

You can add `ask`{:class="block3sensing"} blocks to your **Seller**'s `when this sprite clicked`{:class="block3events"} script and `say`{:class="block3looks"} different things depending on the customer's response.

You could ask whether the service was good, or if they're having a nice day. Or something specific to your shop, like "What are you going to cook?".

--- collapse ---

---

title: Ask and respond to questions

---

```blocks3
ask [Did you find everything you wanted today?] and wait
if <(answer) = [yes]> then
say [That's fantastic!] for [2] seconds
else
say [Maybe I should add more items to my shop] for [2] seconds
end
```

**Debug:** Check that you have spelled the options correctly in your code and in your answer. It's okay if you use capital letters, so "Yes" and "YES" will match "yes". 

Add multiple questions to create a chatbot or non-player character that you can talk to.

--- /collapse ---

--- /task ---

Do you want something else to happen when you add an item? 

--- task ---

The Cool Shirts project has the shirts gliding into a bag.

--- collapse ---

---
title: Make items glide into a container

---

Add a **Container** sprite. You could use an existing sprite like the 'Gift' or 'Take out' or paint your own with simple shapes.

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
+go to [front v] layer
+glide [1] secs to (Bag v) // use the name of your Container sprite
+hide
change [total v] by [12]
+go to x: [-180] y: [68] // start position
+show
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

The ice cream van shows the ice cream as the customer chooses their options.

--- collapse ---

---
title: Customize and show a sprite

---

Each item needs to `broadcast`{:class="block3events"} in its `when this sprite clicked`{:class="block3events"} script:

```blocks3
+broadcast (1 scoop v)
```

Then the sprite you want to show or change needs to respond to that message:

```blocks3
when I receive [1 scoop v]
play sound (Chomp v) until done
switch costume to (1 scoop v)
```

You may also want to change or hide the sprite for a new customer:

```blocks3
when I receive [next customer v]
switch costume to (cone v)
```

If you have multiple items then you will need to add more messages and scripts to to receive them.

--- /collapse ---

--- /task ---

Have you noticed that your customer can add items after they have started to check out?

--- task ---

If you want to stop the customer adding items when they are at the checkout can add a `shop`{:class="block3variables"} variable and use it to control when items can be added.

--- collapse ---

---
title: Only allow buying when the customer isn't at the checkout 

---

Add a `variable`{:class="block3variables"} called `shop` for all sprites. You will set this to `true` when the customer is in the shop and `false` when they are at the checkout.

Select your **Seller** sprite. Update the `when flag clicked`{:class="block3events"} script to allow shopping when your project starts:

```blocks3
+set [shop v] to [true]
```

Now add a block to change the `shop`{:class="block3variables"} to `false` at the beginning of your **Seller**'s `when this sprite clicked`{:class="block3events"} script:

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

**Test:** Click the green flag then try shopping and check that you can still add items and checkout, but you can't add items once you have started checking out. 

**Debug:** Check your code really carefully. You can look at the [Space fruit](https://scratch.mit.edu/projects/528696418/editor){:target="_blank"} project if you need to see a working example.

--- /collapse ---

--- /task ---

--- save ---

