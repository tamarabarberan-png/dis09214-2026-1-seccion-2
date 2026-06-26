# sesión 04 - 23/03
# CLASE: Datos dinámicos 

**Posición del mouse**
* moueseX; mouseY; :
* Variables del sistema númerico que determinan la posición del mouse en las coordenadas X e Y
  * Ejemplo: (mouseX, mouseY) = ellipse(mouseX, mouseY, 100, 100);

**Variables integradas en p5.js**
* Lienzo:
  * Width
  * height

* Mouse:
  * mouseX
  * mouseY
  * pmouseX
  * mouselsPressed
  * mouseButton
 
* Teclado:
  * Key
  * KeyCode
  * KeylsPressed
 
* Tiempo:
  * frameCount
  * deltaTime

* ventana:
  * windowWidth
  * windowHeight
  * focused
 
**Crea tus propias variables**
1. Declara tu vaiable: Para declarar tu variable podemos ocupar
   * let: para variables dinámicas
   * const: para variables constantes
2. Inicializa tu variable: En function draw, es Tu variable = Tu variable;
3. Usa tu variable: ejemplo, ellipse(Tuvariable, 200, 50,50);

**JavaScript Objects**
* Sirven para organizar nuestro código de forma adecuada
* Forma de agrupar muchas variables dentro de una variable
* Estructura de datos que te permite agrupar valores relacionados bajo un mismo nombre. Los objetos funcionan como un "contenedor" que organiza la información mediante pares de clave y valor.
* Luego se accede a la información mediante notación de punto

**Random(); fuction;**
* su trabajo es devolver un número aleatorio dentro de un rango que tu defines.
* random(): si no pones nada, devuelve un número decimal entre 0 y 1
* random(máximo): Devuelve un número decimal entre 0 y el máximo que elijas.
* random(mínimo, máximo): Devuelve un número decimal entre esos dos valores

**(width, height);**
* vaiables integradas en p5.js que corresponden a los valores definidos en el creativeCanvas.

**(windowWidth, windowHeight);**
* Variables integradas en p5.js, que permiten ajustar el tamaño del lienzo al tamaño de la ventana del navegador.

**map(); fuction;**
* Esta función nos permite convertir un valor de un rango a otro.
* Toma un número que esta en una "escala" y lo traduce proporcionalmente a una "escala" nueva.
* sintaxis: map(valor,min_original, max_original, min_nuevo, max_nuevo);
* valor: La variable que quieres transformar ("mapear").
