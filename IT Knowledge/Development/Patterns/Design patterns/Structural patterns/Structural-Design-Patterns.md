---
creation Date: 2024-10-26 09:37
last modification: " 2024-10-26 09:37"
folder: Behavioral patterns
aliases:
  - Patrones de diseño estructurales
tags:
---
___
# Base

[[Design-Patterns]]
___
Los patrones estructurales se centran en la organización de clases y objetos para formar estructuras de sistemas grandes y eficientes, utilizando relaciones de herencia o composición para lograr un diseño flexible y reutilizable.

- **Adapter (Adaptador):**
	Convierte la interfaz de una clase en otra interfaz que el cliente espera. Este patrón es útil para integrar clases incompatibles en un sistema sin modificar su código original.
    
- **Bridge (Puente):**
	Desacopla una abstracción de su implementación para que ambas puedan variar independientemente. Este patrón es común cuando un sistema necesita implementar diferentes combinaciones de abstracciones e implementaciones.
    
- **Composite (Compuesto):**
	Permite componer objetos en estructuras de árbol para representar jerarquías de parte-todo. Es ideal para manejar jerarquías de objetos de manera uniforme, ya que permite tratar objetos individuales y compuestos de la misma manera.
    
- **Decorator (Decorador):**
	Añade responsabilidades adicionales a un objeto dinámicamente. Este patrón es ideal para situaciones donde los comportamientos adicionales de los objetos deben añadirse en tiempo de ejecución, sin modificar la estructura original.
    
- **Facade (Fachada):**
	Proporciona una interfaz simplificada para un sistema complejo. Es ideal para reducir el acoplamiento entre subsistemas, ocultando los detalles internos y simplificando el uso de APIs o sistemas complejos.
    
- **Flyweight (Peso Ligero):**
	Minimiza el uso de memoria compartiendo tantos datos como sea posible con objetos similares. Este patrón es útil para aplicaciones que deben manejar un gran número de objetos similares.
    
- **Proxy:**
	Proporciona un sustituto o intermediario para controlar el acceso a otro objeto. Este patrón es útil para diferir la creación de recursos costosos o proteger el acceso a recursos sensibles.