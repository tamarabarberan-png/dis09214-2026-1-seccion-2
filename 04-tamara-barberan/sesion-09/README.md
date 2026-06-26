# sesión 06 - 14/04

# CLASE 09

**Estdos y Cámara web:**

1. crear y definir variable estados 
 * sintaxsis: les estado =0; //0 = inicio , 1= experoencia 2 = final
   
2. Configurar el lienzo (function setup)
 * Creamos el lienzo de fondo donde va a ocurrir toda la magia.
   
3. Crear la estructura de un estado (function draw)
   * aqui usamos un switch dependiendo del valor de la variable estado, el programa dibujara una cosa u otra
     
4. Programar visualmente cada estado (funciones propias)
 * Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente
   para que se note el cambio.
   
5. La logica del cambio y el reinicio
 * para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la funcion del mousepressed () cada vez que hagas un click, la variable aumentará. si llega a 3 (despues del estado 2), volverá a 0.
 
 * EN PROGRAMACIÓN SE CUENTA DESDE 0!!!
 * Ejemplo ( 0, 1, 2, 3, 4, etc)
### Ojo que hay muchas formas de cambiar de un estado a otro
1. Interacción con el Teclado:
   * Por barra espaciadora o Enter
   * Por teclas específicas (ej.Números): Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la
     experiencia y la 3 al final.

2. Botones Reales en la Pantalla:
   * En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de HTML usando
     la librería de p5.js. Esto es mucho más profesional para menús.

3. Zonas de Clic (Botones dibujados con rect o ellipse):
   * Si no quieres usar botones de HTML y prefieres dibujar tus propios botones con rect(),puedes
     evaluar si el mouse estaba dentro de esa caja al hacer clic.
     
4. Interacciones Automáticas (Por Tiempo):
   * Por Tiempo (Temporizador): Ideal para una pantalla de introducción (Splash Screen) que dura
     3 segundos y pasa sola al menú.

### CÁMARA WEB:

**createCapture(VIDEO);**

* crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web
* inicializar la cámara en el function setup() utilizamos el comando especial creativeCapture(video); esto le pedirá permiso al navegagador para encender la cámara del computador, tambien definimos un tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
* dibujar la cámara en el function draw();, usamos la funcion image ().p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real. 
