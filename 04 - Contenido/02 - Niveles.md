# Niveles

## Descripción de la sección

Cada nivel debe documentar su propósito jugable, estructura, dificultad, contenido y condiciones de entrada/salida.

## Plantilla de nivel

### Capítulo 1: Pradera

**Objetivo principal:**
Introducir al jugador a las mecánicas fundamentales del combate por turnos y completar los cuatro encuentros disponibles para desbloquear la siguiente región.

**Objetivos secundarios:**
- Familiarizarse con las habilidades y características de los cuatro protagonistas.
- Aprender a seleccionar objetivos según su posición y nivel de amenaza.
- Comprender el funcionamiento de los turnos, el daño y la defensa.
- Obtener experiencia y Coronas para fortalecer al equipo y adquirir consumibles.

**Duración estimada:**
Entre 2 y 4 rondas por encuentro. El capítulo contiene cuatro combates, por lo que se estima una duración total de 8 a 16 rondas, sin contar el tiempo de navegación por el mapa.

**Dificultad:**
Baja a media. Funciona como la introducción al sistema de combate, aunque los últimos encuentros requieren mayor atención a la selección de enemigos y al uso de habilidades.

**Mecánicas introducidas:**
- Combate táctico por turnos.
- Orden de actuación basado en velocidad.
- Selección de habilidades y objetivos.
- Posiciones de combate y restricciones de alcance.
- Daño, defensa y puntos de vida.
- Recompensas de experiencia y Coronas.

**Mecánicas utilizadas:**
Uso de habilidades ofensivas y defensivas, tiempos de reutilización, selección estratégica de objetivos, progresión de personajes y recuperación después del combate.

**Enemigos / obstáculos:**
El capítulo cuenta con tres tipos de enemigos:
- Goblin común: enemigo básico especializado en ataques cuerpo a cuerpo.
- Goblin arquero: enemigo capaz de realizar ataques a distancia.
- Goblin bruto: enemigo con mayor resistencia y capacidad ofensiva.
Estos enemigos aparecen en diferentes combinaciones durante los cuatro encuentros de la región.

**Recompensas:**
- 200 XP en total por completar los cuatro encuentros.
- 100 Coronas en total.
- Experiencia para mejorar los atributos de los protagonistas.
- Desbloqueo de la región Bosque.
- Recuperación de vida después de cada victoria.

**Puntos de guardado:**
No existen puntos de guardado. El progreso se conserva temporalmente durante la sesión activa, pero se pierde al abandonar la partida o sufrir una derrota total.

**Condición de entrada:**
Iniciar una nueva partida desde el menú principal. Pradera es la primera región disponible.

**Condición de salida:**
Completar los cuatro encuentros de la región (P1, P2, P3 y P4), derrotando a todos los enemigos correspondientes.

**Eventos narrativos:**
No existe actualmente un evento narrativo independiente implementado en esta región. Su función principal es presentar el sistema de combate y establecer el inicio del recorrido.

**Mapa / diagrama:**
```text
INICIO DE PARTIDA
       |
       v
    PRADERA
       |
       v

    P1 → P2
       |
       v

    P3 → P4
       |
       v
Bosque desbloqueado
```

### Capítulo 2: Bosque

**Objetivo principal:**
Superar los tres encuentros de la región y completar el evento narrativo **La máscara rota**, permitiendo que Noelle desbloquee sus habilidades divinas y que el equipo continúe hacia Corrupción.

**Objetivos secundarios:**
- Enfrentarse a enemigos con mayor velocidad y nuevas habilidades.
- Aprender a contrarrestar efectos de estado como el veneno y el debilitamiento.
- Priorizar enemigos de apoyo que pueden curar o fortalecer a sus aliados.
- Aprovechar las habilidades de protección y curación.
- Adaptarse a las nuevas capacidades de Noelle después de su transformación.

**Duración estimada:**
Entre 4 y 6 rondas por encuentro. El capítulo contiene tres combates, por lo que se estima una duración total de 12 a 18 rondas, más el tiempo dedicado al evento narrativo.

**Dificultad:**
Media-alta a alta. Los enfrentamientos presentan enemigos con comportamientos más estratégicos y requieren mayor atención a las habilidades, posiciones y estados del equipo.

**Mecánicas introducidas:**
- Enemigos con habilidades de apoyo y curación.
- Mayor presencia de efectos de estado.
- Enemigos capaces de fortalecer su defensa.
- Evento narrativo obligatorio.
- Transformación de Noelle y sustitución de habilidades.

**Mecánicas utilizadas:**
Combate táctico, protección de aliados, habilidades curativas, efectos positivos y negativos, administración de cooldowns, uso de consumibles y selección de objetivos prioritarios.

**Enemigos / obstáculos:**
El capítulo cuenta con cuatro tipos de enemigos:
- Lobo salvaje: enemigo veloz con ataques físicos y posibilidad de aplicar veneno.
- Bandido: enemigo ofensivo que puede debilitar a los protagonistas.
- Chamán del bosque: enemigo de apoyo capaz de curar aliados y aplicar efectos negativos.
- Guardián forestal: enemigo resistente que puede aumentar su defensa.

