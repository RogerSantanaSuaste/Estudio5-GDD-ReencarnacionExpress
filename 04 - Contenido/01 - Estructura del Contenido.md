# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

```Reencarnación Express
│
├── Mundo: Aethel
│   │
│   ├── Capítulo 1: Pradera
│   │   ├──
│   │   │   ├── Encuentro P1: Dos goblins comunes
│   │   │   └── Encuentro P2: Goblin común y arquero
│   │   │
│   │   └── 
│   │       ├── Encuentro P3: Dos goblins y arquero
│   │       └── Encuentro P4: Goblin bruto,
│   │           goblin común y arquero
│   │
│   ├── Capítulo 2: Bosque
│   │   ├── 
│   │   │   └── Encuentro B1: Dos lobos salvajes
│   │   │
│   │   ├── Santuario Velado
│   │   │   └── Evento: La máscara rota
│   │   │       └── Transformación de Noelle
│   │   │
│   │   └── 
│   │       ├── Encuentro B2:
│   │       │   Bandido, lobo y chamán
│   │       └── Encuentro B3:
│   │           Guardián forestal,
│   │           bandido y chamán
│   │
│   ├── Capítulo 3: Corrupción
│   │   └── 
│   │       ├── Encuentro C1:
│   │       │   Corrupto errante,
│   │       │   acechador y hechicero
│   │       └── Encuentro C2:
│   │           Guardián corrupto,
│   │           corrupto errante
│   │           y hechicero
│   │
│   └── Final de la demo (planeado)
│       └── 
│           └── Jefe final demo
│              
│
└── Fin del recorrido disponible
```

## Cantidad estimada

| Tipo                 | Cantidad |
| -------------------- | -------: |
| Mundos               |        1 |
| Zonas jugables       |        3 |
| Niveles / encuentros |        9 |
| Enemigos             | 11 tipos |
| Jefes                |        1 |
| NPC                  |        1 |
| Objetos              |        2 |

## Dependencias

¿Qué contenido debe existir antes de otro?

El contenido de Reencarnación Express sigue una progresión principalmente lineal. Para acceder a determinados encuentros o eventos, el jugador debe haber completado previamente otros desafíos.
### Dependencias entre regiones

**Pradera → Bosque**

El jugador debe completar P1, P2, P3 y P4 para desbloquear Bosque.

**Bosque → Corrupción**

El jugador debe completar los encuentros de Bosque y el evento obligatorio de Noelle para desbloquear Corrupción.

**Corrupción → Jefe final**

El jugador debe completar C1 y C2 para cumplir el requisito de progresión hacia el jefe final.
### Dependencias narrativas

El evento La máscara rota solo puede activarse después de completar B1.

Su realización es obligatoria para continuar hacia B2 y permite que Noelle desbloquee sus habilidades divinas.

La transformación permanece activa durante el resto de la sesión.
### Dependencias de progresión

Los personajes obtienen experiencia y Coronas al completar encuentros.

Los niveles y recursos obtenidos ayudan al equipo a afrontar las siguientes zonas, cuya dificultad aumenta progresivamente.

Los encuentros ya completados no pueden volver a generar recompensas.

> **Navegación:** [[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
