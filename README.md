# proContacto

------------------------------EJERCICIO 2------------------------------



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

------------------------------EJERCICIO 3------------------------------

Recomendamos previamente entender los conceptos de la sintaxis “json” antes de arrancar con los ejercicios.
Descargar el POSTMAN (aplicación para realizar request como cliente), adjuntando un screen de resolución para cada ítem:

--Realizar un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json
	
	https://raw.githubusercontent.com/RicardoRoscero/proContacto/master/img/GET.png
	
	
--Realizar un request POST a la URL anterior, y con body:
{
"name":"Tu nombre",
"email":tunombre.tuapellido@procontacto.com.mx
}
	
	https://raw.githubusercontent.com/RicardoRoscero/proContacto/master/img/POST.png
	
	
Tip: (Marcar la opción “raw” como body)
	
--¿Qué diferencias se observan entre las llamadas el punto 1 y 3?
Se muestran los datos agregados mediante el verbo post: 
	
	
	https://raw.githubusercontent.com/RicardoRoscero/proContacto/master/img/DIF_POST.png
	
------------------------------EJERCICIO 4------------------------------
	
https://trailblazer.me/id/roscero


------------------------------EJERCICIO 5------------------------------

Explicar que son conceptualmente, qué datos almacenan en forma estándar y cómo se relacionan el resto (algunos no se relacionan entre sí) cada uno de los siguientes objetos de Salesforce:

	1. Lead : Es un cliente potencial el cual demuestra interés en un producto o servicio ofrecido por la marca mediante la interacción con contenidos y otros materiales. 
	2. Account: Representa una cuenta individual, la cual puede estar relacionada con una persona o con la organización (clientes, competidores o socios).
	3. Contact: Representa un contacto el cual es una persona asociada con una cuenta (account). 
	4. Opportunity: Representa una oportunidad el cual es una venta o un negocio pendiente. 
	5. Product: Representa un producto que es vendido por la compañía.
	6. PriceBook: Representa un libro de precios que contiene la lista de lo que se vende dentro de la organización. 
	7. Quote: Representa una cotización. Es un registro que muestra los precios propuestos para productos y servicios. Las cotizaciones se pueden crear y sincronizar con oportunidades y se pueden enviar mediante correo electrónico como pdf a los clientes. 
	8. Asset: Representa un objeto de valor comercial el cual es vendido por una compañía o por la competencia. 
	9. Case: Es un caso, el cual es un problema o inconveniente con el cliente. 
	10. Article: Es una selección de categoría de datos. Se puede utilizar para asociar un artículo con categorías de datos. 
	
	
	
	
	

	
------------------------------EJERCICIO 6------------------------------

		Soluciones de Salesforce
	
	1.¿Qué es Salesforce?
Empresa Americana conocida por producir el CRM Sales Cloud. 
	
	2.¿Qué es Sales Cloud?
Es un módulo de Salesforce que permite gestionar de forma eficiente las relaciones con tus clientes y la colaboración entre equipos comerciales. Ofrece automatización y productividad para la fuerza de ventas optimizando los procesos comerciales y alineándolos con el marketing de tu empresa y servicio de atención al cliente.
Dispone de gráficos sobre rendimiento en tiempo real y análisis sobre cuentas para que puedas tomar decisiones de forma rápida e inteligente.
	
	3.¿Qué es Service Cloud?
Service Cloud es uno de los componentes de la plataforma Salesforce Customer 360, lo que permite tener una vista de 360 grados de loss clientes y así lograr una atención más inteligente, rápida y personalizada. Con Service Cloud, se pueden automatizar los procesos de servicio, optimizar flujos de trabajo, compartir información relevante para transformar la experiencia de los agentes de servicio y brindar soporte por una diversidad de canales a cualquier hora y en cualquier lugar.
	4.¿Qué es Health Cloud?
Software de gestión de pacientes.
	
	5.¿Qué es Marketing Cloud?
