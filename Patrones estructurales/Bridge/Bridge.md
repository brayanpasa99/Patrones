# Bridge

## Nombre:

Bridge

## Clasificación del patrón:

Estructural

## Intención:

Desacoplar una abstracción de su implementación para que ambas puedan variar
independientemente.

## Otros nombres:

Handle/Body, Puente, Manejar/Cuerpo.

## Motivación:

Cuando una abstracción puede tener varias implementaciones, comúnmente se hace uso de la
herencia para acomodarla a las diferentes necesidades. Lo anterior se hace muy poco flexible,
difícil de mantener y modificar, por lo tanto es necesario que un patrón solucione el problema.

## Aplicabilidad:

**Se debe usar cuando se quiere:**

● Evitar un permanente acoplamiento entre una abstracción y su implementación, en
especial si la implementación tiene que ser cambiada a un runtime.  
● Extender la abstracción y su implementación de manera independiente.  
● Evitar impactos negativos o recompilación total en el cliente cuando la implementación
de una abstracción es cambiada.  
● Evita la proliferación de clases en el código.  

## Estructura:

![Estructura](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Bridge/Im%C3%A1genes/Estructura.png)

## Participantes:

● Abstracción: Define una interfaz abstracta. Mantiene la referencia al Implementador.  
● Abstracción Refinada: Extiende la interfaz definida por la abstracción.  
● Implementador: Define la interface para la implementación de clases. Típicamente, la
interface Implementador define operaciones primitivas mientras que Abstracción define
operaciones de alto nivel con base en las primitivas.  
● Implementador Concreto: Implementa la interface Implementador y define su concreta
implementación.  
 
## Colaboraciones:

Abstracción emite los pedidos de los clientes a su objeto Implementador.

**Ventajas:**

● La abstracción y su implementación son desacopladas. Por ello, la abstracción puede ser
configurada como un runtime con diferentes implementaciones.  
● Permite un tratamiento en capas que permite un enfoque más estructurado al sistema. Por
ejemplo al cambiar una implementación no requiere la recompilación de la abstracción y
su cliente.  
● Es fácil extender su una abstracción y su implementación de manera independiente.  
● Es posible ocultar los detalles de la implementación de una abstracción del cliente.  

**Desventajas:**

● Crea una indirección que puede afectar el rendimiento del sistema.

## Implementación:

● Solo el Implementador: Cuando exista solo una implementación no se hace necesario
crear una clase Implementador abstracta. Es un caso especial del patrón y es muy útil
cuando un cambio en la implementación de una clase no debe afectar a los clientes
existentes.  
● Creando el objeto implementador adecuado: Si una Abstracción conoce todas las clases
ImplementadorConcreto puede decidir cual instanciar dependiendo de los parámetros del
constructor. También es posible cambiar una implementación inicial dependiendo el uso,
o es posible delegar la decisión a otro objeto.  
● Compartiendo implementadores: Handle/Body en C++ se puede usar para compartir
implementaciones de muchos objetos. Body almacena una cuenta de referencia que la
clase Handle incrementa y decrementa.  
● Usando herencia múltiple: Se puede usar para asociar una interfaz con su
implementación.  

## Código de ejemplo:

● Implementor, motor:

![Implementor, motor](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Bridge/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%201.png)

● Diesel:

![Diesel](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Bridge/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%202.png)

● Gasolina:

![Gasolina](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Bridge/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%203.png)

● Vehículo:

![Vehículo](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Bridge/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%204.png)

● Berlina:

![Berlina](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Bridge/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%205.png)

● Mono volúmen:

![Mono volúmen](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Bridge/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%206.png)

## Usos conocidos:

● DOM y KDE3.  
● ET++, framework de aplicaciones.  

## Patrones relacionados:

● Adapter  
● Abstract Factory  

## Bibliografía:

No específico. (No específico). GoF Design Patterns (Versión 2.1.0) [Aplicación móvil].
Descargado de: ​https://drive.google.com/file/d/0BywiVyFlIabXcVhGZlJBcnhWTkU/view​.  

García, D. PATRONES ESTRUCTURALES (IV): PATRÓN BRIDGE. (Marzo 2014).
PATRONES ESTRUCTURALES (IV): PATRÓN BRIDGE. Consultado en:
https://danielggarcia.wordpress.com/2014/03/17/patrones-estructurales-iv-patron-bridge/commen
t-page-1/​.  

Junta de Andalucía. (s.f). Puente. Marco de Desarrollo de la Junta de Andalucía.
http://www.juntadeandalucia.es/servicios/madeja/contenido/recurso/201​.
