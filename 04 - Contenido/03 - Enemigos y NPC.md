# Enemigos y NPC

## Descripción de la sección

## Relación de los enemigos con la historia

Los enemigos de Reencarnación Express aparecen durante el avance de los protagonistas por las Llanuras Centrales y el Bosque Oscuro, donde se desarrolla el conflicto contra las fuerzas expedicionarias del Rey Demonio.

En Pradera, el equipo se enfrenta a diferentes grupos de goblins mientras aprende a combatir y avanza por los territorios humanos amenazados.

En Bosque, aparecen lobos salvajes, bandidos, chamanes y guardianes forestales. Estos enfrentamientos representan los peligros del territorio en el que operan las fuerzas expedicionarias.

En Corrupción, los protagonistas enfrentan criaturas corruptas que reflejan el deterioro provocado en parte del Bosque Oscuro. Estos enemigos representan una amenaza mayor y preparan al equipo para el enfrentamiento final.

La historia todavía no establece la afiliación individual de todos los tipos de enemigos. Por ello, no se considera automáticamente que cada criatura encontrada sea un miembro directo de las fuerzas del Rey Demonio.

El capitán de las fuerzas expedicionarias se contempla como antagonista final de la demo.

# Capítulo 1: Llanuras Centrales

## Enemigo 01: Goblin común

**Rol de combate:**
Atacante cuerpo a cuerpo básico.

**Comportamiento:**
Realiza ataques físicos contra los protagonistas que se encuentran dentro de su alcance. Su inteligencia artificial utiliza principalmente ataques básicos, aunque ocasionalmente puede ejecutar una habilidad más poderosa.

**Vida:** 45 HP.
**Daño:** 9 ATK.
**Defensas:** 2 DEF.
**Velocidad:** 7 SPD.

**Rango de detección:**
No aplica como distancia de exploración. Durante el combate selecciona objetivos válidos según el alcance de sus habilidades.

**Ataques:**
- **Garrotazo:** ataque físico básico, sin tiempo de reutilización.
- **Golpe Torpe:** ataque físico de mayor potencia, con cooldown de tres turnos.
    

**Debilidades:**
Su baja defensa y cantidad de vida lo hacen vulnerable a ataques físicos y mágicos. Su alcance cuerpo a cuerpo también limita los objetivos que puede atacar.

**Recompensa:**
Forma parte de encuentros que entregan 50 XP y 25 Coronas al completarse. No entrega recompensas individuales.

**Estados de IA:**
Evaluar objetivos → Seleccionar ataque disponible → Atacar o reposicionarse → Finalizar turno.

---

## Enemigo 02: Goblin arquero

**Rol de combate:**
Atacante físico a distancia.

**Comportamiento:**
Utiliza ataques a distancia para dañar a los protagonistas desde posiciones posteriores. Puede atacar a diferentes objetivos según su alcance y aprovechar ataques especiales cuando están disponibles.

**Vida:** 35 HP.
**Daño:** 10 ATK.
**Defensas:** 1 DEF.
**Velocidad:** 10 SPD.

**Rango de detección:**
No aplica como detección en tiempo real. Sus ataques pueden alcanzar distintas posiciones enemigas según las restricciones de sus habilidades.

**Ataques:**
- **Flechazo:** ataque básico a distancia.
- **Disparo Preciso:** disparo de mayor potencia, con cooldown de tres turnos.
    

**Debilidades:**
Tiene poca vida y defensa, por lo que puede ser eliminado rápidamente mediante ataques de largo alcance.

**Recompensa:**
Incluida en la recompensa global del encuentro: 50 XP y 25 Coronas.

**Estados de IA:**
Evaluar objetivos → Verificar alcance → Seleccionar disparo → Atacar o reposicionarse → Finalizar turno.

---

## Enemigo 03: Goblin bruto

**Rol de combate:**
Atacante resistente de primera línea.

**Comportamiento:**
Utiliza ataques físicos potentes y busca presionar a los personajes que se encuentran al frente del equipo. Su resistencia es superior a la de los demás goblins.

**Vida:** 65 HP.
**Daño:** 11 ATK.
**Defensas:** 4 DEF.
**Velocidad:** 5 SPD.

