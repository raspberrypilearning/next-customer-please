
--- question ---

---
legend: Question 2 of 3
---

Em uma loja, o **vendedor** tem este código no script de checkout:

```blocks3
ask [How are you today?] and wait
if <(answer) = [good]> then
say [That's fantastic!] for [2] seconds
else
say [Sorry to hear that.] for [2] seconds
end
```

Quando o código é executado, o usuário digita a resposta 'ótimo'. O que o sprite **vendedor** dirá?

![Uma caixa de 'perguntar' com a palavra 'ótimo' escrita.](images/quiz2.png)

--- choices ---

- (x) O **Vendedor** dirá `Lamento ouvir isso.`

  --- feedback ---

  Sim. Os humanos sabem que 'ótimo' significa o mesmo que 'bom', mas '=' verifica se as letras são iguais.

  A **condição** `resposta`{:class="block3sensing"} = `boa` é 'falsa', então `diga`{: O bloco class="block3looks"} na parte `else`{:class="block3control"} será executado.

  --- /feedback ---

- ( ) O **vendedor** dirá `Isso é fantástico!`

  --- feedback ---

Não, apenas a resposta exata `boa` fará com que o **vendedor** diga `Isso é fantástico!`. Olhe o código novamente para ver qual mensagem o **vendedor** dirá para todas as respostas que não são `boas`.

**Dica:** 'Bom' ou 'BOM' corresponderia a 'bom'.

  --- /feedback ---

- ( ) O **vendedor** não fala nada.

  --- feedback ---

Não, o vendedor **** sempre dirá algo. Observe atentamente o código para ver qual será a mensagem.

  --- /feedback ---

- ( ) O **vendedor** dirá `ótimo`.

  --- feedback ---

Não, o **cliente** digitou a resposta 'ótimo', mas o **vendedor** não disse a resposta. Observe atentamente o código para ver qual será a mensagem.

  --- /feedback ---

--- /choices ---

--- /question ---
