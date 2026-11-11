# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

```Reencarnación Express
Reencarnación Express
│
└── Mundo: Aethel
    │
    ├── Capítulo 1: Llanuras Centrales
    │   ├── Campamento del Alba
    │   │   ├── P1: Dos goblins comunes
    │   │   └── P2: Goblin común y arquero
    │   └── Ruinas de Liria
    │       ├── P3: Dos goblins comunes y arquero
    │       └── P4: Goblin bruto, común y arquero
    │
    ├── Capítulo 2: Bosque Oscuro
    │   ├── Claro del Susurro
    │   │   └── B1: Tres lobos salvajes y chamán
    │   ├── Santuario Velado
    │   │   └── Evento: La máscara rota
    │   │       └── Transformación divina de Noelle
    │   └── Sendero Sombrío
    │       ├── B2: Dos bandidos, lobo y chamán
    │       └── B3: Guardián forestal, dos bandidos y chamán
    │
    ├── Valdoria
    │   └── Evento: El informe del último vigía
    │       └── Revela al capitán y abre Corrupción
    │
    ├── Capítulo 3: Corrupción del Bosque
    │   └── Tierras Marchitas
    │       ├── C1: Dos corruptos errantes, acechador y hechicero
    │       └── C2: Guardián corrupto (ocupa dos posiciones), acechador y hechicero
    │
    └── Jefe final
        └── Capitán de las fuerzas expedicionarias
            ├── Enfrentamiento final
            └── Purificación del bosque
```

## Cantidad estimada

| Tipo                 | Cantidad |
| -------------------- | -------: |
| Mundos               |        1 |
| Zonas jugables       |        3 |
| Niveles / encuentros |        9 |
| Enemigos             | 11 tipos |
| Jefes                |        1 |
| NPC                  |        0 |
| Objetos              |        2 |

## Dependencias

¿Qué contenido debe existir antes de otro?

El contenido de Reencarnación Express sigue una progresión principalmente lineal. Para acceder a determinados encuentros o eventos, el jugador debe haber completado previamente otros desafíos.
### Dependencias entre regiones

**Llanuras Centrales → Bosque Oscuro**

El jugador debe completar P1, P2, P3 y P4 para desbloquear Bosque.

**Bosque  Oscuro→ Corrupción del Bosque**

El jugador debe completar los encuentros de Bosque, el evento obligatorio de Noelle y El informe del último vigía (Valdoria) para desbloquear Corrupción.

**Corrupción del Bosque → Jefe final**

El jugador debe completar C1 y C2 para enfrentar al capitán, jefe final de la demo.
### Dependencias narrativas

El evento La máscara rota solo puede activarse después de completar B1.

Su realización es obligatoria para continuar hacia B2. Noelle intercambia sus cuatro habilidades enmascaradas por cuatro habilidades divinas. Las anteriores dejan de estar disponibles.

La transformación permanece activa durante el resto de la sesión.

El evento El informe del último vigía solo puede activarse después de completar B3. Su realización es obligatoria para abrir C1: entrega el Broche del Vigía y revela que el capitán espera en el Trono Sellado.
### Dependencias de progresión

Los personajes obtienen experiencia y Coronas al completar encuentros.

Los niveles y recursos obtenidos ayudan al equipo a afrontar las siguientes zonas, cuya dificultad aumenta progresivamente.

Los encuentros ya completados no pueden volver a generar recompensas.

> **Navegación:** [[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
