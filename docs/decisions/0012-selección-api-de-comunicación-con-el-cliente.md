# Selección componente de comunicación con el cliente

* Status: accepted
* Date: 2024-02-28

## Context and Problem Statement

Por otra parte, pensando en futuras ampliaciones, se pretende que el elemento reparto y rutas pueda notificar a los clientes el estado de su pedido vía mensajes al teléfono móvil y otros posibles canales de comunicación como Instagram.

## Decision Drivers

* RF03-3-3: Comunicación con el cliente

## Considered Options

* 0012-1-Twilio
* 0012-2-Plivo

## Decision Outcome

Chosen option: "0012-1-Twilio", because La elección de Twilio como proveedor de servicios de comunicación se justifica por su amplia estandarización, soporte y capacidad para utilizar múltiples plataformas, como WhatsApp y Facebook Messenger. Su reputación establecida y documentación sólida aseguran una integración rápida y eficiente, lo que nos permite ofrecer un servicio de notificación versátil y confiable a nuestros clientes.
Esta decision conlleva a que sea introducido como componente dentro de un paquete de comunicaciones con una alta prioridad en la arquitectura.

## Pros and Cons of the Options

### 0012-1-Twilio

Twilio es una plataforma de comunicaciones en la nube que ofrece una amplia gama de servicios, incluido el envío de mensajes de texto (SMS), MMS, WhatsApp, Facebook Messenger y Business Messages de Google. Su API es fácil de usar y bien documentada, lo que la hace popular entre los desarrolladores para integrar capacidades de comunicación en aplicaciones.

* Good, because API bien documentada y fácil de usar: Twilio ofrece una API bien documentada y una biblioteca de software desarrollada activamente, lo que facilita la integración y el desarrollo de aplicaciones.
* Good, because Amplio soporte para diferentes tipos de comunicación: Además del envío de mensajes de texto (SMS), Twilio ofrece una amplia gama de servicios de comunicación, como llamadas de voz, videollamadas, mensajería enriquecida (como WhatsApp), entre otros.
* Good, because Escalabilidad: Twilio está diseñado para manejar grandes volúmenes de mensajes, lo que lo hace adecuado para aplicaciones con alta demanda.
* Good, because Funcionalidades adicionales: Twilio ofrece una variedad de funcionalidades adicionales, como enrutamiento inteligente de mensajes, notificaciones de estado de entrega, almacenamiento seguro de datos sensibles, entre otros.
* Bad, because Costo: El uso de Twilio conlleva costos, y estos pueden aumentar a medida que crece el volumen de mensajes. Esto puede ser una preocupación para aplicaciones con presupuestos limitados o modelos de negocio que dependen del volumen de mensajes.
* Bad, because Dependencia externa: Al utilizar Twilio, estás dependiendo de un proveedor externo para el envío de mensajes. Esto puede introducir riesgos de disponibilidad y rendimiento, así como vulnerabilidades de seguridad.

### 0012-2-Plivo

Plivo es otro proveedor de servicios de comunicaciones en la nube que ofrece una API para enviar mensajes de texto (SMS) y realizar llamadas telefónicas. Ofrece funcionalidades similares a Twilio y es una opción popular para integrar capacidades de comunicación en aplicaciones.

* Good, because API sencilla y fácil de usar: Plivo ofrece una API simple y fácil de usar, que facilita la integración y el desarrollo de aplicaciones.
* Good, because Precios competitivos: Plivo tiende a ofrecer precios competitivos en comparación con otros proveedores, lo que puede ser atractivo para aplicaciones con presupuestos limitados.
* Good, because Escalabilidad: Al igual que Twilio, Plivo está diseñado para manejar grandes volúmenes de mensajes, lo que lo hace adecuado para aplicaciones con alta demanda.
* Bad, because Menos funciones avanzadas: En comparación con Twilio, Plivo puede ofrecer menos funciones avanzadas y opciones de personalización. Esto puede limitar las capacidades de ciertas aplicaciones que requieren características específicas.
* Bad, because Soporte al cliente limitado: Plivo puede ofrecer un nivel de soporte al cliente más limitado en comparación con proveedores más grandes como Twilio. Esto podría ser un problema en caso de necesitar ayuda adicional durante la integración o el desarrollo de la aplicación.
* Bad, because Costos por uso: Al igual que Twilio, Plivo cobra por el uso de sus servicios, lo que significa que los costos pueden aumentar a medida que crece el volumen de mensajes.
