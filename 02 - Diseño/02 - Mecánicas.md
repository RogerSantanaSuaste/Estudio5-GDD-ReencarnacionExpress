# Mecánicas

## Mecánicas principales

### Mecánica 01: Combate táctico por turnos

**Propósito:**  
Constituye la mecánica central del videojuego. Permite al jugador enfrentarse a distintos enemigos mediante decisiones estratégicas, considerando los atributos de cada personaje, el orden de los turnos y las acciones disponibles.

**Activación:**  
El jugador selecciona un encuentro disponible en el mapa del mundo y presiona el botón Iniciar combate.

**Reglas:**  
- Los enfrentamientos se desarrollan por turnos.
- El jugador controla un equipo de cuatro protagonistas: Valerian, Elaina, Noelle y Evanora.
- El orden de actuación depende del atributo de velocidad de cada unidad.
- Cada personaje puede realizar una acción por turno, como utilizar una habilidad o consumir un objeto.
- El combate termina cuando todos los enemigos son derrotados o cuando los cuatro protagonistas están caídos.
- Un protagonista que llega a 0 HP no muere: queda caído y fuera de la acción hasta que se le cura.
- Los enemigos grandes (hoy el Guardián Corrupto) ocupan dos posiciones y no se mueven.

**Entrada:**  
Mouse: seleccionar habilidades, objetivos y acciones mediante los botones de la interfaz

**Estado inicial:**
El equipo del jugador y los enemigos aparecen en sus respectivas posiciones de combate, con sus atributos, habilidades y estados correspondientes.

**Estado final:**
El enfrentamiento concluye con una victoria o derrota. En caso de victoria, se procesan las recompensas y se habilita el regreso al mapa.

**Recursos utilizados:**
Puntos de vida (HP), habilidades, turnos, efectos de estado y objetos consumibles.

**Recompensa:**
Experiencia (XP), Coronas y avance en la progresión del mapa.

**Penalización:**
Pérdida de puntos de vida, aplicación de efectos negativos y posible derrota del equipo. Si todos los protagonistas son derrotados, la partida termina y se pierde el progreso de la sesión.

**Interacciones con otras mecánicas:**
Se relaciona directamente con el sistema de habilidades, las posiciones de combate, los efectos de estado, los consumibles y la progresión de personajes.

**Casos límite:**  
- Si un enemigo es derrotado antes de actuar, pierde su turno.
- Si una unidad no tiene objetivos válidos para una habilidad, no puede ejecutarla sobre un objetivo fuera de alcance.
- Si un protagonista llega a 0 HP, queda caído: no actúa ni puede ser objetivo de los enemigos hasta que reciba una Poción de curación o una curación de Noelle.
- Si todos los enemigos son derrotados, el combate termina y no deben generarse recompensas duplicadas.

### Mecánica 02: Sistema de habilidades y posiciones
**Propósito:**  
Aportar profundidad estratégica al combate mediante habilidades únicas para cada protagonista y restricciones de posicionamiento que obliguen al jugador a considerar cómo y cuándo utilizar sus acciones.

**Activación:**  
Durante el turno de un protagonista, el jugador selecciona una de sus habilidades disponibles y, cuando corresponde, elige un objetivo.

**Reglas:**  
- Cada protagonista tiene cuatro habilidades activas.
- Las habilidades pueden causar daño, curar, proteger, aplicar efectos de estado o modificar posiciones.
- Algunas habilidades tienen un tiempo de reutilización o _cooldown_ que impide utilizarlas en turnos consecutivos.
- Las habilidades cuentan con restricciones de posición del usuario y de alcance sobre sus objetivos.
- Los efectos negativos pueden incluir sangrado, veneno, quemadura, debilitamiento, vulnerabilidad y aturdimiento.
- Los efectos de estado tienen una duración determinada.
- Los efectos idénticos no se acumulan de manera ilimitada.
- Algunas habilidades permiten atacar a varios enemigos o modificar la posición de un personaje.
- El sistema de posiciones utiliza cuatro espacios por equipo.

**Entrada:**  
Mouse: seleccionar el botón de habilidad y después el objetivo correspondiente.

**Estado inicial:**
El personaje comienza su turno con sus habilidades disponibles según su posición, sus tiempos de reutilización y los efectos activos.

**Estado final:**
Se ejecuta la habilidad seleccionada, se aplican sus consecuencias y se actualizan los tiempos de reutilización y los estados de las unidades involucradas.

**Recursos utilizados:**
Turno del personaje, disponibilidad de habilidades, tiempos de reutilización, puntos de vida y efectos de estado.

**Recompensa:**
Ventaja táctica, eliminación de amenazas, protección de aliados, recuperación de vida o debilitamiento de enemigos.

