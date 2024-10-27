---
creation Date: 2024-10-26 09:37
last modification: " 2024-10-26 09:37"
folder: Behavioral patterns
aliases:
  - Patrones de diseño creacionales
tags:
---
___
# Base

[[Design-Patterns]]
___
Los patrones creacionales se centran en el proceso de creación de objetos. A menudo, estos patrones abstraen o delegan el proceso de instanciación para proporcionar más flexibilidad y reducir el acoplamiento entre clases.

- **Factory (Fábrica):**
	Facilita la creación de objetos sin especificar la clase exacta del objeto que se creará. Este patrón permite encapsular la lógica de instanciación en un método de fábrica, lo que simplifica el código cliente y facilita cambios futuros en las implementaciones.
    
- **Abstract Factory (Fábrica Abstracta):**
	Proporciona una interfaz para crear familias de objetos relacionados o dependientes sin especificar sus clases concretas. Ideal para sistemas que requieren objetos que deben interactuar entre sí y para evitar la dependencia directa de clases concretas.
    
- **Builder (Constructor):**
	Separa la construcción de un objeto complejo de su representación, permitiendo el mismo proceso de construcción para diferentes representaciones. Este patrón es muy útil cuando se crean objetos con múltiples atributos opcionales.
    
- **Prototype (Prototipo):**
	Permite crear nuevos objetos clonando una instancia existente (prototipo). Este patrón es útil cuando la creación directa de un objeto es costosa en términos de rendimiento.
    
- **Singleton:**
	Asegura que una clase solo tenga una instancia y proporciona un punto de acceso global a ella. Este patrón es útil para manejar recursos compartidos o configuraciones globales, aunque debe usarse con cautela, ya que puede dificultar las pruebas y aumentar el acoplamiento.