# Selección-patrón-diseño-módulos-reparto-y-rutas

* Status: accepted
* Date: 2024-02-20

## Context and Problem Statement

El módulo de Reparto y Rutas debe de desacoplar su funcionalidad debido a la cantidad de funciones que desempeña.

## Decision Drivers

* RF03-3-4 Desacoplar módulos de Reparto y Rutas

## Considered Options

* 0006-1-Patrón de diseño Bridge

## Decision Outcome

Chosen option: "0006-1-Patrón de diseño Bridge", because el patrón Bridge es el que mejor se adapta a nuestro problema y mejor lo resuelve. Sería útil para desacoplar la funcionalidad de gestión del reparto y rutas, permitiendo flexibilidad y facilitando futuras modificaciones o extensiones en el sistema.

## Pros and Cons of the Options

### 0006-1-Patrón de diseño Bridge

Bridge es un patrón de diseño estructural que te permite dividir una clase grande, o un grupo de clases estrechamente relacionadas, en dos jerarquías separadas (abstracción e implementación) que pueden desarrollarse independientemente la una de la otra.

* Good, because Puedes crear clases y aplicaciones independientes de plataforma.
* Good, because Principio de abierto/cerrado. Puedes introducir nuevas abstracciones e implementaciones independientes entre sí.
* Good, because Principio de responsabilidad única. Puedes centrarte en la lógica de alto nivel en la abstracción y en detalles de la plataforma en la implementación.
* Good, because El código cliente funciona con abstracciones de alto nivel. No está expuesto a los detalles de la plataforma.
* Bad, because Puede ser que el código se complique si aplicas el patrón a una clase muy cohesionada.