**Rango de detección:**
No aplica como distancia de exploración. Sus ataques son principalmente cuerpo a cuerpo.

**Ataques:**
- **Mazazo:** ataque físico básico.
- **Pisotón:** ataque de mayor potencia que tiene una probabilidad del 20 % de aplicar debilitamiento de ataque durante un turno. Cooldown de tres turnos.
    

**Debilidades:**
Su velocidad reducida permite que varios protagonistas actúen antes que él. Puede ser debilitado mediante efectos negativos y ataques concentrados.

**Recompensa:**
Forma parte de los encuentros de Pradera, que otorgan 50 XP y 25 Coronas por victoria.

**Estados de IA:**
Evaluar objetivos → Seleccionar ataque → Atacar o reposicionarse → Finalizar turno.

---

# Capítulo 2: Bosque Oscuro

## Enemigo 04: Lobo salvaje

**Rol de combate:**
Atacante rápido de cuerpo a cuerpo.

**Comportamiento:**
Aprovecha su velocidad para atacar y puede concentrar ocasionalmente sus ataques sobre protagonistas debilitados. Sus habilidades pueden provocar daño periódico.

**Vida:** 75 HP.
**Daño:** 15 ATK.
**Defensas:** 4 DEF.
**Velocidad:** 13 SPD.

**Rango de detección:**
No aplica en exploración. Sus habilidades ofensivas tienen alcance cuerpo a cuerpo.

**Ataques:**
- **Mordida:** ataque físico básico.
- **Colmillo Venenoso:** ataque con potencia adicional y 35 % de probabilidad de aplicar veneno de 3 HP durante dos turnos. Cooldown de dos turnos.
    

**Debilidades:**
Depende de su alcance cuerpo a cuerpo y puede ser neutralizado mediante protección, control de posiciones y ataques concentrados.

**Recompensa:**
Incluida en los encuentros de Bosque, que entregan 100 XP y 40 Coronas por victoria.

**Estados de IA:**
Evaluar objetivos → Identificar oportunidad → Seleccionar ataque → Atacar o reposicionarse → Finalizar turno.

---

## Enemigo 05: Bandido

**Rol de combate:**
Atacante físico con capacidad de debilitamiento.

**Comportamiento:**
Ataca a los protagonistas y utiliza habilidades que reducen su capacidad ofensiva. Su IA puede priorizar personajes que representen una amenaza estratégica.

**Vida:** 95 HP.
**Daño:** 16 ATK.
**Defensas:** 6 DEF.
**Velocidad:** 10 SPD.

**Rango de detección:**
No aplica como distancia de exploración. Utiliza ataques principalmente cuerpo a cuerpo.

**Ataques:**
- **Cuchillada:** ataque físico básico.
- **Ataque Sucio:** ataque de mayor potencia que aplica debilitamiento del 20 % del ataque durante dos turnos. Cooldown de tres turnos.
    

**Debilidades:**
Su dependencia del combate cercano puede limitar sus opciones cuando los objetivos están fuera de alcance. También puede ser afectado por habilidades de debilitamiento y protección.

**Recompensa:**
Incluida en la recompensa del encuentro: 100 XP y 40 Coronas.

**Estados de IA:**
Evaluar amenazas → Seleccionar objetivo → Aplicar ataque o debilitamiento → Finalizar turno.

---

## Enemigo 06: Chamán del bosque

**Rol de combate:**
Unidad de apoyo mágico y curación.

**Comportamiento:**
Analiza el estado de sus aliados para determinar cuándo utilizar habilidades curativas. También puede atacar a distancia o debilitar la defensa de los protagonistas.

**Vida:** 65 HP.
**Daño:** 14 ATK.
**Defensas:** 3 DEF.
**Velocidad:** 11 SPD.

**Rango de detección:**
No aplica en exploración. Utiliza habilidades de ataque y apoyo desde las posiciones permitidas.

**Ataques y habilidades:**
- **Descarga Natural:** ataque mágico básico a distancia.
- **Curación Primitiva:** recupera 12 HP de un aliado. Cooldown de tres turnos.
- **Maldición:** reduce la defensa del objetivo un 20 % durante dos turnos. Cooldown de tres turnos.
    

