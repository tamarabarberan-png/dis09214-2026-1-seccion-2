# sesión 06 - 14/04

# CLASE 09

**Estdos y Cámara web:**

1. crear y definir variable estados 
 * sintaxsis: les estado =0; //0 = inicio , 1= experoencia 2 = final
2. crear lienzo
3. crear la estructura de un estado (function draw)
   * aqui usamos un switch dependiendo del valor de la variable estado, el programa dibujara una cosa u otra
4. programar visualmente cada estado (funciones propias)
5. la logica del cambio y el reinicio
 * para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la funcion del mousepressed () cada vez que hagas un click, la variable aumentará. si llega a 3 (despues del estado 2), volverá a 0.
 
 * EN PROGRAMACIÓN SE CUENTA DESDE 0!!!
 * Ejemplo ( 0, 1, 2, 3, 4, etc)

**createCapture(VIDEO);**

* crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web
* inicializar la cámara en el function setup() utilizamos el comando especial creativeCapture(video); esto le pedirá permiso al navegagador para encender la cámara del computador, tambien definimos un tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
* dibujar la cámara en el function draw();, usamos la funcion image ().p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real. 
