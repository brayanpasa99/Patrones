# Flyweight

## Nombre:

Flyweight

## Clasificación del patrón:

Estructural

## Intención:

Uso compartido soporta un largo número de objetos de peso fino eficientemente.

## Otros nombres:

Peso mosca, Peso Ligero.

## Motivación:

Se utilizan objetos que almacenan los estados compartidos y que pueden ser utilizados por varios
objetos de forma simultánea, con éste describe cómo almacenar un gran número de objetos sin
gran costo.

## Aplicabilidad:

**Se usa cuando:**

● Una aplicación usa un gran número de objetos.  
● El costo de almacenamiento es alto por una larga cantidad de objetos.  
● El estado del objeto puede ser hecho extrínseco.  
● La aplicación no depende de la identidad de los objetos.  
● Muchos objetos pueden ser representados por relativamente pocos objetos compartidos
una vez el estado extrínseco es removido.  

## Estructura:

![Estructura](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Flyweight/Im%C3%A1genes/Estructura.png)

## Participantes:
 
● PesoLigeroConcreto: Implementa la interfaz PesoLigero.  
● PesoLigero: Define una interfaz a través de la cual los PesosLigeros pueden recibir y
actuar sobre estados no compartidos.  
● PesoLigeroConcretoNoCompartido: No todas las subclases de PesoLigero son
compartidas.  
● Cliente: Contiene referencias de los PesosLigeros.  
● FactoriaPesoLigero: Crea y gestiona los PesoLigero, garantiza que se compartan
adecuadamente.  

## Colaboraciones:

Los clientes invocan a la FactoriaPesoLigero. El estado se mantiene por el cliente y se pasa
cuando se invocan los métodos que lo solicitan.

**Ventajas:**

● Las ventajas dependerán de la habilidad de compartir intrínsicamente estados entre
objetos.  
● Si el estado instrínseco es largo, resultaría menos memoria de uso.  
● Si el número de PesoLigeros es grande mayor será el almacenamiento ahorrado.  

**Desventajas:**

● El costo del tiempo de ejecución dependerá del tiempo del cálculo extrínseco y luego el
de transferirlo a los objetos.  

## Implementación:

● Asegurar que el rendimiento es un tema primordial y el cliente está dispuesto a asumir los
reajustes.  
● Dividir el objetivo principal en estados: Intrínseco (Elementos compartidos o comunes) y
Extrínsecos (Elementos particulares de cada tipo).  
● Retirar elementos con estado extrínseco de los atributos y añadir llamadas a métodos.  
● Crear una fábrica que pueda almacenar y reutilizar instancias existentes de clases.  
● Se debe usar la fábrica en vez de utilizar “new” o cualquier otra palabra reservada para la
creación de objetos.  

## Código de ejemplo:

● Main:

![Main](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Flyweight/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%201.png)

● Fabrica de lineas:

![Fabrica de lineas](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Flyweight/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%202.png)

● I línea ligera:

![ILínea Ligera](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Flyweight/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%203.png)

● Línea:

![Línea](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Flyweight/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%204.png)

## Usos conocidos:

● Interfaces de usuario de aplicaciones.

## Bibliografía:

No específico. (No específico). GoF Design Patterns (Versión 2.1.0) [Aplicación móvil].
Descargado de: ​https://drive.google.com/file/d/0BywiVyFlIabXcVhGZlJBcnhWTkU/view​.  

Patrones de Diseño Software [Página Web]. (s.f.). Ubicación:
https://informaticapc.com/patrones-de-diseno/flyweight.php​.  

Junta de Andalucía. (s.f). Peso Ligero. Marco de Desarrollo de la Junta de Andalucía.
http://www.juntadeandalucia.es/servicios/madeja/contenido/recurso/197​.
