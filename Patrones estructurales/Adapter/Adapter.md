# Adapter

## Nombre:

Adapter

## Clasificación del patrón:

Estructural

## Intención:

Convierte la interfaz de una clase en otra interfaz esperada por el cliente. Adapter permite que
clases que no podrían trabajar juntas debido a que tienen interfaces incompatibles, lo hagan.

## Otros nombres:

Wrapper, Adaptador, Envoltorio

## Motivación:

En el mundo de hoy es habitual el uso de adaptadores (cargadores, tipos de enchufes,
transformadores, etc.). En el mundo del software algunas veces un conjunto de clases no se
puede reutilizar debido a que la interfaz no concuerda con el dominio que la aplicación requiere.
Allí nace Adapter para facilitar esa reutilización y permite que no se deba modificar a gran escala
el código.

## Aplicabilidad:

**Se debe usar cuando:**

● Usar una clase existente que tenga una interfaz no compatible.  
● El objeto adapter usa varias subclases para la adaptación.  
● La clase adapter invalida algunos de los comportamientos de la adaptación.  

## Estructura:

![Estructura](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Adapter/Im%C3%A1genes/Estructura.png)

## Participantes:

● Objetivo: Define la interfaz específica que espera el Cliente.  
● Cliente: Colabora con la conformación de objetos para la interfaz Objetivo.  
● Inicial: Define una interfaz o clase existente que requiere adaptarse.  
● Adaptador: Adapta la interfaz Inicial a la Objetivo.  

## Colaboraciones:

La clase Cliente llama a las operaciones sobre una instancia Adaptador. Luego, Adaptador llama
a las operaciones de Inicial que llevan a cabo el pedido.

**Ventajas:**

Una clase Adapter:  

○ Usa el adaptador directamente llamando los métodos heredados.  
○ Puede anular el comportamiento del adaptador.  

Un objeto Adapter:

○ Deja que un simple Adapter se relacione con muchos adaptadores.  

## Desventajas:

● Una clase Adapter no puede ser usada si las subclases de adaptación deben ser adaptadas
también.  
● Un Adapter de objetos no puede reemplazar el comportamiento de la adaptación.  

## Implementación:

● ¿Qué nivel de adaptación debe hacer el Adapter?: La cantidad de trabajo que el Adapter
hace depende de la similitud de la clase Inicial y la clase Objetivo, ese trabajo puede ser
simple como cambiar el nombre de las operaciones o puede encerrar todo un espectro de
operaciones diferentes.  
● Adaptadores Pluggables: La adaptación de la interfaz permite incorporar nuestra clase en
sistemas existentes que pueden esperar diferentes interfaces para la clase.
Para implementarlo de forma correcta se aconseja crear una nueva clase que sea el Adapter, que
extienda del componente existente e implemente la interfaz obligatoria.  

## Código de ejemplo:

● Cliente:

![Cliente](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Adapter/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%201.png)

● Objetivo:

![Objetivo](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Adapter/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%202.png)

● Adaptador:

![Adaptador](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Adapter/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%203.png)

● Adaptable:

![Adaptable](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Adapter/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%204.png)

## Usos conocidos:

● EventListener que le permite a un objeto ejecutar un evento.  
● WindowsListener que extiende de EventListener  

## Patrones relacionados:  

● Proxy  
● Decorator  

## Bibliografía:

No específico. (No específico). GoF Design Patterns (Versión 2.1.0) [Aplicación móvil].
Descargado de: ​https://drive.google.com/file/d/0BywiVyFlIabXcVhGZlJBcnhWTkU/view​.  

Patrones de Diseño Software [Página web]. (s.f.). Ubicación
https://informaticapc.com/patrones-de-diseno/adapter.php​.  

Junta de Andalucía. (s.f). Adaptador. Marco de Desarrollo de la Junta de Andalucía.
http://www.juntadeandalucia.es/servicios/madeja/contenido/recurso/181​.
