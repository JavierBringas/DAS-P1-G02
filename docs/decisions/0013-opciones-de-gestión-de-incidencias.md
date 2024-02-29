# Opciones de gestión de incidencias

* Status: accepted
* Date: 2024-02-28

## Context and Problem Statement

Durante la gestión de los repartos, se debe de alertar al sistema sobre las incidencias que puedan ocurrir, existiendo tres tipos de incidencias: “camión averiado”, “demora”, “no entrega de pedido”.

## Decision Drivers

* RF03-3-2: Gestión de incidencias

## Considered Options

* 0013-1-Introducirlo como atributo
* 0013-2-Introducirlo como clase

## Decision Outcome

Chosen option: "0013-1-Introducirlo como atributo", because Hemos decidido introducir las incidencias como un atributo de la clase Reparto porque pueden ser representadas fácilmente como un enumerado y no requieren una funcionalidad compleja detrás. Además, crear una clase separada para manejarlas sería innecesario y podría agregar complejidad innecesaria al diseño. Esto simplifica la estructura de nuestro modelo de datos y hace que la implementación sea más directa y fácil de entender.

## Pros and Cons of the Options

### 0013-1-Introducirlo como atributo

Las incidencias se modelarían como un atributo dentro de la clase Reparto de Reparto y rutas (crítico).

* Good, because Simplicidad: el manejo de incidencias es una parte integral del concepto de Reparto y Rutas, introducirlo como atributo simplifica la estructura del modelo de datos y hace que el código sea más fácil de entender.
* Good, because Acoplamiento: al tener las incidencias como parte de la clase Reparto y Rutas,  acoplamos directamente el concepto de incidencia con estas entidades. Esto es beneficioso ya que las incidencias siempre están asociadas específicamente con repartos y rutas.
* Good, because Facilidad de acceso: Al tener las incidencias como atributos de Reparto y Rutas, puedes acceder fácilmente a ellas cuando se trabaje con instancias de estas clases, lo que puede facilitar la manipulación y el procesamiento de datos.
* Bad, because Acoplamiento fuerte: introducir las incidencias como atributo puede resultar en un acoplamiento más fuerte entre las clases Reparto, Rutas y las incidencias. Esto puede dificultar la reutilización de las clases y la escalabilidad del sistema a largo plazo.
* Bad, because Limitación de reutilización: Si las incidencias necesitan ser utilizadas en otros contextos o por otras clases en el sistema, su inclusión como atributos de Reparto y Rutas puede limitar su reutilización en otras partes del sistema.

### 0013-2-Introducirlo como clase

Las incidencias se modelarían como una clase independiente, separada de las clases Reparto y Rutas.

* Good, because Separación de preocupaciones: Al tener una clase independiente para manejar las incidencias, se promueve una mejor separación de preocupaciones y se reduce el acoplamiento entre las diferentes partes del sistema.
* Good, because Reutilización: La clase de incidencias puede ser reutilizada en otras partes del sistema si es necesario manejar incidencias en diferentes contextos, lo que mejora la modularidad y la escalabilidad del sistema.
* Good, because Extensibilidad: Si las incidencias necesitan funcionalidades adicionales en el futuro, agregar estas funcionalidades a una clase independiente permite una mayor flexibilidad y extensibilidad del diseño.
* Bad, because Mayor complejidad inicial: Introducir una clase independiente para manejar las incidencias puede aumentar la complejidad inicial del diseño y la implementación del sistema.
* Bad, because Posible dificultad de acceso: Acceder y manipular las incidencias asociadas a una instancia específica de Reparto o Rutas puede requerir un poco más de esfuerzo debido a la necesidad de acceder a la clase de incidencias a través de la instancia principal.
* Bad, because Posible sobrecarga: Si las incidencias se manejan a través de una clase independiente, puede introducir una ligera sobrecarga en términos de rendimiento y consumo de recursos en comparación con tenerlas directamente integradas en las clases Reparto y Rutas.
