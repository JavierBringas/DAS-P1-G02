# Elección de pasarela de pago

* Status: proposed
* Date: 2024-02-20

## Context and Problem Statement

El módulo de Gestión de Pedidos debe de contar con una funcionalidad que permita el pago online a los clientes.

## Decision Drivers

* RF03-2-1: Funcionalidad que permita el pago del pedido

## Considered Options

* 0005-1-TPV Virtual Redsys
* 0005-2-TPV Virtual PayPal

## Decision Outcome

Chosen option: ""

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