Marketing Cloud es una plataforma de Salesforce que las pymes y grandes empresas pueden utilizar para invertir en estrategias de email marketing de nivel profesional.
	
		Funcionalidades de Salesforce
	1.¿Qué es un RecordType?
Se usa este objeto para ofrecer diferentes registros de BusinessProcess y subconjuntos de valores de lista de selección a diferentes usuarios en función de su perfil. Su aplicación cliente puede describir o consultar registros de RecordType.
	
	2.¿Qué es un ReportType?
Los eventos de informe contienen información sobre lo que sucedió cuando un usuario hizo un informe. Este tipo de evento incluye toda la actividad que se encuentra en el tipo de evento Exportar informe, y más. Por ejemplo, tiene actividad de usuario para informes exportados como informe formateado y salida de solo detalles.
	
	4.¿Qué es un Page Layout?
Se utiliza para modificar la apariencia de los campos, listas, links y controla los botones que serán visibles en las páginas de detalle. 
¿Qué es un Compact Layout?
Un diseño compacto muestra los campos clave de un registro de un vistazo en la aplicación móvil Salesforce, Lightning Experience y en las integraciones de Outlook y Gmail.
	
	5.¿Qué es un Perfil?
Los perfiles definen cómo acceden  los usuarios a los objetos y datos dentro de la aplicación. Al crear usuarios se deben asignar los perfiles. 
	
	6.¿Qué es un Rol?
Mediante los roles, se especifica: 
Los usuarios solo pueden enviar a los registros a los que tienen acceso.
Los usuarios que envían correos electrónicos necesitan acceso de lectura, anexar y anexar para las entidades a las que envían.
El usuario de seguimiento debe tener acceso de actualización para Cuentas, Clientes potenciales y Contactos.
	
	7.¿Qué es un Validation Rule?
Las reglas de validación verifican que los datos que un usuario ingresa en un registro cumplen con los estándares que usted especifica antes de que el usuario pueda guardar el registro. Una regla de validación puede contener una fórmula o expresión que evalúa los datos en uno o más campos y devuelve un valor de "Verdadero" o "Falso". Las reglas de validación también incluyen un mensaje de error para mostrar al usuario cuando la regla devuelve un valor de "Verdadero" debido a un valor no válido.
	
	8.¿Qué diferencia hay entre una relación Master Detail y Lookup?
Maestro-Detalle (1:n) — Una relación padre-hijo en la que el objeto maestro controla ciertos comportamientos del objeto de detalle:
Cuando se elimina un registro del objeto maestro, también se eliminan sus registros de detalles relacionados.
El campo Propietario en el objeto de detalle no está disponible y se establece automáticamente en el propietario de su registro maestro asociado. Los objetos personalizados en el lado del detalle de una relación maestro-detalle no pueden tener reglas de colaboración, colaboración manual o colas, ya que requieren el campo Propietario.
El registro de detalle hereda la configuración de uso compartido y seguridad de su registro maestro.
El campo de relación maestro-detalle es obligatorio en el formato de página del registro de detalle.
De forma predeterminada, los registros no se pueden cambiar de padre en relaciones maestro-detalle. Sin embargo, los administradores pueden permitir que los registros secundarios en relaciones maestro-detalle en objetos personalizados se vuelvan a vincular a diferentes registros principales seleccionando la opción Permitir cambio de parentesco en la definición de la relación maestro-detalle.

Búsqueda (1:n): este tipo de relación vincula dos objetos, pero no tiene ningún efecto sobre la eliminación o la seguridad. A diferencia de los campos maestro-detalle, los campos de búsqueda no se requieren automáticamente. Cuando define una relación de búsqueda, los datos de un objeto pueden aparecer como una lista relacionada personalizada en los formatos de página para el otro objeto. Consulte la Ayuda de Salesforce para obtener detalles.
	
	9.¿Qué es un Sandbox?
Los entornos Sandbox crean copias de su organización de Salesforce en entornos separados. Utilícelos para el desarrollo, las pruebas y la formación sin comprometer los datos y las aplicaciones de su organización de producción.
	
	10.¿Qué es un ChangeSet?
