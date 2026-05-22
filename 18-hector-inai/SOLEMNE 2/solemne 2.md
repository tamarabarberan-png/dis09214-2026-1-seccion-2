# Desarrollo de identidades de género en ambientes hostiles
**Autor: Héctor Inai Espinoza**

Este proyecto representa en un código de p5.js la dificultad de desarrollar y expresar una identidad de género que se escapa de lo cisgénero y heteronormado.

---

## ¿Qué se ve en la pantalla?

En la pantalla, al entrar, vemos 4 figuras grandes y grises en 4 esquinas del canvas, rodeadas por elipses que cambian de color entre tonos grises, con un texto que dice "haz click para expresarte". Cuando haces click, la pantalla se vuelve progresivamente roja, con líneas aleatorias por toda la pantalla, también ojos y bocas apareciendo y desapareciendo aleatoriamente por todo el canvas.
Las figuras también se mueven al hacer click, se transforman en una figura diferente mientras se glitchean.

---

## ¿Qué elementos visuales aparecen?

Aparecen elementos como elipses pequeñas en loop y 4 figuras en 4 esquinas del canvas; al hacer click aparecen líneas aleatorias e imágenes de ojos y bocas, también un glitch de formas.

---

## Descripción conceptual

La idea central de este proyecto es representar la opresión que pone la sociedad ante una expresión de género diferente a la común, por lo que al presionar el mouse, la presión encima de las figuras empieza a mostrarse.
La presión del mouse es el elemento importante en este sistema; al hacer click las figuras comienzan a "expresarse" y se revela la respuesta del entorno ante esta acción.

### ¿Cómo se relaciona este sistema con la problemática?
Las elipses en el fondo en tonos grises representan a una sociedad heteronormada que rodea a las 4 figuras principales, a las que al hacer click estamos permitiéndoles que se expresen. Al expresarse, cambian de forma a una que no es su original, pero junto a este cambio, el entorno de la sociedad comienza a tornarse rojo, lleno de furia y de ojos y bocas que critican, juzgan y oprimen. Los cuerpos principales se glitchean, representando la dificultad de expresarse libremente.

---

## Reglas que gobiernan el sistema

### 1. INPUT
* **mouseIsPressed:** La acción principal del usuario (Presionado / Suelto).
* **Imágenes:** Los archivos `ojo.png` y `boca.png` desde la memoria.
* **Tiempo:** El pulso constante del programa que corre a 50 fotogramas por segundo.

### 2. ¿Cómo se procesan y transforman?
* **Variable `ruido`:** Si presionas, el `ruido` sube (hasta 255); si sueltas, baja (hasta 0).
* **La Desaparición:** El sistema resta el ruido al valor máximo de opacidad, transformando la presión del mouse en un efecto de desvanecimiento gradual:
  text{Opacidad} = 255 - text{ruido}
* **Elipses de fondo `for`:** El loop procesa las coordenadas `X` e `Y` sumando de 25 en 25 píxeles para multiplicar un solo círculo en una cuadrícula multiplicada y alineada.
* **El Caos `random` y `rotate`:** El sistema muestra ángulos de rotación continuos y genera números al azar para desordenar posiciones, tamaños y colores.

### 3. ¿Qué respuesta visual producen? - OUTPUT
El sistema produce dos estados visuales opuestos:
* **ESTADO A (Sin Click - "El Camuflaje"):** El fondo es gris oscuro. Se ve una cuadrícula perfecta de mil círculos parpadeantes y un texto blanco que dice "haz click para que las figuras se expresen". En el centro, el individuo está representado por figuras grises, pacíficas e inmóviles.
* **ESTADO B (Con Click - "La Expresión"):** El fondo se tiñe de rojo. La cuadrícula de círculos y el texto desaparecen por completo. El individuo central estalla en colores psicodélicos y tiembla violentamente, mientras la pantalla es bombardeada por ojos, bocas y líneas de colores que giran de forma caótica.

---

## 2. Sistema de interactividad

La interactividad funciona como un bucle de tensión y liberación con dos estados:
* **Estado Pasivo (Sin Click):** El sistema invita al usuario con el texto "haz click para expresarte". El entorno es gris, ordenado y monótono. El individuo está camuflado, quieto y en silencio dentro de una estructura rígida (los círculos).
* **Estado Activo (Con Click):** Al presionar, el usuario desata una transformación gradual. El fondo se vuelve rojo, la cuadrícula opresora se borra y el individuo rompe la norma: estalla en colores, tiembla violentamente y el lienzo es bombardeado por líneas de interferencia, ojos y bocas. Al soltar el mouse, el sistema se drena y regresa de inmediato al orden inicial.

![Diagrama de flujo](<img width="4961" height="2063" alt="diagrama de flujo" src="https://github.com/user-attachments/assets/cc76bf9f-405e-4ee6-8e41-030ee69d54cb" />
)
