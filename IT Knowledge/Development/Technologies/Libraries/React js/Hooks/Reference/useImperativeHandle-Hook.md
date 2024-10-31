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
- [[Reference-Hooks]]
#### RELATED
___
- **Versión**: React 16.8
- **Descripción**: Controla el valor expuesto a través de `ref` para componentes funcionales.
- **Caso de uso**: Exponer métodos o propiedades específicas de un componente a sus componentes padres.
- **Ejemplo**:
```jsx
import { useRef, useImperativeHandle, forwardRef } from 'react';

const FancyInput = forwardRef((props, ref) => {
  const inputRef = useRef();
  useImperativeHandle(ref, () => ({
    focus: () => inputRef.current.focus(),
  }));
  return <input ref={inputRef} />;
});
```
- **Motivo**: Necesidad de exponer métodos específicos al padre cuando se usan referencias en componentes funcionales.
- **Problema que solucionó**: Controla lo que se expone a través de `ref` en componentes funcionales.
- **Ejemplo previo**: En componentes de clase, se hacía mediante métodos en la clase, pero no había una forma clara para componentes funcionales hasta la llegada de `useImperativeHandle`.