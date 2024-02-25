# Rectificación Decisión Módulos de la Aplicación

* Status: accepted
* Date: 2024-02-23

## Context and Problem Statement

Se va a volver a decidir el diseño respecto a los módulos de la aplicación para poder ofrecer un mejor diseño en base a los requisitos.

## Decision Drivers

* RF03: Lógica de negocio de la empresa dividida en módulos
* RF03-1: Módulo de Gestión de Clientes
* RF03-2: Módulo de Gestión de Pedidos
* RF03-3: Módulo de Gestión de Reparto y Rutas
* RF03-4: Módulo de Gestión de Estadísticas

## Considered Options

* 0011-1-Introducir 3 clases y el componente de microservicios Amazon QuickSight en la lógica de negocio

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0011-1-Introducir 3 clases y el componente de microservicios Amazon QuickSight en la lógica de negocio

Solo implementariamos como clases en nuestra lógica de negocio: Clientes, Pedidos, Reparto y Rutas.
El módulo de Estadísticas sería introducido como el componente de microservicios Amazon QuickSight: es un servicio de análisis de datos y visualización de Amazon Web Services (AWS) que permite crear informes y paneles interactivos utilizando datos de una variedad de fuentes, como Amazon S3, Amazon Redshift, bases de datos SQL y otros.

* Good, because Integración fácil y nativa, lo que facilita el acceso y la gestión de datos en la nube.
* Good, because Escalabilidad y capacidad para manejar grandes volúmenes de datos, gracias a la infraestructura de AWS.
* Good, because Funcionalidades avanzadas de análisis de datos, como análisis predictivo y detección de anomalías. Ofrece capacidades de machine learning integradas para análisis de datos avanzados.
* Good, because Reducción del esfuerzo de desarrollo: Al utilizar un componente externo para ciertas funcionalidades, puedes reducir el tiempo y el esfuerzo necesarios para desarrollar esas partes de la aplicación. Esto te permite concentrarte en la implementación de las clases internas que son más específicas de tu dominio de negocio.
* Good, because Equilibrio entre personalización y eficiencia: flexibilidad de personalizar ciertas funcionalidades específicas de tu aplicación mientras aprovechas las capacidades y la estabilidad del componente externo para otras partes del sistema. Esto puede conducir a un equilibrio entre la eficiencia del desarrollo y la adaptación a tus necesidades específicas.
* Good, because Permite un buen soporte para arquitecturas basadas en microservicios.
* Bad, because Costo asociado con el uso del servicio, especialmente para grandes volúmenes de datos o para el uso de funcionalidades avanzadas.
* Bad, because Dependencia del componente externo: Al utilizar un componente externo, tu aplicación puede volverse más dependiente de él. Si el componente externo cambia de manera incompatible o deja de mantenerse, tu aplicación podría enfrentar problemas de compatibilidad o incluso de funcionamiento.
* Bad, because Limitaciones en la personalización: Aunque el componente externo puede ofrecer funcionalidades probadas y estables, es posible que no se adapte completamente a las necesidades específicas de tu aplicación. Esto puede requerir ajustes en tu arquitectura o compromisos en términos de personalización.
* Bad, because Complejidad de integración: Integrar un componente externo en tu arquitectura puede agregar complejidad técnica y requerir un esfuerzo adicional de integración. Esto puede incluir la necesidad de aprender una nueva API, resolver problemas de compatibilidad o configurar correctamente el entorno de desarrollo.
