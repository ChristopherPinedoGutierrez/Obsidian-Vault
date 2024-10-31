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
- **Descripción**: Permite agregar y manejar estado en componentes funcionales.
- **Caso de uso**: Manejo de estados básicos, como contadores, valores de formularios o cualquier variable reactiva en un componente.
- **Ejemplo**:
```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```
- **Motivo**: Antes de los hooks, el estado en componentes solo estaba disponible en los componentes de clase. `useState` vino a permitir el uso de estado en componentes funcionales.
- **Problema que solucionó**: Evita la necesidad de componentes de clase para manejar estados, simplificando la estructura y permitiendo una sintaxis más limpia.
- **Ejemplo previo**:
```jsx
class Counter extends React.Component {
  state = { count: 0 };
  
  increment = () => this.setState({ count: this.state.count + 1 });

  render() {
    return <button onClick={this.increment}>Count: {this.state.count}</button>;
  }
}
```