**Debilidades:**
Posee poca vida y defensa. Eliminarlo de manera temprana puede impedir que continúe recuperando a sus aliados o debilitando al equipo.

**Recompensa:**
Forma parte de encuentros que otorgan 100 XP y 40 Coronas.

**Estados de IA:**
Evaluar aliados y enemigos → Priorizar curación o ataque → Seleccionar habilidad válida → Ejecutar acción → Finalizar turno.

---

## Enemigo 07: Guardián forestal

**Rol de combate:**
Defensor resistente de primera línea.

**Comportamiento:**
Utiliza ataques físicos y habilidades para aumentar su resistencia. Su IA intenta aprovechar los beneficios defensivos cuando resultan útiles.

**Vida:** 115 HP.
**Daño:** 17 ATK.
**Defensas:** 8 DEF.
**Velocidad:** 7 SPD.

**Rango de detección:**
No aplica en exploración. Sus ataques ofensivos se realizan principalmente a corta distancia.

**Ataques y habilidades:**
- **Golpe de Raíces:** ataque físico básico.
- **Corteza Endurecida:** aumenta su defensa un 25 % durante dos turnos. Cooldown de tres turnos.
    

**Debilidades:**
Su velocidad relativamente baja permite que el jugador responda antes de sus siguientes acciones. Es vulnerable a estrategias que reduzcan su defensa o aprovechen ataques con penetración defensiva.

**Recompensa:**
Incluida en la recompensa general del encuentro: 100 XP y 40 Coronas.

**Estados de IA:**
Evaluar amenazas → Determinar necesidad de protección → Atacar o fortalecer defensa → Finalizar turno.

---

# Capítulo 3: Corrupción del Bosque

## Enemigo 08: Corrupto errante

**Rol de combate:**
Atacante físico resistente con daño periódico.

**Comportamiento:**
Busca presionar constantemente al equipo mediante ataques físicos y la aplicación de sangrado.

**Vida:** 130 HP.
**Daño:** 20 ATK.
**Defensas:** 7 DEF.
**Velocidad:** 10 SPD.

**Rango de detección:**
No aplica como detección en tiempo real. Sus ataques dependen del alcance establecido en sus habilidades.

**Ataques:**
- **Zarpazo Corrupto:** ataque físico básico.
- **Herida Infectada:** ataque de mayor potencia que aplica sangrado de 4 HP durante dos turnos. Cooldown de dos turnos.
    

**Debilidades:**
Puede ser controlado mediante efectos negativos y habilidades que reduzcan su daño. El sangrado aplicado por este enemigo puede eliminarse mediante antídotos.

**Recompensa:**
Forma parte de encuentros que otorgan 150 XP y 60 Coronas por victoria.

**Estados de IA:**
Evaluar objetivos → Identificar oportunidades → Seleccionar ataque → Atacar o reposicionarse → Finalizar turno.

---

## Enemigo 09: Acechador oscuro

**Rol de combate:**
Atacante rápido de alto daño.

**Comportamiento:**
Prioriza oportunidades ofensivas y puede utilizar ataques poderosos contra protagonistas vulnerables. Representa una amenaza importante por su velocidad y capacidad de daño.

**Vida:** 100 HP.
**Daño:** 23 ATK.
**Defensas:** 5 DEF.
**Velocidad:** 15 SPD.

**Rango de detección:**
No aplica en exploración. Sus ataques pueden alcanzar diferentes posiciones dependiendo de la habilidad.

**Ataques:**
- **Corte Sombrío:** ataque físico básico con alcance extendido.
- **Ataque Letal:** ataque pesado con potencia adicional de +5. Cooldown de tres turnos.
    

**Debilidades:**
Aunque es veloz y ofensivo, posee menor resistencia que los enemigos defensivos de Corrupción. Puede ser prioritario para habilidades que reduzcan su ataque o permitan eliminarlo rápidamente.

**Recompensa:**
Incluida en la recompensa global del encuentro: 150 XP y 60 Coronas.

**Estados de IA:**
Evaluar vulnerabilidades → Seleccionar objetivo válido → Priorizar ataque ofensivo → Ejecutar acción → Finalizar turno.

---

## Enemigo 10: Hechicero corrupto

**Rol de combate:**
Atacante mágico y debilitador.

