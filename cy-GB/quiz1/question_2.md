
--- question ---

---
legend: Cwestiwn 2 o 3
---

Mewn siop, mae gan y **gwerthwr** y cod yma yn y sgript talu:

```blocks3
ask [Sut wyt ti heddiw?] and wait
if <(answer) = [da]> then
say [Mae hynny'n wych!] for [2] seconds
else
say [Mae'n ddrwg gen i glywed hynny.] for [2] seconds
end
```

Pan fydd y cod yn rhedeg, mae'r defnyddiwr yn teipio'r ateb 'grêt'. Beth fydd corlun y **gwerthwr** yn dweud?

![Blwch 'ask' gyda'r gair 'great' wedi'i deipio i mewn.](images/quiz2.png)

--- choices ---

- (x) Bydd y **Gwerthwr** yn dweud `Ddrwg gen i glywed hynny.`

  --- feedback ---

  Cywir. Mae pobl yn gwybod bod 'grêt' yn golygu'r un peth â 'da', ond mae'r '=' yn gwirio a yw'r llythrennau yr un peth.

  Mae'r **amod** `ateb`{:class="block3sensing"} = `da` yn 'anwir' felly bydd y bloc `dweud`{:class="block3looks"} yn y rhan `fel arall`{:class="block3control"} yn rhedeg.

  --- /feedback ---

- ( ) Bydd y **gwerthwr** yn dweud `Mae hynny'n ffantastig!`

  --- feedback ---

Na, dim ond yr union ateb `da` fydd yn gwneud i'r **gwerthwr** ddweud `Mae hynny'n ffantastig!`. Edrycha ar y cod eto i weld pa neges y bydd y **gwerthwr** yn ei ddweud ar gyfer pob ateb sydd ddim yn `da`.

**Awgrym:** Byddai 'Da' neu 'DA' yn cyfateb i 'da'.

  --- /feedback ---

- ( ) Fydd y **gwerthwr** ddim yn dweud unrhyw beth.

  --- feedback ---

Na, bydd y **gwerthwr** bob amser yn dweud rhywbeth. Edrycha yn ofalus ar y cod i weld beth fydd y neges.

  --- /feedback ---

- ( ) Bydd y **gwerthwr** yn dweud `grêt`.

  --- feedback ---

Na, teipiodd y **cwsmer** yr ateb 'grêt' ond dydy'r **gwerthwr** ddim yn dweud yr ateb. Edrycha yn ofalus ar y cod i weld beth fydd y neges.

  --- /feedback ---

--- /choices ---

--- /question ---
