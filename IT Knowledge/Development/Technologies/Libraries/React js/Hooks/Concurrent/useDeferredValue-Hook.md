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
- **Descripción**: Permite posponer un valor hasta que haya tiempo para actualizarlo.
- **Caso de uso**: Para manejar estados que pueden tener retrasos, como actualizaciones de lista en búsquedas complejas.
```jsx
import { useDeferredValue, useState } from 'react';

function DeferredValueComponent() {
  const [text, setText] = useState('');
  const deferredText = useDeferredValue(text);
  return <p>{deferredText}</p>;
}
```
- **Motivo**: Controlar el retraso en actualizaciones de valores para evitar que operaciones intensivas bloqueen la UI.
- **Problema que solucionó**: Ayuda a mantener la interfaz responsiva al diferir cálculos intensivos hasta que el navegador tenga tiempo.
- **Ejemplo previo**: No había un método estándar; se usaban técnicas como `setTimeout` o promesas, que no estaban sincronizadas con el renderizado de React.