Utilice conjuntos de cambios para enviar personalizaciones de una organización de Salesforce a otra. Por ejemplo, puede crear y probar un nuevo objeto en una organización sandbox y luego enviarlo a su organización de producción mediante un conjunto de cambios. Los conjuntos de cambios solo pueden contener modificaciones que puede realizar a través del menú Configuración. Por ejemplo, no puede usar un conjunto de cambios para cargar una lista de registros de contactos. Los conjuntos de cambios contienen información sobre la organización. No contienen datos, como registros
	
	11.¿Para qué sirve el import Wizard de Salesforce?
El Asistente de importación de datos facilita la importación de datos para muchos objetos estándar de Salesforce, incluidas cuentas, contactos, clientes potenciales, soluciones, miembros de campaña y cuentas personales. También puede importar datos para objetos personalizados. Puede importar hasta 50.000 registros a la vez.
	
	12.¿Para qué sirve la funcionalidad Web to Lead?
El proceso de usar un formulario de sitio web para capturar la información del visitante y almacenar esa información como un nuevo prospecto en Salesforce.
	
	13.¿Para qué sirve la funcionalidad Web to Case?
Recopile solicitudes de atención al cliente directamente desde el sitio web de su empresa y genere automáticamente nuevos casos con Web-to-Case. Para configurar Web-to-Case, habilite la función, cree y personalice su formulario web y agregue el formulario a su sitio web.
	
	14.¿Para qué sirve la funcionalidad Omnichannel?
OmniCanal es una característica flexible y personalizable, y puede configurarla de forma declarativa, es decir, sin escribir código. Utilice Omni-Channel para administrar la prioridad de los elementos de trabajo, lo que facilita enrutar elementos de trabajo importantes a los agentes rápidamente. Administre la capacidad de sus agentes para asumir elementos de trabajo para que solo se les asigne la cantidad de asignaciones que pueden manejar. También puede definir qué agentes pueden trabajar en diferentes tipos de asignaciones. Por ejemplo, puede crear un grupo de agentes para responder a clientes potenciales y consultas de ventas, y otro grupo que ayude a los clientes con preguntas de soporte.
	
	15.¿Para qué sirve la funcionalidad Chatter?
Salesforce Chatter permite a los usuarios colaborar en oportunidades de ventas, casos de servicio, campañas y proyectos con aplicaciones integradas y acciones personalizadas. De forma predeterminada, las organizaciones de Salesforce creadas después del 22 de junio de 2010 ya tienen Chatter activado para todos los usuarios. No obstante, si desea que Chatter esté disponible para un grupo limitado de personas en su organización, puede hacer una implantación basada en perfiles en su lugar.


		Conceptos generales
	1.¿Qué significa SaaS?
Software as a Service es un componente de la computación en la nube que permite a los usuarios acceder a recursos y servicios informáticos a través de internet. Los editores de SaaS proporcionarán el servicio alojado en la nube, esto significa que el software es accesible desde la computadora sin la necesidad de instalarlo en la pc.
	
	2.¿Salesforce es Saas?
Salesforce es una plataforma como servicio (PaaS), este concepto se origina a raíz de SaaS. La Sales Cloud, Service Cloud y Community Cloud forman la parte de Software as a Service de Salesforce, mientras que la plataforma Lightning es un componente PaaS.  
	
	3.¿Qué significa que una solución sea Cloud?
Significa que un servicio se ofrece a través de internet y conectividad. Esto implica que los servicios que se ofrecen tienen buen mantenimiento, son seguros, de fácil acceso y se proporcionan bajo demanda. 
Computación en la nube permite el acceso remoto a softwares, almacenamiento de archivos o incluso procesamiento de datos a través de internet. Lo anterior proporciona una alternativa a a la ejecución en una computadora personal o servidor local. 
	4.¿Qué significa que una solución sea On-Premise?
