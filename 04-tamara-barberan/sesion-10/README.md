# sesión 06 - 14/04

# clase 10

1. Crear un canva con dimenciones dinámicas:
2. Crear un evento: windowResized():
   * si el usuiario estira o encoge la ventana dek  navegador....
3. Usar valores relativos:
   * ahora p5js actualiza estas variables width y height automaticamente con el tamaño actual del lienzo
   * entonces ahora todos los valores de posición y tamaño que ocupemos lo stenemos que pensar en relación proporcional a esas variables
   * usaremos fracciones y propporciones:
   * ejemplo: centro del lienzo (width / 2, height / 2).
4. incluir un factor de referencia:
   * sintaxis: referencia = min (width, height);
   * creamos una variable global (referencia) y la asignamos para que calcule el mínimo.
   * observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.
5. usar translate - push y pop
   * en lugar de hacer matemáticas complejas en cada rect() o ellipse(), usamos translate() para mover el origen del mundo.
   * y siempre utilizando ppush() y pop() para cada figura o elemento.

### AGREGAR IMÁGENES:

1. subir la imagen a p5:
   * hacer click a la flechita de la esquina superior izquierda del editor, esto abrirá el menú
  
2. Declarar y precargar la imagen:
   * SINTAXIS: fuction preload();
   * Creamos una variable global al inicio del codigo para guardar la imagen
   * Usamos la función dentro de function preload() y cargamos la imagen con loadImage();

3. dibujar y dimenciona la imagen en el draw
   * la imagen se dibuja usando la función image()
   * esta función requiere mínimo 3 argumentos, pero acepta 5 si queremos controlar su tamaño de forma responsiva.
   * SINTAXIS: image(nombreVariableImagen, x, y, ancho, alto);
  
### EJEMPLOS AVANZADOS DE DISTORSIÓN DE IMAGEN

**loadPixels():**

* Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la memoria de acceso rápido (RAM). Se comunica directamente con la
   tarjeta gráfica píxel por píxel en tiempo real.
* loadPixels() crea un "puente" temporal para que puedas analizar la información de forma masiva y fluida.

**Modificar los pixeles:**

1. get(x, y) — Lectura (El "Ojo"):
   * Función: Va a la coordenada exacta (x, y) y extrae el color de ese píxel.
   * Resultado: Te devuelve un objeto de color o un arreglo con los cuatro canales esenciales: [Rojo, Verde, Azul, Alfa] (valores de 0 a 255).
   * Uso extra: Si lo usas sin coordenadas (imagen.get()), sirve para clonar o hacer una copia de respaldo completa del lienzo.
  
2. set(x, y, nuevoColor) — Escritura (El "Pincel"):
   * Función: Va a la coordenada (x, y) e inyecta un color nuevo, reemplazando por completo el color que existía ahí.
   * Resultado: Modifica el mapa de píxeles en la memoria interna, preparando el nuevo aspecto de la imagen.

3. updatePixels() — La Actualización:
   * Función: Toma todos los cambios que realizaste con set() y los sube de golpe a la pantalla.
   * ¿Por qué es MUY necesario? set() no dibuja inmediatamente; solo guarda los cambios en un borrador secreto. updatePixels() es el comando que
     efectivamente "publica" y renderiza el resultado final en el lienzo para que el usuario pueda verlo.
  












