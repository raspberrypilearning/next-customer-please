## Compras

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">

El objeto**vendedor** necesita:
- preguntar si el cliente está listo para pagar los artículos
- aceptar el pago
- prepararse para el próximo cliente
</div>
<div>
![](images/step4-image.png){:width="300px"}
</div>
</div>

Cuando hayas terminado de elegir artículos, el cliente hará clic en el sprite **vendedor** para pagar.

--- task ---

 Dile al cliente cuánto costarán sus artículos.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds 
```

--- /task ---

--- task ---

Agrega un sonido de pago a su sprite **vendedor** para que el cliente sepa que se está realizando el pago.

![El icono para agregar un sonido](images/add-sound.png)

[[[scratch3-add-sound]]]

Agrega el sonido de reproducción `hasta que termine el bloque`{:class="block3sound"} a su script.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
+ play sound [machine v] until done 
```

--- /task ---

--- task ---

Termina la venta. Establece `total`{:class="block3variables"} volver a `0` después del pago, `decir`{:class="block3looks"} adiós y `transmitir`{:class="block3control"} `próximo cliente`{: clase="bloque3control"}.

```blocks3
when this sprite clicked
say (join [That will be ] (total)) for (2) seconds
play sound [machine v] until done 
+ set [total v] to (0)
+ say (join [Thanks for shopping at ] (name)) for (2) seconds
+ broadcast (next customer v)
```

--- /task ---

--- task ---

**Prueba:** Prueba tu proyecto y asegúrate de: lo siguiente:
- El cliente puede pagar con los efectos de sonido correctos
- El `total`{:class="block3variables"} se regresa a `0` después de que un cliente paga o cancela.

--- /task ---


--- task ---

**Depuración:** Es posible que encuentres algunos errores en tu proyecto que necesites corregir.

Estos son algunos errores comunes:

--- collapse ---
---
title: El vendedor no hace nada cuando hago clic en él
---

Tienes bastantes objetos en tu proyecto. Asegúrate de que el script `al hacer clic en este objeto `{:class="block3events"} esté en tu objeto **vendedor**.

**Sugerencia:** Si lo agregaste al objeto incorrecto, puedes arrastrar el código al objeto **vendedor** y luego eliminarlo del otro objeto.

--- /collapse ---

--- collapse ---
---
title: Las palabras en los bloques de hablar se fusionan
---

Cuando `unes `{:class="block3operators"} dos piezas, debes agregar un espacio al final de tu primera pieza de texto o al comienzo de tu segunda pieza de texto.

Estos tienen un espacio al final de la primera parte de la unión:

```blocks3
say {join [That will be ](total)} for (2) seconds

say {join [Thanks for shopping at ](name)} for (2) seconds
```

--- /collapse ---

--- collapse ---
---
title: El total no se reinicia después de una venta
---

Comprueba que has utilizado:

```blocks3
set [total v] to (0)
```

**no**:

```blocks3
change [total v] by (0)
```

--- /collapse ---

--- collapse ---
---
title: El vendedor no responde
---

Asegúrate de que el `operador`{:class="block3operators"} en la condición `if`{:class="block3control"} sea el símbolo mayor que `>`{:class="block3operators"}.

```blocks3
if <(total) > [0]> then
```

--- /collapse ---

**Sugerencia:** Compara tu código con los ejemplos de código. ¿Hay alguna diferencia que no debería estar ahí?

--- /task ---

--- save ---
