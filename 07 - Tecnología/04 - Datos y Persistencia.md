# Datos y Persistencia

## Datos de la sesión

La demo no tiene guardado permanente. Estos datos permanecen en memoria mientras la sesión está activa y se descartan si el equipo es derrotado o si el jugador abandona la partida:

- Progreso de los nueve encuentros, de La máscara rota y de El informe del último vigía; héroes caídos; reliquias poseídas y equipadas; existencias de la tienda.
- Inventario, Coronas y consumibles.
- Niveles, experiencia, vida y estadísticas.
- Regiones desbloqueadas y habilidades actuales de Noelle.

## Modelo de datos

Datos de contenido (fijos, definidos antes de jugar):

| Entidad | Campos principales |
|---|---|
| Protagonista | Nombre, clase, estadísticas base (vida, daño mínimo y máximo, protección, evasión, velocidad, crítico), crecimiento por nivel (vida por nivel y niveles en los que sube el daño) y habilidades (cuatro activas; Noelle tiene además el conjunto divino) |
| Enemigo | Nombre, vida, daño mínimo y máximo, protección, evasión, velocidad, crítico, jefe, ocupa dos posiciones, tamaño de la barra de vida, recorte del retrato, desplazamiento tras una unidad grande y habilidades |
| Habilidad | Tipo (ataque, curación, apoyo), objetivo, porcentaje de daño, daño base, posiciones del usuario y alcanzables, penetración, estados (potencia, duración, probabilidad), curación, movimiento, recarga y si se prepara |
| Encuentro | Identificador (P1 a C2, capitán), título, región, fondo, enemigos y posiciones, XP, Coronas, huida de los secuaces al caer el jefe |
| Reliquia | Identificador, nombre, descripción, icono, rareza, bonificaciones, desventajas, efecto especial, héroe exclusivo, disponible en tienda, precio, propiedad única, solo evento |
| Diálogo | Líneas con hablante, texto, luz y acción (por ejemplo, la máscara que se agrieta) |
| Consumible | Nombre, efecto, precio de compra y de venta, límite por inventario, existencias de la tienda |

Datos de la sesión (cambian al jugar):

| Entidad | Campos principales |
|---|---|
| Sesión | Coronas, consumibles, existencias de la tienda, encuentros y eventos completados, reliquias poseídas y equipadas, contador de combates sin reliquia, avisos de tutorial pendientes |
| Estado del protagonista | Id, nivel, XP, HP actual y máximo, caído (HP = 0), transformado (sí/no), estado curable |

Relaciones: la sesión contiene el estado de los cuatro protagonistas y la lista de encuentros completados. Cada encuentro referencia a sus enemigos, y cada enemigo y protagonista a sus habilidades.

## Formato

**Formato de guardado:** No aplica en la demo. El progreso no se escribe a disco ni usa `PlayerPrefs`.

**Ubicación:** Memoria de la sesión activa (`GameSession`, clase estática). Los datos de contenido son ScriptableObjects incluidos en la build.

**Excepción:** el diagnóstico de balance puede exportar `combat_metrics.csv` a `Application.persistentDataPath` durante el desarrollo. No es progreso del jugador.

**Versionado de datos:** No aplica en la demo. Los datos de contenido viajan dentro de la build.

## Migraciones

No aplica. Al no existir archivos de guardado, un cambio en la estructura de datos entre versiones no afecta a partidas anteriores.


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
