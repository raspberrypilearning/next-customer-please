## Szybki quiz

Odpowiedz na trzy pytania. Podpowiedzi naprowadzą Cię na właściwą odpowiedź.

When you have answered each question, click on **Check my answer**.

Miłej zabawy!

--- question ---

---
legend: Question 1 of 3
---

A shop project uses a `total`{:class="block3variables"} variable to store the total for each customer.

+ A customer adds items that total `50` and pays
+ A new customer adds items that total `40` but the `total`{:class="block3variables"} is now showing as `90` for the second customer

Which block would you need to add to the payment script to make the total go back to `0` when each customer pays?

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

Tak, to jest poprawna odpowiedź. Musisz ustawić `set`{:class="block3variables"} zmienną `total`{:class="block3variables"} na `0` po dokonaniu płatności przez każdego klienta.

 --- /feedback ---

- ( )

```blocks3
change [total v] by [-50]
```

 --- feedback ---

To zadziałałoby w tym przykładzie, ale co by było, gdyby pierwszy klient wydał inną kwotę? Twoje rozwiązanie musi działać, gdy poprzedni klient wydawał różne kwoty.

 --- /feedback ---

--- /choices ---

--- /question ---
