# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos de la sesión

La demo no tiene guardado permanente. Estos datos permanecen en memoria mientras la sesión está activa y se descartan si el equipo es derrotado o si el jugador abandona la partida:

- Progreso de los nueve encuentros y de La máscara rota.
- Inventario, Coronas y consumibles.
- Niveles, experiencia, vida y estadísticas.
- Regiones desbloqueadas y habilidades actuales de Noelle.

## Modelo de datos

Datos de contenido (fijos, definidos antes de jugar):

| Entidad | Campos principales |
|---|---|
| Protagonista | Nombre, clase, crecimiento de estadísticas por nivel, habilidades (cuatro activas; Noelle tiene además el conjunto divino) |
| Enemigo | Nombre, HP, ATK, DEF, SPD, habilidades, cooldowns |
| Habilidad | Efecto, poder, posiciones del usuario, posiciones alcanzables, cooldown, estado aplicado, duración |
| Encuentro | Identificador (P1 a C2, capitán), región, enemigos, XP, Coronas, requisitos de desbloqueo |
| Consumible | Nombre, efecto, precio, límite por inventario |

Datos de la sesión (cambian al jugar):

| Entidad | Campos principales |
|---|---|
| Sesión | Coronas, consumibles, existencias de la tienda, encuentros completados, estado de La máscara rota |
| Estado del protagonista | Id, nivel, XP, HP actual y máximo, transformado (sí/no), estado curable |

Relaciones: la sesión contiene el estado de los cuatro protagonistas y la lista de encuentros completados. Cada encuentro referencia a sus enemigos, y cada enemigo y protagonista a sus habilidades.

## Formato

**Formato de guardado:** No aplica en la demo. El progreso no se escribe a disco ni usa `PlayerPrefs`.

**Ubicación:** Memoria de la sesión activa (`GameSession`, clase estática). Los datos de contenido son ScriptableObjects incluidos en la build.

**Excepción:** el diagnóstico de balance puede exportar `combat_metrics.csv` a `Application.persistentDataPath` durante el desarrollo. No es progreso del jugador.

**Versionado de datos:** No aplica en la demo. Los datos de contenido viajan dentro de la build.

## Migraciones

No aplica. Al no existir archivos de guardado, un cambio en la estructura de datos entre versiones no afecta a partidas anteriores.


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
