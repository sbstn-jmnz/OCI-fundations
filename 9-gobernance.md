# Gobierno y administración

Bienvenido a este módulo sobre gobernanza y administración. Como parte de este módulo, la primera lección que veremos es sobre los precios. 

Ahora el precio es un tema complejo. Muchos precios con muchos proveedores de nube son complejos. El precio de Oracle es simple. Es transparente. Y es un precio más bajo que el de nuestros competidores. Entonces, veamos algunos de estos en esta lección en particular.

Lo primero es ¿qué tipo de modelos de precios apoyamos? Por lo tanto, definitivamente apoyamos los precios de pago por uso, en los que cobra solo por los recursos que consume. No hay ningún compromiso inicial. No existe un período mínimo de servicio. Y el uso está medido. Este es un sistema de pago por uso para la mayoría de los recursos.

Pero para algunos recursos, como nuestra plataforma administrada sin servidor llamada Functions, lo lleva al siguiente nivel. Entonces tenemos este concepto de precios basados ​​en el consumo, en el que se le cobra solo cuando consume el recurso, lo cual es diferente al pago por uso, porque tiene que pagar por las máquinas virtuales, aunque no las esté usando o puedan estarlo funcionando inactivo.

Por lo tanto, apoyamos el pago por uso y los precios basados ​​en el consumo y todo tipo de modelos intermedios. Y luego, el segundo modelo que apoyamos se llama **Créditos Universales Anuales**. Y la idea aquí es que se comprometa con un fondo común anual. A cambio, gracias a este compromiso, obtendrá importantes ahorros. Pero la cuestión es que debes utilizar estos créditos dentro de los 12 meses.

Si termina con un mayor uso de recursos, entonces los paga según el uso. Y los descuentos aquí varían según el tamaño y el plazo de la oferta. También existe algo llamado **Crédito Universal Mensual**. Y debería leer más sobre eso en nuestro sitio web.

Y la última opción es traer tus propias licencias. Esto es para clientes que ejecutan licencias locales si desean reutilizarlas en la nube. ¿Por qué lo harías? Reduce su costo general y puede reutilizar esas licencias en la nube.

Ahora veamos los factores que afectan los precios. El primer factor que afecta el precio es el tamaño del recurso. Por lo tanto, mayores recursos le costarán más. Eso es natural, porque el **precio del servicio se basa en el consumo y el tipo de recurso que utiliza (tamaño)**. Por lo tanto, los recursos más grandes le costarán más.

La transferencia de datos es una gran parte del precio. Y hablaremos de algo de eso en la siguiente diapositiva. El tipo de recurso que elija también determina su precio. Por lo tanto, las máquinas virtuales frente a las bare metal tienen un precio diferente y las máquinas sin servidor tienen un precio diferente. Si trae sus propias licencias, tendrán un modelo de precios completamente diferente. Así que ten todo eso en cuenta.

**Una cosa a tener en cuenta con OCI es que tenemos los mismos precios en todo el mundo**. Entonces todas las regiones de OCI tienen el mismo precio. Esto es muy diferente al típico modelo tradicional de nube, donde el precio es muy local. Entonces pagas un lugar diferente en Estados Unidos. Pagas un lugar diferente fuera de EE. UU. en diferentes países donde operan las regiones de la Nube.

Veamos el costo de la transferencia de datos y por qué es tan importante. Bueno, la cuestión es que la transferencia de datos puede suponer hasta una cuarta parte de tu factura o incluso más. Y la razón es que sus aplicaciones siempre se están comunicando, ya sea con los usuarios finales o internamente.

Entonces, para dar un ejemplo, si nos fijamos en la Región 1 de OCI, tenemos 2 dominios de disponibilidad. Tiene una aplicación que podría estar ejecutándose en modo de alta disponibilidad en dos dominios de disponibilidad. Ahora bien, en el caso de OCI, realmente no paga por ninguna transferencia de datos que se realice entre estos dos AD, como puede ver en el gráfico aquí. En el caso de otros proveedores de nube, le cobran por la transferencia de datos entre AD.

En cierto modo, esto penaliza a los clientes por lograr una alta disponibilidad, que es uno de los objetivos de la computación en la nube. Entonces no tiene mucho sentido de esa manera. Además, con Oracle, el tráfico entrante es gratuito ya que es el estándar de la industria. **Pero el tráfico saliente es 10 veces menor que el de algunos de los otros proveedores de la nube**. Y me escuchaste bien. Es 10 veces menor. No es un 10% más bajo. Es casi 10 veces menor.

