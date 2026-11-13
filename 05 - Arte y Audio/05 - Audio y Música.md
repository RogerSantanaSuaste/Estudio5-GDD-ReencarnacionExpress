# Audio y Música
## Música

Estilo: El estilo musical varía mucho según el entorno y momento, a veces puede ser algo Luffy, a veces puede ser más ambiental y en ocasiones puede ser tipo opera, blues, jazz y rock, a veces suele ser una fusión de varios géneros para lograr tramitar más sobre el entorno.

Instrumentación: guitarra eléctrica, sintetizadores virtuales, percusiones, voces corales, bajos, orquestas.

Temas principales:  
Tema del Menú Principal: Melodía introductoria, atmosférica, ambiental, sentimiento melancólico.

Tema de los actos:  
Muerte y reencarnación: Ambientación constante, staccatos para dar sensación de alerta, sentimiento de melancolía, violines trágicos, en la reencarnación la melodía es agridulce, hay más rítmica pero se nota que algo no anda bien.

Llanuras Centrales: Algo tranquilo, alegre, inspiración de island song de Adventure Time, percusiones sencillas y animadas, con una tensión ligera para dar a entender que aun siendo una llanura alegre, hay peligros de que cuidarse.  
  
Bosque Oscuro: Modo lidio para dar esa sensación de magia pero también de oscuridad, dar sensación de alerta de forma discreta, generar algo de tensión con Cheelos para dar ese toque mágico oscuro y fantasioso.  
  
Corrupción del Bosque: Modo Locrio, violines chillantes, notas agudas y graves de forma sincopadas, percusiones pesadas generando alerta a cada rato, notas super tensas con una melodía disonante que indican que algo no va bien.

  

Tema de Combate: High-tempo, percusivo y urgente, guitarras con distorsión generando entorno épico, recordándote que estás bajo ataque pero que aun tienes el control, tomando inspiración de Life Will Change de persona 5 royale.

  

Música dinámica: La música será dinámica según lo que pase en pantalla, según los escenarios y eventos, además se prioriza los efectos especiales como al comprar un objeto o desbloquear una región.

Tema Game over: Piano melancólico con violines exagerados entendiendo que todo terminó y no hay vuelta atrás.

Pistas implementadas en la demo: tema del menú, tema del mapa (entra con fundido), tema de combate y música de la introducción. Los créditos reutilizan el tema del menú. Los temas por región descritos arriba siguen siendo la intención de diseño.

## Efectos de sonido

Estado en la demo: todos los efectos de la tabla están implementados en Unity. Se crearon a partir de descripciones (generación con IA) y se ajustaron a mano a la animación: cada sonido de golpe se adelanta lo necesario para coincidir con el impacto visual.

| Evento                     | Sonido                                                                                                                                                                                                                  | Propósito                                                                      |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| Conversación de personajes | Cuatro voces sintéticas muy breves; cada pocas letras suena una al azar (sin repetir la anterior) mientras el texto se escribe, con volumen bajo.                                                                        | Dar a entender que los personajes hablan sin voces grabadas.                   |
| Botones y menús            | Un sonido de cursor al entrar en un botón y otro de clic al pulsar (también en Volver y en la X de Opciones); Nueva partida tiene su propio sonido. Suenan igual en introducción, mapa, tienda, combate, habilidades y reliquias de la ficha. En el mapa no suena el cursor sobre lugares bloqueados o ya completados. | Respuesta inmediata a cada interacción; el mapa solo suena donde hay misión.   |
| Inicio de combate          | Choque de espadas.                                                                                                                                                                                                      | Marcar la entrada al combate.                                                  |
| Selección de habilidad     | Sonido grave de selección inspirado en Darkest Dungeon, a volumen muy bajo.                                                                                                                                             | Confirmar la habilidad elegida.                                                |
| Ataque y habilidades       | Efecto propio para cada una de las 20 habilidades de los cuatro héroes y para todas las de los enemigos (incluido el capitán), con un adelanto por habilidad para coincidir con el golpe. Suenan de fondo, por debajo de la música. | Que cada ataque se identifique por el oído.                                    |
| Capitán (jefe)             | Sonidos propios de cada habilidad, de la entrada a fase 2, del aura de fase 2 (bucle suave) y de su derrota.                                                                                                             | Dar peso al jefe y señalar el cambio de fase.                                  |
| Curación                   | Un único sonido de curación compartido por las pociones, las habilidades de curación de los héroes (Auxilio improvisado, Plegaria focalizada, Bendición continua) y la del chamán enemigo.                                  | Reconocer cualquier curación al instante.                                      |
| Refuerzo                   | Sonido de mejora al recibir un beneficio de estado.                                                                                                                                                                      | Señalar que una unidad se fortalece.                                           |
| Cofre y tienda             | Efecto corto (0,4 s) de apertura, el mismo para ambos.                                                                                                                                                                   | Confirmar que se abre el panel.                                                |
| Comprar y vender           | Monedas que se gastan al comprar y monedas que se reciben al vender.                                                                                                                                                      | Dar sensación de intercambio.                                                  |
| Subida de nivel            | Efecto ascendente en la pantalla de Victoria cuando una barra se llena y el héroe sube de nivel.                                                                                                                         | Celebrar el progreso.                                                          |
| Equipar reliquia           | Deslizamiento metálico de anillo con un brillo mágico suave, al soltar la reliquia en una casilla válida.                                                                                                                | Confirmar el equipamiento.                                                     |
| Ataque crítico, fallo, estado alterado, objeto adquirido, pausa | Sin sonido propio todavía (se apoyan en el texto flotante y en los sonidos de interfaz).                                                                                                                    | Pendiente de diseño.                                                           |
## Audio espacial

No se utilizara audio espacial, se utilizara audio plano plano típico de juegos RPG 2D.


## Voz

Para diálogos hablados tanto para narradores y personajes, se utilizará un sintetizador grabe para voces hombre, sintesidar medio / agudo para voz de mujer, ambos son notas aleatorizadas en el sintetizador. 

Idiomas: El videojuego estará principalmente en Español, para la demo no habrá más idiomas.


## Mezcla

Prioridades y volumen relativo: la música de mapa y combate suena al mismo nivel que la del menú (ajustable en Opciones); los efectos de habilidad quedan de fondo, por debajo de la música; los sonidos de interfaz (cursor y clic) son moderados y las voces de escritura son las más bajas. En la introducción, la música y los ambientes bajan mientras habla el narrador.

Comportamiento ante eventos: no hay reducción automática de la música ante los efectos de combate; la jerarquía se consigue con los volúmenes fijos de cada grupo. La música del mapa y del combate entra con un fundido para no empezar de golpe.
> **Navegación:** [[00 - Índice]] · ← [[04 - Interfaz Visual]] · [[06 - Registro visual]] →