---
creation Date: 2024-10-30 13:05
last modification: " 2024-10-30 13:05"
aliases: 
tags:
  - React-16
---
___
#### BASE
- [[Debugging-Hooks]]
#### RELATED
___

___
- **Versión**: React 16.8
- **Descripción**: Muestra un valor personalizado en las DevTools de React para mejorar la depuración.
- **Caso de uso**: Facilitar la depuración de custom hooks mostrando valores específicos.
```jsx
import { useDebugValue, useState } from 'react';

function useCustomHook() {
  const [state, setState] = useState(0);
  useDebugValue(state > 0 ? 'Positive' : 'Negative');
  return [state, setState];
}
```
- **Motivo**: Proporciona contexto adicional al depurar custom hooks, facilitando la identificación de su estado interno.
- **Problema que solucionó**: Facilita la depuración de hooks personalizados en las DevTools.
- **Ejemplo previo**: Los valores internos de hooks personalizados eran difíciles de monitorear y depurar sin este hook.