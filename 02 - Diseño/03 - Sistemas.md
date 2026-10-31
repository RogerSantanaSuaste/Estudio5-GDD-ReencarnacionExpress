# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema                          | Propósito                                           | Dependencias                        | Estado |
| -------------------------------- | --------------------------------------------------- | ----------------------------------- | ------ |
| Sistema de combate               | Administrar los enfrentamientos por turnos          | Personajes, habilidades, IA         |        |
| Sistema de habilidades y estados | Ejecutar ataques, curaciones y efectos especiales   | Combate, atributos                  |        |
| Inteligencia artificial enemiga  | Controlar las decisiones de los enemigos            | Combate, habilidades, posiciones    |        |
| Mapa y progresión de zonas       | Administrar encuentros, eventos y desbloqueos       | Sesión, combate                     |        |
| Progresión de personajes         | Administrar experiencia, niveles y estadísticas     | Combate, sesión                     |        |
| Inventario y economía            | Administrar Coronas, compras y consumibles          | Sesión, combate, mapa               |        |
| Sesión de juego                  | Mantener el progreso mientras dure la partida       | Sistemas de progresión e inventario |        |
| Eventos narrativos               | Activar acontecimientos que modifican la progresión | Mapa, sesión, habilidades           |        |
| Interfaz de usuario              | Permitir la interacción con los sistemas            | Combate, mapa, inventario           |        |


## Plantilla de sistema

### Sistema 01: Sistema de combate

**Objetivo:**
Gestionar los enfrentamientos entre los cuatro protagonistas y los enemigos mediante un sistema de turnos estratégicos.

**Entradas:**
- Encuentro seleccionado desde el mapa.
- Estadísticas de protagonistas y enemigos.
- Habilidades disponibles.
- Acciones seleccionadas por el jugador.
- Decisiones de la inteligencia artificial.
    

**Procesamiento / reglas:**
El sistema prepara las unidades correspondientes al encuentro y determina el orden de actuación mediante su velocidad. Durante cada turno permite ejecutar una acción válida, procesa el daño, las curaciones y los efectos aplicados, y verifica si se cumplieron las condiciones para finalizar la batalla.

Cada equipo dispone de cuatro posiciones que afectan las acciones disponibles.

**Salidas:**
- Actualización de vida y estados.
- Cambio de turnos.
- Resultado de victoria o derrota.
- Activación del procesamiento de recompensas.
    

**Estados posibles:**
Preparación, combate activo, turno del jugador, turno enemigo, victoria y derrota.

**Dependencias:**
Sistema de habilidades, personajes, inteligencia artificial y sesión de juego.

**Interacciones:**
Recibe encuentros del mapa, solicita decisiones de la IA y comunica el resultado al sistema de progresión.

**Datos que necesita:**
Vida, ataque, defensa, velocidad, posición, habilidades, enemigos y estado del encuentro.

**Datos que genera:**
Resultado del combate, unidades derrotadas, cambios de HP y eventos de finalización.

**Riesgos:**
Errores en el orden de turnos, acciones duplicadas, habilidades ejecutadas fuera de rango o combates que no terminan correctamente.

**Criterios de aceptación:**
- Todos los participantes actúan respetando el orden de turnos.
- Cada unidad ejecuta como máximo una acción por turno.
- Se respetan las posiciones y restricciones de habilidades.
- El combate termina correctamente cuando un equipo es derrotado.
- No se entregan recompensas duplicadas.
    
---

### Sistema 02: Sistema de habilidades y efectos de estado

**Objetivo:**
Administrar las capacidades de los personajes y enemigos, permitiendo ejecutar ataques, curaciones, protecciones y efectos especiales.

**Entradas:**
Habilidad seleccionada, unidad ejecutora, objetivo, estadísticas y estados activos.

**Procesamiento / reglas:**
El sistema valida la disponibilidad de una habilidad, su tiempo de reutilización, la posición del personaje y los objetivos permitidos.

Después calcula sus efectos y modifica los atributos o condiciones de las unidades afectadas.

Las habilidades pueden producir daño directo, daño periódico, curación, protección o alteraciones temporales.

