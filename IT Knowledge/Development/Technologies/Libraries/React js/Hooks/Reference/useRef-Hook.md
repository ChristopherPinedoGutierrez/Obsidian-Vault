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
- **Descripción**: Permite crear una referencia mutable que persiste entre renderizados y puede apuntar a un nodo DOM o almacenar cualquier valor.
- **Caso de uso**: Control de focos, acceso a elementos DOM o almacenar valores persistentes como identificadores.
- **Ejemplo**:
```jsx
import { useRef, useEffect } from 'react';

function FocusInput() {
  const inputRef = useRef(null);
  useEffect(() => {
    inputRef.current.focus();
  }, []);
  return <input ref={inputRef} />;
}
```
- **Motivo**: Se necesitaba acceder al DOM directamente o almacenar valores que no debían generar re-renderizados.
- **Problema que solucionó**: Facilita el uso de referencias mutables a nodos DOM o valores persistentes sin causar renderizados adicionales.
- **Ejemplo previo**:
```jsx
class FocusComponent extends React.Component {
  componentDidMount() {
    this.inputRef.focus();
  }
  
  render() {
    return <input ref={input => this.inputRef = input} />;
  }
}
```