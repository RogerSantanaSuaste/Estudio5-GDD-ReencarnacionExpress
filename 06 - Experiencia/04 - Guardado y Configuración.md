# Guardado y Configuración

## Descripción de la sección

Define cómo se conserva el progreso y qué opciones puede modificar el jugador.

## Guardado

**Tipo:** No hay.

**NO SE PLANEA INCLUIR SISTEMA DE GUARDADO EN ESTA DEMO.**

**Cuándo se guarda:** nunca. El progreso vive en memoria durante la sesión (clase estática `GameSession`) y se descarta al volver al menú, al ser derrotado o al cerrar el juego.

**Qué datos se mantienen durante la sesión:** niveles, experiencia y vida de los cuatro héroes (incluidos los caídos), Coronas, consumibles, reliquias poseídas y equipadas, existencias de la tienda, encuentros y eventos completados, estado de Noelle (enmascarada o no) y los avisos de tutorial pendientes.

**Cantidad de ranuras:** no aplica.

**Qué ocurre si el guardado falla:** no aplica; no se escribe a disco ni se usa `PlayerPrefs`. El progreso del jugador no se corrompe porque no se guarda.

## Configuración

| Categoría | Opciones |
| --- | --- |
| Audio | Volumen general y volumen de la música (controles deslizantes en Opciones del menú principal y de la pausa). Los efectos y las voces siguen el volumen general. |
| Video | Sin opciones. Resolución de referencia 1920 × 1080, ventana a pantalla completa. |
| Controles | Sin reasignación. Ratón para todo; Esc (pausa), ESPACIO (avanzar diálogo y tutorial), ENTER (saltar tutorial). |
| Accesibilidad | Ver [[03 - Accesibilidad]]. |
| Jugabilidad | Sin opciones: dificultad única. |

El volumen de la música se recuerda entre escenas durante la sesión, pero no se escribe a disco.

## Restablecimiento

Al iniciar una **Nueva partida** se reinician niveles, experiencia, vida, Coronas, consumibles, reliquias, tienda, encuentros, eventos y tutoriales. Los volúmenes conservan su valor de la sesión.

> **Navegación:** [[00 - Índice]] · ← [[03 - Accesibilidad]] · [[01 - Arquitectura Técnica]] →
