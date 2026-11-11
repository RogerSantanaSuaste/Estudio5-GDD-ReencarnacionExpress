# Pruebas

## Descripción de la sección

Define cómo se comprobará que el videojuego funciona como fue diseñado y recoge las pruebas ya ejecutadas.

## Tipos de prueba

### Pruebas funcionales

Comprueban que una característica haga lo que debe. Se ejecutan en modo Play de Unity y con las herramientas de prueba del proyecto (`BattleTest`, `AbilityTest`, `MovementTest`, `StatusEffectTest` y `ExperienceTest`).

### Pruebas de integración

Comprueban que varios sistemas funcionen juntos: combate con sesión, mapa con tienda, tutorial con ventanas reales, reliquias con estadísticas. Se recorren los flujos mapa → combate → victoria → mapa.

### Pruebas de usabilidad

Comprueban si los jugadores entienden y pueden utilizar el sistema: primeros minutos, tutoriales, tienda y ficha de héroe. Se hacen con integrantes del equipo y con jugadores externos que no han leído el GDD.

### Pruebas de rendimiento

Comprueban FPS, memoria, tiempos de carga y estabilidad. Objetivo: 60 FPS a 1920 × 1080.

### Diagnóstico de balance

El sistema de métricas de combate genera un informe por encuentro (rondas, daño real, vida final, consumibles usados, recompensas) y puede exportar `combat_metrics.csv`. Las rondas esperadas son 2–4 en Pradera, 4–6 en Bosque y 5–7 en Corrupción.

## Casos de prueba

| ID | Caso | Resultado esperado | Estado |
| --- | --- | --- | --- |
| CP-01 | Vender una Poción de curación y otra vez sin existencias | +18 CR la primera vez; la segunda se rechaza con mensaje | Correcto (Play, 2026-11-10) |
| CP-02 | Vender una reliquia equipada, una libre y una ya vendida | La equipada se rechaza; la libre paga el 50 % (por ejemplo 25 CR); la vendida se rechaza | Correcto (Play, 2026-11-10) |
| CP-03 | Recorrer el tutorial del mapa completo | Abrir tienda, comprar, vender, cerrar, abrir inventario, abrir ficha, abrir inventario desde la casilla y equipar la reliquia de práctica; termina en el mensaje final | Correcto (Play automatizado, 2026-11-10) |
| CP-04 | C2: movimiento con el Guardián Corrupto de dos posiciones | El Guardián no se mueve y el Acechador no puede entrar en su segunda posición | Correcto (Play, 2026-11-10) |
| CP-05 | Usar una Poción sobre un héroe caído | El héroe se levanta con el 30 % de su vida máxima | Correcto (Play, al implementarlo) |
| CP-06 | Subir de nivel con el héroe vivo y con el héroe caído | El vivo recupera el 100 %; el caído sigue caído | Correcto el caso vivo (Play); caso caído pendiente |
| CP-07 | Antídoto sobre un héroe caído | Se rechaza con mensaje | Pendiente |
| CP-08 | Repetir un encuentro completado | No se puede iniciar ni entrega recompensas | Pendiente |
| CP-09 | Derrota total | Pantalla de Derrota y vuelta al menú con la sesión descartada | Pendiente (recorrido completo) |
| CP-10 | Recorrido completo P1 → capitán | Los diez encuentros y los dos eventos se completan en orden sin errores | Pendiente |
| CP-11 | Balance por región | Rondas dentro de los rangos esperados | Pendiente (tras subir el Guardián Corrupto a 65 HP) |
| CP-12 | Rendimiento | 60 FPS en el mapa y el combate | Pendiente |

> **Navegación:** [[00 - Índice]] · ← [[01 - Criterios de Calidad]] · [[03 - Bugs y Seguimiento]] →
