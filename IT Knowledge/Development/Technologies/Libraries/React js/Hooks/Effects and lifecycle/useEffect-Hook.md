---
creation Date: 2024-10-30 11:31
last modification: " 2024-10-30 11:32"
folder: Hooks
aliases:
  - useEffect
tags:
  - React-16
---
___
#### BASE
- [[Effects-and-Lifecycle-Hooks]]
#### RELATED
___
- **Versión**: React 16.8
- **Descripción**: Ejecuta efectos secundarios en componentes funcionales, como la carga de datos, suscripción a eventos o manipulación del DOM.
- **Caso de uso**: Realizar peticiones API al montar el componente, o reaccionar a cambios en dependencias específicas.
- **Ejemplo**:
```jsx
import { useEffect } from 'react';

function FetchDataComponent() {
  useEffect(() => {
    fetch('/api/data')
      .then((response) => response.json())
      .then((data) => console.log(data));
  }, []);
  return <div>Data loaded</div>;
}
```
- **Motivo**: Los efectos secundarios, como la carga de datos o suscripciones, eran manejados en el ciclo de vida de los componentes de clase (`componentDidMount`, `componentDidUpdate`, y `componentWillUnmount`), lo cual resultaba en código extenso y difícil de manejar.
- **Problema que solucionó**: Simplifica el manejo de efectos secundarios en componentes funcionales, permitiendo declarar todos los efectos en un mismo lugar.
- **Ejemplo previo**:
```jsx
class FetchData extends React.Component {
  componentDidMount() {
    fetch('/api/data')
      .then(response => response.json())
      .then(data => this.setState({ data }));
  }

  componentWillUnmount() {
    // Cleanup code
  }

  render() {
    return <div>Data Loaded</div>;
  }
}
```
