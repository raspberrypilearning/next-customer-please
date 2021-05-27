## Reflection

Well done, you have learned a lot! Now it's time to reflect - reflecting is an important part of learning because it helps make new connections in your brain.

Answer the three questions below to reflect on what you've learned.

After each question, press submit. You will be guided towards the correct answer. You can do this activity as many times as you want to.

Have fun!

--- question ---

---
legend: Question 1 of 3
---

A shop project uses a `total`{:class="block3variables"} variable to store the total for each customer.

+ A customer adds items totalling `50` and pays.
+ A new customer adds items totalling `40` but the `total`{:class="block3variables"} is now showing as `90` for the second customer.

Which block would you need to add to the payment script to make the total go back to `0` when each customer pays?

```blocks3
when this sprite clicked
ask [Would you like to pay or cancel?] and wait
if {(answer) = [pay]} then
say (join [That will be ] (total)) for (2) seconds
play sound [coin v] until done 
say (join [Thanks for shopping at ] (name)) for (2) seconds
broadcast [next customer v]
end
```

--- choices ---

- ( ) 
```blocks3
change [total v] by [0]
```

 --- feedback ---

Not quite, `total`{:class="block3variables"} should be `0` after a customer pays but it is not the `change`{:class="block3variables"} block you need.

 --- /feedback ---

- ( ) 
```blocks3
set [total v] to [40]
```

 --- feedback --- 

 Not quite, this would work for the second customer but the `total`{:class="block3variables"} would be wrong for other customers.

 --- /feedback ---

- (x)

```blocks3
set [total v] to [0]
```

 --- feedback ---

Yes, that's correct. You need to `set`{:class="block3variables"} the `total`{:class="block3variables"} to `0` after each customer pays.

 --- /feedback ---

- ( ) 

```blocks3
change [total v] by [-50]
```

 --- feedback ---

That would work for this example, but what if the first customer spent a different amount? Your solution needs to work when the previous customer spends different amounts. 

 --- /feedback ---

--- /choices ---

--- /question ---