**Salidas:**
- Daño o curación aplicada.
- Efectos positivos y negativos.
- Actualización de tiempos de reutilización.
- Cambios de posición cuando corresponda.
    

**Estados posibles:**
Habilidad disponible, bloqueada por cooldown, objetivo inválido, habilidad en preparación y habilidad ejecutada.

**Dependencias:**
Sistema de combate, atributos y posiciones de las unidades.

**Interacciones:**
Es utilizado por los protagonistas, la IA enemiga, el sistema de transformación de Noelle y el sistema de diagnóstico.

**Datos que necesita:**
Poder de habilidad, alcance, duración, probabilidad de aplicación, cooldown y estadísticas.

**Datos que genera:**
Daño, curación, modificaciones de atributos y estados temporales.

**Riesgos:**
Aplicación repetida de efectos, errores en el cálculo de daño, habilidades utilizables desde posiciones incorrectas y cooldowns inconsistentes.

**Criterios de aceptación:**
- Las habilidades cumplen sus restricciones.
- El daño y la curación se calculan correctamente.
- Los estados respetan su duración.
- No se acumulan efectos idénticos de manera indebida.
- Los cooldowns se actualizan de acuerdo con las reglas definidas.
    
---

### Sistema 03: Inteligencia artificial enemiga

**Objetivo:**
Controlar automáticamente las acciones de los enemigos y proporcionar enfrentamientos estratégicos con una dificultad Alta — Exigente.

**Entradas:**
- Estadísticas de las unidades.
- Puntos de vida actuales.
- Posiciones de aliados y enemigos.
- Habilidades y cooldowns disponibles.
- Estados positivos y negativos.
    

**Procesamiento / reglas:**
La IA evalúa las acciones disponibles y selecciona una opción considerando factores como el estado de sus aliados, la vulnerabilidad de los protagonistas y el beneficio estratégico de cada habilidad.
Los enemigos de las regiones avanzadas toman decisiones más exigentes, como aprovechar debilidades, curar aliados heridos o utilizar habilidades especiales en momentos oportunos.
Se conserva cierta variabilidad para evitar comportamientos completamente predecibles.

**Salidas:**
Selección de habilidad, selección de objetivo o movimiento de posición.

**Estados posibles:**
Evaluación de acciones, selección de objetivo, ejecución de habilidad, movimiento y finalización de turno.

**Dependencias:**
Sistema de combate, habilidades, posiciones y estados.

**Interacciones:**
Controla los turnos enemigos y utiliza las mismas reglas de combate que se aplican a las demás unidades.

**Datos que necesita:**
HP, atributos, habilidades, cooldowns, posiciones, condiciones y objetivos disponibles.

**Datos que genera:**
Decisión táctica y acción ejecutada por el enemigo.

**Riesgos:**
Acciones inválidas, decisiones repetitivas, concentración excesiva de ataques sobre un personaje o turnos bloqueados.

**Criterios de aceptación:**
- Los enemigos respetan sus limitaciones de habilidad y posición.
- Aprovechan oportunidades estratégicas.
- Utilizan curaciones y protecciones cuando resultan convenientes.
- No ejecutan acciones adicionales fuera de su turno.
- Mantienen un nivel de dificultad desafiante, pero justo.
    

---

### Sistema 04: Mapa interactivo y progresión de zonas

**Objetivo:**
Organizar el recorrido del jugador y administrar el acceso a encuentros y eventos dentro de las diferentes regiones de la demo.

**Entradas:**
- Selección de una localización.
- Encuentros completados.
- Estado de las regiones.
- Acciones del jugador sobre la interfaz.
    

**Procesamiento / reglas:**
El sistema consulta el progreso de la partida para determinar qué encuentros y localizaciones están disponibles.
La demo cuenta con tres regiones principales: Pradera, Bosque y Corrupción.
Pradera contiene cuatro combates; Bosque, tres; y Corrupción, dos. Los encuentros deben superarse siguiendo la progresión establecida.
También existe el evento La máscara rota y el acceso al jefe final, el capitán, en el Trono Sellado.

