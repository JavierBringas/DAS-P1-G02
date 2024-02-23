# Rectificación decisión módulos reparto y rutas

* Status: accepted
* Date: 2024-02-23

## Context and Problem Statement

Se va a volver a decidir el diseño respecto a los módulos de reparto y rutas para poder ofrecer un mejor diseño en base a los requisitos.

## Decision Drivers

* RF03-3-4 Desacoplar módulos de Reparto y Rutas

## Considered Options

* 0009-1-Separar los módulso de reparto y rutas en dos clases independientes

## Decision Outcome

Chosen option: "0009-1-Separar los módulso de reparto y rutas en dos clases independientes", because es la mejor forma de representar e implementar la independencia entre módulos de la aplicación.

### Positive Consequences

* Autonomía e independencia de os módulos

## Pros and Cons of the Options

### 0009-1-Separar los módulso de reparto y rutas en dos clases independientes

Dividir las módulos en clases completamente independientes para poder hacer un buen desaacoplamiento de los mismos y que su funcionalidad no esté relacionada de forma fundamental.

* Good, because Nos permite otorgar la autonomía necesaria.
