# Elección de pasarela de pago

* Status: accepted
* Date: 2024-02-20

## Context and Problem Statement

El módulo de Gestión de Pedidos debe de contar con una funcionalidad que permita el pago online a los clientes.

## Decision Drivers

* RF03-2-1: Funcionalidad que permita el pago del pedido

## Considered Options

* 0005-1-TPV Virtual Redsys
* 0005-2-TPV Virtual PayPal
* 0005-3-TPV Virtual MONEI

## Decision Outcome

Chosen option: "0005-3-TPV Virtual MONEI", because Permite una mayor cantidad de caracerisiticas y recursos frente a sus competidores. La seguridad es puntera y el abanico de metodos de pago es mucho mayor al resto. Soporte competente y activo.

## Pros and Cons of the Options

### 0005-1-TPV Virtual Redsys

El TPV virtual Redsys actúa como pasarela de pago online. Su principal labor es permitir que todo tipo de negocios puedan vender sus productos o servicios desde una tienda online o mediante botones de pago de manera segura y confiable.
En otras palabras, Redsys ofrece un entorno altamente fiable, estable y completamente seguro para que las empresas y clientes puedan realizar sus transacciones en línea sin ningún inconveniente y de la forma más cómoda posible, ya que es bastante sencilla su instalación. Por ello, cada vez son más los negocios que deciden implementar un TPV virtual como Redsys.

* Good, because Compatibilidad: Es compatible con una amplia gama de tarjetas de crédito y débito, lo que lo hace conveniente para clientes de diferentes países.
* Good, because Seguridad: Redsys ofrece altos estándares de seguridad en sus transacciones, cumpliendo con los protocolos de seguridad PCI-DSS.
* Good, because Soporte: Ofrece un buen servicio de atención al cliente y soporte técnico para resolver problemas o dudas que está disponible las 24h.
* Good, because Integración: Es relativamente fácil de integrar en sitios web y sistemas de punto de venta, con plugins disponibles para diversas plataformas.
* Bad, because Costos: Puede tener tarifas y comisiones relativamente altas, especialmente para pequeños comercios.
* Bad, because Proceso de alta: El proceso de registro y activación puede ser algo tedioso y nos podría llevar un tiempo.

### 0005-2-TPV Virtual PayPal

El TPV virtual PayPal actúa como pasarela de pago online. Su principal labor es permitir que todo tipo de negocios puedan vender sus productos o servicios desde una tienda online o mediante botones de pago de manera segura y confiable. PayPal es una plataforma de pagos electrónicos globalmente reconocida que ofrece servicios de TPV tanto para comercios físicos como virtuales. Es ampliamente utilizada en todo el mundo.

* Good, because Reconocimiento global: PayPal es una marca reconocida y confiable en todo el mundo, lo que puede generar confianza en los clientes.
* Good, because Facilidad de uso: Ofrece una experiencia de usuario intuitiva tanto para los comerciantes como para los clientes.
* Good, because Flexibilidad: Permite a los usuarios pagar con diferentes métodos, incluyendo tarjetas de crédito, débito y cuentas bancarias vinculadas.
* Bad, because Tarifas: Las tarifas por transacción pueden ser más altas en comparación con otros proveedores de TPV.
* Bad, because Retención de fondos: PayPal a veces retiene fondos en cuentas de comerciantes durante ciertos períodos, lo que puede afectar la liquidez.
* Bad, because Proceso de resolución de disputas: El proceso de resolución de disputas puede ser complicado y llevar tiempo, especialmente para los comerciantes.
* Bad, because Menores capacidades: debido a que Redsys ofrece realizar operaciones mediante PayPal, pdríamos deducir que Redsys integra muchas más opciones y es mucho más amplio que Paypal.

### 0005-3-TPV Virtual MONEI

MONEI es una solución de TPV virtual que facilita a los comercios la aceptación de pagos en línea. Proporciona una variedad de herramientas y características diseñadas para mejorar la experiencia del cliente y simplificar el proceso de pago.

* Good, because Pasarela de Pago Segura: MONEI proporciona una pasarela de pago segura que cumple con los estándares de seguridad PCI-DSS, lo que garantiza que los datos de los clientes estén protegidos durante las transacciones en línea.
* Good, because Integración Sencilla: Ofrece integraciones fáciles con plataformas de comercio electrónico populares y sistemas de gestión empresarial, lo que permite a los comercios comenzar a aceptar pagos en línea rápidamente.
* Good, because Múltiples Métodos de Pago: MONEI admite una variedad de métodos de pago, incluyendo tarjetas de crédito y débito, transferencias bancarias, billeteras electrónicas y otros métodos de pago alternativos.
* Good, because Análisis y Reporting: Proporciona herramientas de análisis y reporting que permiten a los comercios realizar un seguimiento de las transacciones, analizar el rendimiento y tomar decisiones informadas para optimizar su negocio.
* Bad, because Costos: MONEI puede implicar costos adicionales, como tarifas de transacción y tarifas de servicio, lo que puede afectar la rentabilidad para algunos comercios, especialmente para aquellos con volúmenes de transacción más bajos.
* Bad, because Competencia: En un mercado competitivo, MONEI compite con otras soluciones de TPV virtual, lo que significa que los comercios deben evaluar cuidadosamente las características, costos y reputación del proveedor antes de tomar una decisión.
* Bad, because Dependencia del Proveedor: Al utilizar un servicio de TPV virtual como MONEI, los comercios pueden volverse dependientes del proveedor para procesar sus transacciones en línea, lo que podría plantear riesgos en caso de interrupciones del servicio o cambios en las políticas del proveedor.
