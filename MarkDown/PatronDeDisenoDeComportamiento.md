# Anexo - Aplicación de Patrón de Diseño de Comportamiento - Observer
Los patrones de diseño creacionales, similar a los principios SOLID, son guias o diseños sugeridos que estan encargados de ayudar a solucionar problemas comunes, 
logrando una comunicación mas efectiva y la correcta asignación de responsabilidades entre objetos.

Tambien, estos patrones se basan o integran los principios SOLID dentro de su propuesta. Al proponer como definir las interacciones entre objetos, estos diseños
pueden velar por la separacion correcta de responsabilidades o menor acoplamiento, por dar un ejemplo.

Propósito y Tipo del Patrón: En el caso de la clinica, existe la necesidad de avisar de cualquier cambio que pueda 
tener un turno tanto al doctor que provee la atencion, como al paciente dueño del turno.
Esto se debe hacer por varios medios segun su disponibilidad.
Este comportamiento se ve bastante beneficiado por el patron observer, 
que disponiendo de un organizador al que las implementaciones especificas se pueden subscribir, se simplifica
la posible expansion de las vias de comunicacion y los objetos que necesiten de utilizarlos 
pueden contactarse facilmente al invocar un evento en el organizador.

## Motivación
El sistema, al dar uso a varios metodos posibles de comunicacion, necesita de una forma util
En este caso, se resolvio aplicar el patron de comportamiento Observer al introducir a un organizador
denominado AdministradorNotificaciones, encargado de administrar eventos de notificacion
que activan las implementaciones especificas subscriptas (AutoNotificacionTelefono, AutoNotificacionEmail), este evento
es invocado por la funcion SolicitarNotificacion() del objeto Turno.
Las implementaciones especificas se encuentran abstraidas dentro de AdministradorNotificaciones 
utilizando la interfaz << IAutoNotificacion >> que implementa la funcion Notificar().

## [Estructura de Clases](https://drive.google.com/file/d/1sN_XM9FRif1y0mlLrJBKkoF6hUz4Mvz7/view?usp=drive_link)

![Diagrama de patron de diseño Observer](../Imagenes/NotificacionObserverYSingleton.jpg)