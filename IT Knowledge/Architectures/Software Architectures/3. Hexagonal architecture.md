---
creation Date: 2024-10-25 14:58
last modification: " 2024-10-25 14:58"
folder: Architecture-Software-Types
aliases:
  - Arquitectura hexagonal
tags:
---
___
**Relacionado**

[[Software-Architecture|Arquitectura de software]]
___

___
- **Descripción**: Separa el núcleo de la aplicación (lógica de negocio) de los detalles de implementación (como bases de datos, APIs externas y interfaces de usuario). Utiliza puertos y adaptadores para interactuar con el exterior.
- **Utilización**:
    - Adecuada para aplicaciones que necesitan ser fácilmente testables y adaptables a diferentes entornos.
    - Proyectos donde se espera que las tecnologías cambien con el tiempo.
- **Ejemplo**: Una aplicación que puede funcionar con diferentes bases de datos o APIs, donde el núcleo de la aplicación se mantiene separado de la lógica de conexión y comunicación.