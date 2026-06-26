# LOOPS, WHILE & FOR

**BUCLE**
* En informática: Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.

**LOOP**
* Es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.

**WHILE**
* Los bucles while son útiles para repetir instrucciones mientras una condición sea verdadera.
* SINTAXIS: While(condición booleana) { ejecuta este código si es true }.

**for**
* Una forma de repetir un bloque de código cuando se conoce el número de iteraciones.
* Los bucles `for` son útiles para repetir instrucciones un número determinado de veces.
* SINTAXIS: for(inicialización variable; condición booleana; actualización){ Lo que queremos que pase cuando la condición sea verdadera }.

**NESTED LOOPS: Un loop dentro de otro loop**
* Un for dentro de otro for
* SINTAXIS: for(inicialización variable; condición booleana; actualización) { lo que queremos que pase cuando la condición sea verdadera
  for(inicialización variable; condición booleana; actualización) { lo que queremos que pase cuando la condición sea verdadera
  }
}

**frameCount**
* Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto.
* El valor de `frameCount` es 0 dentro de `setup()`.
* Se incrementa en 1 cada vez que finaliza la ejecución del código en `draw()`.
