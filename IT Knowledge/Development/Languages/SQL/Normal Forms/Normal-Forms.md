---
creation Date: 2024-11-16 14:22
last modification: " 2024-11-16 14:22"
aliases: 
tags:
---
___
#### BASE
- [[Hub-SQL]]
#### RELATED
- 
___
### **Formas Normales:**

1. **1NF (Primera Forma Normal)**: Los valores deben ser atómicos, sin listas ni conjuntos.
2. **2NF (Segunda Forma Normal)**: Elimina dependencias parciales (cuando se tiene una clave primaria compuesta).
3. **3NF (Tercera Forma Normal)**: Elimina dependencias transitivas (cuando un atributo depende de otro atributo no clave).
4. **4NF (Cuarta Forma Normal)**: Elimina dependencias multivaluadas (cuando una tabla tiene columnas con valores independientes entre sí).
5. **5NF (Quinta Forma Normal)**: Elimina dependencias de unión (cuando una tabla puede dividirse sin perder datos).

### **¿Cuándo usar las formas normales?**

- **1NF**: Siempre debe cumplirse al inicio del proceso de diseño, ya que establece la estructura básica de la tabla.
- **2NF y 3NF**: Se aplican para eliminar redundancias y mejorar la integridad de los datos. Son recomendadas para la mayoría de las bases de datos transaccionales.
- **4NF y 5NF**: Son más útiles en situaciones complejas o muy específicas donde hay muchas dependencias multivaluadas o uniones que afectan la integridad de los datos.

El uso de las **formas normales** (FN) es un enfoque sistemático para organizar y estructurar las bases de datos de forma eficiente. Sin embargo, no siempre es necesario o recomendable aplicar todas las formas normales a cada tabla o modelo de base de datos, ya que depende de varios factores como el **rendimiento**, **complejidad**, y **casos de uso específicos**. Vamos a detallar cuándo y por qué aplicar estas formas, y cuándo podrías hacer excepciones.

#### 1. **Primera Forma Normal (1NF)**:

- **¿Cuándo usarla?**: Siempre debes aplicar **1NF**. Es la base de la normalización. Asegura que todos los datos en una tabla sean atómicos (es decir, no haya listas ni conjuntos) y que cada fila sea única.
    
    - **Ejemplo**: Si tienes una tabla de ventas donde una columna tiene una lista de productos comprados, deberías dividir esa lista en filas separadas para cada producto.

#### 2. **Segunda Forma Normal (2NF)**:

- **¿Cuándo usarla?**: La **2NF** se debe aplicar cuando tu tabla tiene una **clave primaria compuesta** (formada por más de una columna). Asegúrate de que no existan dependencias parciales (es decir, que los atributos no clave dependan completamente de la clave primaria).
    
    - **Ejemplo**: Si tienes una tabla de **ventas por producto** donde la clave primaria es la combinación de `id_venta` e `id_producto`, y hay un atributo `nombre_cliente` que depende solo de `id_venta`, debes normalizar esta tabla dividiéndola para que cada atributo dependa completamente de la clave primaria.

#### 3. **Tercera Forma Normal (3NF)**:

- **¿Cuándo usarla?**: La **3NF** se debe aplicar cuando ya has resuelto las dependencias parciales (con 2NF), y ahora quieres eliminar las **dependencias transitivas** (es decir, cuando un atributo no clave depende de otro atributo no clave, y no de la clave primaria).
    
    - **Ejemplo**: Si tienes una tabla de **empleados** con la columna `departamento_id`, y la columna `nombre_departamento` que depende de `departamento_id`, deberías dividir esta tabla en dos: una tabla de empleados y otra de departamentos. Así, la columna `nombre_departamento` ya no dependerá de `departamento_id` en la tabla de empleados.

#### 4. **Cuarta Forma Normal (4NF)**:

- **¿Cuándo usarla?**: La **4NF** es útil cuando hay **dependencias multivaluadas**, es decir, cuando un atributo tiene múltiples valores independientes de otros atributos. Si tienes una tabla donde un atributo tiene múltiples valores que no dependen de la clave primaria, deberías aplicar 4NF para separar esos valores en tablas distintas.
    
    - **Ejemplo**: Si tienes una tabla que almacena información de productos y sus **colores** y **tamaños** (con una columna que almacena ambos), debes separarlos en tablas distintas para garantizar que no haya dependencias multivaluadas.

