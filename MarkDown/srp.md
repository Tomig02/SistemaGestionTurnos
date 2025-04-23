# Principio de Responsabilidad Única (SRP)

Este principio indica que una clase debería ser responsable de una única funcionalidad y solo debería tener una única razón para cambiar.
Esta responsabilidad debe estar encapsulada en su totalidad por la clase.

Ignorar este principio puede tener consecuencias como dificultar la depuración de errores, ya que varios errores apuntan al mismo sitio, las funcionalidades estárian más acopladas y las modificaciones a futuro serian mas complejas.

Tomando el ejemplo del sistema para la clinica, seria incorrecto que una clase que busque los datos de un paciente tambien los muestre en la pantalla, ya que generaria un cambio innecesario en la clase buscadora si, por ejemplo, se quisiera cambiar el diseño u orden al mostrar los datos. Seria conveniente cumplir con el principio y separar estas tareas en clases diferentes, por ejemplo "BuscadorDePacientes" y "DisplayDeDatos" 