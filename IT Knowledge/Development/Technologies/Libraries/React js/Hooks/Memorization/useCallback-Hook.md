---
creation Date: 2024-10-30 11:31
last modification: " 2024-10-30 11:32"
folder: Hooks
aliases: 
tags:
  - React-16
---
___
#### BASE
- [[Memorization-Hooks]]
#### RELATED
___
- **Versión**: React 16.8
- **Descripción**: Memoriza funciones para evitar que se vuelvan a crear en cada renderizado.
- **Caso de uso**: Optimizar rendimiento cuando se pasan funciones como props en componentes con renderizados frecuentes.
- **Ejemplo**:
```jsx
import { useCallback, useState } from 'react';

function ParentComponent() {
  const [count, setCount] = useState(0);
  const increment = useCallback(() => setCount((c) => c + 1), []);
  return <ChildComponent increment={increment} />;
}
```
- **Motivo**: En aplicaciones grandes, el recrear funciones en cada renderizado ocasionaba problemas de rendimiento debido a renderizados innecesarios en componentes hijos.
- **Problema que solucionó**: Ayuda a memorizar funciones para evitar recrearlas en cada renderizado y reduce el uso de memoria.
- **Ejemplo previo**: No había una forma fácil de memorizar funciones en componentes de clase, por lo que se recurría a métodos de optimización manuales o librerías externas.