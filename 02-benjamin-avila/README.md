# Repo solemne 2

---

# *Información del Proyecto*

## *Nombre del proyecto*  
Desigualdad de Género en la Política Chilena

## *Autores*  
Benjamin Ávila y Sara Graadt

---

# *Descripción Objetiva*

## *¿Qué es el proyecto?*

Es una visualización interactiva desarrollada en p5.js que representa *estadísticas reales sobre la representación femenina y masculina en distintos espacios de la política chilena durante 2024*. El proyecto busca evidenciar la notable baja participación del género femenino en cargos políticos y de toma de decisiones en Chile, mostrando cómo históricamente los hombres han ocupado la mayor parte de estos espacios de poder, representado a través de gráficos comparativos que permite observar de una manera clara la desigualdad de género presente en instituciones políticas como el Senado, la Cámara de Diputadas y Diputados y las alcaldías del país.

---

## *¿Qué se ve en pantalla?*

En la pantalla se observa una composición visual interactiva de un tamaño de 800x500 píxeles con una fotografía del Palacio de la Moneda de Chile con una pequeña trasnparencia y una mínima capa oscura para que se lea bien como fondo principal. A ambos lados aparecen ilustraciónes de figuras políticas femenina y masculina, mientras que en el centro se despliega un gráfico de barras comparativo que cambia mediante interacción del usuario.

Además, se visualizan sobres de votación animados que caen constantemente desde la parte superior de la pantalla, utilizando colores rojos y azules para simbolizar la desigualdad de representación política entre mujeres y hombres.

---

## *¿Qué elementos visuales aparecen?*

- Fotografía de fondo del Palacio de la Moneda de Chile.
- Ilustración de figura política femenina.
- Ilustración de figura política masculina.
- Panel central con gráficos de barras comparativos con datos verídicos del país.
- Sobres rojos y azules animados cayendo en pantalla.
- Título animado palpitante.
- Indicadores visuales de navegación.
- Textos explicativos y porcentajes.
- Textos con fuentes que confirman la información.

-----

# *Descripción Conceptual*

## *Idea central del proyecto y relación con el sistema diseñado*

Nuestro proyecto busca visibilizar la desigualdad de género en la política chilena mediante una traducción visual de estadísticas con porcentajes reales. El sistema convierte datos numéricos en relaciones visuales de tamaño, color, movimiento y cantidad.

Las barras comparativas permiten observar inmediatamente la diferencia entre representación masculina y femenina, mientras que la lluvia de los votos animados simbolizan la distribución desigual del poder político.

La interacción convierte la visualización en una experiencia dinámica que invita a reflexionar sobre la brecha de género en espacios importantes de toma de decisiones del país.

---

## *Regla de oro del sistema*

> “A mayor porcentaje masculino en el cargo político, mayor altura tendrá la barra azul y mayor cantidad de sobres azules aparecerán en pantalla.”

---

## *¿Cómo se relaciona esta lógica con la problemática de género?*

Cada componente visual representa directamente una desigualdad estructural existente en la política chilena.

- Los sobres azules predominan sobre los rojos para representar la mayor presencia masculina en los cargos políticos.
- La altura de las barras evidencia visualmente la diferencia de representación.
- El color de las barras femeninas cambia según el nivel de desigualdad:
  - Rojo fuerte → representación crítica
  - Rojo medio → representación baja
  - Rojo claro → acercamiento parcial a la paridad

De esta manera, el sistema no solo comunica datos, sino también genera una percepción visual de desequilibrio y desproporción al momento de representar las estadisticas analizadas.

---

# *Input / Output y Sistema*

## *¿Qué datos entran? (INPUT)*

- Clic del mouse del usuario.
- Posición horizontal del mouse (`mouseX`).
- Datos estadísticos reales sobre representación política.
- Contador de fotogramas (`frameCount`).

### *Datos utilizados*

| Institución | Mujeres | Hombres |
|---|---|---|
| Cámara de Diputadas/os | 35,5% | 64,5% |
| Senado | 24% | 76% |
| Alcaldías | 16,5% | 83,5% |
| Candidaturas Alcalde 2024 | 25% | 75% |

