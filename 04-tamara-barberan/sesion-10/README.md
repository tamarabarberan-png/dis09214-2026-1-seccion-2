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
