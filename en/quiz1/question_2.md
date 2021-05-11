
--- question ---

---
legend: Question 2 of 3
---

In a shop, the **Seller** has this code in the checkout script:

```blocks3
ask [How are you today?] and wait
if <(answer) = [good]> then
say [That's fantastic!] for [2] seconds
else
say [Sorry to hear that.] for [2] seconds
end
```

When the code runs, the user types the answer 'great'. What will the **Seller** sprite say?

![An 'ask' box with the word 'great' typed in.](images/quiz2.png)

--- choices ---

- (x) The **Seller** will say `Sorry to hear that.`

  --- feedback ---

  Yes. Humans know that 'great' means the same as 'good', but the '=' checks whether the letters are the same. 

  The **condition** `answer`{:class="block3sensing"} = `good` is 'false' so the `say`{:class="block3looks"} block in the `else`{:class="block3control"} part will run.

  --- /feedback ---

- ( ) The **Seller** will say `That's fantastic!`

  --- feedback ---
  
No, only the exact answer `good` will make the **Seller** say `That's fantastic!`. Look at the code again to see what message the **Seller** say for all answers that are not `good`.

**Tip:** 'Good' or 'GOOD' would match 'good'.

  --- /feedback ---

- ( ) The **Seller** won't say anything

  --- feedback ---
  
No, the **Seller** will always say something. Look carefully at the code to see what the message will be.

  --- /feedback ---

- ( ) The **Seller** will say `great`

  --- feedback ---

No, the **Customer** typed the answer 'great' but the **Seller** does not say the answer. Look carefully at the code to see what the message will be.

  --- /feedback ---

--- /choices ---

--- /question ---
