# Principio de Inversión de Dependencias (DIP)

Este principio propone que las clases de un sistema deberian depender no de la implementacion especifica de una clase, sino de una abstraccion o interface.
Evitando asi depender de los detalles de la propia implementacion.

La idea es aislar nuestra clase detras un limite formado por las abstracciones. Asi si llegaran a cambiar los detalles de la implementacion, nuestra clase sigue siendo segura. 
Esto ayuda a mantener un bajo acoplamiento y facilita la modificación de nuestro diseño.

## Motivacion

Un gran problema del sistema de turnos es que este dependia de los sistemas de bajo nivel implementados para dar apoyo a sus funcionalidades, como puede ser el sistema de correo electronico utilizado o los software que entregan su funcionalidad al sistema.

Aplicando este principio se pudo separar al programa de estos sistemas a traves de interfaces que nos permiten abstraernos de estos sistemas, como puede ser una interfaz de almacenamiento que se comunique con el gestor de bases de datos, La interfaz de comunicaniones que nos permite enviar notificaciones a traves de cual sea el medio y proveedor utilizado, etc.

Esto nos permite una gran flexibilidad comercial y fiabilidad sin necesidad de implementar soluciones especificas para cada herramienta utilizada.

Un ejemplo del mundo real seria si un fabricante de telefonos diseñara su sistema operativo para que utilize un procesador especifico. En cuanto este sea descontinuado, el fabricante se veria forzado a descontinuar la produccion hasta rediseñar la totalidad de su sistema.

Al implementar una interface que se encargue de comunicarse con el procesador, se podria evitar esta situacion y solo rediseñar esta interfaz, evitando un rediseño completo.

## [Estructura de clases](https://drive.google.com/file/d/1zaYJx8ratpRkXbpawFEIE9smDY4H86pp/view?usp=drive_link)

![Esquema de clase DIP](../Imagenes/dip.jpeg)