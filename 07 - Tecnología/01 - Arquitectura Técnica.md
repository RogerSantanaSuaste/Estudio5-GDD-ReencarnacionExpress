# Arquitectura Técnica

## Descripción de la sección

Explica cómo está construido técnicamente el videojuego y cómo se comunican sus componentes.


## Arquitectura

```text
Entrada (mouse, ESC)
  ↓
Interfaz (Scripts/UI: menú, mapa, tienda, pausa · Scripts/Combat/UI: HUD de combate)
  ↓
Lógica de juego (TurnManager, PositionManager, MapProgression)
  ↓
Sistemas (AbilitySystem, estados, IA enemiga, progresión, consumibles)
  ↓
Datos (ScriptableObjects) + Sesión en memoria (GameSession)
  ↓
Presentación (escenas, sprites, audio)
```

## Componentes principales

| Componente | Responsabilidad | Dependencias |
|---|---|---|
| `GameSession` (estática) | Sesión en memoria: Coronas, consumibles, existencias de la tienda, encuentros completados, estado de cada protagonista (nivel, XP, vida, transformación). Se descarta con `EndSession()`. Sin `PlayerPrefs`. | Ninguna |
| `MapProgression` (estática) | Orden secuencial P1 → P4, B1, evento de Noelle, B2, B3, C1, C2 y BOSS. Deduce Bloqueado, Disponible o Completado a partir de `GameSession`. | `GameSession` |
| `WorldMapController` (parcial) | Mapa: localizaciones, ventana de misión, HUD, medallones, pausa y visuales. | `MapProgression`, `GameSession` |
| `MapShopController`, `ConsumableService` | Tienda e inventario. Compra con validación y uso de consumibles. | `GameSession` |
| `MainMenuController`, `MapPauseMenu` | Menú principal, pausa y confirmaciones. | `GameSession` |
| `TurnManager` | Orden por velocidad, un turno por unidad, victoria y derrota (`OnBattleWon`, `OnPartyDefeated`). | `BattleUnit`, `PositionManager` |
| `PositionManager`, `TargetSelector` | Posiciones de combate y validación de objetivos. | `BattleUnit` |
| `AbilitySystem`, `AbilityData`, `AbilityCooldownController`, `PreparedAbilityController` | Ejecución de habilidades, cooldowns, ataques anunciados y habilidades de área. | `StatusEffectController`, `DamageCalculator` |
| `StatusEffectController`, `StatusEffectType` | Aplicar y expirar estados: sangrado, marca, regeneración, aturdimiento, quemadura, debilitamiento, vulnerabilidad, veneno, aumento de defensa, guardia y objetivo prioritario. | `BattleUnit` |
| `EnemyAIController` (con `.Tactical` y `.Boss`), `EnemyAISettings` | IA enemiga que puntúa pares habilidad-objetivo, más lógica del jefe. | `AbilitySystem`, `TurnManager` |
| `BossPhaseController`, `BossPhaseData` | Fases del jefe según su vida. | `BattleUnit` |
| `EncounterData`, `EncounterLoader`, `CombatSessionBinder` | Carga del encuentro seleccionado y entrega de XP, Coronas y recuperación al terminar el combate. | `GameSession`, `TurnManager` |
| `CharacterProgression`, `CharacterProgressionData` | XP, subida de nivel y crecimiento por clase. | `GameSession` |
| `CombatMetrics`, `CombatMetricsCollector` | Diagnóstico de balance y exportación a CSV. | `TurnManager` |
| `CombatHudController` | HUD de combate. | Todos los de combate |

Escenas incluidas en la build: `Menu`, `IntroCinematic`, `Map` y `CombateIntegracion`.

## Comunicación

- **Estado compartido:** solo en `GameSession`. Las escenas lo leen al abrir y le devuelven resultados al cerrar. Por ser estática, no se duplica al cambiar de escena.
- **Eventos de C#:** los componentes se avisan con eventos (`OnBattleWon`, `OnPartyDefeated`, `OnBattleStarted`, `OnDefeated`, `OnEffectApplied`, `OnLevelUp`, `PhaseChanged`, etc.). La interfaz se suscribe a ellos.
- **Datos:** habilidades, unidades, encuentros, enemigos y progresión se definen como **ScriptableObjects** (`AbilityData`, `UnitData`, `EncounterData`, `EnemyArchetypeData`, `CharacterProgressionData`), separados de la lógica.
- **Mapa → combate:** el identificador del encuentro (P1, B2, BOSS…) viaja a `EncounterLoader`. El resultado vuelve a `GameSession`.

## Principios técnicos

- Bajo acoplamiento cuando sea razonable.
- Responsabilidades claras.
- Código mantenible.
- Datos separados de lógica cuando corresponda.
- Evitar dependencias innecesarias.
- Clases grandes divididas en archivos parciales (por ejemplo, `WorldMapController.*`).
- Los ids de encuentros y los valores serializados no se renombran para no romper assets y escenas. Los enums nuevos se agregan al final.

## Pendientes y diferencias con el GDD

- La tienda tiene existencias por producto (`StartingShopStock = 3`, sin reposición). El GDD no lo menciona.
- Hay una escena `IntroCinematic` y un `BossPhaseController` con fases para el capitán. El GDD todavía no documenta las fases ni la ficha de combate del capitán.
- El orden narrativo y de desbloqueo coincide con el GDD (P1 … B1 → La máscara rota → B2 … C2 → capitán).


> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