#### 5. **Quinta Forma Normal (5NF)**:

- **¿Cuándo usarla?**: La **5NF** se aplica en casos muy específicos donde **no puede haber más descomposición de la tabla** sin perder información, pero es raro. Esto es para situaciones de **dependencias de unión** donde una tabla contiene información de varias entidades relacionadas que pueden ser descompuestas sin redundancia.
    
    - **Ejemplo**: Cuando tienes una tabla que mezcla tres entidades como `curso`, `profesor`, y `alumno` en una sola tabla, y deseas descomponerla en relaciones más simples sin redundancia.

### **¿Debo aplicar todas las formas normales?**

La respuesta corta es **no**. Aunque la normalización es una buena práctica para la mayoría de las bases de datos, en algunos casos **puedes hacer excepciones**. Esto dependerá de:

1. **Requerimientos del rendimiento**:
    
    - En bases de datos muy grandes o con consultas muy complejas, la normalización completa (hasta 5NF) puede llevar a un **rendimiento más bajo** debido a la necesidad de realizar **más uniones entre tablas**. En estos casos, a veces se recurre a la **desnormalización**, que es el proceso contrario a la normalización y se utiliza para mejorar la velocidad de lectura de datos.
    - Por ejemplo, una base de datos **de lectura intensiva**, como las de **reportes** o **análisis**, puede beneficiarse de la desnormalización porque el costo de realizar uniones repetitivas puede ser alto.
2. **Complejidad del modelo**:
    
    - Si la base de datos tiene muchas relaciones y columnas, dividirla en demasiadas tablas puede hacer que el modelo se vuelva **demasiado complejo**. En algunos casos, es mejor mantener la **simpleza** y evitar la sobre-normalización.
    - Si una relación entre dos entidades no cambia y se utiliza frecuentemente, puedes decidir mantenerla en una sola tabla para simplificar las consultas.
3. **Casos de uso específicos**:
    
    - En situaciones donde **la integridad de los datos** no sea tan crítica (por ejemplo, aplicaciones que no requieren alta precisión en los datos o bases de datos temporales), puedes decidir no aplicar todas las formas normales.
    - En sistemas donde las **consultas de escritura son más frecuentes que las de lectura**, podrías optar por denormalizar algunas tablas para mejorar la velocidad de escritura.
4. **Problemas de integridad de datos**:
    
    - Si tu sistema necesita garantizar una **alta integridad** de los datos, la normalización es muy útil para evitar redundancias, inconsistencias o anomalías.

### **¿Cuándo optar por la desnormalización?**

Si estás buscando **optimizar el rendimiento**, la **desnormalización** puede ser una opción. Este proceso implica **unir tablas** y almacenar redundancia de datos para evitar hacer muchas consultas de **JOIN** o para que los datos estén más accesibles.

#### **Ejemplo de desnormalización**:

Si en una tabla de **clientes y sus pedidos** tienes información del cliente duplicada en cada registro de pedido, desnormalizarías esa tabla para incluir directamente todos los datos del cliente en la tabla de pedidos, reduciendo la necesidad de hacer **JOINs** entre la tabla de **clientes** y la tabla de **pedidos**.

---

### **Conclusión**:

1. **Normaliza siempre hasta 3NF**: La mayoría de los modelos de bases de datos deben cumplir al menos con **3NF** para evitar redundancia y mantener la integridad.
2. **Aplica 4NF y 5NF solo si es necesario**: Usualmente son útiles en modelos complejos con dependencias multivaluadas o de unión.
3. **Considera el rendimiento y la simplicidad**: En algunos casos, la **desnormalización** o no aplicar todas las formas normales puede ser más eficiente, dependiendo del tipo de consultas y la naturaleza de la aplicación.

No se trata de aplicar todas las formas normales como **estándar obligatorio**, sino de elegir el enfoque correcto según las necesidades del sistema.