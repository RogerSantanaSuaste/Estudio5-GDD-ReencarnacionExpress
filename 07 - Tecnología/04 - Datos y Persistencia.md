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

Describe las entidades y relaciones.

## Formato

**Formato de guardado:** No aplica en la demo. El progreso no se escribe a disco.

**Ubicación:** Memoria de la sesión activa.

**Versionado de datos:**

## Migraciones

¿Qué ocurre si cambia la estructura de los datos entre versiones?


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