**Salidas:**
- Desbloqueo de encuentros y regiones.
- Información de localizaciones.
- Inicio del combate seleccionado.
- Acceso a eventos narrativos.
    

**Estados posibles:**
Localización disponible, bloqueada, completada o asociada a un evento.

**Dependencias:**
Sesión de juego, sistema de combate y eventos narrativos.

**Interacciones:**
Permite iniciar combates, consultar el progreso, acceder a la tienda y activar eventos especiales.

**Datos que necesita:**
Identificador del encuentro, estado de desbloqueo, región, enemigos y recompensas.

**Datos que genera:**z
Encuentro seleccionado y actualización de progreso.

**Riesgos:**
Desbloqueos incorrectos, acceso anticipado a regiones, encuentros repetidos o selección de combates equivocados.

**Criterios de aceptación:**
- El jugador solo puede iniciar encuentros disponibles.
- La progresión respeta el orden establecido.
- Los encuentros completados no vuelven a otorgar recompensas.
- El mapa mantiene el progreso al regresar del combate.
- Los eventos especiales respetan sus condiciones de activación.
    

---

### Sistema 05: Progresión de personajes

**Objetivo:**
Permitir que los protagonistas mejoren sus capacidades conforme superan los enfrentamientos.

**Entradas:**
Experiencia obtenida, nivel actual y estadísticas del personaje.

**Procesamiento / reglas:**
Al completar un combate, se otorga la experiencia correspondiente. El sistema comprueba si el personaje acumuló suficiente experiencia para subir de nivel.
Cuando se cumple el requisito, actualiza el nivel y los atributos conforme a las reglas de progresión.

**Salidas:**
Nuevo nivel, estadísticas actualizadas y experiencia acumulada.

**Estados posibles:**
Nivel actual, experiencia insuficiente y subida de nivel.

**Dependencias:**
Combate, recompensas y sesión de juego.

**Interacciones:**
Se relaciona con la dificultad de los encuentros y con la conservación de las estadísticas entre combates.

**Datos que necesita:**
Nivel, experiencia, atributos y umbral necesario para subir de nivel.

**Datos que genera:**
Nivel actualizado y valores nuevos de estadísticas.

**Riesgos:**
Subidas de nivel duplicadas, pérdida de experiencia o atributos inconsistentes entre escenas.

**Criterios de aceptación:**
- La experiencia se entrega únicamente al ganar.
- Las subidas de nivel ocurren al alcanzar los umbrales.
- Los atributos se actualizan correctamente.
- El progreso permanece durante toda la sesión.
    

---

### Sistema 06: Inventario y economía

**Objetivo:**
Administrar los recursos económicos del jugador y permitir la compra y utilización de objetos consumibles.

**Entradas:**
Coronas disponibles, objetos existentes, selección de compra y selección de consumible.

**Procesamiento / reglas:**
El sistema valida el costo y la disponibilidad de los objetos.
La moneda utilizada son las **Coronas (CR)**.
Los consumibles disponibles en la beta son:
- Poción de curación: 35 CR.
- Antídoto: 20 CR.

Las pociones recuperan el 50 % del HP máximo de un aliado vivo. Los antídotos eliminan sangrado, veneno y quemadura.
El inventario permite almacenar un máximo de cinco unidades por tipo de consumible.

**Salidas:**
- Actualización de Coronas.
- Actualización del inventario.
- Aplicación de efectos de objetos.
- Mensajes de compra o uso inválido.
    

**Estados posibles:**
Inventario disponible, compra válida, fondos insuficientes, inventario lleno y objeto no utilizable.

**Dependencias:**
Sesión de juego, interfaz y combate.

**Interacciones:**
La tienda permite adquirir consumibles desde el mapa; durante los combates, utilizarlos consume la acción del personaje.

**Datos que necesita:**
Cantidad de Coronas, precio, tipo de objeto, cantidad disponible y estado del personaje objetivo.

**Datos que genera:**
Saldo actualizado, cantidades del inventario y efectos aplicados.

**Riesgos:**
Compras sin fondos suficientes, cantidades negativas, duplicación de objetos o utilización sobre objetivos inválidos.

