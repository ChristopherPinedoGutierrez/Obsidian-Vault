---
creation Date: 2024-10-25 13:58
last modification: " 2024-10-25 13:58"
folder: Types Arch-Software
aliases:
  - Arquitectura orientada a eventos
tags:
---
___
**Relacionado**

[[Architecture-Software|Arquitectura de software]]
___
**Tabla de contenidos**

- [[#Descripción|Descripción]]
- [[#Utilización|Utilización]]
- [[#Ejemplo|Ejemplo]]

___
### Descripción
En esta arquitectura, los componentes del sistema se comunican mediante la producción y consumo de eventos. Esto permite una alta desacoplación entre los distintos componentes.

### Utilización
- Adecuada para sistemas donde los componentes deben reaccionar a eventos en tiempo real.
- Proyectos que requieren escalabilidad y flexibilidad en el manejo de datos.

### Ejemplo
Una aplicación de mensajería en tiempo real donde los mensajes se envían a través de un sistema de eventos, como Apache Kafka o RabbitMQ.