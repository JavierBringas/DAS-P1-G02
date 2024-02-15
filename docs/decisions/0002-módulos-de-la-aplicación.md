# Módulos de la lógica de negocio

* Status: proposed
* Date: 2024-02-13

## Context and Problem Statement

La lógica de negocio del sistema cuenta con los siguientes módulos: Clientes, Pedidos, Reparto y Rutas, Estadísticas.

El sistema debe contar con un módulo que permita acceder a los datos personales de los clientes consistentes en identificador de cliente, email, nombre, apellidos, móvil y, opcional, una cuenta como Instagram.

La aplicación contará con el módulo de pedidos, que permitirá a los usuarios realizar pedidos, con un número máximo de intentos (3). Los pedidos deberán llevar ID del pedido, precio, productos, ID del cliente, dirección, fecha y estado del pedido (en proceso, preparado, en reparto, entregado).

La aplicación contará con el módulo de reparto y rutas, que permitirá gestionar el reparto de las flotas de transporte a los clientes y las rutas de los camiones. Realizará la elección de las mejores rutas, hará el seguimiento de las rutas y asignación de flotas de transporte.

El sistema deberá incluir un módulo de estadísticas. La funcionalidad del módulo permitirá a los usuarios acceder a información detallada sobre los pedidos, como fechas de solicitud, fechas de entrega estimadas y reales, productos incluidos, y cualquier problema o incidencia registrada durante el proceso de entrega. Además, el estado actual de los camiones se visualizará en tiempo real, mostrando su ubicación exacta, rutas planificadas y posibles desviaciones. La funcionalidad del módulo permitirá además a los usuarios acceder a los detalles relevantes sobre los clientes, el módulo proporcionará información detallada sobre la actividad de cada cliente, como la frecuencia de compra, historial de pedidos, categorías de productos preferidas y tendencias de gasto.

## Decision Drivers

* RF03: Lógica de negocio de la empresa dividida en módulos
* RF03-1: Módulo de Gestión de Clientes
* RF03-2: Módulo de Gestión de Pedidos
* RF03-3: Módulo de Gestión de Reparto y Rutas
* RF03-4: Módulo de Gestión de Estadísticas

## Considered Options

* 0002-1-Introducir 4 clases en la lógica de negocio
* 0002-2-Introducir 3 clases y el componente de microservicios Google Maps Platform en la lógica de negocio
* 0002-3-Introducir 3 clases y el componente de microservicios AWS IoT Core en la lógica de negocio

## Decision Outcome

Chosen option: ""

## Pros and Cons of the Options

### 0002-1-Introducir 4 clases en la lógica de negocio

Todos los modulos especificados serían incluidos como clases en nuestra lógica de negocio. Clases implementadas: Clientes, Pedidos, Reparto y Rutas, Estadísticas.

* Good, because Control total: Al implementar clases dentro de la arquitectura, tienes un control completo sobre su diseño, comportamiento y funcionalidad. No estás limitado por las características o restricciones de un componente externo.
* Good, because Personalización: Puedes personalizar las clases para que se adapten exactamente a las necesidades de tu aplicación. Esto puede conducir a un mejor rendimiento y una mejor experiencia de usuario.
* Good, because Menor dependencia externa: Al no depender de componentes externos, reduces el riesgo de fallos o problemas relacionados con la compatibilidad de versiones o cambios en los componentes externos.
* Bad, because Reinvención de la rueda: Si decides implementar tus propias clases en lugar de utilizar componentes externos, podrías estar recreando funcionalidades que ya están disponibles en bibliotecas o frameworks existentes. Esto podría resultar en un desperdicio de tiempo y recursos.
* Bad, because Mayor carga de trabajo: Implementar y mantener clases internas requiere tiempo y esfuerzo adicionales por parte del equipo de desarrollo. Esto puede aumentar los costos y retrasar el lanzamiento de nuevas funcionalidades.
* Bad, because Posible falta de soporte y documentación: Los componentes externos a menudo vienen con documentación detallada y soporte de la comunidad, lo que facilita su uso y resolución de problemas. Al implementar clases internamente, podrías carecer de esta ventaja.

### 0002-2-Introducir 3 clases y el componente de microservicios Google Maps Platform en la lógica de negocio

Solo implementariamos como clases en nuestra lógica de negocio: Clientes, Pedidos, Reparto y Rutas.
El módulo de Estadísticas sería introducido como el componente de microservicios Google Maps Platform: permite realizar seguimiento de la ubicación en tiempo real de los camiones y visualizar rutas planificadas. También se puede aprovechar Google Cloud Firestore o BigQuery para almacenar y gestionar los datos relacionados con los pedidos y clientes, y luego utilizar Google Data Studio para generar informes y visualizaciones de estadísticas.

