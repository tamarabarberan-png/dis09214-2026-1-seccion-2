# sesión 05 - 10/04
# CLASE: Transformaciones y condicionales

### Transformaciones:

**Angulos: angleMode();**
* por defecto p5 usa RADIANES para medir los ángulos
  * angleMode(RADIANS)
* Para cabiar a grados se usa esto en el funtion SETUP
  *angleMode(DEGREES)

**ROTACIÓN: rotate();**
* sirve para rotar elementos.
* Siempre rot al rededor del punto de origen.
* Se recomienda usar con translate(); y en alguno casos con recMode(CENTER);
  * SINTAXIS: rotate(valor radianes o en grados);
 
**TRASLADAR: translate();**
* sirve para trasladar el punto de origen (0,0) a otra coordenada de mi canvas
  * SINTAXIS: translate(x, y);
 
**GUARDAR Y RESTAURAR: push(); pop();**
* funciones que trabajan juntas como un "sistema de memoria temporal" para el estilo y las transformaciones del lienzo
  * SINTAXIS: push();
  * SINTAXIS: pop();

**ESCALA: scale();**
* Ajusta la escala del sistema de coordenadas actual por el factor especificado.
  * SINTAXIS: scale();
 
### Condicionales:

**Expresión BOOLEANA**
* Es cualquier instrucción que, al ser evaluado, solo puede arrojar uno de dos valores posibles: verdadero (True) o falso (False).

**Operadores:**
* Para construir este tipo de expresiones se utilizan 3 tipos de elementos:
1. Operandos (o Valores): Son los datos básicos que se evalúan. Pueden ser:
   * Variables: (como x, y o mouseX,mouseY, etc).
   * Constantes o Literales: Valores fijos como los mismos valores booleanos True y False.
2. Operadores de comparación: Permiten contrastar dos valores.
   * == (Igual a)
   * != (Diferente de)
   * > o < (Mayor o menor que)
   * >= o <= (Mayor o igual / Menor o igual)
  
3. Operadores Lógicos: Sirven para combinar varias expresiones.
   * AND (&&): Es verdadero solo si ambas partes son verdaderas.
   * OR (||): Es verdadero si al menos una de las partes es verdadera.
   * NOT (!): Invierte el valor (si era verdadero, pasa a ser falso).

**EJEMPLOS OPERADORES DE COMPARACIÓN**
1. menor que < y mayor que >:
* Al comparar números, el operador devuelve un booleano basado en la comparación matemática.
  * EJEMPLO: // menor que 2 < 3 // devuelve true; 3 < 2 // devuelve false
* Al comparar cadenas de texto, el operador compara carácter por carácter basándose en su orden alfabético.
  * EJEMPLO: 'b' < 'a' // devuelve false; 'b' < 'c' // devuelve true
2. menor o igual que: <= y mayor o igual que: >=
* Similar a < y >, pero también devuelve true cuando ambos valores son iguales.
  * EJEMPLO: 12 < 12 // devuelve false; 12 <= 12 // devuelve true
* Lo mismo se aplica a las cadenas de texto, comparando siempre su orden alfabético.
  * EJEMPLO: 'a' <= 'a' // devuelve true
3. Igual == y No igual !=
* El operador igual == devuelve true cuando los operandos son iguales y false cuando no lo son, mientras que el no igual != devuelve true cuando los operandos no son iguales y false cuando son iguales.
  * EJEMPLOS: // número - número 2 == 2 // devuelve true; 2 != 2 // devuelve false

**EJEMPLO OPERADORES LÓGICOS**
1. AND &&:
* El operador AND devuelve true solo si los dos operandos son true; de lo contrario, devuelve false.
  * EJEMPLO: let bool1 = true; let bool2 = false;
  * console.log(bool1 && bool2); // imprimirá false
 
2. OR ||:
* A diferencia de AND, OR devuelve true cuando al menos uno de los operandos es igual a true.
  * EJEMPLO: let bool1 = true; let bool2 = false;
  * console.log(bool1 || bool2); // imprimirá true

3. NOT !:
* El operador NOT devuelve el opuesto del valor booleano actual.
  * EJEMPLO: let bool1 = true;
  * console.log(bool1); // imprime true
  * console.log(!bool1); // imprime false

**SENTENCIA CONDICIONAL: If - else if - else**
* La sentencia if es una estructura especial que existe en casi todos los lenguajes de programación; toma una condición –expresada como un booleano– y ejecuta una pieza de código contenida dentro de las llaves { }
* La sentencia if puede complementarse con la sentencia else if, que añade condiciones de prueba complementarias a la original, y con la sentencia else, que implica todos los casos que no cumplen con la condición original.

1. If(condición){ejecuta este código si es true}
2. else if (condición 2) {ejecuta este código si es true}
3. else {ejecuta este código si ambas condiciones son falsas}
