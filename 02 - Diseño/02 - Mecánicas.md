# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Plantilla de mecánica

### Nombre de la mecánica

**Propósito:**  
¿Qué aporta a la experiencia?

**Activación:**  
¿Qué debe hacer el jugador?

**Reglas:**  
¿Qué puede y qué no puede ocurrir?

**Entrada:**  
¿Qué botón, gesto o acción la activa?

**Estado inicial:**

**Estado final:**

**Recursos utilizados:**

**Recompensa:**

**Penalización:**

**Interacciones con otras mecánicas:**

**Casos límite:**  
¿Qué ocurre en situaciones poco comunes?

## Mecánicas principales

### Mecánica 01: Combate táctico por turnos

### Nombre de la mecánica

**Propósito:**  
¿Qué aporta a la experiencia?

**Activación:**  
¿Qué debe hacer el jugador?

**Reglas:**  
¿Qué puede y qué no puede ocurrir?

**Entrada:**  
¿Qué botón, gesto o acción la activa?

**Estado inicial:**

**Estado final:**

**Recursos utilizados:**

**Recompensa:**

**Penalización:**

**Interacciones con otras mecánicas:**

**Casos límite:**  
¿Qué ocurre en situaciones poco comunes?

**Reglas:**  
- El mapa representa diferentes regiones del mundo mediante localizaciones interactivas.
- La progresión inicial se divide en tres zonas: Pradera, Bosque y Corrupción.
- Cada región contiene encuentros que deben completarse en un orden determinado.
- Los encuentros bloqueados pueden consultarse, pero no iniciarse.
- Completar los encuentros requeridos permite desbloquear nuevas localizaciones.
- Algunos lugares contienen eventos especiales en lugar de combates.
- Los encuentros completados permanecen registrados durante la sesión y no pueden otorgar recompensas nuevamente.
- El mapa permite acceder a la tienda y consultar el inventario.
- El progreso de la partida se mantiene durante la sesión de juego.

**Entrada:**  
Mouse: seleccionar localizaciones, consultar encuentros y utilizar el botón **Iniciar combate**.

**Estado inicial:**
Al iniciar una nueva partida, únicamente el primer encuentro de Pradera está disponible. Las demás localizaciones permanecen bloqueadas.

**Estado final:**
El jugador completa los encuentros disponibles y desbloquea progresivamente Bosque y Corrupción, acercándose al desafío final.

**Recursos utilizados:**
Estado de progresión de la sesión, encuentros disponibles, información del equipo y recursos del inventario.

**Recompensa:**
Acceso a nuevas regiones, encuentros, eventos narrativos, experiencia y Coronas obtenidas mediante combates.

**Penalización:**
El jugador no puede avanzar a una región mientras no cumpla las condiciones de desbloqueo. Si el equipo sufre una derrota total, pierde el progreso de la partida.

**Interacciones con otras mecánicas:**
Combate por turnos, progresión de personajes, economía, consumibles y eventos narrativos.

**Casos límite:**  
- Un encuentro bloqueado no puede iniciarse.
- Un encuentro completado no puede recompensar nuevamente al jugador.
- Si el jugador selecciona repetidamente el botón de iniciar combate, solo debe producirse una transición.
- El evento de Noelle debe completarse antes de continuar con determinados encuentros de Bosque.
- El acceso al jefe final permanece bloqueado mientras no esté disponible en la versión del juego.

## Mecánicas secundarias

### 1. Progresión y subida de nivel

Los protagonistas obtienen experiencia al ganar combates. Al alcanzar la cantidad necesaria, suben de nivel y mejoran sus atributos.

Esta mecánica permite que el equipo aumente sus capacidades conforme se enfrenta a enemigos más peligrosos.

### 2. Sistema de economía y tienda

El jugador obtiene una moneda llamada **Coronas (CR)** al completar encuentros.
Las Coronas pueden utilizarse en la tienda del mapa para adquirir objetos consumibles.
Los precios establecidos son:
- Poción de curación: 35 CR.
- Antídoto: 20 CR.
El jugador comienza una nueva partida con 50 Coronas, una poción y ningún antídoto.

### 3. Uso de consumibles

Los objetos permiten recuperar puntos de vida o eliminar determinados efectos negativos.
**Poción:** recupera el 30 % de la vida máxima de un aliado que siga con vida.
**Antídoto:** elimina efectos de sangrado, veneno y quemadura.
Durante el combate, utilizar un consumible consume la acción del personaje correspondiente.
Cada tipo de consumible tiene un límite de cinco unidades en el inventario.
Los consumibles no permiten resucitar personajes derrotados.

### 4. Recuperación después del combate

Al obtener una victoria, los integrantes supervivientes recuperan una cantidad adicional de vida equivalente al 40 % de su HP máximo, sin superar su límite.
Los personajes que terminaron derrotados regresan con el 40 % de su vida máxima.
El equipo conserva su progresión y recupera su formación original para el siguiente encuentro.

### 5. Transformación de Noelle

Noelle comienza la aventura utilizando habilidades convencionales mientras oculta su verdadera identidad.
Después de completar el primer encuentro de Bosque, el jugador puede acceder al evento narrativo **La máscara rota**.
Al completar este evento, Noelle desbloquea cuatro habilidades divinas que sustituyen a sus habilidades anteriores.
La transformación se mantiene durante el resto de la partida y no altera su nivel, experiencia ni atributos.
El evento solo puede completarse una vez por sesión y es obligatorio para continuar avanzando en Bosque.

### 6. Inteligencia artificial enemiga

Los enemigos seleccionan acciones automáticamente durante sus turnos.
Su comportamiento considera factores como disponibilidad de habilidades, posiciones, puntos de vida, estados activos y oportunidades estratégicas.
La dificultad aumenta progresivamente entre regiones, y los enemigos de Bosque y Corrupción utilizan decisiones tácticas más exigentes.
La intención es que el jugador deba planificar sus acciones en lugar de depender únicamente de ataques básicos.

### 7. Sistema de derrota y reinicio

Cuando todos los protagonistas son derrotados, la partida termina.
El jugador regresa al menú principal y pierde el progreso acumulado durante esa sesión.
Al comenzar una nueva partida, se reinician los niveles, recursos, encuentros completados y eventos narrativos.
La versión beta no incluye un sistema de guardado permanente.

### 8. Eventos narrativos

Algunas localizaciones del mapa contienen eventos especiales que afectan la historia o el desarrollo de los protagonistas.
Estos eventos pueden desbloquear nuevas capacidades o modificar la progresión.
El evento **La máscara rota** es el primero de este tipo implementado en la demo.
No todos los eventos necesitan otorgar recompensas económicas o experiencia.

### 9. Efectos de estado

Durante el combate, determinadas habilidades pueden aplicar condiciones temporales a aliados o enemigos.
Los principales efectos incluyen sangrado, veneno, quemadura, debilitamiento, vulnerabilidad, protección, regeneración y aturdimiento.
Cada efecto dispone de reglas de duración y aplicación que afectan las decisiones del jugador.
Estos estados permiten generar ventajas y desventajas tácticas sin depender exclusivamente del daño directo.

### 10. Interacción con localizaciones

El mapa incluye marcadores interactivos que permiten consultar los lugares disponibles y sus encuentros asociados.
Al seleccionar una localización, aparece un panel contextual con información sobre enemigos, recompensas y condiciones de acceso.
Los estados visuales permiten identificar lugares disponibles, completados, bloqueados o relacionados con eventos especiales.
Esta mecánica complementa la exploración y facilita la navegación por el mundo del juego.


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
