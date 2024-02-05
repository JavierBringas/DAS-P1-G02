# Selección-Estilo-Arquitectura

* Status: proposed
* Date: 2024-02-05

## Context and Problem Statement

Se necesita una arquitectura de software para migrar la arquitectura de un sistema monolítico a una basada en microservicios.

## Decision Drivers

* RF01: Migración a arquitectura basada en microservicios

## Considered Options

* 0001-1-Arquitectura Cliente-Servidor
* 0001-2-Arquitectura MVC
* 0001-3-Arquitectura por Capas

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0001-1-Arquitectura Cliente-Servidor

Modelo de comunicación que permite la distribución de tareas dentro de una red de ordenadores. Un servidor acepta las peticiones del cliente, las procesa y proporciona la respuesta solicitada.

* Good, because Administración central: el servidor está en el centro de la red. Todos los usuarios o clientes lo utilizan. Los recursos importantes, como bases de datos, se encuentran en el servidor y son accesibles de forma centralizada. Esto simplifica la administración y el mantenimiento de los recursos importantes que requieren protección. La ubicación central del servidor hace que la realización de actualizaciones sea cómoda y de bajo riesgo.
* Good, because Derechos de acceso controlados globalmente: el almacenamiento central de recursos importantes permite una gestión segura y global de los derechos de acceso. Cuando se trata de datos sensibles, es importante saber quién puede ver los datos y quién puede manipularlos. Para proteger los datos de la mejor manera posible, hay que establecer derechos de acceso.
* Good, because Un solo servidor para muchos clientes: el número de clientes puede ampliarse. Varios clientes trabajan simultáneamente utilizando un único servidor. Los clientes comparten los recursos del servidor. También es posible que el servidor esté situado en un lugar distinto al de los clientes. Lo más importante es que el servidor y los clientes estén conectados a través de una red. Y por ende, no es necesario que los recursos estén en el mismo sitio.
* Bad, because Caída del servidor: debido a la disposición centralizada y a la dependencia en un modelo cliente-servidor, la caída del servidor conlleva la caída de todo el sistema. Si el servidor se cae, los clientes dejan de funcionar porque no pueden recibir las respuestas necesarias del servidor.
* Bad, because Recursos de un servidor: el servidor realiza las tareas que requieren muchos recursos. La demanda de recursos de los clientes es mucho menor. Si el servidor tiene muy pocos recursos, afecta a todos los clientes. Por eso es importante elegir un proveedor que proporcione estos recursos de forma fiable.
* Bad, because Inversión de tiempo: otro factor que no hay que subestimar es el tiempo necesario para hacer funcionar tu servidor. Además de los conocimientos técnicos correspondientes, por ejemplo, para proteger y configurar servidores, su uso requiere una considerable inversión de tiempo.

### 0001-2-Arquitectura MVC

Modelo que separa los datos, y principalmente lo que es la lógica de negocio de una aplicación, de su representación y el módulo encargado de gestionar los eventos y las comunicaciones.

* Good, because Fácil colaboración: al separar fuertemente responsabilidades es posible desarrollar muchas nuevas características sin necesidad, muchas veces, de tocar todas las piezas implicadas, de forma que la colaboración entre diferentes desarrolladores se amplifica notablemente.
* Good, because Aplicaciones multi-vista: al aislar las vistas del resto de la lógica de la aplicación es posible presentar las mismas funcionalidades en diferentes vistas que pueden dirigirse incluso a diversos dispositivos distintos.
* Good, because Alta cohesión: permite la agrupación de lógica de acciones relacionadas en un controlador, lo que lo hace más fácil de leer y reutilizar.
* Bad, because Complejidad: es un patrón complejo que requiere que los desarrolladores implicados tengan muy claros los conceptos de responsabilidad asignados a cada una de las tres partes implicadas.Tener varias capas nos incrementa la complejidad del sistema.
* Bad, because Lento en ocasiones: en comparación a otros patrones, desarrollar este puede implicar tocar muchas y diversas piezas y tener que seguir un flujo de trabajo cerrado que a veces dificulta meter cambios que para cualquier otro desarrollo basado en otro patrón serían nimios.

### 0001-3-Arquitectura por Capas

Modelo de diseño de software, cuya base es la separación de las diferentes funcionalidades del sistema en capas o niveles, donde cada capa se encarga de un conjunto de tareas específicas y se comunica con los niveles adyacentes mediante interfaces bien definidas.

* Good, because Capacidad de testeo: al tener cada capa por separado la implementación del testing es muy elevada respecto a otros patrones, ya que es posible realizar tests sobre cada capa de manera separada.
* Good, because Facilidad de desarrollo: debido a la alta distribución es mucho más sencillo coordinar un equipo para su desarrollo, ya que cada miembro o equipo tiene claro el objetivo de cada capa y sólo es necesario crear una interfaz clara de comunicación entre ellas.
* Bad, because Violan los principios de diseño: a veces las capas no están claras y hay llamadas directas entre elementos de una capa.
* Bad, because Rendimiento: debido a que cada funcionalidad está en una capa diferente normalmente este patrón sufre de menor rendimiento que otros debido a que cualquier petición debe de atravesar de forma individual cada capa de diseño.
* Bad, because Escalabilidad: debido a que cada capa depende de la anterior y de la interfaz entre ellas, modificar un software que utilice este patrón puede ser tedioso y costoso ya que para modificar cualquiera de las capas es necesario hacer cambios en todas las anteriores.
