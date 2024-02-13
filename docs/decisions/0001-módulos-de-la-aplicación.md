# Módulos de la aplicación

* Status: proposed
* Date: 2024-02-13

## Context and Problem Statement

La lógica de negocio del sistema cuenta con los siguientes módulos: Clientes, Pedidos, Reparto y Rutas, Estadísticas. Por lo que sería necesario incluirlo en la arquitectura.

## Decision Drivers

* RF03: Lógica de negocio de la empresa dividida en módulos

## Considered Options

* 0002-1-Incluir los módulos en la arquitectura

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0002-1-Incluir los módulos en la arquitectura

Se trata de incluir en el modelo de la aplicación los diferentes módulos con los que se desea trabajar.

* Good, because Los módulos son reutilizables, lo que significa que se pueden utilizar en otros proyectos.
* Good, because Es fácil agregar nuevos módulos a medida que se desarrolla el proyecto
* Bad, because Los módulos están altamente acoplados, lo que puede dificultar la implementación de cambios en el proyecto.
* Bad, because Puede ser difícil determinar la dependencia de un módulo con otros. Esto puede dificultar la identificación de problemas y errores en el proyecto en su totalidad.
