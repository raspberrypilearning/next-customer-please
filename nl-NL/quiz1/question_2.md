
--- question ---

---
legend: Vraag 2 van 3
---

In een winkel heeft de **verkoper** deze code in het afrekenscript:

```blocks3
ask [How are you today?] and wait
if <(answer) = [good]> then
say [That's fantastic!] for [2] seconds
else
say [Sorry to hear that.] for [2] seconds
end
```

Wanneer de code wordt uitgevoerd, typt de gebruiker het antwoord 'geweldig'. Wat zal de **verkoper** sprite zeggen?

![Een 'vraag' vak met het woord 'geweldig' ingetypt.](images/quiz2.png)

--- choices ---

- (X) de **Verkoper** zal `Sorry om dat te horen zeggen.`

  --- feedback ---

  Ja. Mensen weten dat 'geweldig' hetzelfde betekent als 'goed', maar de '=' controleert of de letters hetzelfde zijn.

  De **voorwaarde** `antwoord`{:class="block3sensing"} = `goed` is 'niet juist', dus het `zeg`{:class="block3looks"} blok in het `anders`{:class="block3control"} gedeelte zal worden uitgevoerd.

  --- /feedback ---

- ( ) de **verkoper** zal zeggen `dat is fantastisch!`

  --- feedback ---

Nee, alleen het exacte antwoord `goed` zal ervoor zorgen dat de **verkoper** zegt `dat is fantastisch!`. Kijk opnieuw naar de code om te zien welk bericht de **verkoper** zal zeggen voor alle antwoorden die niet `goed` zijn.

**Tip:** 'goed' of 'GOED' zou overeenkomen met 'goed'.

  --- /feedback ---

- ( ) de **verkoper** zal niets zeggen.

  --- feedback ---

Nee, de **verkoper** zal altijd iets zeggen. Kijk goed naar de code om te zien wat het bericht zal zijn.

  --- /feedback ---

- ( ) de **verkoper** zal `geweldig` zeggen.

  --- feedback ---

Nee, de **klant** heeft het antwoord 'geweldig' getypt, maar de **verkoper** zegt het antwoord niet. Kijk goed naar de code om te zien wat het bericht zal zijn.

  --- /feedback ---

--- /choices ---

--- /question ---
