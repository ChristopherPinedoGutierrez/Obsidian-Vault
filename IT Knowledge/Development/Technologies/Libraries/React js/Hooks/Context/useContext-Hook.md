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
- [[Context-Hooks]]
#### RELATED
___
- - **Versión**: React 16.8
- **Descripción**: Permite consumir el contexto y acceder a valores compartidos en un árbol de componentes sin prop drilling.
- **Caso de uso**: Compartir temas, configuraciones de usuario o cualquier dato global a lo largo de una aplicación sin pasar props en múltiples niveles.
- **Ejemplo**:
```jsx
import { useContext } from 'react';
import { ThemeContext } from './ThemeContext';

function ThemedComponent() {
  const theme = useContext(ThemeContext);
  return <div style={{ background: theme.background }}>Themed Component</div>;
}
```
- **Motivo**: La necesidad de pasar props a través de múltiples niveles (prop drilling) para componentes que no los necesitaban hacía el código complejo.
- **Problema que solucionó**: Facilita la obtención de valores de contexto sin prop drilling, lo que hace el código más limpio y fácil de leer.
- **Ejemplo previo**:
```jsx
class ThemeComponent extends React.Component {
  render() {
    return (
      <ThemeContext.Consumer>
        {theme => <div style={{ background: theme.background }}>Content</div>}
      </ThemeContext.Consumer>
    );
  }
}
```