**Comportamiento:**
Utiliza magia ofensiva y efectos negativos para aumentar el daño que recibe el equipo del jugador. Su inteligencia artificial aprovecha objetivos vulnerables y las oportunidades para aplicar alteraciones de estado.

**Vida:** 90 HP.
**Daño:** 25 ATK.
**Defensas:** 4 DEF.
**Velocidad:** 12 SPD.

**Rango de detección:**
No aplica como detección en tiempo real. Sus habilidades mágicas tienen alcance determinado por las reglas del combate.

**Ataques y habilidades:**
- **Orbe Maldito:** ataque mágico básico.
- **Llama Corrupta:** ataque de mayor potencia que aplica quemadura de 4 HP durante tres turnos. Cooldown de dos turnos.
- **Maleficio:** aplica vulnerabilidad que reduce la defensa un 25 % durante dos turnos. Cooldown de tres turnos.
    

**Debilidades:**
Posee una vida y defensa relativamente bajas. El jugador puede disminuir su impacto mediante ataques prioritarios, protección y habilidades que afecten su capacidad ofensiva.

**Recompensa:**
Forma parte de encuentros que entregan 150 XP y 60 Coronas.

**Estados de IA:**
Evaluar objetivos → Revisar estados activos → Seleccionar ataque o debilitamiento → Ejecutar acción → Finalizar turno.

---

## Enemigo 11: Guardián corrupto

**Rol de combate:**
Defensor de alta resistencia y atacante pesado.

**Comportamiento:**
Utiliza ataques físicos poderosos y habilidades defensivas para prolongar su supervivencia. Su inteligencia artificial decide cuándo fortalecer su defensa y cuándo aprovechar sus ataques de mayor potencia.

**Vida:** 180 HP.
**Daño:** 22 ATK.
**Defensas:** 11 DEF.
**Velocidad:** 7 SPD.

**Rango de detección:**
No aplica en exploración. Sus ataques son principalmente cuerpo a cuerpo.

**Ataques y habilidades:**
- **Impacto Pesado:** ataque físico básico de tipo pesado.
- **Coraza Corrupta:** aumenta su defensa un 30 % durante dos turnos. Cooldown de tres turnos.
- **Golpe Devastador:** ataque pesado con potencia adicional de +6. Cooldown de cuatro turnos.
    

**Debilidades:**
Su baja velocidad y dependencia de habilidades defensivas permiten utilizar ataques con penetración de defensa y efectos de vulnerabilidad para reducir su resistencia.

**Recompensa:**
Incluida en la recompensa global del encuentro: 150 XP y 60 Coronas.

**Estados de IA:**
Evaluar amenazas → Revisar protección activa → Seleccionar ataque o defensa → Ejecutar acción → Finalizar turno.


# Funcionamiento general de la inteligencia artificial

A diferencia de los videojuegos con desplazamiento libre, Reencarnación Express no utiliza un sistema de patrullaje, persecución o detección de enemigos en tiempo real.

Los enfrentamientos ocurren dentro de un escenario de combate por turnos, donde los enemigos conocen las unidades participantes y evalúan sus acciones durante el turno correspondiente.

## Diagrama de estados de IA

```text
INICIO DEL TURNO ENEMIGO
           |
           v
   Evaluar estado actual
           |
           v
   Consultar habilidades
       disponibles
           |
           v
   Identificar objetivos
         válidos
           |
           v
   Seleccionar la acción
      más conveniente
           |
       ┌───┴────┐
       |        |
       v        v
   Atacar /   Reposicionarse
   Apoyar      si hace falta
       |        |
       └───┬────┘
           |
           v
     Ejecutar acción
           |
           v
     Finalizar turno
```
## Plantilla de NPC

**Nombre:**

**Función:**

**Ubicación:**

**Interacción:**

**Diálogos:**

**Condiciones:**

**Recompensas / información:**

## NPC narrativos futuros

Los personajes secundarios que participarán en diálogos, misiones o acontecimientos de la historia todavía se encuentran en desarrollo.

Cuando sus diseños y funciones sean aprobados, cada NPC deberá documentarse con su nombre, ubicación, propósito narrativo, condiciones de interacción, diálogos y posibles recompensas.


> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
