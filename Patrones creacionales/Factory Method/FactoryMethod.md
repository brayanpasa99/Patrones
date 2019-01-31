# Factory Method

## Nombre:

Factory Method

## Clasificación del patrón:

Creacional

## Intención:

Define una interfaz para crear un objeto, pero deja que las subclases decidan la clase a instanciar.
Factory Method permite dejar la instanciación de las clases a las subclases.

## Otros nombres:

Constructor virtual

## Motivación:

En un Framework se puede identificar o suponer que se usan las clases abstractas para el
mantenimiento y la definición de objetos.

## Aplicabilidad:

**Se debe usar cuando:**

● El cliente no sepa que clase puede requerir un Runtime  
● Una clase quiere que sus subclases especifiquen los objetos que crea  
● Se requiere encapsular la creación de objetos  
● Una instancia de un objeto debe ser inicializada con algún dato no disponible por el
cliente  
● Una instanciación requiere muchos datos y hay muchas varaciones basados en los datos.
Se provee un static Factory Method que crea las instancias con base en las diferentes
variaciones.  

## Estructura:

![Estructura](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20creacionales/Factory%20Method/Im%C3%A1genes/Estructura.png)

## Participantes:

● Producto: Define la interfaz de los objetos que la factoría crea.  
● Producto Concreto: Define la interfaz del producto.  
● Creador: Declara el método factoría que devuelve un producto concreto.  
● Creador Concreto: Sobreescribe el método factoría para que devuelva un Producto
Concreto.  

## Colaboraciones:  

El creador busca entre las subclases y devuelve una instancia adecuada de Producto Concreto.  

**Ventajas:**

● Promueve el bajo acoplamiento entre el cliente y las clases que utiliza.  
○ No necesita depender de clases concretas.  
● Encapsula la creación.  
○ Controla la creación.  
● Se comporta como un constructor virtual.  
○ Se crea una instancia virtual. El cliente no sabe cual instancia obtuvo.  
● Puede no crear un nuevo objeto con cada llamado.  
○ Los objetos pueden almacenarse en caché para su rendimiento y reutilización.  

**Desventajas:**

● Se requiere que corresponda una clase factoría para cada clase concreta.  

## Implementación:  

**Se deben considerar dos variantes:**

○ La clase Creador es abstracta y no existe una implementación del método
Factoría.  
○ Creador es una clase concreta y provee una implementación del método Factoría.  

● Existe una variación del patrón que consiste en Factory Method con parámetros.  
● Variantes y especificaciones del lenguaje.  
● Plantillas para evitar la herencia.  

## Código de ejemplo:  

● Producto:

![Producto](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20creacionales/Factory%20Method/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%201.png)

● Pago con tarjeta:

![Pago con tarjeta](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20creacionales/Factory%20Method/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%202.png)

● Pago con Paypal:

![Pago con Paypal](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20creacionales/Factory%20Method/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%203.png)

● Pago transferencia bancaria:

![Pago transferencia bancaria](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20creacionales/Factory%20Method/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%205.png)

● Creador concreto:

![Creador concreto](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20creacionales/Factory%20Method/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%205.png)

● Principal:

![Principal](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20creacionales/Factory%20Method/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%207.png)

## Usos conocidos:

● Frameworks.  
● Creación de proxys en middlewares.  

## Patrones relacionados:

● Abstract Factory

## Bibliografía:

No específico. (No específico). GoF Design Patterns (Versión 2.1.0) [Aplicación móvil].
Descargado de: ​https://drive.google.com/file/d/0BywiVyFlIabXcVhGZlJBcnhWTkU/view​.  

Patrones de diseño clásicos [Página web]. (s. f.). Ubicación
http://www.lsi.us.es/docencia/get.php?id=604​.  

Zuluaga, P. (21 de abril de 2015). Factory Method. Patrones de Software.
http://patronesdedis.blogspot.com/2015/04/factory-method.html  

Junta de Andalucía. (s.f). Factoría. Marco de Desarrollo de la Junta de Andalucía.
http://www.juntadeandalucia.es/servicios/madeja/print/424​.