On-premise hace referencia a que el sistema se encuentra localizado dentro de la propia empresa;  es necesario un servidor y manutención por parte de un equipo de TI propio. 
	
	5.¿Qué es un pipeline de ventas?
Es una herramienta dentro de la cual se incluyen los pasos que se llevan a cabo dentro de cualquier proceso de ventas y estos apoyan a comprenderlos de mejor manera. 
Un buen control del pipeline se traduce en mayores beneficios. 
	
	6.¿Qué es un funnel de ventas?
El embudo de ventas es la forma en la que una empresa planea y establece los procesos para ponerse en contexto con los diversos usuarios y así lograr un objetivo final (cuáles sean los objetivos, conversión de clientes, lograr un registro, cerrar una venta, etc). 
	7.¿Qué significa Customer Experience?
La experiencia del cliente es una disciplina estratégica importante dentro de cualquier compañía. Puede generar un valor a las empresas que aumenten sus ventas y a su vez consumidores. 
Hace referencia explícita a generar una relación entre el consumidor y la marca. 
Customer experience es el recuerdo que es generado en la mente del consumidor como consecuencia de una relación con la marca. 
	
	8.¿Qué significa omnicanalidad?
Es una estrategia de comunicación utilizada para contactar con prospectos o clientes a través de diversos canales. El uso de diferentes canales debe realizarse bajo una misma estrategia para lograr llegar al consumidor en el momento indicado. 
	
	9.¿Qué significa que un negocio sea B2B?¿Qué significa que un negocio sea B2C?¿Qué es un KPI?
Es un modelo de negocio que consiste en servicios entre compañías o negocios con el objetivo de mejorar las ventas de los productos y bienes que son ofrecidos. En pocas palabras se habla de una transacción comercial entre empresas. 
Por otro lado, cuando hablamos del modelo de negocio B2C hacemos referencia al Business to consumer, es decir, la actividad comercial entre un negocio y un consumidor individual. 
Esto aplica a cualquier tipo de negocio de venta directa al consumidor y se encuentra fuertemente asociado con el e-commerce.  
	
	10.¿Qué es una API y en qué se diferencia de una Rest API?
API es la Interfaz de Programación de Aplicaciones y presenta funciones y reglas que permiten la interacción y comunicación entre varias aplicaciones. Estas interfaces facilitan la integración de aplicaciones. 
En cuanto a Rest API, es un estilo arquitectónico para diseñar API mediante el protocolo HTTP. Cuenta con gran flexibilidad. 
Se utiliza la Rest API cuando es necesario proporcionar datos al usuario de una aplicación o sitio web desde el servidor de manera directa.
	
	11.¿Qué es un Proceso Batch?
El procesamiento por lotes es el proceso mediante el cual, una computadora completa lotes de trabajo los cuales son a menudo procesados de manera simultánea, secuencial y sin parar. 
Se logra que los trabajos grandes se calculen en partes pequeñas, lo cual permite mejorar la eficiencia cuando se realiza la depuración. 
	
	12.¿Qué es Kanban?
Establecida en primer lugar por Toyota para la mejora del sistema de producción a finales de la década de 1940, KanBan es una forma de apoyar a los equipos a encontrar un equilibrio entre el trabajo que necesitan hacer y la disponibilidad de cada miembro. 
Esta metodología es implementada a través de tableros KanBan y es un método visual de gestión de proyectos que permite a los equipos observar los flujos de trabajos y carga de los mismos. 
Cada columna representa una etapa del trabajo
	
	13.¿Qué es un ERP? 
Planificación de recursos empresariales. Sistema que ayuda a automatizar y administrar los procesos empresariales de diversas áreas (finanzas,venta al por menor, fabricación, cadena de suministro, operaciones y recursos humanos.)
	
	14.¿Salesforce es un ERP?
Salesforce es un CRM (Customer Relationship Management), sin embargo se pueden integrar ambos para que trabajen de manera conjunta.
No es un ERP, Salesforce ofrece diversas soluciones de negocio que pueden ser integradas para mejorar el soporte al ERP, pero no es un producto ERP.
