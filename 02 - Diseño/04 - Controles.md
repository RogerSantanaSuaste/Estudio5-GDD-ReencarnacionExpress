# Controles

## Descripción de la sección

Define la relación entre las acciones del jugador y las entradas físicas del dispositivo.

## Mapa de controles

| Acción                       | Teclado | Mouse                                            | Control | Táctil |
| ---------------------------- | ------- | ------------------------------------------------ | ------- | ------ |
| Navegar por el mapa          |         | Clic izquierdo en una localización               |         |        |
| Interactuar con elementos    |         | Clic izquierdo                                   |         |        |
| Seleccionar habilidad        |         | Clic izquierdo en el botón de habilidad          |         |        |
| Seleccionar objetivo         |         | Clic izquierdo sobre el objetivo válido          |         |        |
| Ataque principal             |         | Seleccionar habilidad ofensiva y objetivo        |         |        |
| Ataque secundario o especial |         | Seleccionar habilidad especial y objetivo        |         |        |
| Iniciar combate              |         | Clic izquierdo  Botón Iniciar combate            |         |        |
| Confirmar evento narrativo   |         | Clic izquierdo  Botón de confirmación del evento |         |        |
| Cerrar paneles               | ESC     | Clic izquierdo Botón de cerrar                   |         |        |
| Usar consumibles             |         | Botón Objetos y selección del consumible         |         |        |


## Principios de control

**Consistencia:**
El clic izquierdo funciona como entrada principal para seleccionar acciones tanto en el mapa como durante los combates. Los botones mantienen comportamientos similares en las distintas pantallas.

**Claridad:**
Las acciones disponibles se presentan mediante botones e indicadores visuales. Las habilidades y encuentros bloqueados deben distinguirse claramente de las opciones que sí pueden utilizarse.

**Retroalimentación inmediata:**
La interfaz debe responder a cada acción mediante cambios visuales, actualización de información o ejecución de la acción correspondiente.

Por ejemplo, al seleccionar una habilidad se indica qué objetivos son válidos; al ejecutar un ataque se actualizan los puntos de vida del objetivo.

**Prevención de errores:**
El sistema debe impedir acciones inválidas, como utilizar habilidades en tiempo de reutilización, atacar objetivos fuera de alcance o iniciar encuentros bloqueados.
Las decisiones importantes, como abandonar una partida, requieren confirmación para evitar la pérdida accidental del progreso.

**Simplicidad:**
No se requieren combinaciones complejas de teclas ni reflejos rápidos, ya que el enfoque del videojuego es la estrategia por turnos.

## Reasignación

En la versión beta de Reencarnación Express, no se contempla la reasignación de controles por parte del jugador.

## Entrada y retroalimentación

|Entrada del jugador|Respuesta del sistema|
|---|---|
|Seleccionar una localización del mapa|Se abre un panel con información sobre el lugar y sus encuentros.|
|Seleccionar un encuentro|Se muestran sus enemigos, recompensas y estado de disponibilidad.|
|Presionar Iniciar combate|Se carga la escena de combate correspondiente al encuentro seleccionado.|
|Seleccionar una habilidad|El sistema comprueba su disponibilidad y permite seleccionar un objetivo válido.|
|Seleccionar un enemigo|Si el objetivo es válido, se ejecuta la habilidad y se actualizan sus atributos.|
|Utilizar una curación|Se recuperan puntos de vida sin superar el máximo permitido.|
|Utilizar un antídoto|Se eliminan los efectos negativos que puede tratar el consumible.|
|Seleccionar un objeto en la tienda|Se verifica el costo y, si la compra es válida, se actualizan las Coronas y el inventario.|
|Presionar un encuentro bloqueado|Se muestra su estado, pero no se permite iniciar el combate.|
|Abrir el evento de Noelle|Se presenta el panel narrativo con opciones para confirmar o regresar.|
|Confirmar La máscara rota|Noelle intercambia sus cuatro habilidades por las divinas y se abre el siguiente encuentro de Bosque.|
|Seleccionar Volver al menú|Se solicita una segunda confirmación antes de descartar la partida.|
|Ganar un combate|Se muestra el resultado y la opción para continuar hacia el mapa.|
|Perder un combate|Se presenta la derrota y la opción de regresar al menú principal.|


> **Navegación:** [[00 - Índice]] · ← [[03 - Sistemas]] · [[05 - Progresión]] →
