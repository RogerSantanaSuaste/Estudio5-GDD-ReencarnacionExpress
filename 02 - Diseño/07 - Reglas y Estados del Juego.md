# Reglas y Estados del Juego

## Estados principales

- Menú principal
- Intro (animación de nueva partida)
- Carga
- Mapa
- Diálogo
- Combate (el primero incluye un tutorial interactivo)
- Tienda (compra y venta)
- Inventario y ficha de personaje (reliquias)
- Tutorial del mapa
- Pausa
- Victoria de combate
- Derrota
- Game Over
- Epílogo
- Créditos

## Transiciones

| Estado origen            | Evento                        | Estado destino      | Condición                        |
| ------------------------ | ----------------------------- | ------------------- | -------------------------------- |
| Menú principal           | Nueva partida                 | Intro               | —                                |
| Intro                    | Termina animación             | Mapa                | —                                |
| Mapa                     | Selecciona misión             | Diálogo             | La misión tiene escena previa    |
| Mapa                     | Selecciona misión             | Combate             | La misión no tiene escena previa |
| Diálogo                  | Termina escena                | Combate             | La misión tiene combate          |
| Diálogo                  | Termina escena                | Mapa                | La misión no tiene combate       |
| Combate                  | Todos los enemigos derrotados | Victoria de combate | —                                |
| Combate                  | Los 4 protagonistas caen      | Derrota             | —                                |
| Victoria de combate      | Confirmar recompensas         | Mapa                | Cualquier combate salvo el del capitán |
| Victoria de combate      | Confirmar recompensas         | Epílogo             | Combate contra el capitán        |
| Epílogo                  | Termina o se omite el diálogo | Créditos            | —                                |
| Derrota                  | Salir al menú                 | Menú principal      | —                                |
| Mapa                     | Interactuar con tienda        | Tienda              | —                                |
| Tienda                   | Salir                         | Mapa                | —                                |
| Mapa / Diálogo / Combate | Pausar                        | Pausa               | —                                |
| Pausa                    | Continuar                     | Estado anterior     | —                                |
| Créditos                 | Terminan o se omiten          | Menú principal      | La sesión se cierra              |

### Transiciones adicionales

| Estado origen | Evento | Estado destino | Condición |
| --- | --- | --- | --- |
| Victoria del primer combate | Confirmar recompensas | Mapa con tutorial interactivo | Solo la primera vez de la partida |
| Tutorial del mapa | Completar o saltar con ENTER | Mapa | — |
| Mapa | Botón Inventario o tarjeta de héroe | Inventario / ficha de personaje | — |
| Mapa | Evento narrativo (La máscara rota, El informe del último vigía) | Diálogo | El evento está disponible |
| Combate | Un protagonista llega a 0 HP | Héroe caído (sigue en el combate sin actuar) | — |

## Reglas globales

1. Los protagonistas no mueren: a 0 HP quedan caídos y, si el equipo gana, reviven al terminar el combate con el 30 % de su vida máxima. Quienes siguen en pie conservan la vida con la que cerraron el combate.
2. La Poción de curación solo se usa en combate. Cuesta la acción del personaje, restaura el 30 % de la vida máxima de un aliado y levanta a un héroe caído.
3. El juego se puede pausar desde el mapa, el diálogo y el combate.
4. El inventario admite hasta cinco Pociones de curación y cinco Antídotos. El Antídoto elimina sangrado, veneno y quemadura.
5. Subir de nivel restaura la vida al 100 % de los héroes que siguen en pie.
6. Las Coronas y la reliquia de un combate solo se entregan la primera vez que se gana.
7. Las reliquias solo se equipan o quitan fuera de combate. Cada héroe tiene dos casillas.
8. La tienda se puede usar para vender consumibles y reliquias sin equipar por el 50 % de su precio.
9. Un enemigo grande ocupa dos posiciones, no se mueve y nadie puede colocarse en la segunda.

## Casos especiales

- Si el jugador intenta iniciar un combate sin pociones suficientes o con el equipo en mal estado, el juego no lo impide. La responsabilidad de la preparación es del jugador.
- En la demo no hay guardado manual ni automático entre combates.
- La tienda solo está disponible desde el mapa.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
