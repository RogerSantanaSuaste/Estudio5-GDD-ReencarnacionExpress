# Registro visual

## Descripción de la sección

Documenta de dónde sale cada referencia visual del GDD, cuándo se obtuvo y en qué condiciones, para poder repetirla o sustituirla cuando el juego cambie. Todas las imágenes están en la carpeta `Media/` del repositorio.

## Estructura de la carpeta Media

| Carpeta | Contenido |
| --- | --- |
| `Media/Avance_2026-11-10/Interfaz` | Capturas del mapa, la tienda, la ficha de héroe, el tutorial, la victoria y la derrota |
| `Media/Avance_2026-11-10/Combate` | Capturas de combates de las tres regiones jugables |
| `Media/Avance_2026-11-10/Enemigos` | Hoja de retratos de los enemigos |
| `Media/Arte/Personajes` | Imágenes base de los héroes (copias reducidas) |
| `Media/Arte/Iconos` | Iconos oficiales de los héroes |
| `Media/Arte/Enemigos` | Los once sprites de enemigos |
| `Media/Arte/Reliquias` | Iconos de 20 reliquias |
| `Media/Arte/Estados` | Iconos de estado |
| `Media/Arte/Fondos` | Fondos de combate, menú principal, Santuario y Valdoria |
| `Sprites/` | Imágenes originales de héroes (con y sin máscara), iconos y los once enemigos, sin reducir |

## Condiciones de captura

- **Origen de las capturas:** ventana Game del editor de Unity 6 en modo Play, con la versión del proyecto del 2026-11-10. No son maquetas ni arte conceptual: muestran el juego tal como se ejecuta.
- **Relación de aspecto:** 16:9. Las copias del repositorio se reducen a 1600 px de ancho como máximo y se guardan en JPEG para mantener el repositorio ligero.
- **Arte original:** los sprites y fondos se guardan reducidos (PNG con transparencia hasta 512–600 px; fondos en JPEG de 1200 px). Los originales están en `Assets/Sprites/` del proyecto de Unity y no se duplican aquí.

## Inventario de capturas

| Archivo | Qué muestra | Sección donde se usa |
| --- | --- | --- |
| `Interfaz/Mapa_Mundo.jpg` | Mapa del Reino Aethel | [[02 - UI y Menús]], [[04 - Interfaz Visual]], [[03 - Entornos]] |
| `Interfaz/Ficha_Heroe_Noelle.jpg` | Ficha de héroe sin habilidades repetidas en el panel | [[02 - UI y Menús]], [[02 - Personajes y Animación]] |
| `Interfaz/Tienda_Vender.jpg` | Pestaña Vender | [[04 - Objetos y Coleccionables]] |
| `Interfaz/Tutorial_Tienda.jpg`, `Tutorial_Altar_Reliquia.jpg`, `Tutorial_Inventario.jpg`, `Tutorial_Final.jpg` | Pasos del tutorial interactivo del mapa | [[01 - UX y Flujo del Jugador]], [[02 - UI y Menús]] |
| `Interfaz/Evento_Valdoria.jpg` | Misión El informe del último vigía | [[05 - Misiones y Desafíos]] |
| `Interfaz/Victoria_Recompensas.jpg`, `Victoria_Nivel.jpg` | Victoria con recompensas y con subida de nivel | [[04 - Objetos y Coleccionables]], [[02 - UI y Menús]] |
| `Interfaz/Derrota.jpg` | Pantalla de derrota | [[02 - UI y Menús]] |
| `Interfaz/Reliquias_Hoja.jpg` | Hoja de iconos de reliquias | Referencia |
| `Interfaz/Menu_Principal.jpg`, `Introduccion_Cinematica_1.jpg`, `Introduccion_Dialogo.jpg`, `Dialogo_Santuario.jpg` | Menú principal, introducción y diálogos | [[02 - UI y Menús]] |
| `Interfaz/Pausa_Mapa.jpg`, `Ayuda_Mapa.jpg`, `Combate/Pausa_Combate.jpg` | Pausa y ayuda | [[02 - UI y Menús]] |
| `Combate/Pradera_P1.jpg`, `Pradera_P4.jpg`, `Bosque_B1.jpg`, `Bosque_B3.jpg`, `Jefe_Final.jpg` | Combates de Pradera, Bosque y jefe final (con unidades provisionales) | [[02 - Niveles]] |
| `Combate/Heroes_Combate.jpg` | Los cuatro héroes en C1 | [[02 - Personajes y Animación]], [[04 - Interfaz Visual]] |
| `Combate/Corrupcion_C1.jpg`, `Corrupcion_C2_Guardian.jpg` | Combates de Corrupción; el segundo con el Guardián Corrupto de dos posiciones | [[03 - Enemigos y NPC]] |
| `Combate/Pradera_Orden_Turno.jpg`, `Bosque_B2_Barras.jpg` | Combates de Pradera y Bosque | [[03 - Enemigos y NPC]] |
| `Enemigos/Retratos_Enemigos.jpg` | Retratos de los enemigos en el orden de turno | [[03 - Enemigos y NPC]] |

## Cómo actualizar

1. Ejecutar el juego en el editor y capturar la pantalla en 16:9.
2. Guardar la imagen en una carpeta `Avance_AAAA-MM-DD` con la fecha de la captura, en la categoría que corresponda.
3. Sustituir el enlace en la sección que la usa y actualizar este inventario.
4. Conservar el pie de imagen en cursiva: debe describir qué se ve, no solo el nombre de la pantalla.

## Pendiente

- Capturas de los combates P2, P3, B2, C1 y C2 con el arte actual, y del evento del Santuario.
- Capturas del tutorial de combate.
- Animaciones en GIF: el proyecto ya contiene fotogramas de animación de Valerian (reposo, ataques, defensa y heridas) que aún no se han convertido a GIF.
- Arte del Capitán de las Fuerzas Expedicionarias.

> **Navegación:** [[00 - Índice]] · ← [[05 - Audio y Música]] · [[01 - UX y Flujo del Jugador]] →