*Fuentes utilizada:* MinMujeryEG / CEPAL / El Mostrador 2024


---

## *¿Cómo se procesan y transforman?*

- `mousePressed()` cambia la estadística visualizada.
- `map()` transforma porcentajes en alturas visuales de barras.
- `random()` genera posiciones aleatorias para los sobres.
- `rotate()` aplica rotación dinámica a los votos en movimiento.
- `sin(frameCount)` genera pulsaciones suaves en el título.

---

## *¿Qué respuesta visual producen? (OUTPUT)*

- Cambio dinámico de gráficos comparativos.
- Modificación del color de las barras femeninas.
- Animación continua de votos cayendo.
- Título con efecto de pulso.
- Variación de brillo en textos interactivos
- Circulos inferiores de paginación.

---

# *Pensamiento Computacional*

## *Reglas que gobiernan el sistema*

| Elemento | Regla |
|---|---|
| Barras | `altura = map(porcentaje, 0, 100, 0, 160)` |
| Color barra mujer | Condicional según porcentaje |
| Votos | Nacen cada 4 frames |
| Color sobres | 15% rojos / 85% azul |
| Eliminación de votos | Se borran fuera de pantalla |
| Título | Pulso con `sin(frameCount)` |
| Brillo texto | `map(mouseX, 0, width, 120, 255)` |

---

## *Explicación del sistema de interactividad*

La interacción principal ocurre mediante clics del mouse en el rectangulo del centro. Cada clic cambia la categoría estadística visualizada mediante la variable `slideActual`.

Esto modifica:

- Altura de barras
- Porcentajes
- Colores
- Textos
- Datos visualizados

Además, el movimiento horizontal del mouse altera el brillo del texto inferior (Clic para cambiar estadística), generando una interacción secundaria bastante más sutil.

---

# *Referentes*

## *Referentes Visuales*

### *Barbara Kruger*
Artista visual feminista reconocida por utilizar tipografía, fotografía y mensajes políticos directos para cuestionar las estructuras de poder, el género y los medios de comunicación. Inspiró el uso de un contraste visual dentro del proyecto.

### *Wind Map*  
Visualización de corrientes de viento mediante partículas animadas, referente directo para el sistema de votos en movimiento.

### *Lotty Rosenfeld*
Artista chilena perteneciente a la Escena de Avanzada. Utilizó intervenciones urbanas y símbolos visuales para cuestionar el poder político y las estructuras patriarcales en Chile durante la dictadura. Referente por el uso del espacio visual como denuncia política.

---

## *Referentes Teóricos*

### *Feminism for the 99%*  
Texto sobre desigualdad estructural de género en sistemas políticos y económicos.

### *CEPAL*  
Fuente de datos estadísticos sobre igualdad de género en América Latina.

### *Ministerio de la Mujer y la Equidad de Género*  
Fuente oficial de indicadores de género utilizados en el proyecto.

### *Simone de Beauvoir*
Autora de “El segundo sexo”, obra fundamental para comprender la desigualdad histórica entre hombres y mujeres y la exclusión femenina en espacios de poder.

---

## *Referentes Históricos*

### *Sufragio femenino en Chile (1949)*  
Contexto histórico fundamental para comprender la representación política femenina en Chile.

## *Sufragistas chilenas*
Movimiento feminista que logró el derecho a voto femenino en elecciones presidenciales en Chile en 1949. Referente histórico clave para contextualizar la baja representación política femenina actual.

### *Revuelta feminista chilena de 2018*
Movimiento estudiantil y social que visibilizó masivamente desigualdades estructurales de género en Chile, utilizando performance, gráfica y activismo visual como herramientas de protesta. :contentReference[oaicite:1]{index=1}

### *CEPAL — Observatorio de Igualdad de Género*
Fuente oficial de estadísticas e investigaciones sobre participación política femenina en América Latina y Chile.

---

# *Diagrama de Flujo*

