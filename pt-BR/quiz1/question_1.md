## Quiz rápido

Responda três perguntas. Existem dicas para guiá-lo para a resposta correta.

Depois de responder a cada pergunta, clique em **Verificar minha resposta**.

Divirta-se!

--- question ---

---
legend: Question 1 of 3
---

Um projeto de loja usa uma variável `total`{:class="block3variables"} para armazenar o total de cada cliente.

+ Um cliente adiciona itens que totalizam `50` e paga
+ Um novo cliente adiciona itens que totalizam `40` mas o `total`{:class="block3variables"} agora apresenta `90` para o segundo cliente

Qual bloco você precisaria adicionar ao script de pagamento para que o total voltasse para `0` quando cada cliente pagasse?

--- choices ---

- ( )
```blocks3
change [total v] by [0]
```

 --- feedback ---

Não exatamente, `total`{:class="block3variables"} deveria ser `0` depois que um cliente paga, mas não é o `altere`{:class="block3variables"} bloco que você precisa.

 --- /feedback ---

- ( )
```blocks3
set [total v] to [40]
```

 --- feedback ---

 Não exatamente, isso funcionaria para o segundo cliente, mas o `total`{:class="block3variables"} seria errado para outros clientes.

 --- /feedback ---

- (x)

```blocks3
set [total v] to [0]
```

 --- feedback ---

Sim, está correto. Você precisa `definir`{:class="block3variables"} o `total`{:class="block3variables"} para `0` após cada pagamento dos clientes.

 --- /feedback ---

- ( )

```blocks3
change [total v] by [-50]
```

 --- feedback ---

Isso funcionaria neste exemplo, mas e se o primeiro cliente gastasse uma quantia diferente? Sua solução precisa funcionar quando o cliente anterior gasta valores diferentes.

 --- /feedback ---

--- /choices ---

--- /question ---
