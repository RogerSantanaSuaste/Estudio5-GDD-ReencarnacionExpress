# Alcance

## Descripción de la sección

Define qué se va a construir y, sobre todo, qué queda fuera del proyecto.

## Alcance de la versión objetivo

La versión objetivo es una demo de un jugador para PC (Windows), hecha en Unity 6 y C#. Se juega con teclado y ratón, en español, a 1920×1080, y no requiere conexión. Una partida dura entre 30 minutos y 1 hora: no hay guardado permanente, así que la sesión y el recorrido completo son la misma partida.

El recorrido está fijado en [[01 - Estructura del Contenido]] y en [[03 - Sistemas]].

### Incluido

- Mundo de Aethel y tres regiones jugables: Llanuras Centrales (Pradera), Bosque Oscuro y Corrupción del Bosque.
- Nueve encuentros regulares: P1 a P4, B1 a B3 y C1 a C2. Cada encuentro completado paga experiencia y Coronas una sola vez.
- Evento obligatorio **La máscara rota**, después de B1. Noelle intercambia sus cuatro habilidades enmascaradas por Impacto Consagrado, Plegaria Focalizada, Bendición Continua y Amparo Divino. Conserva nivel, experiencia y estadísticas. El intercambio abre B2.
- Evento obligatorio **El informe del último vigía** (Valdoria), después de B3: entrega el Broche del Vigía, revela al capitán y abre C1. No da experiencia ni Coronas.
- El capitán de las fuerzas expedicionarias como jefe final, en el Trono Sellado, después de C1 y C2. La victoria purifica el bosque y muestra los créditos. La guerra contra el Rey Demonio continúa fuera de esta demo. En el proyecto de Unity el capitán otorga 200 XP y 100 Coronas, tiene fases de jefe y es inmune al aturdimiento.
- Cuatro protagonistas jugables: Valerian (caballero), Elaina (arquera), Noelle (clérigo) y Evanora (maga). La subida de nivel mejora las estadísticas según la clase.
- Once tipos de enemigos normales, con combate por turnos, posiciones, habilidades, efectos de estado e inteligencia artificial.
- Mapa de la sesión, escenas de diálogo del recorrido principal, tienda e inventario.
- Dos consumibles: Poción de curación (30 % de la vida máxima de un aliado; también levanta a un héroe caído; 35 Coronas, máximo cinco) y Antídoto (sangrado, veneno y quemadura, 20 Coronas, máximo cinco). La partida empieza con 50 Coronas y una poción.
- Reliquias: catálogo de 20 (12 universales y 8 exclusivas, dos por héroe), dos casillas por héroe, recompensa de combate y de eventos, y una tienda de cuatro espacios que se renueva con el avance. Consumibles y reliquias sin equipar se pueden vender por el 50 % de su precio.
- Tutoriales interactivos: uno en el primer combate y otro en el mapa, justo después de ganarlo (tienda, venta, inventario y reliquias).
- Héroes caídos en lugar de muertos: los enemigos no pueden atacarlos ni ellos actúan hasta que se les cura.
- Sesión en memoria. La derrota total, o abandonar la partida, borra el progreso y devuelve al menú principal. Los protagonistas no mueren: a 0 HP quedan caídos y siguen así tras la victoria hasta que se les cura con una Poción de curación o con una curación de Noelle. Subir de nivel restaura la vida al 100 % de quien siga en pie, y quienes terminan el combate vivos conservan su vida.

### No incluido

- Misiones secundarias. Quedaron descartadas como característica del proyecto, no reservadas para una versión posterior.
- NPC y personajes secundarios. Quedaron descartados como característica del proyecto. El recuento de la demo es cero y no hay una lista pendiente de diseño.
- Guardado permanente, continuación de partida y varias ranuras.
- Multijugador, otras plataformas, otros idiomas y funciones en línea.
- Mundo abierto, exploración libre y el Asentamiento Humano como zona jugable.
- Combate en tiempo real.
- Árboles de habilidades, reparto manual de puntos y desbloqueo de habilidades distintas del intercambio de Noelle.
- Armas y armaduras como objetos separados. El único equipo son las reliquias (dos casillas por héroe).
- Consumibles distintos de la Poción de curación y el Antídoto. No hay vendas ni pociones de daño extra.
- Combate contra el Rey Demonio y regiones posteriores, incluida la Forja de Combustión. Aparecen solo como contexto del cierre.
- Repetir las recompensas de un encuentro ya completado. Levantar a un héroe caído con la Poción de curación sí está permitido.

## MVP

El **Producto Mínimo Viable** debe contener únicamente lo necesario para demostrar que la experiencia principal funciona.

**MVP del proyecto:**

Una partida nueva llega al mapa, se juega P1 con los cuatro protagonistas y termina en victoria o en derrota total. La victoria entrega experiencia y Coronas, permite comprar en la tienda y devuelve al mapa. La derrota total cierra la sesión. Con eso queda demostrado el bucle de [[01 - Jugabilidad]]: mapa, combate por turnos, recompensa y preparación.

## Vertical Slice

El corte vertical es el Capítulo 1 completo, de punta a punta y con la dirección visual y sonora de las Llanuras Centrales.

Incluye Campamento del Alba (P1 y P2), Ruinas de Liria (P3 y P4), los tres tipos de goblin, 200 XP, 100 Coronas, la tienda, la introducción narrativa y el desbloqueo de Bosque Oscuro. El combate, el mapa y la interfaz deben poder leerse en una partida real. Este corte todavía no incluye La máscara rota ni al capitán.

## Criterios de recorte

Si el tiempo o los recursos no alcanzan, se recorta en este orden:

1. Variedad de animaciones, música adicional y pulido visual que no cambie la lectura del combate, del mapa o de los efectos de estado.
2. Extensión de las escenas de diálogo. Se conservan la introducción, **La máscara rota** y los cierres de victoria y derrota.
3. Complejidad del kit del capitán. El enfrentamiento se mantiene, aunque use menos habilidades que los once enemigos ya descritos.
4. El diagnóstico de balance exportado a CSV. Puede quedar como herramienta interna y salir de la build entregada.

No se recortan el combate por turnos, los cuatro protagonistas, los dos consumibles, las reglas de sesión, el intercambio de habilidades de Noelle ni el capitán como jefe final. Tampoco se reintroducen misiones secundarias ni NPC para sustituir contenido.


> **Navegación:** [[00 - Índice]] · ← [[05 - Seguridad y Riesgos Técnicos]] · [[02 - Roles y Responsabilidades]] →
