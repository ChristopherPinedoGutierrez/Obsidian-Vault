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
- [[State-Management-Hooks]]
#### RELATED
___
- **Versión**: React 16.8
- **Descripción**: Maneja estados complejos con una lógica similar a Redux, usando acciones y reducers.
- **Caso de uso**: Ideal para estados con múltiples variables y lógica compleja, como formularios o listas de elementos.
- **Ejemplo**:
```jsx
import { useReducer } from 'react';

function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return { count: state.count + 1 };
    default:
      return state;
  }
}

function Counter() {
  const [state, dispatch] = useReducer(reducer, { count: 0 });
  return (
    <button onClick={() => dispatch({ type: 'increment' })}>
      Count: {state.count}
    </button>
  );
}
```
- **Motivo**: Componentes con múltiples variables de estado y lógica compleja, como formularios, eran difíciles de manejar con solo `useState`.
- **Problema que solucionó**: Permite una lógica de actualización del estado más estructurada mediante un reducer, similar a Redux.
- **Ejemplo previo**: Para manejar estado complejo antes se usaban varias llamadas a `setState` en componentes de clase, lo cual resultaba en lógica repetitiva y fragmentada.