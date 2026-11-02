# Motor y Herramientas

## Descripción de la sección

Documenta las herramientas utilizadas para crear el videojuego y por qué fueron seleccionadas.

## Motor

**Motor:** Unity 6

**Versión:** 6000.6.4f1

**Renderizado:** Universal Render Pipeline (URP 17.6.0) con renderer 2D.

**Física:** Física 2D de Unity. El combate es por turnos y no depende de colisiones.

**Sistema de entrada:** Input System 1.20.0 (`activeInputHandler` = Input System). Mouse como entrada principal y ESC para cerrar paneles (ver [[04 - Controles]]).

## Lenguajes

| Lenguaje | Uso |
|---|---|
| C# | Toda la lógica de juego, sistemas, IA e interfaz (≈ 67 scripts en `Assets/Scripts` y `Assets/Editor`). |

## Herramientas

| Herramienta | Propósito | Versión |
|---|---|---|
| Unity Editor | Motor y editor del proyecto | 6000.6.4f1 |
| Visual Studio / Visual Studio Code / Rider | Edición de código C# (el proyecto incluye integración con Visual Studio y Rider) | Sin fijar |
| Git y Git LFS | Control de versiones. LFS para imágenes, sprites y música | Sin fijar |
| GitHub | Repositorio privado `ReencarnacinExprs` | — |
| GitHub Actions | CI sobre la rama `develop` (rama `feature/configurar-ci`): comprueba estructura, versión de Unity y Git LFS | — |
| Herramientas de editor propias | `BossBalanceHarness` (balance del jefe), `CombatHudPreviewWindow`, `SceneGuides`, `SceneViewFraming`, `GameViewResolution` | — |
| Obsidian | Edición y navegación del GDD | — |

## Dependencias

Paquetes de Unity (`Packages/manifest.json`):

| Paquete | Versión | Uso |
|---|---|---|
| Universal Render Pipeline | 17.6.0 | Renderizado 2D |
| Input System | 1.20.0 | Entrada |
| uGUI | 2.6.0 | Botones y paneles (incluye TextMeshPro) |
| 2D Animation | 16.0.1 | Animación de sprites |
| 2D Sprite, Tilemap, Tilemap Extras, SpriteShape, Tooling | 1.0.0 / 1.0.0 / 9.0.1 / 16.0.0 / 4.0.1 | Arte 2D y mapa |
| 2D PSD Importer, 2D Aseprite Importer | 15.0.1 / 6.0.0 | Importación de arte |
| Timeline | 6.6.0 | Secuencias |
| Test Framework | 1.8.0 | Pruebas (aún no hay pruebas en el proyecto) |
| AI Assistant, AI Inference | 2.20.0-pre.2 / 2.6.1 | Herramientas de editor; no forman parte del juego |
| Visual Scripting, Collaborate, Learn IET | 1.9.12 / 2.13.6 / 6.0.7 | Heredados de la plantilla; sin uso en el diseño |

No hay servicios externos ni conexión a internet ([[03 - Público y Plataforma]]).

## Convenciones del proyecto

- **Estructura de carpetas:**
  - `Assets/Scripts`: `Combat` (Abilities, Core, Diagnostics, Effects, Encounters, UI, Units), `Core`, `UI`.
  - `Assets/ScriptableObjects`: Abilities, Encounters, Enemies, Players, UI.
  - `Assets/Sprites`, `Assets/Art`, `Assets/Audio`, `Assets/Fonts`, `Assets/Prefabs`, `Assets/Scenes`, `Assets/Editor`.
  - `Docs`: documentos de diseño y balance, y capturas.
- **Nomenclatura:** clases en PascalCase. Los datos usan el prefijo del personaje o enemigo (por ejemplo, `Elaina_MarcaDelCazador`) y los encuentros usan sus ids (P1, B2, C1, BOSS).
- **Control de versiones:** ramas `main`, `develop` y `feature/*` (por ejemplo, `feature/sistema-combate`, `feature/menu-principal`). Commits en formato `feat:` y `merge:`.
- **Formato de assets:** pixel art para iconos y efectos ([[01 - Dirección de Arte]]); música en WAV.
- **Convenciones de código:** comentarios en español al inicio de cada clase, clases estáticas para la sesión y eventos de C# para comunicar componentes.


> **Navegación:** [[00 - Índice]] · ← [[01 - Arquitectura Técnica]] · [[03 - Requisitos Técnicos]] →
