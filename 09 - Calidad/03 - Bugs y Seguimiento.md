# Bugs y Seguimiento

## Registro

| ID | Bug | Severidad | Responsable | Estado |
| --- | --- | --- | --- | --- |
| BUG-001 | Algunos enemigos no atacaban y se saltaban su turno | Alta | Programación | Resuelto: el turno enemigo siempre actúa y deja pausas legibles antes y después |
| BUG-002 | La animación de muerte del primer enemigo no se veía cuando caía uno de tres | Media | Programación | Resuelto |
| BUG-003 | Sprites de iconos y diálogos importados como «Multiple» dejaban referencias de escena rotas | Media | Programación | Resuelto: se importan como sprite único |
| BUG-004 | El tutorial del mapa podía bloquear los clics si la zona resaltada no existía | Alta | Programación | Resuelto (2026-11-10): sin zona, el paso no bloquea |
| BUG-005 | El Acechador Oscuro se solapaba con el Corrupto errante en C1 | Baja | Programación | Resuelto: el desplazamiento solo se aplica detrás de una unidad grande |
| BUG-006 | El nombre del encuentro C2 aún mencionaba al Corrupto errante | Baja | Programación | Resuelto (2026-11-10) |
| BUG-008 | El Capitán usa un sprite provisional | Media | Arte | Resuelto (2026-11-13): el sprite actual es el definitivo |
| BUG-009 | Los héroes y enemigos no tienen animaciones propias (idle, ataque, daño, caída) | Media | Arte y Animación | Resuelto (2026-11-13): héroes, enemigos y capitán tienen animaciones por fotogramas |
| BUG-010 | La pantalla de créditos está prevista y no existe; tras el capitán se vuelve al mapa | Media | Programación | Resuelto (2026-11-13): epílogo y créditos implementados; falta probar el recorrido completo |
| BUG-011 | Requisitos mínimos de hardware sin medir | Media | QA | Abierto: depende de CP-12 |

> **Navegación:** [[00 - Índice]] · ← [[02 - Pruebas]] · [[04 - Criterios de Aceptación]] →