**Criterios de aceptación:**
- No se permiten compras sin Coronas suficientes.
- Se respeta la capacidad máxima del inventario.
- Los objetos aplican correctamente sus efectos.
- El inventario se actualiza al comprar o consumir.
- No se permite resucitar personajes mediante consumibles.
    

---

### Sistema 07: Sesión de juego

**Objetivo:**
Conservar temporalmente el estado de la partida mientras el jugador avanza entre el menú, el mapa y los combates.

**Entradas:**
Inicio de nueva partida, resultados de combate, cambios de inventario, experiencia, eventos y decisiones de abandonar.

**Procesamiento / reglas:**
El sistema mantiene en memoria los datos de los protagonistas, sus recursos y el progreso del mundo.
Al cambiar entre escenas, utiliza la información almacenada para reconstruir el estado correspondiente.
La beta no cuenta con un sistema de guardado permanente.
Si el equipo es derrotado o el jugador confirma que desea abandonar la partida, se descarta el progreso de la sesión.

**Salidas:**
Estado actualizado del equipo y del progreso; datos necesarios para cargar los encuentros.

**Estados posibles:**
Sesión no iniciada, sesión activa, victoria, derrota y sesión finalizada.

**Dependencias:**
Personajes, combate, mapa, inventario y progresión.

**Interacciones:**
Centraliza la información que necesitan los demás sistemas para mantener la continuidad del juego.

**Datos que necesita:**
Vida, niveles, experiencia, Coronas, inventario, encuentros completados y eventos activados.

**Datos que genera:**
Estado persistente en memoria durante la sesión y datos para inicializar las escenas.

**Riesgos:**
Pérdida inesperada de información, duplicación de recompensas o conservación incorrecta de datos entre partidas.

**Criterios de aceptación:**
- El progreso se conserva entre combates y mapa.
- Los recursos y estadísticas mantienen sus valores.
- Las derrotas descartan correctamente el progreso.
- Nueva partida reinicia todos los datos de la sesión.
- No se conserva información de una partida anterior.
    

---

### Sistema 08: Eventos narrativos

**Objetivo:**
Integrar acontecimientos de la historia que afecten la experiencia, las capacidades de los protagonistas o el avance del jugador.

**Entradas:**
Progreso de encuentros, selección de eventos y confirmaciones del jugador.

**Procesamiento / reglas:**
El sistema verifica si se cumplen las condiciones para activar un evento.
Actualmente, el evento implementado es **La máscara rota**, disponible después de completar el primer combate de Bosque.
Al confirmarlo, Noelle intercambia sus cuatro habilidades convencionales por sus cuatro habilidades divinas. Las anteriores dejan de estar disponibles. El cambio permanece activo durante el resto de la sesión.

**Salidas:**
- Evento completado.
- Transformación de Noelle.
- Desbloqueo del siguiente encuentro de Bosque.
- Actualización del mapa.
    

**Estados posibles:**
Evento bloqueado, disponible, abierto, cancelado y completado.

**Dependencias:**
Mapa, sesión de juego, personajes y habilidades.

**Interacciones:**
Modifica las habilidades disponibles de Noelle y determina cuándo puede continuar la progresión.

**Datos que necesita:**
Estado de B1, estado del evento y etapa actual de Noelle.

**Datos que genera:**
Confirmación de transformación y desbloqueo de B2.

**Riesgos:**
Activación anticipada, repetición del evento o pérdida de la transformación al cambiar de escena.

**Criterios de aceptación:**
- El evento aparece después de completar B1.
- No puede completarse antes de cumplir sus requisitos.
- La transformación ocurre una sola vez por sesión.
- Noelle conserva nivel, experiencia y atributos.
- Sus habilidades divinas permanecen disponibles en los combates posteriores.
- Una nueva partida restablece su estado inicial.
    

---

### Sistema 09: Interfaz de usuario

**Objetivo:**
Presentar información relevante y permitir que el jugador interactúe con los sistemas del videojuego de manera clara e intuitiva.

**Entradas:**
Clics del jugador, selección de botones, estado de personajes, recursos y progresión.

