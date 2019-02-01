# Proxy

## Nombre:

Proxy

## Clasificación del patrón:

Estructural

## Intención:

Suministra un sustituto o un delegado para controlar el acceso de un objeto.

## Otros nombres:

Surrogate, sustituto.

## Motivación:

Entre las razones principales de no proporcionar el acceso directo a un objeto radica en reducir el
costo de la creación y mantenimiento del mismo hasta que es realmente necesario. Un ejemplo
sería algún software que implemente varias imágenes en diferentes instancias de la página, para
que el sitio cargue de manera eficiente se puede restringir el acceso de las imágenes hasta que se
muestren realmente.

## Aplicabilidad:

**Se debe usar cuando el acceso al objeto real puede no ser posible:**

● Se debe utilizar un componente remoto.  
● Un objeto costoso tiene que ser creado por demanda.  
● El acceso al objeto original debe ser restringido.  
● Solicitud frecuente de almacenamiento en caché para evitar llamadas de red.  
● Gestión automática de recursos en el caso de C++.  

## Estructura:

![Estructura](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Proxy/Im%C3%A1genes/Estructura.png)

## Participantes:

● Sujeto: Define una interfaz común para el Proxy y el Sujeto real, de manera que se pueda
usar Proxy donde espera un objeto real.  
● SujetoReal: Define el objeto real representado.  
● Proxy: Mantiene una referencia que le permite acceder al objeto real. Proporciona una
interfaz idéntica al Sujeto de manera que se pueda aplicar la sustitución por el
SujetoReal. Puede ser responsable de la creación y borrado de SujetoReal.  

## Colaboraciones:

Proxy hace las veces del SujetoReal cuando se considere apropiado.

**Ventajas:**

● Proxy introduce una indirección que puede ser útil.  
● El proxy remoto oculta la ubicación del objeto real al cliente que lo está usando.  
● Los proxies virtuales pueden crear objetos por demanda.  
● La protección del proxy limita el acceso al objeto.  
● Los puntos inteligentes ayudan a la gestión automática en C++.  

**Desventajas:**

● Puede haber un acoplamiento “apretado” entre el proxy y el sujeto real.  
○ En especial si el objeto inicia su creación por demanda.  

## Implementación:

● Proxy no siempre conoce el tipo de objeto de SujetoReal. En caso de que no se deben
instanciar objetos del SujetoReal no ocurre nada, mientras que en otro caso sí.  
● Sobrecarga de operadores de acceso.  

## Código de ejemplo:

● Interfaz del servidor de descargas:

![Interfaz del servidor de descargas](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Proxy/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%201.png)

● Servidor real:

![Servidor real](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Proxy/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%202.png)

● Proxy:

![Proxy](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Proxy/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%203.png)

● Principal:

![Principal](https://github.com/brayanpasa99/Patrones/blob/master/Patrones%20estructurales/Proxy/Im%C3%A1genes/C%C3%B3digo%20de%20ejemplo%204.png)

## Usos conocidos:

● NEXTSTEP para representar objetos en distribución, NXProxy.

## Patrones relacionados:

● Adapter  
● Decorator  
● Iterator  

## Bibliografía:
No específico. (No específico). GoF Design Patterns (Versión 2.1.0) [Aplicación móvil].
Descargado de: ​https://drive.google.com/file/d/0BywiVyFlIabXcVhGZlJBcnhWTkU/view​.  

Patrones de Diseño (XIII): Patrones Estructurales - Proxy [Página web]. (s.f.). Ubicación
https://programacion.net/articulo/patrones_de_diseno_xiii_patrones_estructurales_proxy_1016​.  

O. Patrones de diseño. (Mayo de 2009). Proxy. Consultado en:
http://dracohaste.blogspot.com/2009/05/patron-proxy.html​.  

Junta de Andalucía. (s.f). Proxy. Marco de Desarrollo de la Junta de Andalucía.
http://www.juntadeandalucia.es/servicios/madeja/contenido/recurso/200​.