De esta manera ahorrarás mucho dinero, especialmente si tienes aplicaciones que tienen un alto uso de transferencia de datos. Terminarás ahorrando significativamente usando OCI. Y eso es. Queríamos mantenerlo en un nivel muy alto, muy simple: los tres modelos de precios que apoyamos.

Y lo más destacado de nuestros precios es que son simples. Es transparente. Y algunos de los elementos como la transferencia de datos te cuestan 10 veces menos. Por lo tanto, definitivamente es mucho más barato que algunos de los precios tradicionales de la nube que existen.

## Administración de costos

Bienvenido a esta lección sobre Gestión de Costos. Veamos qué herramientas le proporciona OCI para gestionar sus costos. Entonces, la primera opción que tiene son estas cosas llamadas **Presupuestos OCI**. Puede utilizar presupuestos para realizar un seguimiento de los costos de su arrendamiento. Después de crear un presupuesto para un compartimento, puede configurar alertas que le notificarán si se prevé que se excederá un presupuesto o si el gasto supera una determinada cantidad.

Como puede ver aquí en la pantalla, tenemos dos tipos de presupuestos establecidos, uno para $1000 y otro para $100. Y podrías mirar el pronóstico y otras cosas y recibir una notificación si estás cerca de excederlo o si lo has excedido. Es una forma importante de administrar sus costos y recibir notificaciones si el costo supera su pronóstico o sus planes.

La segunda herramienta, que está a su disposición, se refiere al análisis de costes. Y esto, como su nombre lo indica, puede analizar su costo después de haberlo gastado, pero es una buena manera de ver su costo pasado y luego realizar cambios para el futuro. Si hay elementos que desea cambiar, esta es una excelente manera de hacerlo.

También hay informes de uso. Hoy en día, los informes de uso se descargan en forma de estos archivos CSV y se generan diariamente. Y muestran datos de uso de cada recurso de su arrendamiento. Los archivos CSV se almacenan en un depósito de almacenamiento de objetos al que se puede acceder mediante una política de arrendamiento cruzado, por lo que puede examinar no solo su arrendamiento, sino también varios arrendamientos si se utilizan varios arrendamientos.

Ahora, un par de herramientas más en esta área incluyen límites de servicio, la herramienta para establecer sus límites, cuota y uso. Entonces, como ocurre con cualquier nube, limitamos la cantidad de recursos que puede ejecutar en un arrendamiento tradicional para evitar situaciones como fraude y uso indebido. Pero siempre puedes... en casos legítimos, siempre puedes cambiar tus límites para un servicio en particular, y hay una manera de ver tus límites actuales y cambiarlos. Y podría enviar una solicitud de soporte para hacerlo, pero esa herramienta le proporciona de un vistazo qué tipo de límites ha desglosado por cosas como su dominio de disponibilidad para que pueda profundizar más y obtener más detalles aquí.

Luego, finalmente, como mencionamos, los compartimentos son estas entidades lógicas, que puede usar para aislar recursos y tener mejor acceso a estos recursos, por lo que si usa estos compartimentos, tiene la posibilidad de configurar cuotas de compartimentos. Y la forma en que funciona es que usted tiene estas diferentes políticas que puede escribir, donde puede establecer la cantidad máxima de recursos de la nube que se pueden usar para un compartimento. Entonces se podría decir que, en este compartimento en particular, solo se pueden usar, digamos, 10 máquinas virtuales. Puede desarmar eso y volver a los límites de servicio predeterminados, o puede ponerlo a cero. Entonces, a modo de ejemplo, se podría decir que este compartimento en particular no debería tener ningún recurso de Exadata. Y podría hacerlo para evitar el uso indebido y también ahorrar costos.

En resumen, esa es su gestión de costos: muchas herramientas disponibles, incluido el presupuesto, incluidos informes de uso, análisis de costos, capacidad para establecer cuotas, capacidad para aumentar sus límites de servicio y mucho más. Debe consultar nuestra documentación para obtener más información sobre todas las formas en que puede administrar sus costos en OCI. Espero que hayas encontrado útil esta lección. Gracias por ver.
