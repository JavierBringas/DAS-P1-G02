# Propuestas de API Gateway

* Status: proposed
* Date: 2024-02-13

## Considered Options

* 0004-1-Amazon
* 0004-2-Azure
* 0004-3-Tyk

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0004-1-Amazon

Es un servicio completamente administrado, diseñado para facilitar a los desarrolladores la creación y gestión de API a cualquier escala. Los desarrolladores pueden crear API para usar en sus propias aplicaciones cliente o para ponerlas a disposición de desarrolladores de aplicaciones de terceros.

* Good, because Puedes crear y publicar API que acceden a AWS, otros servicios web o datos almacenados en la nube de AWS
* Good, because Puede aceptar y procesar hasta cientos de miles de llamadas API simultáneas
* Good, because No hay tarifas ni costos de inicio
* Bad, because Incluye un límite estricto de 30 segundos que no funciona bien si tiene código de larga duración

### 0004-2-Azure

Se trata del servicio gateway ofrecido por Microsoft

* Good, because Es fácil de integrar con otros serivcios de Azure.
* Good, because Soporta muchos procolos y formatos de datos.
* Bad, because Incluye costes iniciales
* Bad, because Requiere de Azure Active Directory para la autenticación

### 0004-3-Tyk

Es una API Gateway de tipo open-source, escrita en Golang

* Good, because Escalabilidad: Tyk está diseñado para escalar horizontalmente de manera eficiente, lo que significa que puede manejar cargas de trabajo crecientes sin problemas, lo que lo hace ideal para aplicaciones y sistemas de gran escala.
* Good, because Flexibilidad: Tyk ofrece una variedad de opciones de configuración y personalización, lo que te permite adaptar la configuración de la API Gateway a las necesidades específicas de tu aplicación.
* Good, because Administración Centralizada: Tyk proporciona una interfaz de administración centralizada que te permite administrar y monitorear tus APIs de manera eficiente, lo que simplifica la gestión de API y permite un mayor control sobre el tráfico de la API.
* Bad, because Curva de Aprendizaje: Tyk puede tener una curva de aprendizaje empinada para los nuevos usuarios, especialmente aquellos que no están familiarizados con los conceptos de API Management y API Gateway.
* Bad, because Costo: Aunque Tyk ofrece una versión de código abierto, las características más avanzadas y el soporte técnico pueden requerir una suscripción paga, lo que puede ser costoso para algunas organizaciones, especialmente las más pequeñas o startups.
* Bad, because Dependencia de Proveedor: Utilizar Tyk como API Gateway significa depender de un proveedor externo para la gestión de tus APIs, lo que puede plantear preocupaciones sobre la dependencia del proveedor y la disponibilidad del servicio a largo plazo.