**Procesamiento / reglas:**
La interfaz presenta las acciones disponibles dependiendo del contexto.
Durante el combate muestra habilidades, unidades, objetivos y opciones de consumibles.
En el mapa muestra localizaciones, encuentros, progreso, tienda e inventario.
La interfaz también presenta paneles de victoria, derrota y confirmaciones importantes.

**Salidas:**
Información visual actualizada y solicitudes de acciones hacia los sistemas correspondientes.

**Estados posibles:**
Menú principal, mapa, panel contextual, tienda, inventario, combate, victoria, derrota y evento narrativo.

**Dependencias:**
Combate, mapa, inventario, sesión y eventos.

**Interacciones:**
Funciona como medio de comunicación entre el jugador y los sistemas del juego.

**Datos que necesita:**
Vida, habilidades, cooldowns, Coronas, objetos, localizaciones y estados.

**Datos que genera:**
Solicitudes de selección, confirmación y ejecución de acciones.

**Riesgos:**
Información desactualizada, botones incorrectamente habilitados, superposición de paneles o acciones ejecutadas varias veces.

**Criterios de aceptación:**
- La información mostrada coincide con el estado real del juego.
- Los controles permiten ejecutar las acciones correspondientes.
- Las acciones bloqueadas no pueden ejecutarse.
- Los paneles pueden abrirse y cerrarse correctamente.
- La interfaz mantiene su legibilidad en distintas resoluciones.

---

### Sistema 10: Diagnóstico de balance

**Objetivo:**
Facilitar las pruebas del videojuego mediante el registro de información sobre los combates, permitiendo evaluar su dificultad y detectar posibles problemas.

**Entradas:**
Eventos de combate, daño recibido, rondas, consumibles utilizados y recompensas entregadas.

**Procesamiento / reglas:**
El sistema recopila métricas de cada encuentro y genera un resumen para los desarrolladores.
Compara la duración del combate con las rondas esperadas para cada región:

- Pradera: 2–4 rondas.
- Bosque: 4–6 rondas.
- Corrupción: 5–7 rondas.
    
Los resultados pueden consultarse mediante la consola de Unity y exportarse a CSV durante el desarrollo.

**Salidas:**
Informes de combate, estadísticas de rendimiento del equipo y registros CSV.

**Estados posibles:**
Sin registro, recopilando información y reporte generado.

**Dependencias:**
Sistema de combate, unidades, daño, consumibles y recompensas.

**Interacciones:**
Permite al equipo de desarrollo evaluar el equilibrio de encuentros y comparar resultados entre pruebas.

**Datos que necesita:**
Rondas, daño, HP final, personajes derrotados, objetos usados y recompensas.

**Datos que genera:**
Reportes de balance y archivos de diagnóstico.

**Riesgos:**
Registros duplicados, datos incorrectos o diagnósticos que no reflejen correctamente las condiciones del combate.

**Criterios de aceptación:**
- Se genera un informe por combate.
- El daño registrado corresponde a la vida realmente perdida.
- Los HP finales se capturan antes de la recuperación poscombate.
- Los objetos utilizados se contabilizan correctamente.
- Las recompensas registradas coinciden con las entregadas.
- Las métricas no alteran el funcionamiento de los combates.

## Relaciones entre sistemas

1. El **sistema de sesión** funciona como administrador del progreso temporal, conservando la información necesaria para pasar entre el mapa y los combates.

2. El **mapa interactivo** consulta los encuentros disponibles y envía al sistema de combate la información del enfrentamiento seleccionado.

3. Durante el combate, el **sistema de turnos** coordina las acciones del jugador y de la **inteligencia artificial enemiga**, mientras que el **sistema de habilidades** procesa ataques, curaciones y efectos de estado.

4. Al finalizar una victoria, el sistema de **progresión de personajes** procesa la experiencia, mientras que la **economía** actualiza las recompensas obtenidas.

5. El **inventario** permite utilizar objetos durante el combate o adquirir nuevos consumibles desde el mapa.

6. Los **eventos narrativos** interactúan con la progresión y las habilidades, como sucede con la transformación de Noelle.


> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
