# Selección Patrón Diseño Algoritmo de Optimización en reparto

* Status: proposed
* Date: 2024-02-20

## Context and Problem Statement

El sistema deberá elegir entre 2 algoritmos de optimización para el reparto, con una demora máxima de 30 minutos. Es decir, si la duración de la demora es inferior a 30 minutos se escogerá un algoritmo y si es superior o igual a 30 minutos se escogerá el otro.

## Decision Drivers

* RF03-3-1 Selección del algoritmo de optimización de reparto

## Considered Options

* 0007-1-Patrón de Diseño Strategy
* 0007-2-Patrón de Diseño State

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0007-1-Patrón de Diseño Strategy

Strategy es un patrón de diseño de comportamiento que te permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables.

* Good, because Puedes intercambiar algoritmos usados dentro de un objeto durante el tiempo de ejecución.
* Good, because Puedes sustituir la herencia por composición.
* Good, because Principio de abierto/cerrado. Puedes introducir nuevas estrategias sin tener que cambiar el contexto.
* Good, because Puedes aislar los detalles de implementación de un algoritmo del código que lo utiliza.
* Bad, because Si sólo tienes un par de algoritmos que raramente cambian, no hay una razón real para complicar el programa en exceso con nuevas clases e interfaces que vengan con el patrón.
* Bad, because Los clientes deben conocer las diferencias entre estrategias para poder seleccionar la adecuada.
* Bad, because Muchos lenguajes de programación modernos tienen un soporte de tipo funcional que te permite implementar distintas versiones de un algoritmo dentro de un grupo de funciones anónimas. Entonces puedes utilizar estas funciones exactamente como habrías utilizado los objetos de estrategia, pero sin saturar tu código con clases e interfaces adicionales.

### 0007-2-Patrón de Diseño State

State es un patrón de diseño de comportamiento que permite a un objeto alterar su comportamiento cuando su estado interno cambia. Parece como si el objeto cambiara su clase.

* Good, because Principio de responsabilidad única. Organiza el código relacionado con estados particulares en clases separadas.
* Good, because Principio de abierto/cerrado. Introduce nuevos estados sin cambiar clases de estado existentes o la clase contexto.
* Good, because Simplifica el código del contexto eliminando voluminosos condicionales de máquina de estados.
* Bad, because Aplicar el patrón puede resultar excesivo si una máquina de estados sólo tiene unos pocos estados o raramente cambia.
