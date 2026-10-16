# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

- Menú principal
- Intro (animación de nueva partida)
- Carga
- Mapa
- Diálogo
- Combate
- Tienda
- Pausa
- Victoria de combate
- Derrota
- Game Over
- Créditos

## Transiciones

| Estado origen       | Evento                          | Estado destino       | Condición                     |
|---------------------|---------------------------------|----------------------|-------------------------------|
| Menú principal      | Nueva partida                   | Intro                | —                             |
| Intro               | Termina animación               | Mapa                 | —                             |
| Mapa                | Selecciona misión               | Diálogo              | La misión tiene escena previa |
| Mapa                | Selecciona misión               | Combate              | La misión no tiene escena previa |
| Diálogo             | Termina escena                  | Combate              | La misión tiene combate       |
| Diálogo             | Termina escena                  | Mapa                 | La misión no tiene combate    |
| Combate             | Todos los enemigos derrotados   | Victoria de combate  | —                             |
| Combate             | Los 4 protagonistas caen        | Derrota              | —                             |
| Victoria de combate | Confirmar recompensas           | Mapa                 | —                             |
| Derrota             | Continuar                       | Mapa                 | —                             |
| Derrota             | Salir al menú                   | Menú principal       | —                             |
| Mapa                | Interactuar con tienda          | Tienda               | —                             |
| Tienda              | Salir                           | Mapa                 | —                             |
| Mapa / Diálogo / Combate | Pausar                     | Pausa                | —                             |
| Pausa               | Continuar                       | Estado anterior      | —                             |
| Mapa                | Completar demo                  | Créditos             | —                             |

## Reglas globales

1. La vida de los protagonistas se conserva al terminar un combate. No se regenera automáticamente.
2. Fuera de combate, usar una poción de vida restaura el 100% de la vida de todos los protagonistas.
3. El juego se puede pausar desde el mapa, el diálogo y el combate.
4. Las pociones de vida, daño extra y antídoto tienen límites de inventario (3, 4 y 4 respectivamente).

## Casos especiales

- Si el jugador intenta iniciar un combate sin pociones suficientes o con el equipo en mal estado, el juego no lo impide. La responsabilidad de la preparación es del jugador.
- En la demo no hay guardado manual ni automático entre combates.
- La tienda solo está disponible desde el mapa.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
