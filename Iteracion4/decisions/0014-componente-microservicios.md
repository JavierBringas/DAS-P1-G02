# Componente software para ejecutar microservicios

* Status: accepted
* Date: 2024-03-02

## Context and Problem Statement

La nueva arquitectura debe contar con los elementos software adecuados para ejecutar los microservicios y estos deben estar descritos en la arquitectura.

## Decision Drivers

* RF04: Componente software necesario para ejecutar los microservicios

## Considered Options

* 0014-1-Docker Swarm
* 0014-2-AWS Fargate

## Decision Outcome

Chosen option: "0014-2-AWS Fargate", because Al seleccionar AWS Fargate para nuestra arquitectura, podemos aprovechar su simplicidad, integración nativa con AWS, escalabilidad automática y seguridad inherente para ejecutar y gestionar nuestros microservicios de manera eficiente y confiable. La facilidad de uso de Fargate nos permite centrarnos en el desarrollo de microservicios y en la visualización de datos con QuickSight, sin preocuparnos por la administración de la infraestructura subyacente. En última instancia, la elección de Fargate nos garantiza una infraestructura robusta y altamente disponible para admitir nuestras necesidades de análisis de datos con Amazon QuickSight.
En nuestra arquitectura existente, AWS Fargate se integra como un paquete sirviendo como la base fundamental debajo de toda la infraestructura. Por debajo de esta base, se encuentra el paquete de comunicaciones, representado por Twilio, que se utiliza para gestionar las comunicaciones de la aplicación.

## Pros and Cons of the Options

### 0014-1-Docker Swarm

Docker Swarm es una herramienta software que permite ejecutar los contenedores en una granja de nodos, esto implica uno o varios balanceadores de carga implementados en uno o varios nodos maestros y los nodos que prestan el servicio, implementados en nodos trabajadores. Los contenedores que se ejecutan en modo Swarm se les denomina en ocasiones como modo enjambre.

* Good, because Integración con Docker: Docker Swarm está integrado nativamente con Docker Engine, lo que significa que puedes utilizar las mismas herramientas y comandos que ya conoces para trabajar con contenedores Docker.
* Good, because Escalabilidad: Docker Swarm facilita el escalado de tus aplicaciones mediante la adición o eliminación de nodos en el clúster. Puedes escalar horizontalmente tus servicios de contenedor para satisfacer la demanda de tráfico.
* Bad, because Menor flexibilidad: Docker Swarm puede ofrecer menos flexibilidad en comparación con otras herramientas de orquestación de contenedores.
* Bad, because Menos características avanzadas: Docker Swarm puede carecer de algunas características avanzadas, como la gestión avanzada de estado o la gestión de recursos más granular.
* Bad, because Menor comunidad y soporte: Aunque Swarm es ampliamente utilizado, la comunidad y el soporte pueden ser menores en comparación con otras opciones, lo que puede dificultar la resolución de problemas o la obtención de ayuda en línea.

### 0014-2-AWS Fargate

AWS Fargate es un motor de computación sin servidor de pago por uso que permite centrarse en la creación de aplicaciones sin tener que administrar los servidores. Trasladar tareas como la administración de servidores, la asignación de recursos y el escalamiento a AWS no solo mejora su posición operativa, sino que también acelera el proceso de pasar de la idea a la producción en la nube y reduce el costo total de propiedad.

* Good, because Optimizacion de los costos: se paga solo por los recursos de computación que se usen, sin gastos iniciales.
* Good, because Integración con otros servicios de AWS: Fargate se integra estrechamente con otros servicios de AWS, lo que facilita la integración con Amazon QuickSight.
* Good, because Escalabilidad: Fargate escala automáticamente la infraestructura en función de la carga de trabajo, lo que garantiza un rendimiento óptimo y una alta disponibilidad para tus microservicios. Procesamiento de datos escalable a 16 vCPU y 120 GB de memoria
* Good, because Seguridad: Fargate proporciona aislamiento de recursos a nivel de contenedor y se integra con los servicios de seguridad de AWS, como IAM y VPC, para garantizar un entorno seguro para microservicios.
* Good, because Simplicidad: Fargate elimina la necesidad de gestionar servidores o clústeres de contenedores, lo que simplifica la configuración y operación de tus microservicios.
* Bad, because Limitaciones de personalización: Fargate puede tener algunas limitaciones en términos de personalización y configuración avanzada en comparación con otras soluciones más flexibles.
* Bad, because Menor control sobre la infraestructura: Al ser un servicio completamente gestionado, Fargate proporciona menos control sobre la infraestructura subyacente.
