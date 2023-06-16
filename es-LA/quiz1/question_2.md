
--- question ---

---
legend: Pregunta 2 de 3
---

En una tienda, el **vendedor** tiene este código en el script de pago:

```blocks3
ask [¿Cómo estás hoy?] and wait
if <(answer) = [bien]> then
say [¡Eso es fantástico!] for [2] seconds
else
say [Lamento escuchar eso.] for [2] seconds
end
```

Cuando se ejecuta el código, el usuario escribe la respuesta "excelente". ¿Qué dirá el objeto **vendedor**?

![Un cuadro de 'preguntar' con la palabra 'genial' escrita.](images/quiz2.png)

--- choices ---

- (x) El **Vendedor** dirá `Lamento escuchar eso.`

  --- feedback ---

  Sí. Los humanos saben que 'genial' es lo mismo que 'bueno', pero el '=' comprueba si las letras son iguales.

  La **condición** `respuesta`{:class="block3sensing"} = `bueno` es 'falso' entonces se ejecutará el bloque `decir`{:class="block3looks"} en la parte `entonces`{:class="block3control"}.

  --- /feedback ---

- ( ) El **vendedor** dirá `¡Eso es fantástico!`

  --- feedback ---

No, solo la respuesta exacta `buena` hará que el **vendedor** diga `¡Eso es fantástico!`. Vuelve a ver el código para ver qué mensaje dirá el **vendedor** para todas las respuestas que no sean `buenas`.

**Sugerencia:** 'Bueno' o 'BUENO' coincidiría con 'bueno'.

  --- /feedback ---

- ( ) El **vendedor** no dirá nada.

  --- feedback ---

No, el **vendedor** siempre dirá algo. Mira cuidadosamente el código para ver cuál será el mensaje.

  --- /feedback ---

- ( ) El **vendedor** dirá `genial`.

  --- feedback ---

No, el **cliente** escribió la respuesta 'genial' pero el **vendedor** no dice la respuesta. Mira cuidadosamente el código para ver cuál será el mensaje.

  --- /feedback ---

--- /choices ---

--- /question ---
