## Paying

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you'll add code to the **Seller** sprite to ask if the customer is ready to pay for the items, take payment, then get ready for the next customer.
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

When they have finished choosing items the customer will click on the **Seller** sprite to pay.

--- task ---

 Tell the customer how much their items will cost.

 ```blocks3
 when this sprite clicked
 say {join [That will be ](total)} for (2) seconds 
 ```

--- /task ---

--- task ---

Add a payment sound to your **Seller** sprite so the customer knows that payment is taking place. 

![The add a sound icon](images/add-sound.png)

[[[scratch3-add-sound]]]

Add the `play sound until done`{:class="block3sound"} block to your script.

 ```blocks3
 when this sprite clicked
 say {join [That will be ](total)} for (2) seconds
 + play sound [coin v] until done  
 ```

--- /task ---

--- task ---

Finish the sale. Set `total`{:class="block3variables"} back to `0` after payment, `say`{:class="block3looks"} goodbye and `broadcast`{:class="block3control"} `next customer`.

 ```blocks3
 when this sprite clicked
 say {join [That will be ](total)} for (2) seconds
 play sound [coin v] until done  
 + set [total v] to (0)
 + say {join [Thanks for shopping at ](name)} for (2) seconds
 + broadcast [next customer v]
 ```

--- /task ---

--- task ---

You might want to give the customer the option to cancel their shopping.

--- collapse ---

---
title: Set up pay and cancel options 
---

`Ask`{:class="block3sensing"} `Would you like to pay or cancel?`. Add an `If`{:class="block3control"} block for `answer`{:class="block3sensing"} `=`{:class="block3operators"} `pay` and inside it put your existing payment blocks.

```blocks3
 when this sprite clicked
 say {join [That will be ](total)} for (2) seconds
 + ask [Would you like to pay or cancel?] and wait
 + if {(answer) = [pay]} then
 play sound [coin v] until done  
 set [total v] to (0)
 say {join [Thanks for shopping at ](name)} for (2) seconds
 broadcast [next customer v]
 end
```

Add a second `If`{:class="block3control"} block for `answer`{:class="block3sensing"} `=`{:class="block3operators"} `cancel` and inside it add code to cancel the order.

```blocks3
 when this sprite clicked
 say {join [That will be ](total)} for (2) seconds
 ask [Would you like to pay or cancel?] and wait
 if {(answer) = [pay]} then
 play sound [coin v] until done  
 set [total v] to (0)
 say {join [Thanks for shopping at ](name)} for (2) seconds
 broadcast [next customer v]
 end
 + if {(answer) = [cancel]} then
 set [total v] to (0)
 say [Ok. No problem] for (2) seconds
 broadcast [next customer v]
 end
```

--- /collapse ---

--- /task ---

--- task ---

To make sure your customer has items in their basket before paying, you can insert an `if...else` block.

--- collapse ---

---
title: Check total amount
---

`If`{:class="block3control"} `total`{:class="block3variables"} `>`{:class="block3operators"} `0` then insert your existing script.

`Else`{:class="block3control"} `say`{:class="block3looks"} a helpful message.

```blocks3
 when this sprite clicked
+ if <(total) > [0]>then
 say {join [That will be ](total)} for (2) seconds
 ask [Would you like to pay or cancel?] and wait
 if {(answer) = [pay]} then
 play sound [coin v] until done  
 set [total v] to (0)
 say {join [Thanks for shopping at ](name)} for (2) seconds
 broadcast [next customer v]
 if {(answer) = [cancel]} then
 set [total v] to (0)
 say [Ok. No problem] for (2) seconds
 broadcast [next customer v]
 end
 end
 else 
 say [Choose some items] for (2) seconds
 end
```

--- /collapse ---

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