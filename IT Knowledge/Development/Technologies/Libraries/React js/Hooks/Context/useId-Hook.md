---
creation Date: 2024-10-30 13:05
last modification: " 2024-10-30 13:05"
aliases: 
tags:
  - React-18
---
___
#### BASE
- [[Context-Hooks]]
#### RELATED
___

___
- **Versión**: React 18
- **Descripción**: Genera IDs únicos para componentes en renderizados concurrentes.
- **Caso de uso**: Ideal para generar IDs únicos en listas o formularios que necesitan accesibilidad.
```jsx
import { useId } from 'react';

function UniqueLabelInput() {
  const id = useId();
  return (
    <>
      <label htmlFor={id}>Name</label>
      <input id={id} type="text" />
    </>
  );
}
```
- **Motivo**: Generar IDs únicos y seguros para renderizados concurrentes.
- **Problema que solucionó**: Garantiza unicidad en IDs para elementos, manteniendo la accesibilidad y evitando conflictos en listas de elementos.
- **Ejemplo previo**: Generar IDs únicos requería métodos externos o librerías, que eran propensas a errores en renderizados concurrentes.