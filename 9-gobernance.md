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


## Etiquetado

Bienvenido a esta lección sobre etiquetado. El etiquetado es una capacidad muy, muy importante dentro de OCI y definitivamente deberías aprovecharla. Hablemos más sobre ello. Entonces, en esencia, ¿qué es el etiquetado? Las etiquetas son básicamente estos pares de valores clave, que podría utilizar para organizar mejor sus recursos.

Como pueden ver aquí, en este caso en particular, puse dos etiquetas diferentes. Entonces hay una etiqueta que es ambiente con un valor de producción. Y hay otra etiqueta que es proyecto y tiene valor alfa. Y podría hacer varias etiquetas. Siempre debes verificar los límites del servicio en cuanto a cuántas etiquetas puedo colocar en un objeto de la nube en particular. Pero en este caso, pondré dos etiquetas aquí.

Y estos nuevamente, solo para recapitular, son pares clave-valor simples o pares de nombre-valor donde la clave es la clave de la etiqueta, y luego el valor es el valor que desea asignar. Entonces, la idea aquí es que ejecutará cientos o miles de recursos en la nube. Y a medida que crea aplicaciones, crea arquitecturas complejas, puede etiquetarlas. Y podría identificar sus aplicaciones y sus recursos utilizando estas etiquetas.

Esa es la primera razón por la que usarías tus etiquetas, porque tus cuentas y tus recursos... vas a usar muchos, muchos recursos. Y las etiquetas son un mecanismo muy sencillo para organizar mejor sus recursos.

La segunda razón por la que usarías etiquetas sería para la gestión de costos. Ahora imagina todos estos recursos que estás etiquetando, podrías extraerlos por etiqueta. Y podría averiguar cuál es el costo de uso de esos recursos. Y esa es una forma muy importante de determinar cuánto consume su aplicación.

Recuerde que la nube se trata de precios de pago por uso. Y podría identificar el tipo de costo en el que está incurriendo en un conjunto particular de recursos. Entonces, la segunda razón por la que usarías etiquetas es la gestión de costos.

También puedes hacer esto llamado control de acceso basado en etiquetas. Por lo tanto, podría controlar el acceso en función de las etiquetas de los recursos, no de los usuarios y los grupos. **Entonces, en cierto modo, al usar etiquetas, la capacidad de escribir políticas basadas en etiquetas se vuelve aún más poderosa.** Estos son algunos de los casos de uso. y hay muchos, muchos mas. Pero esas son algunas de las razones por las que usarías etiquetas.

Como hablamos en OCI, hay dos tipos de etiquetas. Hay etiquetas de formato libre. Y hay etiquetas definidas. Primero, veamos las etiquetas de formato libre. Como puede ver en el gráfico aquí, hay una clave y un valor. Entonces, para esta etiqueta en particular, la clave es el medio ambiente. El valor es la producción. Es un pagador de valor clave muy simple. No hay un esquema definido. O no existe ningún tipo de restricción de acceso.

Luego hemos definido etiquetas. Y estos tienen más funciones y control. Y lo primero que hay que tener en cuenta aquí, como se puede ver en el gráfico, es que estas etiquetas ahora están contenidas dentro de algo llamado espacio de nombres. Entonces especificas un espacio de nombres que dice, en este caso, son operaciones. Y luego puedes poner tantas etiquetas como quieras en esos espacios de nombres. Entonces estás definiendo un esquema.

Y otra cosa que podría hacer también respalda las políticas. Por lo tanto, defina políticas de soporte de etiquetas para permitirle controlar quién puede aplicar sus etiquetas definidas. Por lo tanto, no todo el mundo podría utilizar estas etiquetas definidas. Podrías escribir eso en la póliza. Y el espacio de nombres de la etiqueta es la entidad a la que aplica esta política. Entonces se podría decir que un grupo particular de administradores de operaciones solo puede aplicar esta etiqueta en particular, porque el espacio de nombres tiene operaciones en eso. Entonces podrías redactar una política contra eso.

Entonces, ¿cómo se ve realmente en la práctica? Como ejemplo aquí, hay un espacio de nombres que son operaciones. Y dentro, estoy definiendo un par clave-valor. Entonces la clave es el medio ambiente y el valor es la producción. Y podrías llevarlo al siguiente nivel. Como puede ver aquí, las operaciones son el espacio de nombres. El medio ambiente es la clave. Y la producción es el valor.

Ahora, como hablamos, el espacio de nombres es un contenedor para un conjunto de etiquetas con definiciones de claves de etiquetas. Las definiciones de claves de etiquetas especifican la clave como está aquí. Y también podría especificar el tipo de valores permitidos. Se podría decir que el tipo es una cadena. Y permite cualquier valor, o está en blanco. O podría establecer un conjunto específico de valores. Y cuando los usuarios aplican esta etiqueta en particular, solo pueden elegir entre esos valores en particular.

Por lo tanto, es otra forma de determinar primero quién aplica la etiqueta escribiendo las políticas. Y luego también puedes especificar qué tipo de valores están permitidos. Entonces, esto realmente es que el esquema definido junto con la política hace que los recursos estén aún mejor organizados.

Una cosa a tener en cuenta es que el espacio de nombres de etiquetas, una vez definido, no se puede eliminar. Pero siempre puedes retirarlos y no tienes que usarlos. Esto es más por motivos de gobernanza. Entonces, independientemente de los espacios de nombres que tenga, puede realizar una auditoría de los espacios de nombres que tenía en su cuenta. Eso es todo.

Etiquetado: una característica muy importante y útil en la nube. Y en OCI, llevamos el etiquetado al siguiente nivel utilizando estas etiquetas definidas. 
