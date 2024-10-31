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
- **Descripción**: Memoriza el resultado de una función, recalculándolo solo si cambian las dependencias.
- **Caso de uso**: Acelerar cálculos costosos que dependen de ciertos valores en un componente.
- **Ejemplo**:
```jsx
import { useMemo } from 'react';

function ExpensiveCalculationComponent({ number }) {
  const result = useMemo(() => heavyComputation(number), [number]);
  return <div>Result: {result}</div>;
}
```
- **Motivo**: Cálculos costosos que se realizaban en cada renderizado impactaban el rendimiento.
- **Problema que solucionó**: Permite memorizar el resultado de cálculos para que solo se ejecuten cuando las dependencias cambian.
- **Ejemplo previo**: No existía una alternativa directa para este comportamiento en componentes de clase. Los desarrolladores tenían que implementar manualmente lógica para prevenir renderizados innecesarios.