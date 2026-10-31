# Roadmap

## Descripción de la sección

El roadmap organiza el desarrollo en etapas y entregables.

## Etapas

La demo recorre un solo mundo, Aethel, en tres capítulos, nueve encuentros, el evento obligatorio **La máscara rota** y el enfrentamiento contra el capitán de las fuerzas expedicionarias. El orden de trabajo sigue las dependencias de [[01 - Estructura del Contenido]]: Llanuras Centrales, Bosque Oscuro, Corrupción del Bosque y, al final, el Trono Sellado.

Cada etapa indica a su encargado según [[02 - Roles y Responsabilidades]]. El estado del proyecto parte de la ficha: el concepto, el alcance inicial, la mecánica principal y un prototipo funcional ya existen. El corte vertical, la producción completa, las pruebas y la versión entregable siguen pendientes.

### Concepto

**Objetivo:**
Definir qué demo se va a construir y qué experiencia debe demostrar. El encargado de la etapa es Santana Suaste Roger Emmanuel. Esta etapa está cerrada.

**Entregables:**

- Ficha del proyecto: RPG de combate por turnos, un jugador, PC (Windows), Unity 6 y C#.
- Visión y pilares: cuatro protagonistas reencarnados, el jugador como deidad que los guía, combate táctico, mapa de eventos, progresión y administración de consumibles.
- Premisa de la demo: detener la amenaza inmediata sobre las Llanuras Centrales al derrotar al capitán. La guerra contra el Rey Demonio continúa después de ese cierre.
- Bucle principal: seleccionar una misión en el mapa, combatir, obtener experiencia y Coronas, preparar al equipo y desbloquear el siguiente tramo.
- Criterio de éxito: una demo jugable que integre narrativa, estrategia y progresión, con mapa, cuatro protagonistas, combates regulares, jefe de zona, efectos de estado y tienda.

### Preproducción

**Objetivo:**
Convertir el prototipo de combate en un corte vertical del Capítulo 1 y dejar cerrado todo el diseño que la producción necesita para no detenerse. El encargado de la etapa es Herrera Pérez Ángel Daniel.

**Entregables:**

- Prototipo funcional del combate por turnos, con orden por velocidad, posiciones, habilidades, daño, defensa y fin del encuentro. Este entregable ya existe y sirve de base al corte vertical.
- Corte vertical del Capítulo 1, Llanuras Centrales: Campamento del Alba (P1 y P2), Ruinas de Liria (P3 y P4), los tres tipos de goblin, recompensas de 200 XP y 100 Coronas, tienda accesible desde el mapa y desbloqueo de Bosque Oscuro.
- Reglas de sesión aplicables a toda la demo: sin guardado permanente, recompensas únicas por encuentro, derrota total de regreso al menú principal y pérdida del progreso de esa partida. Tras una victoria, los personajes derrotados regresan con el 40 % de su vida máxima y quienes siguen en pie conservan la vida del cierre del combate.
- Economía cerrada para la demo: el jugador empieza con 50 Coronas y una Poción de curación; el Antídoto se compra; cada consumible admite hasta cinco unidades, a 35 y 20 Coronas. La poción restaura el 50 % de la vida máxima de un aliado vivo. El Antídoto solo quita sangrado, veneno y quemadura.
- Ficha de combate del capitán, con el mismo nivel de detalle que los once enemigos ya documentados: rol, estadísticas, habilidades, inteligencia artificial y condición de victoria. Sin esta ficha no se produce el enfrentamiento final.
- Dirección de arte y temas musicales por zona, suficientes para distinguir Llanuras, Bosque, Corrupción, combate, menú y derrota.

### Producción

**Objetivo:**
Construir el recorrido completo de la demo en el orden en que el jugador lo desbloquea. El encargado de la etapa es Reyes Chan Erick Gilberto. El audio de cada bloque lo coordina Romano Chávez Steven.

**Entregables:**

- Cuatro protagonistas jugables, con su rol de combate: Valerian como caballero, Elaina como arquera, Noelle como clérigo y Evanora como maga. La subida de nivel mejora las estadísticas según la clase. En la demo no hay reparto manual de puntos ni árboles de habilidades.
- Mapa de la sesión, con las localizaciones del recorrido: Campamento del Alba, Ruinas de Liria, Claro del Susurro, Santuario Velado, Sendero Sombrío, Tierras Marchitas y Trono Sellado. Cada lugar muestra si está disponible, bloqueado o completado.
- Capítulo 2, Bosque Oscuro. Después de P4 se abre el Claro del Susurro (B1, dos lobos salvajes). **La máscara rota** se activa en el Santuario Velado, sustituye las cuatro habilidades de Noelle por Impacto Consagrado, Plegaria Focalizada, Bendición Continua y Amparo Divino, no otorga experiencia ni Coronas y es obligatorio para entrar a B2. El Sendero Sombrío contiene B2 y B3, con bandido, lobo, chamán y guardián forestal. Las recompensas del capítulo son 300 XP y 120 Coronas. Al terminar se desbloquea Corrupción.
- Capítulo 3, Corrupción del Bosque. Tierras Marchitas contiene C1 y C2, con corrupto errante, acechador oscuro, hechicero corrupto y guardián corrupto. Las recompensas del capítulo son 300 XP y 120 Coronas. Completar ambos encuentros habilita al capitán.
- Jefe y desenlace en el Trono Sellado. La victoria purifica el sector corrompido del bosque, las fuerzas supervivientes se retiran hacia la Forja de Combustión y los protagonistas regresan como héroes del primer tramo. La derrota total corta el vínculo del jugador con Aethel y devuelve al menú principal.
- Escenas narrativas del recorrido principal: introducción de la reencarnación, **La máscara rota** y los cierres de victoria y derrota. El texto de cada misión principal acompaña a su encuentro. El proyecto no incluye NPC ni misiones secundarias.
- Tienda del mapa, inventario y uso de la Poción de curación y del Antídoto durante el turno de un protagonista.
- Pase visual y sonoro de las tres zonas, de los once enemigos, de los cuatro protagonistas, del capitán y de la interfaz de mapa, combate y tienda. El idioma de la demo es español.

