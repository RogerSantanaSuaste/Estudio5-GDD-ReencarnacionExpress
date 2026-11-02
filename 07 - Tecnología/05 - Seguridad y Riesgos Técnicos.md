# Seguridad y Riesgos Técnicos

## Descripción de la sección

Documenta riesgos técnicos y medidas para reducir fallos, pérdida de datos o abuso de sistemas.

## Riesgos

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Errores en el orden de turnos o acciones duplicadas | Media | Alto | Una sola cola de turnos y verificación de una acción por unidad. Pruebas del criterio de aceptación de [[03 - Sistemas]]. |
| Recompensas duplicadas al repetir o cerrar un combate | Media | Alto | Marcar el encuentro como completado en la sesión antes de entregar XP y Coronas, y entregarlas en un único punto. |
| Pérdida o inconsistencia del estado al cambiar de escena | Media | Alto | Sesión centralizada en memoria; las escenas leen y devuelven datos a ella. |
| Desbloqueos incorrectos (B2 sin La máscara rota, capitán sin C1 y C2) | Media | Alto | Prueba de la puerta narrativa y del orden de desbloqueo ([[03 - Roadmap]]). |
| Doble clic en Iniciar combate o en la tienda | Alta | Medio | Deshabilitar el botón tras el primer clic y validar compras. |
| Balance de dificultad fuera de los rangos de rondas | Alta | Medio | Sistema de diagnóstico de balance con exportación a CSV. |
| Rendimiento por debajo de 60 FPS en equipos de gama baja | Baja | Medio | Uso limitado de efectos, pruebas de rendimiento en Windows a 1920 x 1080. |
| Conflictos y pérdida de archivos binarios en Git | Media | Medio | Git LFS para imágenes, sprites y música; escenas editadas por una sola persona a la vez. |
| Paquetes de la plantilla sin uso que aumentan el tamaño de la build | Baja | Bajo | Retirar paquetes innecesarios antes de la entrega. |
| Rama de combate sin integrar a `develop` ni `main` | Media | Alto | Integrar `feature/sistema-combate` por pull request y ejecutar el CI de `develop`. |
| Cambios de escena y assets que producen conflictos de merge | Media | Medio | Editar cada escena una persona a la vez; no renombrar ids ni valores serializados. |
| No hay pruebas automáticas (Test Framework instalado, sin tests) | Alta | Medio | Cubrir al menos turnos, recompensas únicas y desbloqueos con pruebas de editor. |

## Datos sensibles

No. La demo no almacena información personal, cuentas ni estadísticas en línea. El progreso no se escribe a disco ([[04 - Datos y Persistencia]]). La única escritura es el CSV opcional de diagnóstico de balance en `persistentDataPath`, que no contiene datos personales.

## Multijugador

No aplica. El juego es de un jugador y no requiere conexión.

## Recuperación

- Si el equipo es derrotado, el jugador abandona la partida o el programa se cierra, la sesión se pierde y se vuelve al menú principal. No existe corrupción de datos posible porque no hay archivos de guardado.
- No hay pérdida de conexión porque el juego no usa red.
- Ante un fallo de escena, el jugador puede iniciar una nueva partida desde el menú.


> **Navegación:** [[00 - Índice]] · ← [[04 - Datos y Persistencia]] · [[01 - Alcance]] →
