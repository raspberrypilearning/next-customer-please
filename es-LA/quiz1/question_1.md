## Test rápido

Contesta las tres preguntas. Hay sugerencias para guiarlo a la respuesta correcta.

Cuando haya respondido a cada pregunta, haga clic en **Verificar mi respuesta**.

¡Diviértete!

--- question ---

---
legend: Pregunta 1 de 3
---

Un proyecto de tienda utiliza una variable `total`{:class="block3variables"} para almacenar el total de cada cliente.

+ Un cliente agrega artículos que suman `50` y paga
+ Un nuevo cliente agrega elementos que suman `40`, pero el `total`{:class="block3variables"} ahora se muestra como `90` para el segundo cliente

¿Qué bloque necesitarías agregar al script de pago para que el total vuelva a `0` cuando cada cliente pague?

```blocks3
when this sprite clicked
ask [¿Quieres pagar o cancelar?] and wait
if {(answer) = [pagar]} then
say (join [Son ] (total)) for (2) seconds
play sound [coin v] until done 
say (join [Gracias por comprar en ] (name)) for (2) seconds
broadcast [next customer v]
end
```

--- choices ---

- ( )
```blocks3
change [total v] by [0]
```

 --- feedback ---

No del todo. `total`{:class="block3variables"} debería ser `0` después de que un cliente paga, pero no es el bloque `cambiar`{:class="block3variables"} que necesitas.

 --- /feedback ---

- ( )
```blocks3
set [total v] to [40]
```

 --- feedback ---

 No del todo; esto funcionaría para el segundo cliente, pero el `total`{:class="block3variables"} sería incorrecto para otros clientes.

 --- /feedback ---

- (x)

```blocks3
set [total v] to [0]
```

 --- feedback ---

Sí, correcto. Debes `fijar`{:class="block3variables"} el `total`{:class="block3variables"} a `0` después de que cada cliente pague.

 --- /feedback ---

- ( )

```blocks3
change [total v] by [-50]
```

 --- feedback ---

Eso funcionaría para este ejemplo, pero ¿qué pasa si el primer cliente gastó una cantidad diferente? Tu solución debe funcionar cuando el cliente anterior gasta cantidades diferentes.

 --- /feedback ---

--- /choices ---

--- /question ---
