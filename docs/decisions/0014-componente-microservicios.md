# Componente microservicios

* Status: proposed
* Date: 2024-03-02

## Context and Problem Statement

La nueva arquitectura debe contar con los elementos software adecuados para ejecutar los microservicios y estos deben estar descritos en la arquitectura.

## Decision Drivers

* RF04 Componente software necesario para ejecutar los microservicios

## Considered Options

* 0014-01-Docker Swarm
* 0014-02-AWS Fargate

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0014-01-Docker Swarm

Docker Swarm es una herramienta software que permite ejecutar los contenedores en una granja de nodos, esto implica uno o varios balanceadores de carga implementados en uno o varios nodos maestros y los nodos que prestan el servicio, implementados en nodos trabajadores. Los contenedores que se ejecutan en modo Swarm se les denomina en ocasiones como modo enjambre.

* Good, because Es una plataforma de contenedores que es muy utilizada para construir y desplegar aplicaciones.
* Good, because Las herramientas, servicios y software que se ejecutan con contenedores Docker también funcionarán bien con Swarm.
* Bad, because Poca capacidad de automatización.
* Bad, because Poca capacidad de personalización.

### 0014-02-AWS Fargate

AWS Fargate es un motor de computación sin servidor de pago por uso que permite centrarse en la creación de aplicaciones sin tener que administrar los servidores. Trasladar tareas como la administración de servidores, la asignación de recursos y el escalamiento a AWS no solo mejora su posición operativa, sino que también acelera el proceso de pasar de la idea a la producción en la nube y reduce el costo total de propiedad.

* Good, because AWS Fargate es compatible con Amazon Elastic Container Service (Amazon ECS) y Amazon Elastic Kubernetes Service (Amazon EKS)
* Good, because Procesamiento de datos escalable a 16 vCPU y 120 GB de memoria
* Good, because Se cobra solo por los recursos de computación utilizados, sin gastos iniciales.
* Bad, because Menos posibilidades de control e influencia.
