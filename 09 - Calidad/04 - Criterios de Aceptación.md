# Criterios de Aceptación

## Criterios por característica

### Orden de turnos

**Dado que** hay un combate en curso, **cuando** empieza una ronda, **entonces** las unidades vivas actúan de mayor a menor velocidad y cada una hace como máximo una acción.

### Habilidades y posiciones

**Dado que** un héroe está en una posición no permitida o su habilidad está en recarga, **cuando** el jugador abre su panel, **entonces** la habilidad aparece bloqueada y no se puede ejecutar.

### Héroe caído

**Dado que** un héroe llega a 0 HP, **cuando** termina esa acción, **entonces** queda caído, no actúa ni es objetivo de los enemigos, y sigue caído al ganar hasta que recibe una Poción de curación o una curación de Noelle.

### Poción de curación

**Dado que** el jugador tiene una poción, **cuando** la usa sobre un aliado, **entonces** restaura el 30 % de su vida máxima sin superarla, levanta al héroe si estaba caído y consume la acción del turno.

### Recompensas únicas

**Dado que** un encuentro ya fue completado, **cuando** se vuelve a ganar o a cargar, **entonces** no entrega Coronas, reliquia ni se puede iniciar de nuevo.

### Tienda

**Dado que** el jugador abre la tienda, **cuando** compra con fondos suficientes y espacio, **entonces** se descuentan las Coronas y el objeto entra en el inventario; sin fondos, sin espacio o agotado, la compra se rechaza con un mensaje.

### Venta

**Dado que** el jugador tiene un consumible o una reliquia sin equipar, **cuando** la vende, **entonces** recibe el 50 % del precio; una reliquia equipada, exclusiva o de evento no se puede vender.

### Reliquias

**Dado que** el jugador abre la ficha de un héroe fuera de combate, **cuando** arrastra una reliquia válida a una casilla, **entonces** se equipa y las estadísticas cambian; si no es válida, no se mueve y se indica el motivo. En combate no se puede cambiar el equipo.

### Subida de nivel

**Dado que** un héroe vivo alcanza la experiencia necesaria, **cuando** termina el combate, **entonces** sube de nivel, mejora sus estadísticas y recupera el 100 % de su vida.

### Eventos narrativos

**Dado que** se completó el combate previo, **cuando** el jugador abre el evento, **entonces** se muestra la escena una sola vez, se aplican sus efectos (La máscara rota: habilidades de Noelle y Fragmento; El informe del último vigía: Broche del Vigía) y se abre el siguiente encuentro.

### Enemigo grande

**Dado que** el Guardián Corrupto está en el campo, **cuando** se mueve cualquier unidad, **entonces** nadie ocupa su segunda posición y él no se mueve; las habilidades de área lo golpean una sola vez.

### Tutoriales

**Dado que** es la primera victoria de la partida, **cuando** el jugador llega al mapa, **entonces** se lanza el tutorial una sola vez, se puede saltar con ENTER y nunca bloquea los clics.

### Derrota

**Dado que** los cuatro héroes están caídos, **cuando** termina la acción, **entonces** se muestra la pantalla de Derrota y, al continuar, se vuelve al menú con la sesión descartada.

## Criterios del proyecto

| Criterio | Estado |
| --- | --- |
| El bucle principal funciona (mapa, combate, recompensa, preparación) | Cumplido en las pruebas parciales; falta el recorrido completo (CP-10) |
| Las condiciones de victoria y derrota funcionan | Cumplido; pendiente probar el flujo completo de derrota (CP-09) |
| Los sistemas principales están integrados | Cumplido: combate, sesión, tienda, reliquias, eventos y tutoriales |
| Las pruebas críticas están aprobadas | Parcial: CP-01 a CP-05 correctos; CP-07 a CP-12 pendientes |
| El rendimiento cumple el objetivo definido | Sin medir (CP-12) |
| No existen errores bloqueantes conocidos | Cumplido: sin bloqueantes abiertos (ver [[03 - Bugs y Seguimiento]]) |

> **Navegación:** [[00 - Índice]] · ← [[03 - Bugs y Seguimiento]] · [[01 - Glosario]] →
