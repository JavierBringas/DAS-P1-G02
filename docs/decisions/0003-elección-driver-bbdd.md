# Elección-driver-bbdd

* Status: proposed
* Date: 2024-02-13

## Context and Problem Statement

La capa de acceso a datos contendrá dos bases de datos SQL. Una se encargará de almacenar datos de los pedidos: ID del pedido, precio, productos, ID del cliente, dirección, fecha y estado del pedido (en proceso, preparado, en reparto, entregado). 
La otra, almacenará los datos de los clientes: identificador de cliente, nombre, apellidos, email, teléfono móvil y otros métodos de comunicación opcionales como Instagram.

## Decision Drivers

* RF02: almacenamiento de los datos en 2 Bases de Datos

## Considered Options

* 0003-1-MySQL
* 0003-2-MariaDB

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0003-1-MySQL

MySQL es un sistema de gestión de bases de datos relacional desarrollado bajo licencia dual: Licencia pública general/Licencia comercial por Oracle Corporation y está considerada como la base de datos de código abierto más popular del mundo.

* Good, because Amplia adopción: MySQL ha sido ampliamente adoptado por la comunidad y la industria, lo que significa que hay una gran cantidad de recursos, documentación y soporte disponibles.
* Good, because Propiedad de Oracle: Aunque esto puede ser una desventaja en algunos aspectos (como la preocupación por la propiedad de una gran empresa), también puede ser una ventaja para empresas que ya tienen una relación con Oracle o utilizan otros productos de Oracle.
* Good, because Rendimiento establecido: MySQL ha sido probado en producción durante muchos años y se ha optimizado para una variedad de casos de uso, lo que lo convierte en una opción confiable para muchas aplicaciones.
* Bad, because Algunas características retrasadas: En comparación con MariaDB, MySQL puede tardar más en implementar nuevas características y mejoras debido a su estructura de desarrollo.
* Bad, because Limitaciones de la Edición Comunitaria: Algunas características avanzadas están disponibles solo en la edición comercial de MySQL, lo que puede ser una limitación para proyectos que requieren estas características sin incurrir en costos adicionales.

### 0003-2-MariaDB

MariaDB es un sistema de gestión de bases de datos derivado de MySQL con licencia GPL (General Public License). Tiene una alta compatibilidad con MySQL ya que posee las mismas órdenes, interfaces, API y bibliotecas, siendo su objetivo poder cambiar un servidor por otro directamente.

* Good, because Compatibilidad: MariaDB se esfuerza por mantener la compatibilidad con MySQL, lo que significa que muchas aplicaciones diseñadas para MySQL pueden ejecutarse sin problemas en MariaDB.
* Good, because Licencia más amigable: MariaDB está disponible bajo la Licencia Pública General de la Empresa (EPL), que es más permisiva que la GPL de MySQL, lo que hace que sea más fácil para algunas empresas incorporarla en sus productos sin preocuparse por la licencia.
* Good, because Desarrollo más rápido: MariaDB tiende a implementar nuevas características y mejoras más rápidamente que MySQL debido a su modelo de desarrollo comunitario más ágil.
* Bad, because Menor estabilidad: MariaDB es menos estable que MySQL debido a su naturaleza de fork y su ritmo de desarrollo más rápido, aunque esto puede variar según la versión específica y el caso de uso.
* Bad, because Menos Herramientas y Recursos: Aunque MariaDB tiene un conjunto decente de herramientas, documentación y recursos disponibles, puede haber menos opciones en comparación con MySQL debido a su menor adopción.