**Penalización:**
Una habilidad utilizada en un momento inadecuado puede desperdiciar una oportunidad estratégica. Además, su tiempo de reutilización puede impedir utilizarla cuando resulte más necesaria.

**Interacciones con otras mecánicas:**
Combate por turnos, efectos de estado, inteligencia artificial, consumibles y transformación de Noelle.

**Casos límite:**  
- Una habilidad en cooldown o usada desde una posición no permitida aparece bloqueada y no puede ejecutarse.
- Si no hay objetivos válidos para una habilidad, no puede seleccionarse.
- Un efecto idéntico ya activo no se acumula de forma ilimitada.
- Tras La máscara rota, las habilidades enmascaradas de Noelle dejan de estar disponibles de inmediato.

### Mecánica 03: Exploración y progresión mediante el mapa

**Propósito:**  
Permitir al jugador avanzar a través de las diferentes regiones del videojuego, seleccionando encuentros, descubriendo eventos y desbloqueando nuevas zonas conforme supera desafíos.

**Activación:**  
El jugador accede al mapa al comenzar una nueva partida o después de completar un encuentro.

**Reglas:**  
- El mapa representa diferentes regiones del mundo mediante localizaciones interactivas.
- La progresión inicial se divide en tres zonas: Pradera, Bosque y Corrupción.
- Cada región contiene encuentros que deben completarse en un orden determinado.
- Los encuentros bloqueados pueden consultarse, pero no iniciarse.
- Completar los encuentros requeridos permite desbloquear nuevas localizaciones.
- Algunos lugares contienen eventos especiales en lugar de combates.
- Los encuentros completados permanecen registrados durante la sesión y no pueden otorgar recompensas nuevamente.
- El mapa permite acceder a la tienda (comprar y vender), al inventario y a la ficha de cada héroe, donde se equipan las reliquias. Tras ganar el primer combate, un tutorial interactivo enseña estas opciones.
- El progreso de la partida se mantiene durante la sesión de juego.

**Entrada:**  
Mouse: seleccionar localizaciones, consultar encuentros y utilizar el botón **Iniciar combate**.

**Estado inicial:**
Al iniciar una nueva partida, únicamente el primer encuentro de Pradera está disponible. Las demás localizaciones permanecen bloqueadas.

**Estado final:**
El jugador completa los encuentros disponibles y desbloquea progresivamente Bosque y Corrupción, acercándose al desafío final.

**Recursos utilizados:**
Estado de progresión de la sesión, encuentros disponibles, información del equipo y recursos del inventario.

**Recompensa:**
Acceso a nuevas regiones, encuentros, eventos narrativos, experiencia y Coronas obtenidas mediante combates.

**Penalización:**
El jugador no puede avanzar a una región mientras no cumpla las condiciones de desbloqueo. Si el equipo sufre una derrota total, pierde el progreso de la partida.

**Interacciones con otras mecánicas:**
Combate por turnos, progresión de personajes, economía, consumibles y eventos narrativos.

**Casos límite:**  
- Un encuentro bloqueado no puede iniciarse.
- Un encuentro completado no puede recompensar nuevamente al jugador.
- Si el jugador selecciona repetidamente el botón de iniciar combate, solo debe producirse una transición.
- El evento de Noelle debe completarse antes de continuar con determinados encuentros de Bosque.
- El informe del último vigía (Valdoria) debe completarse después de B3 para abrir C1.
- El capitán es el jefe final de la demo. Su encuentro permanece bloqueado hasta completar C1 y C2.

## Mecánicas secundarias

### 1. Progresión y subida de nivel

Los protagonistas obtienen experiencia al ganar combates. Al alcanzar la cantidad necesaria, suben de nivel y mejoran sus atributos.

Esta mecánica permite que el equipo aumente sus capacidades conforme se enfrenta a enemigos más peligrosos.

### 2. Sistema de economía y tienda

El jugador obtiene una moneda llamada **Coronas (CR)** al completar encuentros.
Las Coronas pueden utilizarse en la tienda del mapa para comprar consumibles y reliquias. También se obtienen vendiendo consumibles y reliquias sin equipar por el 50 % de su precio.
Los precios establecidos son:
- Poción de curación: 35 CR.
- Antídoto: 20 CR.
El jugador comienza una nueva partida con 50 Coronas, una poción y ningún antídoto.

### 3. Uso de consumibles

Los objetos permiten recuperar puntos de vida o eliminar determinados efectos negativos.
**Poción:** recupera el 30 % de la vida máxima de un aliado y levanta a un héroe caído.
**Antídoto:** elimina efectos de sangrado, veneno y quemadura.
Durante el combate, utilizar un consumible consume la acción del personaje correspondiente.
Cada tipo de consumible tiene un límite de cinco unidades en el inventario.
Solo la Poción de curación levanta a un héroe caído; el Antídoto no actúa sobre ellos.

### 4. Héroes caídos y recuperación

