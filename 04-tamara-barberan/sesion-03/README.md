# sesión 03 - 27/03
# CLASE: p5.js

**Algoritmo:**

* secuencia de intrucciones paso a paso
* Logicas, definidas, ordenadas y finitas que permitan solucionar un problema o realizar una tarea.

  * **Características:**
  * Precisión: Cada paso debe estar clarisimo
  * Orden: LOs pasos llevan una secuencia logica
  * Finitud: Si sigues el mismo algoritmo dos veces con los mismo datos, deberias obtener siempre el mismo resultado

 **Estructura:**

1. Imput (entrada): la informacion olos ingredientes que necesitas opara empezar
2. Proceso: Los pasos Lógicos que transforman esa entrada:
3. Output(Salida): El resultado final o la solución al problema.

**Diagrama de flujo**

* Representación grafica de un algoritmos o de los pasos de un proceso 
* se utiliza como una herramienta de planificación para visualizar la logica de un programa antes de escribir una sola linea de de codigo.
* se utilizas componentes estandar (simbología)

**Lenguaje de programación:**
* Proposito General: Python, Java, C++, C#
* Desarrollo Web: JavaScript, TypeScript; PHP, Ruby
* sistema y bajo nivel: C, Rust, Go
* Analisis de datos: R, Python, Julia
* Movil: Swift (iOS), Kotlin (android)

**Funciones maestras:**
* Setup: Se ejecuta una sola vez al principio (para crear el lienzo)
  * **su proposito:** Configurar el entorno inicial.
* Draw (){: Se ejecuta en un bucle infinito, lo que permite crear animaciones.
  * **Proposito:** Crear movimiento y responder a la interacción en tiempo real.
  * **Qué sucede aquí?:**Dibujas formas que cambian de posición, detectas donde está el ratón o cambias colores gradualmente.

### CreateCanvas:
* Sintaxis: createCanvas([width], [height], [renderer], [canvas]);
  * Ejemplo: createCanvas(100, 100);
**CreateCanvas (widht, height):**
* Sirve para crear el lienzo (Canvas) y determinar su tamaño en pixeles.
* Solo se pone una vez y siempre dentro del setup();

**Renderer:**
* define el motor de renderizado.
* P2D (Default): Modo 2D, es el que usas por defecto si no escribes nada. Está optimizado para forma basicas, texto e imagenes planas.
* WEBGL: Activa el modo 3D, utiliza la tarjeta grafica (GPU) de tu pc. Es indispensable pra funsiones como box(), sphere(), luces o texturas complejas.

**Canvas** 
* Es útil si quieres desarrollar web.
* Por defecto, p5.js crea un elemento <canvas> nuevo y lo inyecta en tu HTML.

### Background:
* Sintaxis: background(v1, v2, v3, [a]);
* * ejemplo: background(250, 150, 228,150);
**background:**
* Nos sirve para designar el color de nuestro lienzo (canvas).
* Se puede poner en el setup(); o en el draw(), pero tienes resultados diferentes.

**[v1,v2,v3]**
* Son los valores de colores R,G,B.
*  [COLORES RGB] (https://htmlcolorcodes.com/)

**[a]:**
* Par+ametro para el canal alpha
* Sirve para darle semitransparencia al color del fondo. (0-255)
* Donde 1 será muy transparente y 255 muy poco transparente.

1. Escala de grises (1 número): background(220); (donde 0 es negro y 255 es blanco).
2. Color RGB (3 números): background(255, 0, 0); (Rojo, Verde, Azul).
3. Nombres de colores: background('blue'); (siempre entre comillas).
4. Transparencia (4 números): background(0, 0, 255, 50); (R,G,B y el cuarto número es el canal "Alpha").

**Espacio de color RGB**
• R: Red [0 - 255]
• G: Green [0 - 255]
• B: Blue [0 - 255]
* colorMode(RGB);

**Espacio de color HSV /HSB**
• H: Hue [0 - 360o]
• S: Saturation [0 - 100%]
• B: Brightness [0 - 100%]
* colorMode(HSB);

### Dibujar en p5.js:
* Hay que entender el Canvas funciona con un sistema de coordenadas (x,y)
* el punto(0,0) no está en el centro, sino en la esquina superior izquierda.

### FIGURAS GEOMÉTRICAS 2D}

•point(x, y); Dibuja un solo píxel en las coordenadas dadas.
•line(x1, y1, x2, y2); Dibuja una línea desde un punto inicial hasta un punto final.
•rect(x, y, ancho, alto); Dibuja un rectángulo. Por defecto, x e y definen la esquina superior izquierda.
•ellipse(x, y, ancho, alto); Dibuja un óvalo o círculo. A diferencia del rectángulo, x e y definen el centro de la figura.
•circle(x, y, diámetro); Una versión simplificada de la elipse cuando quieres un círculo perfecto.
•square(x, y, lado); Un rectángulo donde todos los lados son iguales.
•triangle(x1, y1, x2, y2, x3, y3); Necesitas darle las coordenadas de sus tres esquinas.
•quad(x1, y1, x2, y2, x3, y3, x4, y4); Un cuadrilátero. Sirve para hacer formas irregulares de cuatro lados.

### Tamaños del borde:

**StrokeWeight():**
* Establece el tamaño del borde de las figuras
* Siempre se pone arriba de Stroke();
* Sintaxis: strokeWeight(weight);

**noStroke():**
* Se usa para que mi figura no tenga borde.

### Color del borde:

**Stroke();**
* Establece el color que se utiliza para dibujar puntos, lineas y contornos de figuras.
* Se pone arriba de la linea de código de la figura.
* Sintaxis: stroke(v1, v2, v3, [alpha]);

**StrokeCap();**
* Define la forma de la linea o borde de nuestras figuras.
* Las constantes son: ROUND, SQUARE y PROJECT.
* Sintaxis: strokeCap(cap);

### Figuras geometricas 2D avanzadas:

**arc();**
* sirve para hacer arcos o medio círculo.
* X e y son las coordenadas del centro del círculo que contiene este arco, w y h son la anchura y alto del círculo que contiene este arco, star y stop, es donde comienza y termina el ángulo de este arco.
* Sintaxis: arc(x, y, w, h, start, stop)
* Les sugiero activar el modo ángulos en el SETUP(); para que sea más fácil : angleMode(DEGREES);
* el grado 0 no está arriba, sino a la derecha (en el eje X positivo). Y se mueve en el sentido del reloj.
• 0° / 0 rad: A las 3 en punto (derecha).
• 90° / HALF_PI: A las 6 en punto (abajo).
• 180° / PI: A las 9 en punto (izquierda).
• 270° / (PI + HALF_PI): A las 12 en punto (arriba).
