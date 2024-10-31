---
creation Date: 2024-10-30 13:05
last modification: " 2024-10-30 13:05"
aliases: 
tags:
  - React-18
---
___
#### BASE
- [[Concurrent-Hooks]]
#### RELATED
___

___
- **Versión**: React 18
- **Descripción**: Permite realizar transiciones no bloqueantes para actualizaciones de estado, dividiendo actualizaciones entre urgentes y no urgentes.
- **Caso de uso**: Mejorar la experiencia del usuario en actualizaciones de UI con retraso, como cambios en listas grandes.
```jsx
import { useTransition, useState } from 'react';

function TransitionComponent() {
  const [isPending, startTransition] = useTransition();
  const [value, setValue] = useState(0);
  return (
    <button
      onClick={() => startTransition(() => setValue((v) => v + 1))}
    >
      {isPending ? 'Updating...' : `Value: ${value}`}
    </button>
  );
}
```
- **Motivo**: La transición de interfaces complejas que dependían de renderizados simultáneos de tareas urgentes y no urgentes podía causar bloqueos y demoras en la interfaz.
- **Problema que solucionó**: Permite diferenciar tareas de prioridad alta y baja, mejorando la fluidez en la UI.
- **Ejemplo previo**: Antes se gestionaba mediante estados independientes o con lógica de optimización personalizada.