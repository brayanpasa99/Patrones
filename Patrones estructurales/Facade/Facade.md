# Fachada

## Nombre:

Fachada

## Clasificación del patrón:

Estructural

## Intención:

Provee una interfaz unificada para un conjunto de interfaces en un subsistema. Fachada define un
alto nivel de interfaces que hace el subsistema fácil de usar.

## Otros nombres:

Facade

## Motivación:

Uno de los objetivos comúnes en cuanto al desarrollo de software consiste en reducir y
minimizar las comunicaciones entre subsistemas (acoplamiento), una forma de conseguirlo es
precisamente usando Fachada para suministrar una interfaz simple ampliando la facilidad del
sistema.

## Aplicabilidad:

**Se debe usar cuando:**

● Se quiere avituallar una interfaz simple a un sistema complejo.  
● Se busca hacer el sistema más fácil para nuevos usuarios, pero viejos usuarios quieran
mantener su aplicación, se da un poderoso acceso al subsistema.  
● Se piensa abastecer de nuevas y poderosas interfaces a diferentes niveles de usuario.  
● Se reducen en gran medida las dependencias entre clientes y las clases que usan.  

## Estructura:

![Estructura](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Facade/Im%C3%A1genes/Estructura.png)

## Participantes:

● Fachada: Delegan la petición del cliente a sus respectivos objetos en los subsistemas.  
● Clase de subsistemas: Implementan la funcionalidad del sistema.  

## Colaboraciones:

● Los Clientes se comunican con el subsistema por medio de la Fachada que envía las
peticiones a los objetos encargados.  
● Los clientes que usan la Fachada no necesitan tener acceso directo a cada objeto con el
que interactúan.  

**Ventajas:**

● Aisla clases de las clases más complejas. Lo cual reduce el número de objetos con los que
el cliente interactúa y también reduce la dependencia en la compilación de sistemas
grandes.  
● Existe un débil acoplamiento entre las clases del cliente y las clases del subsistema,
porque las clases del subsistema pueden cambiar sin afectar las clases de los clientes.  
● La Fachada no impide que los clientes usen las clases del subsistema.  
● Para funciones de bajo nivel y estructuras de datos, se proporciona una interfaz orientada
a objetos reduciendo los errores de programación.  
 
**Desventajas:**
● El uso excesivo del patrón nos guía a un sistema poco funcional, con muchas capas y
errores del funcionamiento.  

## Implementación:

● Se puede hacer una reducción extra del acoplamiento haciendo a la Fachada una clase
abstracta que permita escoger entre diferentes implementaciones del subsistema.  
● En Java se facilita la definición de clases privadas a un subsistema.  

## Código de ejemplo:

● Retiro de efectivo de un cajero automático.

![Retiro de un cajero automático](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Facade/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%201.png)

● Fachada:

![Fachada](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Facade/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo2.png)

● Clase principal:

![Clase Principal](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Facade/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%203.png)

## Usos conocidos:

● Varias librerías de Software, como Font y Graphics en el caso de Java.

## Patrones relacionados:

● Singletón

## Bibliografía:
No específico. (No específico). GoF Design Patterns (Versión 2.1.0) [Aplicación móvil].
Descargado de: ​https://drive.google.com/file/d/0BywiVyFlIabXcVhGZlJBcnhWTkU/view​.  

Patrones de Diseño (XI): Patrones Estructurales - Facade [Página web]. (s.f.). Ubicación
https://programacion.net/articulo/patrones_de_diseno_xi_patrones_estructurales_facade_1014​.  

Sánchez, Giovanni. Patrones. (Mayo de 2009). Facade. Consultado en:
http://giovanni-sanchez.blogspot.com/2009/05/facade.html​.  

Junta de Andalucía. (s.f). Fachada. Marco de Desarrollo de la Junta de Andalucía.
http://www.juntadeandalucia.es/servicios/madeja/contenido/recurso/189​.
