---
creation Date: 2024-10-26 09:37
last modification: " 2024-10-26 09:37"
folder: Behavioral patterns
aliases:
  - Patrones de diseño de comportamiento
tags:
---
___
**Relacionado**
[[Design-Patterns]]
___
Los patrones de comportamiento se enfocan en la interacción entre objetos y la asignación de responsabilidades, permitiendo que los objetos colaboren de manera eficiente.

- **Chain of Responsibility (Cadena de Responsabilidad):**
	Permite que varios objetos tengan la oportunidad de manejar una solicitud, pasando la solicitud a lo largo de una cadena de manejadores. Es útil cuando se requiere un procesamiento flexible de solicitudes en una serie de objetos.
    
- **Command (Comando):**
	Encapsula una solicitud como un objeto, permitiendo que las operaciones se parametrizen, se deshagan o se almacenen. Es útil para sistemas con operaciones complejas que necesitan ser ejecutadas, deshechas o almacenadas.
    
- **Interpreter (Intérprete):**
	Dada una representación de gramática, este patrón define una forma de interpretar las expresiones en ese lenguaje. Es útil en aplicaciones que necesitan implementar y evaluar lenguajes o reglas propias.
    
- **Iterator (Iterador):**
	Proporciona una forma de acceder a los elementos de una colección de manera secuencial sin exponer su estructura subyacente. Es útil en cualquier sistema que maneje colecciones de objetos.
    
- **Mediator (Mediador):**
	Define un objeto que encapsula cómo interactúan un conjunto de objetos. Este patrón es ideal cuando un sistema tiene muchas dependencias entre objetos que se deben manejar centralizadamente.
    
- **Memento (Recuerdo):**
	Permite capturar y restaurar el estado de un objeto sin violar su encapsulación. Este patrón es útil para implementar funcionalidades de deshacer y rehacer.
    
- **Observer (Observador):**
	Permite que un objeto (sujeto) notifique a otros objetos (observadores) cuando cambia su estado, sin depender de ellos. Es común en aplicaciones donde varios elementos deben actualizarse en respuesta a cambios de estado.
    
- **State (Estado):**
	Permite que un objeto altere su comportamiento cuando su estado interno cambia. Es útil para sistemas que deben comportarse de manera diferente según su estado.
    
- **Strategy (Estrategia):**
	Define una familia de algoritmos, encapsulándolos de forma que puedan intercambiarse entre sí. Es ideal para sistemas que necesitan cambiar algoritmos de manera dinámica.
    
- **Template Method (Método Plantilla):**
	Define el esqueleto de un algoritmo en una clase base, permitiendo que las subclases implementen ciertos pasos. Es útil para definir flujos de procesos.
    
- **Visitor (Visitante):**
	Permite añadir operaciones a un objeto sin modificar su estructura. Es ideal para sistemas donde se necesitan aplicar operaciones diferentes a una jerarquía de objetos.