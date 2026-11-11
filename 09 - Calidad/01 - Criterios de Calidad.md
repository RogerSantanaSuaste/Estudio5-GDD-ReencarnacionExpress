# Criterios de Calidad

## Descripción de la sección

Define qué significa que una característica esté correctamente terminada.

## Calidad funcional

- [ ] Funciona según las reglas documentadas en el GDD (los números del juego y los del documento coinciden).
- [ ] No produce errores conocidos críticos ni mensajes de error en la consola de Unity.
- [ ] Maneja casos límite importantes: inventario lleno, fondos insuficientes, héroe caído, objetivo fuera de alcance, pulsaciones repetidas.
- [ ] No entrega recompensas duplicadas ni permite repetir un encuentro completado.
- [ ] Respeta el orden de turnos y el máximo de una acción por unidad y turno.

## Calidad de experiencia

- [ ] El jugador entiende el objetivo de cada pantalla sin leer el código ni el GDD.
- [ ] Las respuestas del juego son claras: cada acción produce un cambio visible (barra, texto flotante, mensaje).
- [ ] La dificultad es coherente con la región: Pradera 2 a 4 rondas, Bosque 4 a 6, Corrupción 5 a 7.
- [ ] La interfaz es comprensible: las opciones bloqueadas se distinguen y explican su motivo.
- [ ] Los textos no se cortan ni se solapan a 1920 × 1080.
- [ ] Los tutoriales no pueden dejar al jugador atascado.

## Calidad técnica

- [ ] Rendimiento aceptable: 60 FPS objetivo.
- [ ] Sin errores críticos en la consola durante un recorrido completo.
- [ ] No existen dependencias rotas: referencias de escena, sprites y datos de contenido enlazados.
- [ ] La sesión se reinicia por completo al empezar una nueva partida.
- [ ] La build de Windows arranca y recorre menú, mapa, combate y victoria.

## Definición de terminado

Una característica se considera terminada cuando:

1. Está implementada en Unity y conectada a sus escenas y datos, sin pasos manuales pendientes.
2. Se probó en modo Play sin errores en la consola y, si afecta al combate, con al menos un encuentro de cada región que la use.
3. Sus reglas y números están reflejados en el GDD y en el [[04 - Historial de Versiones]] cuando cambian.
4. Cumple sus criterios de [[04 - Criterios de Aceptación]].
5. Los fallos encontrados quedaron registrados en [[03 - Bugs y Seguimiento]] y no queda ninguno crítico abierto.

> **Navegación:** [[00 - Índice]] · ← [[05 - Gestión de Cambios]] · [[02 - Pruebas]] →
