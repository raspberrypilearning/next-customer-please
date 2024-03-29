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
when this sprite clicked
ask [Wil je betalen of annuleren?] and wait
if {(answer) = [betalen]} then
say (join [Dat is dan ] (totaal)) for (2) seconds
play sound [coin v] until done 
say (join [Bedankt voor het winkelen bij ] (name)) for (2) seconds
broadcast [volgende klant v]
end
```

--- choices ---

- ( )
```blocks3
change [totaal v] by [0]
```

 --- feedback ---

Niet helemaal, dit zou voor de tweede klant werken, maar het `totaal`{:class="block3variables"} zou verkeerd zijn voor andere klanten.

 --- /feedback ---

- ( )
```blocks3
set [totaal v] to [40]
```

 --- feedback ---

Niet helemaal, `totaal`{:class="block3variables"} moet `0` zijn nadat een klant betaalt, maar het is niet het `verander`{:class="block3variables"} blok dat je nodig hebt.

 --- /feedback ---

- (x)

```blocks3
set [totaal v] to [0]
```

 --- feedback ---

Ja dat is goed. Je moet `maak`{:class="block3variables"} het `totaal`{:class="block3variables"} `0` maken nadat elke klant betaalt.

 --- /feedback ---

- ( )

```blocks3
change [totaal v] by [-50]
```

 --- feedback ---

Dat zou voor dit voorbeeld werken, maar wat als de eerste klant een ander bedrag besteedde? Je oplossing moet werken wanneer de vorige klant verschillende bedragen uitgeeft.

 --- /feedback ---

--- /choices ---

--- /question ---