* Good, because Amplia documentación y soporte de la comunidad.
* Good, because Escalabilidad y disponibilidad confiables.
* Good, because Integración sencilla con otras herramientas y servicios de Google Cloud Platform.
* Good, because Reducción del esfuerzo de desarrollo: Al utilizar un componente externo para ciertas funcionalidades, puedes reducir el tiempo y el esfuerzo necesarios para desarrollar esas partes de la aplicación. Esto te permite concentrarte en la implementación de las clases internas que son más específicas de tu dominio de negocio.
* Good, because Equilibrio entre personalización y eficiencia: flexibilidad de personalizar ciertas funcionalidades específicas de tu aplicación mientras aprovechas las capacidades y la estabilidad del componente externo para otras partes del sistema. Esto puede conducir a un equilibrio entre la eficiencia del desarrollo y la adaptación a tus necesidades específicas.
* Bad, because Costo asociado con el uso de la API, especialmente para volúmenes de uso elevados.
* Bad, because Dependencia del componente externo: Al utilizar un componente externo, tu aplicación puede volverse más dependiente de él. Si el componente externo cambia de manera incompatible o deja de mantenerse, tu aplicación podría enfrentar problemas de compatibilidad o incluso de funcionamiento.
* Bad, because Limitaciones en la personalización: Aunque el componente externo puede ofrecer funcionalidades probadas y estables, es posible que no se adapte completamente a las necesidades específicas de tu aplicación. Esto puede requerir ajustes en tu arquitectura o compromisos en términos de personalización.
* Bad, because Complejidad de integración: Integrar un componente externo en tu arquitectura puede agregar complejidad técnica y requerir un esfuerzo adicional de integración. Esto puede incluir la necesidad de aprender una nueva API, resolver problemas de compatibilidad o configurar correctamente el entorno de desarrollo.

### 0002-3-Introducir 3 clases y el componente de microservicios AWS IoT Core en la lógica de negocio

Solo implementariamos como clases en nuestra lógica de negocio: Clientes, Pedidos, Reparto y Rutas.
El módulo de Estadísticas sería introducido como el componente de microservicios AWS IoT Core: permite rastrear la ubicación en tiempo real de los camiones y detectar desviaciones en las rutas planificadas. Almacenar datos relacionados con los pedidos y clientes en servicios como Amazon DynamoDB o Amazon Aurora, y utilizar Amazon QuickSight para analizar y visualizar las estadísticas.

* Good, because Integración fácil con otros servicios de AWS.
* Good, because Escalabilidad y capacidad para manejar grandes flujos de datos de dispositivos IoT.
* Good, because Amplias capacidades de seguridad y gestión de dispositivos.
* Good, because Reducción del esfuerzo de desarrollo: Al utilizar un componente externo para ciertas funcionalidades, puedes reducir el tiempo y el esfuerzo necesarios para desarrollar esas partes de la aplicación. Esto te permite concentrarte en la implementación de las clases internas que son más específicas de tu dominio de negocio.
* Good, because Equilibrio entre personalización y eficiencia: flexibilidad de personalizar ciertas funcionalidades específicas de tu aplicación mientras aprovechas las capacidades y la estabilidad del componente externo para otras partes del sistema. Esto puede conducir a un equilibrio entre la eficiencia del desarrollo y la adaptación a tus necesidades específicas.
* Bad, because Costo asociado con el uso de la API, especialmente para volúmenes de uso elevados.
* Bad, because Dependencia del componente externo: Al utilizar un componente externo, tu aplicación puede volverse más dependiente de él. Si el componente externo cambia de manera incompatible o deja de mantenerse, tu aplicación podría enfrentar problemas de compatibilidad o incluso de funcionamiento.
* Bad, because Limitaciones en la personalización: Aunque el componente externo puede ofrecer funcionalidades probadas y estables, es posible que no se adapte completamente a las necesidades específicas de tu aplicación. Esto puede requerir ajustes en tu arquitectura o compromisos en términos de personalización.
* Bad, because Complejidad de integración: Integrar un componente externo en tu arquitectura puede agregar complejidad técnica y requerir un esfuerzo adicional de integración. Esto puede incluir la necesidad de aprender una nueva API, resolver problemas de compatibilidad o configurar correctamente el entorno de desarrollo.
