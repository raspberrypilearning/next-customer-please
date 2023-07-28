## Snelle quiz

Beantwoord de drie vragen. Je wordt naar het juiste antwoord geleid.

Klik na het beantwoorden van elke vraag op **Controleer mijn antwoord**.

Veel plezier!

--- question ---

---
legend: Vraag 1 van 3
---

Een winkelproject gebruikt een `totaal`{:class="block3variables"} variabele om het totaal voor elke klant op te slaan.

+ Een klant voegt items toe die in totaal `50` bedragen en betaalt
+ Een nieuwe klant voegt items toe die in totaal `40` bedragen, maar het `totaal`{:class="block3variables"} wordt nu weergegeven als `90` voor de tweede klant

Welk blok zou je aan het betalingsscript moeten toevoegen om het totaal terug te laten gaan naar `0` nadat elke klant heeft betaald?

```blocks3
Wanneer deze sprite klikte
vraag [wil je betalen of annuleren?] En wacht
als {(answer) = [pay]} dan
zeg (join [that will be ] (total)) gedurende (2) seconden
speel geluid [coin v] totdat done
zeg (join [Thanks for shopping at ] (name))) gedurende (2) seconden
uitzending [next customer v]
einde
```

--- choices ---

- ( )
```blocks3
wijzig [total v] met [0]
```

 --- feedback ---

Niet helemaal, dit zou voor de tweede klant werken, maar het `totaal`{:class="block3variables"} zou verkeerd zijn voor andere klanten.

 --- /feedback ---

- ( )
```blocks3
stel [total v] in op [40]
```

 --- feedback ---

 Niet helemaal, `totaal`{:class="block3variables"} moet `0` zijn nadat een klant betaalt, maar het is niet het `verander`{:class="block3variables"} blok dat je nodig hebt.

 --- /feedback ---

- (x)

```blocks3
stel [total v] in op [0]
```

 --- feedback ---

Ja dat is goed. Je moet `maak`{:class="block3variables"} het `totaal`{:class="block3variables"} `0` maken nadat elke klant betaalt.

 --- /feedback ---

- ( )

```blocks3
wijzig [total v] met [-50]
```

 --- feedback ---

Dat zou voor dit voorbeeld werken, maar wat als de eerste klant een ander bedrag besteedde? Je oplossing moet werken wanneer de vorige klant verschillende bedragen uitgeeft.

 --- /feedback ---

--- /choices ---

--- /question ---
