# Backlog del Proyecto

## Descripción de la sección

El backlog contiene el trabajo necesario para convertir el diseño en un videojuego funcional.

## Formato de tarea

### Tarea

**Descripción:**

**Responsable:**

**Prioridad:** Alta / Media / Baja

**Dependencias:**

**Criterio de aceptación:**

**Estado:** Pendiente / En progreso / Bloqueada / Terminada

## Backlog

Responsable: *por asignar*. Las prioridades son una propuesta basada en el estado del proyecto al 2 de noviembre de 2026.

| Tarea | Prioridad | Estado | Dependencias | Criterio de aceptación |
|---|---|---|---|---|
| Documentar al capitán en [[03 - Enemigos y NPC]] (rol, estadísticas, habilidades, fases, IA) a partir de Unity | Alta | Pendiente | Datos del capitán en Unity | Misma estructura que los once enemigos |
| Documentar estadísticas base y crecimiento de los cuatro protagonistas | Alta | Pendiente | ScriptableObjects de Players | Cada protagonista tiene HP, ATK, DEF, SPD y XP por nivel en el GDD |
| Definir la recompensa del capitán en [[06 - Economía y Recursos]] (200 XP y 100 Coronas en el código) | Alta | Pendiente | — | Total de Coronas con jefe coherente en Economía, Niveles y Roadmap |
| Confirmar las existencias de la tienda (3 por producto en el código) y reflejarlas en el GDD | Media | Pendiente | — | GDD y código dicen lo mismo |
| Integrar `feature/sistema-combate` a `develop` por pull request | Alta | Pendiente | Revisión del equipo | CI de `develop` en verde |
| Partida completa de prueba: P1 a capitán | Alta | Pendiente | Integración | Recorrido sin errores bloqueantes |
| Prueba de desbloqueos y de La máscara rota | Alta | Pendiente | Partida de prueba | B2 cerrado hasta confirmar; Volver deja el evento pendiente |
| Pruebas automáticas de turnos, recompensas únicas y desbloqueos | Media | Pendiente | Test Framework (instalado) | Pruebas ejecutables en el editor |
| Confirmar pantalla de créditos tras vencer al capitán | Media | Pendiente | — | Créditos y regreso al menú |
| Pruebas de rendimiento a 1920x1080 y requisitos mínimos de hardware | Media | Pendiente | Build de Windows | 60 FPS en equipos de gama baja y media |
| Retirar paquetes de plantilla sin uso | Baja | Pendiente | — | Manifest sin Visual Scripting, Collaborate ni Learn IET |
| Completar secciones vacías del GDD (Trama, UI y Menús, UX, Guardado) | Media | Pendiente | — | Sin plantillas vacías |
| Paquete de entrega: build, instrucciones y repositorio | Media | Pendiente | Pruebas | Persona ajena completa la demo |

## Priorización

Prioriza aquello que desbloquea otras tareas o valida primero las partes más riesgosas del proyecto. Primero se alinea el GDD con lo ya implementado, después se integra y prueba el recorrido completo.


> **Navegación:** [[00 - Índice]] · ← [[03 - Roadmap]] · [[05 - Gestión de Cambios]] →
