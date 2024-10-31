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
- [[Effects-and-Lifecycle-Hooks]]
#### RELATED
- [[useEffect-Hook|useEffect]]
___
- **Versión**: React 16.8
- **Descripción**: Similar a useEffect pero se ejecuta después de todas las modificaciones del DOM y antes de que el navegador pinte la pantalla.
- **Caso de uso**: Medir o cambiar el layout del DOM antes de la pintura, útil en animaciones y ajustes visuales complejos.
- **Ejemplo**:
```jsx
import { useLayoutEffect, useRef } from 'react';

function ResizableBox() {
  const boxRef = useRef();
  useLayoutEffect(() => {
    boxRef.current.style.width = '100px';
  }, []);
  return <div ref={boxRef} />;
}
```
- **Motivo**: Se necesitaba manipular el DOM justo después de que el navegador aplicara cambios visuales y antes de que se actualice en pantalla.
- **Problema que solucionó**: Permite efectos sincronizados para manipular el DOM y evitar parpadeos visuales.
- **Ejemplo previo**: Antes se usaba `componentDidMount` o `componentDidUpdate`, aunque no tenían el mismo efecto preciso.