Los protagonistas no mueren. Al llegar a 0 HP caen al suelo, se atenúan y pasan a una casilla libre de la retaguardia; no actúan ni pueden ser objetivo. Tras la victoria se levantan con el 30 % de su vida máxima; quienes terminaron en pie conservan exactamente su vida. Durante el combate solo los levanta una Poción de curación o una curación de Noelle. Subir de nivel restaura la vida al 100 % de los héroes que no están caídos. El equipo conserva su progresión para el siguiente encuentro.

### 5. Transformación de Noelle

Noelle comienza la aventura utilizando habilidades convencionales mientras oculta su verdadera identidad.
Después de completar el primer encuentro de Bosque, el jugador puede acceder al evento narrativo **La máscara rota**.
Al completar este evento, Noelle intercambia sus cuatro habilidades convencionales por cuatro habilidades divinas. Sigue teniendo cuatro habilidades activas y las anteriores dejan de estar disponibles.
La transformación se mantiene durante el resto de la partida y no altera su nivel, experiencia ni atributos.
El evento solo puede completarse una vez por sesión y es obligatorio para continuar avanzando en Bosque.

### 6. Inteligencia artificial enemiga

Los enemigos seleccionan acciones automáticamente durante sus turnos.
Su comportamiento considera factores como disponibilidad de habilidades, posiciones, puntos de vida, estados activos y oportunidades estratégicas.
La dificultad aumenta progresivamente entre regiones, y los enemigos de Bosque y Corrupción utilizan decisiones tácticas más exigentes.
La intención es que el jugador deba planificar sus acciones en lugar de depender únicamente de ataques básicos.

### 7. Sistema de derrota y reinicio

Cuando todos los protagonistas son derrotados, la partida termina.
El jugador regresa al menú principal y pierde el progreso acumulado durante esa sesión.
Al comenzar una nueva partida, se reinician los niveles, recursos, encuentros completados y eventos narrativos.
La versión beta no incluye un sistema de guardado permanente.

### 8. Eventos narrativos

Algunas localizaciones del mapa contienen eventos especiales que afectan la historia o el desarrollo de los protagonistas.
Estos eventos pueden desbloquear nuevas capacidades o modificar la progresión.
Hay dos en la demo: **La máscara rota** (después de B1) y **El informe del último vigía**, en Valdoria (después de B3), que entrega el Broche del Vigía, revela al capitán y abre C1.
No todos los eventos necesitan otorgar recompensas económicas o experiencia.

### 9. Efectos de estado

Durante el combate, determinadas habilidades pueden aplicar condiciones temporales a aliados o enemigos.
Los principales efectos incluyen sangrado, veneno, quemadura, debilitamiento, vulnerabilidad, protección, regeneración y aturdimiento.
Cada efecto dispone de reglas de duración y aplicación que afectan las decisiones del jugador.
Estos estados permiten generar ventajas y desventajas tácticas sin depender exclusivamente del daño directo.

### 10. Interacción con localizaciones

El mapa incluye marcadores interactivos que permiten consultar los lugares disponibles y sus encuentros asociados.
Al seleccionar una localización, aparece un panel contextual con información sobre enemigos, recompensas y condiciones de acceso.
Los estados visuales permiten identificar lugares disponibles, completados, bloqueados o relacionados con eventos especiales.
Esta mecánica complementa la exploración y facilita la navegación por el mundo del juego.


### 11. Reliquias

Cada héroe tiene dos casillas de reliquia que se llenan desde el inventario en su ficha (solo fuera de combate). Las reliquias dan bonificaciones y casi siempre una desventaja, y muchas añaden un efecto especial: por ejemplo, el Colmillo de Lobo hace más daño a enemigos con Sangrado, Veneno o Quemadura, y el Ídolo del Último Aliento evita una derrota inmediata una vez por combate. Se obtienen como recompensa de la primera victoria de cada combate, en los eventos o en la tienda, y se pueden vender. Algunos enemigos también portan una durante el combate. El catálogo completo está en [[04 - Objetos y Coleccionables]].

### 12. Enemigos grandes

Un enemigo grande ocupa dos posiciones de la formación, al estilo de los jefes de *Darkest Dungeon*. Hoy solo es grande el Guardián Corrupto: se dibuja centrado entre sus dos posiciones, no se mueve, nadie puede ocupar su segunda posición y las habilidades de área lo alcanzan una sola vez.

### 13. Tutoriales interactivos

El primer combate incluye un tutorial guiado de combate. Al ganarlo, el mapa lanza un segundo tutorial que oscurece la pantalla y resalta cada zona: el jugador abre la tienda, compra, vende, abre el inventario y equipa una reliquia en la ficha de un héroe (el Altar le entrega una reliquia de práctica). Se puede saltar en cualquier momento con ENTER y solo aparece una vez por partida.

> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
