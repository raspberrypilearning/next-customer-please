## Quick quiz

Answer the three questions. There are hints to guide you to the correct answer.

When you have answered each question, click on **Check my answer**.

Have fun!

--- question ---

---
legend: Pregunta 1 de 3
---

A shop project uses a `total`{:class="block3variables"} variable to store the total for each customer.

+ Un cliente agrega artículos que suman `50` y paga
+ Un nuevo cliente agrega elementos que suman `40`, pero el `total`{:class="block3variables"} ahora se muestra como `90` para el segundo cliente

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

Not quite, `total`{:class="block3variables"} should be `0` after a customer pays, but it is not the `change`{:class="block3variables"} block you need.

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
