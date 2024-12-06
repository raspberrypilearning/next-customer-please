## Cwis cyflym

Ateba'r tri chwestiwn. Mae yna awgrymiadau i dy helpu i gael yr ateb cywir.

Pan fyddi di wedi ateb bob cwestiwn, clicia ar **Gwirio fy ateb**.

Mwynha!

--- question ---

---
legend: Cwestiwn 1 o 3
---

Mae prosiect siop yn defnyddio newidyn `cyfanswm`{:class="block3variables"} i storio'r cyfanswm ar gyfer pob cwsmer.

+ Mae cwsmer yn ychwanegu eitemau sy'n dod i gyfanswm o `50` ac yn talu
+ Mae cwsmer newydd yn ychwanegu eitemau sy'n dod i gyfanswm o `40` ond mae'r `cyfanswm`{:class="block3variables"} bellach yn ymddangos fel `90` ar gyfer yr ail gwsmer

Pa floc fyddai angen i ti ei ychwanegu at y sgript talu i wneud i'r cyfanswm fynd yn ôl i `0` pan fydd pob cwsmer yn talu?

--- choices ---

- ( )
```blocks3
change [total v] by [0]
```

 --- feedback ---

Anghywir, dylai'r `cyfanswm`{:class="block3variables"} fod yn `0` ar ôl i gwsmer dalu, ond nid y bloc `newid`{:class="block3variables"} sydd ei angen arnat ti.

 --- /feedback ---

- ( )
```blocks3
set [total v] to [40]
```

 --- feedback ---

 Anghywir, byddai hyn yn gweithio i'r ail gwsmer ond byddai'r `cyfanswm`{:class="block3variables"} yn anghywir i gwsmeriaid eraill.

 --- /feedback ---

- (x)

```blocks3
set [total v] to [0]
```

 --- feedback ---

Cywir. Mae angen `gosod`{:class="block3variables"} y `cyfanswm`{:class="block3variables"} i `0` ar ôl i bob cwsmer dalu.

 --- /feedback ---

- ( )

```blocks3
change [total v] by [-50]
```

 --- feedback ---

Byddai hynny'n gweithio ar gyfer yr enghraifft hon, ond beth petai'r cwsmer cyntaf yn gwario swm gwahanol? Mae angen i dy ddatrysiad weithio pan fydd y cwsmer blaenorol yn gwario symiau gwahanol.

 --- /feedback ---

--- /choices ---

--- /question ---
