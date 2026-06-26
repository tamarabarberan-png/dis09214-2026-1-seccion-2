# sesión 06 - 14/04
# CLASE: Funciones propias

**LOS 4 PILARES**

1. DESCOMPOSICIÓN: Consiste en tomar un problema grande y complejo y romperlo en partes más pequeñas y manejables.
   * En diseño: Si quieres visualizar la "Brecha Salarial", no programas todo de una vez. Primero diseñas cómo se ve el "Sueldo A", luego el "Sueldo B", luego la "Interacción" y finalmente el "Fondo".
   * En el código: Se traduce en el uso de Funciones Propias. En lugar de un draw() gigante, tienes una función dibujarIconos() y otra calcularDiferencia(), etc.
  
2. RECONOCIMIENTO DE PATRONES: Es observar tendencias o regularidades dentro de un problema. Si algo se repite o sigue una lógica constante, podemos automatizarlo.
   * En diseño: Notas que para representar a 100 personas, no necesitas dibujar 100 veces. Notas que todas son un círculo con una posición x distinta.
   * En el código: Se traduce en el uso de Bucles (for). Si hay un patrón, el código lo repite por ti con solo tres líneas.
  
3. ABSTRACCIÓN: Es filtrar la información innecesaria y quedarse solo con las características que definen el problema. Es crear una representación simbólica de la realidad.
   * En diseño: Para representar la "presión social" no necesitas dibujar a toda la sociedad; quizás un círculo que se achica cuando el mouse se acerca es suficiente.
   * En el código: Se traduce en el uso de Variables y la función map(). Una posición de mouse (mouseX) se "abstrae" para convertirse en un valor de opacidad o miedo.
  
4. ALGORITMOS: Es el diseño de una serie de reglas ordenadas para resolver el problema. Es el "plan de acción" que debe seguir el sistema.
   * En diseño: Es el flujo de la experiencia. "Si el usuario hace esto, pasa aquello; si no, pasa esto otro”.
   * En el código: Se traduce en el Diagrama de Flujo y en las Condicionales (if/else). Es el mapa lógico que conecta todas las partes anteriores.

**TIPOS DE INTERACCIÓN:**

1. Interacción Discreta (Eventos): Es cuando curre un evento específico (clic) y el sistema responde con una acción única (aparecen círculos). Es un interruptor de "encendido/apagado" o "acción/reacción".
   * En el código: Se suele usar dentro de la función mousePressed() o con un if(mouseIsPressed).

2. Interacción Continua (Input de Datos): Es cuando el sistema reacciona constantemente al movimiento o estado del usuario, sin necesidad de hacer algo especifico (clic).
   * En el código: Usar mouseX o mouseY directamente para afectar el tamaño, color o velocidad de algo.

**FUNCIONES PROPIAS**

* FUNCIÓN function() {}.
* SINTAXIS: function Nombredelafunción() {}.
