# sesión 06 - 14/04

## SONIDOS EN p5js:

**Paso 1: Subir sus sonidos a p5js**
1. Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior
  izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.
2. Hacer clic en el icono de + o el menú desplegable junto a Files.
3. Seleccionar Upload file (Subir archivo).
4. Arrastrar el archivo de sonido. Formatos recomendados: .mp3 o .wav
5. Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una
   carpeta llamada ASSETS
     
**Paso 2: Declarar y precargar el sonido: function preload()**
1. creamos una variable global al inicio del código para guardar nuestro sonido.
2. usamos la function preload iniciualizamos nuestra variable y cargamos el sonido con
loadSound()

**Paso 3: Activae mi sonido**

1. Le damos play al sonido en el function setup con: nombreVariable.play();
2. Con esta instrucción, el sonido va a comenzar cuando le demos play a nuestro sketch.

### LO IDEAL ES ACTIVAR MI SONIDO CON UN MOUSEPRESSED

#### COMO CONTROLAR MI SONIDO?

**Métodos de control de sonido**
1. nombreVariable.play() : Reproduce el sonido una vez.
2. nombreVariable.loop() : Reproduce el sonido en bucle infinito.
3. nombreVariable.stop() : Detiene el sonido por completo.
4. nombreVariable.pause() : Pausa el sonido en el segundo actual.
5. nombreVariable.setVolume(valor) :
 * Modifica el volumen.
 * Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).
6. nombreVariable.rate(valor) :
 * Modifica la velocidad de
 * reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más grave) y 2.0
   es el doble (suena más agudo).

**Métodos de consulta o estados del sonido**

1. nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y false si no.
2. nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().
3. nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en loop().
4. nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción (ej: 12.45).
5. nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej: 180.0).
6. nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un número entre 0.0
y 1.0).
7. nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para normal, 2.0 para el
doble).

**SINTESIS DE AUDIO: p5.sound()**

1. El Oscilador (p5.Oscillator): Es el motor que genera el sonido. Puede tener distintas "formas
de onda" que cambian el timbre del sonido:
* 'sine' (onda senoidal ó sinusoidal: un sonido suave, como una flauta).
* 'triangle' (onda triangular: sonido intermedio).
*  'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los
80).
* 'square' (onda cuadrada: sonido retro, tipo videojuego de 8 bits).