### Pruebas

**Objetivo:**
Recorrer la demo de principio a fin y comprobar que la progresión, la economía y la dificultad coinciden con lo documentado. La encargada de la etapa es Concepción Jaimes Lizbeth.

**Entregables:**

- Partida completa sin interrupciones: menú, P1 a P4, B1, **La máscara rota**, B2, B3, C1, C2 y capitán.
- Prueba de la puerta narrativa: B2 permanece cerrado hasta confirmar **Romper la máscara**. La opción **Volver** deja el evento pendiente. La transformación de Noelle se conserva el resto de la sesión y no cambia su nivel ni sus estadísticas.
- Prueba de recompensas: 200 XP y 100 Coronas en Llanuras, 300 XP y 120 Coronas en Bosque, 300 XP y 120 Coronas en Corrupción. Un encuentro ya completado no vuelve a pagar. El evento de Noelle no entrega experiencia ni Coronas.
- Prueba de economía: con 50 Coronas iniciales y ninguna compra, el recorrido de los nueve encuentros termina en 390 Coronas. La tienda rechaza compras sin fondos y respeta el tope de cinco unidades por consumible.
- Prueba de derrota: si los cuatro protagonistas caen, la sesión termina y una partida nueva empieza otra vez en Llanuras Centrales, con Noelle enmascarada.
- Revisión de dificultad por capítulo: Llanuras en dificultad baja a media, Bosque en media-alta a alta y Corrupción en dificultad alta. Los encuentros deben poder resolverse dentro de los rangos de rondas documentados en [[02 - Niveles]].
- Informe de bloqueantes, balance y rendimiento en Windows a 1920×1080, con el objetivo de 60 FPS en equipos de gama baja y media. Los requisitos mínimos de hardware se anotan a partir de estas pruebas.

### Publicación / Entrega

**Objetivo:**
Entregar una demo de Windows que pueda jugarse de principio a fin y cuyo GDD describa esa misma versión. El encargado de la etapa es Santana Suaste Roger Emmanuel.

**Entregables:**

- Build de Windows, en español, jugable con teclado y ratón.
- Recorrido verificable de Aethel: nueve encuentros, **La máscara rota**, jefe y los dos cierres de la demo.
- Créditos al completar la victoria contra el capitán.
- Lista de problemas conocidos que no impiden terminar la demo.
- GDD actualizado a la versión entregada, con el historial de versiones y el estado del proyecto alineados a la build.
- Paquete de entrega académica: build, instrucciones de ejecución y enlace o copia del repositorio.

## Hitos

| Hito | Entregable | Criterio de finalización | Estado |
|---|---|---|---|
| Concepto de la demo | Ficha, visión, pilares y premisa | El equipo puede explicar el bucle, la plataforma y el cierre de la demo sin recurrir a decisiones orales | Terminada |
| Prototipo de combate | Encuentro jugable por turnos | Un combate se resuelve con velocidad, posiciones, habilidades, daño y una condición clara de victoria o derrota | Terminada |
| Contenido de la demo | Estructura, niveles, enemigos, objetos y misiones | Quedan descritos un mundo, tres zonas, nueve encuentros, once enemigos, dos consumibles, el intercambio de habilidades de Noelle y el capitán como jefe final | Terminada |
| Corte vertical | Capítulo 1 jugable de punta a punta | P1, P2, P3 y P4 se completan en una sesión, pagan 200 XP y 100 Coronas, permiten usar la tienda y desbloquean Bosque Oscuro | Pendiente |
| Ficha del capitán | Diseño de combate del jefe | Rol, estadísticas, habilidades e inteligencia artificial quedan documentados al mismo nivel que el resto de enemigos | Pendiente |
| Bosque Oscuro | Capítulo 2 integrado | B1, **La máscara rota**, B2 y B3 se juegan en ese orden; Noelle intercambia sus cuatro habilidades y Corrupción queda desbloqueada | Pendiente |
| Corrupción del Bosque | Capítulo 3 integrado | C1 y C2 se vencen con los cuatro tipos de enemigos corruptos y habilitan el Trono Sellado | Pendiente |
| Desenlace de la demo | Jefe, victoria y derrota | Derrotar al capitán purifica el bosque y muestra los créditos. La caída del equipo devuelve al menú y borra la sesión | Pendiente |
| Pase de pruebas | Informe del recorrido completo | No quedan errores bloqueantes en progresión, economía, evento, jefe ni rendimiento acordado | Pendiente |
| Entrega | Build de Windows y GDD de esa versión | Una persona ajena al desarrollo ejecuta la demo y completa el recorrido de Aethel con las instrucciones entregadas | Pendiente |


> **Navegación:** [[00 - Índice]] · ← [[02 - Roles y Responsabilidades]] · [[04 - Backlog del Proyecto]] →