La región también presenta un obstáculo de progresión: el jugador debe completar el evento de Noelle antes de acceder a los últimos encuentros.

**Recompensas:**
- 300 XP en total por los tres encuentros.
- 120 Coronas en total. 
- Desbloqueo de las cuatro habilidades divinas de Noelle mediante el evento La máscara rota.
- Desbloqueo de Corrupción.
- Recuperación de vida después de cada victoria.
El evento de Noelle no entrega experiencia ni Coronas adicionales.

**Puntos de guardado:**
No existen puntos de guardado permanentes. Los encuentros completados, la transformación de Noelle y los recursos obtenidos permanecen registrados únicamente durante la sesión activa.

**Condición de entrada:**
Haber completado los cuatro encuentros de Pradera.

**Condición de salida:**
Derrotar a los enemigos de B1, completar La máscara rota y superar B2 y B3.

**Eventos narrativos:**
**La máscara rota:** evento obligatorio disponible después del primer combate de Bosque. El jugador accede al Santuario Velado, donde Noelle abandona su etapa enmascarada y desbloquea sus habilidades divinas.

Este cambio permanece durante el resto de la partida y permite continuar hacia el siguiente encuentro.

**Mapa / diagrama:**
```text
Bosque desbloqueado
        |
        v

        B1
        |
        v
   Santuario Velado
   LA MÁSCARA ROTA
        |
        v

      B2 → B3
        |
        v
Corrupción desbloqueada
```

### Capítulo 3: Corrupción

**Objetivo principal:**
Superar los enfrentamientos más exigentes de la demo, utilizando las habilidades adquiridas y administrando correctamente la vida, los estados y los recursos del equipo.

**Objetivos secundarios:**
- Identificar y eliminar enemigos prioritarios.
- Contrarrestar efectos negativos de mayor peligro.
- Proteger a los personajes más vulnerables.
- Utilizar estratégicamente las habilidades divinas de Noelle.
- Administrar consumibles y curaciones para mantener vivo al equipo.  
- Prepararse para el futuro enfrentamiento contra el jefe final.

**Duración estimada:**
Entre 5 y 7 rondas por encuentro como objetivo de balance. El capítulo contiene dos combates, por lo que se estima una duración total de 10 a 14 rondas.

La duración real puede variar según las decisiones del jugador y el comportamiento enemigo.

**Dificultad:**
Alta — Exigente. Es la región de mayor dificultad entre los encuentros normales de la demo.

**Mecánicas introducidas:**
- Combinaciones de enemigos con gran poder ofensivo.
- Mayor presión mediante daño periódico.
- Enemigos con alta resistencia y habilidades defensivas.
- Selección táctica avanzada de objetivos por parte de la IA.

**Mecánicas utilizadas:**
Todas las mecánicas principales aprendidas anteriormente: combate por turnos, posiciones, protección, curación, habilidades ofensivas, estados alterados, administración de cooldowns, consumibles y selección estratégica de objetivos.

**Enemigos / obstáculos:**
El capítulo cuenta con cuatro tipos de enemigos:
- Corrupto errante: enemigo físico capaz de aplicar sangrado.
- Acechador oscuro: enemigo ofensivo de gran velocidad y ataques poderosos.
- Hechicero corrupto: enemigo mágico que utiliza quemaduras y debilitamientos defensivos.
- Guardián corrupto: enemigo de gran resistencia, capaz de fortalecer su defensa y ejecutar ataques de alto daño.

Las diferentes combinaciones enemigas buscan obligar al jugador a administrar sus recursos y tomar decisiones estratégicas.


**Recompensas:**
- 300 XP en total por los dos encuentros.
- 120 Coronas en total.
- Experiencia y progresión adicional para los protagonistas.
- Cumplimiento de los requisitos para acceder al futuro jefe final.
- Recuperación de vida después de cada victoria.

**Puntos de guardado:**
No existen puntos de guardado. Si el equipo completo es derrotado, termina la sesión y el jugador debe comenzar una nueva partida.

**Condición de entrada:**
Haber completado los tres encuentros de Bosque y el evento La máscara rota.

**Condición de salida:**
Derrotar a todos los enemigos de C1 y C2.

**Eventos narrativos:**
No existe todavía un evento narrativo independiente implementado para esta región. Su función actual es presentar la amenaza más importante del recorrido y preparar el acceso al jefe final.

**Mapa / diagrama:**
## Flujo del nivel

```
```text
Corrupción desbloqueada
          |
          v

          |
       C1 → C2
          |
          v
    Trono Sellado
       (Jefe)
```



## Criterios de calidad

- El objetivo es comprensible.
- Las reglas se pueden aprender.
- El desafío corresponde al nivel de progresión.
- Existe retroalimentación suficiente.
- El jugador entiende por qué tuvo éxito o fracaso.


> **Navegación:** [[00 - Índice]] · ← [[01 - Estructura del Contenido]] · [[03 - Enemigos y NPC]] →
