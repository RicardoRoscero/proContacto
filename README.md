# proContacto

EJERCICIO 2 



Las siguientes preguntas están orientadas a la comprensión del protocolo HTTP. Son agnósticas al lenguaje de programación, la idea es comprender los conceptos del estándar:
1. ¿Qué es un servidor HTTP? 
Un servidor HTTP, en términos más sencillos, es un ordenador que procesa, almacena y entrega archivos pertenecientes a sitios web a los navegadores. Se conforman por hardware y software que utilizan el protocolo de transferencia de hipertexto para lograr responder peticiones de los usuarios dentro de la web.  
2. ¿Qué son los verbos HTTP? Mencionar los más conocidos
Son utilizados para la recuperación de información proveniente de un recurso. Los verbos involucrados en un servicio REST son: 
Get
Post 
Put
Patch 
Delete
		Get es utilizado para consultar un recurso .
		Post es utilizado para creación de nuevos recursos.
		Put y patch son similares, se utilizan para modificar un recurso ya existente. 
		Delete, como su nombre lo indica se utiliza para eliminación de registros. 
3. ¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers? 
Resquest: Línea de salida de una petición HTTP. Esta siempre formará parte de la primera línea del mensaje de solicitud y se conforma por tres campos 
Un método HTTP.
Un identificador universal de recursos (Url)
La versión del protocolo http utilizado.  
Response: Una vez que el servidor recibió y procesó la solicitud este devuelve un mensaje  de respuesta HTTP que es conocido también como línea de estado (Por ejemplo: HTTP/1.1 200 OK). 
En cuanto a los headers o cabeceras, estas permiten al cliente y al servidor el envío de información adicional junto a un request o response. Una cabecera de petición se encuentra compuesta por su nombre seguido de dos puntos (:) y a continuación un valor (que no contiene saltos de línea). 
Pueden existir diversos tipos de headers dependiendo del contexto: 
-Cabecera en general.
-Cabecera de consulta.
-Cabecera de respuesta. 
-Cabecera de entidad. 
4. ¿Qué es un queryString? (En el contexto de una url)
El queryString forma parte de una url que asigna valores a los parámetros que son especificados. Hace referencia a una interacción con una base de datos.
Es la parte de una URL que contiene los datos que deben ser transmitidos a aplicaciones web. Dentro de los métodos, query string permite mayor precisión al momento de enviar información a través de la url. Un ejemplo sería: 
Al realizar una petición a la ruta “/users” la respuesta (ya sea un objeto, una página web, un objeto JSON o XML) tendrá relación con los usuarios. 
Al nosotros realizar la petición de la siguiente forma: “/users?order=true” se realizará la misma petición, con la diferencia de que el servidor nos debe retornar a los usuarios de manera ordenada. Todo lo que está después del signo de interrogación es el queryString y se conforma por la siguiente estructura: 
__ llave (nombre del parametro) , signo igual (=) y valor. __
5. ¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?
Representan el status de completitud de una solicitud HTTP específica. Las respuestas se agrupan en los siguientes tipos: 
Respuestas informativas (Que van del 100-199)
Respuestas satisfactorias (Que van del 200-299)
Redirecciones (Que van del 300-399)
Errores de los clientes (400-499)
Errores de los servidores(500-599)
6. ¿Cómo se envía la data en un Get y cómo en un POST? 

En cuanto al envío de información: 
Dentro del método GET, los datos son visibles por la URL, por ejemplo:
www.uvm.com.mx/action.php?nombre=pedro&apellidos1= gomez
Dentro del método POST envía los datos de manera “oculta”, no se muestra en la url, por ejemplo: 
<form action="http://www.uvm.com.mx/prog/newuser" method ="post">

