## Purchases

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">

The **seller** sprite needs to:
- ask if the customer is ready to pay for the items
- take payment
- get ready for the next customer
</div>
<div>
![](images/step4-image.png){:width="300px"}
</div>
</div>

When they have finished choosing items, the customer will click on the **seller** sprite to pay.

--- task ---

 Tell the customer how much their items will cost.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds 
```

--- /task ---

--- task ---

Add a payment sound to your **seller** sprite so the customer knows that payment is taking place.

![The add a sound icon](images/add-sound.png)

[[[scratch3-add-sound]]]

Add the `play sound until done`{:class="block3sound"} block to your script.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
+ play sound [machine v] until done 
```

--- /task ---

--- task ---

Finish the sale. Set `total`{:class="block3variables"} back to `0` after payment, `say`{:class="block3looks"} goodbye and `broadcast`{:class="block3control"} `next customer`{:class="block3control"}.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
play sound [machine v] until done 
+ set [total v] to (0)
+ say (join [Thanks for shopping at ] (name)) for (2) seconds
+ broadcast (next customer v)
```

--- /task ---

--- task ---

**Test:** Test your project and make sure:
- The customer can check out with the correct sound effects
- The `total`{:class="block3variables"} gets set back to `0` after a customer pays or cancels.

--- /task ---


--- task ---

**Debug:** You might find some bugs in your project that you need to fix. 

Here are some common bugs:

--- collapse ---
---
title: The seller doesn't do anything when I click on them
---

You have quite a lot of sprites in your project. Make sure the `when this sprite clicked`{:class="block3events"} script is on your **seller** sprite. 

**Tip:** If you have added it to the wrong sprite, you can drag the code to the **seller** sprite, then delete it from the other sprite.

--- /collapse ---

--- collapse ---
---
title: The words in the say blocks merge together
---

When you `join`{:class="block3operators"} two pieces together, you need to add a space at the end of your first piece of text or at the beginning of your second piece of text. 

These have a space at the end of the first part of the join:

```blocks3
say {join [That will be ](total)} for (2) seconds

say {join [Thanks for shopping at ](name)} for (2) seconds
```

--- /collapse ---

--- collapse ---
---
title: The total doesn't reset after a sale
---

Check that you have used:

```blocks3
set [total v] to (0)
```

**not**: 

```blocks3
change [total v] by (0)
```

--- /collapse ---

--- collapse ---
---
title: The seller isn't responding
---

Make sure the `operator`{:class="block3operators"} in the `if`{:class="block3control"} condition is the greater than symbol `>`{:class="block3operators"}.

```blocks3
if <(total) > [0]> then
```

--- /collapse ---

**Tip:** Compare your code with the code examples. Are there any differences that shouldn't be there?

--- /task ---

--- save ---