7. ¿Qué verbo http utiliza el navegador cuando accedemos a una página?
GET, ya que es utilizado cuando se solicita un recurso. 
8. Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.
JSON: Formato basado en texto que representan datos estructurados dentro de la sintaxis de objetos de JavaScript. Se utiliza ampliamente para transmitir datos en aplicaciones web. Se puede dar una jerarquía de datos como la siguiente: 
{
  "nombreGrupo": "Escuadrón de superhéroes",
  "ciudadNatal": "Ciudad de México",
  "formado": 2015,
  "baseSecreta": "Súper torre",
  "activo": true,
  "miembros": [
    {
      "nombre": "Hómbre Molécula",
      "edad": 30,
      "identidadSecreta": "Ricardo Roscero",
      "poderes": [
        "resistencia a la radiación”
      ]
    }
] … 
XML: El Lenguaje de Marcado Extensible permite definir, compartir y almacenar datos de forma compartible, por lo que esto le da un alto grado de portabilidad y admite el intercambio de información entre sistemas (como bien podrían ser sitios web, bases de datos, aplicaciones de terceros, etc). Utilizando como ejemplo, un XML que contiene información sobre libros: 

<?xml version="1.0"?>
<Catalog>
   <Book id="bk101">
      <Author>Garghentini, Davide</Author>
      <Title>XML Developer's Guide</Title>
      <Genre>Computer</Genre>
      <Price>44.95</Price>
      <PublishDate>2000-10-01</PublishDate>
      <Description>An in-depth look at creating applications
      with XML.</Description>
   </Book>
   <Book id="bk102">
      <Author>Garcia, Debra</Author>
      <Title>Midnight Rain</Title>
      <Genre>Fantasy</Genre>
      <Price>5.95</Price>
      <PublishDate>2000-12-16</PublishDate>
      <Description>A former architect battles corporate zombies,
      an evil sorceress, and her own childhood to become queen
      of the world.</Description>
   </Book>
</Catalog>

9. Explicar brevemente el estándar SOAP
Simple Object Acces Protocol es un protocolo ligero utilizado para intercambiar información dentro de entornos descentralizados y distribuídos. Los mensajes SOAP pueden combinarse para crear patrones de petición o respuesta. 
SOAP se encuentra basado en XML el cual define en tres partes los mensajes: 
Sobre.
Reglas de codificación.
Estilos de comunicación.  
10. Explicar brevemente el estándar REST Full
Se encuentra considerada como un servicio que funciona como un estándar para compartir información en un sistema de doble vía (Request - Response)
Esta arquitectura trabaja sobre el protocolo HTTP, los procedimientos y métodos de comunicación (verbos) son los mismos que HTTP. 
Un componente importante de un REST full Api es “HTTP Status Code” el cual tiene como tarea principal informar al cliente o consumidor del API, qué debe hacer con la respuesta recibida. Es una referencia universal del resultado obtenido.

11. ¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?
Son esquemas clave-valor que contienen información sobre el HTTP request y el navegador; de igual forma aquí se alojan los datos de las cookies. La mayoría de los headers son opcionales. 
El content-type (También conocido como media type o MIME type), es un recurso que se utiliza dentro del header HTTP y que indica al cliente o navegador qué clase de medio o archivo le está enviando el servidor. 
Dicho de otra forma, especificar el tipo de contenido ayuda a los user agents a comprender el contexto y poder así mejorar la experiencia de usabilidad, al mostrar el medio o archivo de la mejor manera posible.  

EJERCIICIO 3 

Recomendamos previamente entender los conceptos de la sintaxis “json” antes de arrancar con los ejercicios.
Descargar el POSTMAN (aplicación para realizar request como cliente), adjuntando un screen de resolución para cada ítem:

Realizar un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json
Realizar un request POST a la URL anterior, y con body:
{
"name":"Tu nombre",
"email":tunombre.tuapellido@procontacto.com.mx
}
Tip: (Marcar la opción “raw” como body)
Realizar nuevamente un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.jso
¿Qué diferencias se observan entre las llamadas el punto 1 y 3?
Se muestran los datos agregados mediante el verbo post: 


