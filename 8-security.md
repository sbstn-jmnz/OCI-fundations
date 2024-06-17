# Seguridad

## Modelo de seguridad compartido

Bienvenido a este módulo sobre seguridad OCI. Comencemos con una introducción. En seguridad, siempre se escucha este término llamado **modelo de seguridad compartido**. ¿Qué significa esto realmente? Bueno, en un entorno local, usted es dueño de todo el hardware (stack) y es responsable de la seguridad de un extremo a otro.

A medida que se traslada a la nube, algunas de las responsabilidades se transfieren al proveedor de la nube, en este caso, Oracle, y otras las conserva usted. Eso es lo que queremos decir con un modelo de seguridad compartido. ¿Cómo se ve en la nube?

Bueno, en la nube, Oracle Cloud Infrastructure es responsable de la seguridad de la nube, lo que significa cosas como el centro de datos físico, la red física, el host físico e incluso la capa de virtualización, asegurándose de que sea rápido y esté actualizado. Todas esas son responsabilidades de Oracle. Esa es básicamente la seguridad de la nube.

el centro de datos físico,
la red física,
el host físico e incluso la capa de virtualización

Eres responsable de la seguridad en la Nube. ¿Qué significa eso? Bueno,
eso significa que usted es responsable de:

los datos, es responsable de los terminales (endpoints o url), dispositivos, dispositivos móviles o PC o los servidores de sus PC que acceden a ellos. 

Y usted es responsable de la gestión de cuentas y accesos.

Entonces, gestión de identidades y accesos. Y hay algunas otras cosas de las que usted es responsable, como si usa sistemas operativos, debe asegurarse de que estén parcheados y actualizados. Entonces este es el modelo en la Nube. Algunas responsabilidades pasan al proveedor de la nube. Algunas responsabilidades aún quedan en usted.

Entonces, echemos un vistazo a la cartera de seguridad de OCI disponible actualmente con... disponible actualmente en OCI. He incluido en esta diapositiva los casos de uso y los servicios, para que realmente comprendan no solo los servicios, sino también el contexto en el que operan.

En OCI, la seguridad se integra utilizando la metodología de defensa en profundidad, lo que significa que la seguridad se integra en varias capas de la pila. Entonces, una buena manera de representar esto es desglosar estos servicios por casos de uso y luego enumerar los servicios de seguridad OCI que están disponibles para cada caso de uso.

Así que comencemos desde abajo con la protección de la infraestructura. Y aquí puedes ver que hay varios servicios que se enumeran. Debido a que esta es una lección de introducción, las repasaré rápidamente y cubriré un par de ellas en cada capa.

El primero aquí es un servicio llamado firewall de aplicaciones web. Protege las aplicaciones del tráfico de Internet malicioso y no deseado. Puede ayudar a mitigar los ataques DDoS de capa 7. Y luego también hay un servicio llamado firewall de red. Y eso monitorea su red en busca de actividad maliciosa. Y puede ayudar con la intrusión, la detección y la prevención.

Entonces, esta capa tiene que ver con la protección de la infraestructura. La capa superior a esto tiene que ver con la gestión de identidades y accesos. Y se trata principalmente de los usuarios que tienen acceso a sus sistemas, ¿quiénes son los usuarios y qué tipo de nivel de acceso tienen? ¿Qué tipo de permisos tienen para sus sistemas?

Luego también tenemos servicios como la autenticación multifactor. Y la autenticación MFA o multifactor es un método de autenticación que requiere el uso de más de un factor para verificar la identidad de un usuario. Y luego hay algunos otros servicios en esta capa.

La siguiente capa tiene que ver con la protección del sistema operativo y la carga de trabajo. Entonces, al igual que las capas anteriores, esta capa también tiene muchos servicios. Permítanme mencionar rápidamente un par de ellos. Las instancias blindadas que ve allí son una especie de máquina virtual que ofrece seguridad adicional para los clientes que necesitan cumplir estrictos requisitos de seguridad y cumplimiento.

Entonces, por ejemplo, una de las características de las instancias protegidas es el arranque seguro. Y lo que hace es que cuando se inicia una VM, solo utiliza software confiable debido a ese arranque seguro. Entonces esa es una característica que está ahí. Y hay varias otras características.

Luego tenemos algo así como un host de VM dedicado, que es un inquilino único de máquina básica dedicado a usted donde puede ejecutar sus VM. Y luego tenemos un servicio como OS Management, que monitorea y administra actualizaciones y parches, no solo para una sola máquina, sino que literalmente podrían ser miles de máquinas, es decir, a escala. Entonces, esta capa tiene que ver con la protección del sistema operativo y la carga de trabajo.

Luego, el siguiente nivel es el de la protección de datos. Esto es súper crítico. Los primeros dos componentes que ve aquí están relacionados con un servicio llamado Vault. Este servicio le ayuda a administrar de forma centralizada las claves de cifrado que protegen sus datos y las credenciales secretas, como contraseñas, que utiliza para acceder a los recursos.

Ahora también tenemos un servicio llamado certificados, que le permite crear y administrar autoridades certificadoras, también conocidas como CA y certificados en sí. Entonces, esta capa trata sobre los servicios que ayudan a cumplir con los casos de uso para la protección de datos.

Finalmente tenemos esta capa, que se llama detección y remediación. También se le conoce como gestión de la postura de seguridad en la nube. La idea es mejorar la postura de seguridad de una organización. Entonces, **los servicios aquí monitorean continuamente su entorno.**

Y si notan algún tipo de configuración incorrecta o actividades del usuario o del operador, pueden notificárselo. De hecho, también puede solucionar el problema automáticamente. Entonces, el primer servicio que aparece allí, **Cloud Guard**, es un servicio que hace eso. Realiza la gestión de la postura de seguridad en la nube.

Luego también hay un servicio llamado **Zonas de seguridad**. Y piense en esto porque la forma en que funciona es designar sus **compartimentos** como zonas seguras. Y estos cumplen con las políticas de seguridad de Oracle. Y puede definir estas políticas como que no puede tener acceso público, los recursos no pueden tener acceso público, se requiere cifrado, etc.

Y los recursos que usted defina en estas Zonas de Seguridad en realidad cumplirán con estas políticas de seguridad. En pocas palabras, esta es una descripción general de muy alto nivel de los servicios de seguridad. Pero espero que esto le brinde una buena descripción general de cómo se clasifican estos servicios de seguridad según los casos de uso. Y cómo se implementa en este mecanismo de defensa en profundidad en el que se tiene seguridad integrada en diferentes capas de la pila.

Entonces, ¿cómo funciona todo esto? Como puede ver en este gráfico aquí, tiene un entorno donde tiene algunas redes virtuales. Y está utilizando varios servicios de seguridad, ya sea escaneo de vulnerabilidades, ya sea auditoría, ya sea el servicio bastión o Vault o el servicio de administración de acceso a identidad.

Nuevamente, en la siguiente lección, analizaremos en detalle muchos de estos servicios. Pero tenga en cuenta que contamos con un conjunto muy amplio y extenso de servicios de seguridad. Entonces, para resumir, en la nube, cuando te mudas a la nube, básicamente obtienes este modelo de seguridad compartido y eres responsable de algunos de los aspectos de seguridad y el proveedor de la nube se encarga de los otros aspectos.

Y la seguridad no es sólo un servicio o un complemento. Hay un amplio conjunto de servicios disponibles en diferentes capas de la pila. 

## Cloud Guard

Bienvenido de nuevo. En esta lección, veremos Oracle Cloud Guard. Oracle Cloud Guard es una característica única disponible dentro de Oracle Cloud Infrastructure.

¿Qué es Oracle Cloud Guard? Cloud Guard es un servicio que se incluye en la categoría de seguridad: gestión de la postura de seguridad en la nube. Ayuda a monitorear e identificar posibles problemas de seguridad y luego solucionarlos. Lo realmente interesante de Cloud Guard es que puede automatizar completamente la corrección.

Como puedes ver aquí, los dos aspectos clave: detectas un problema. Y hay un par de formas de hacerlo. Puede verificar las configuraciones, puede monitorear las actividades y luego puede aplicar una respuesta. Y puedes automatizar esta respuesta.

Entonces, ¿cómo funciona esto realmente en la práctica? Entonces, lo primero que debe hacer es especificar un objetivo. Y un objetivo básicamente establece el alcance de los recursos que se examinarán para OCI. Los compartimentos pueden ser objetivo y su compartimento secundario puede ser el objetivo. Por tanto, el objetivo no son más que recursos que deben examinarse.

Luego tienes detectores. Y estos detectores son básicamente problemas identificados. Los detectores son componentes de Cloud Guard que identifican problemas con los recursos o las acciones del usuario y alertan cuando se encuentra un problema. Entonces, como puede ver aquí, si hay una instancia pública donde no debería estar, la marcará. Si hay un depósito (bucket) público, lo marcará, etcétera.

Entonces tienes problemas, y los problemas son posibles problemas de seguridad. Entonces, en cierto modo, hablar de problemas como notificaciones de una configuración o actividad es un posible problema de seguridad. Y, finalmente, tenemos los servicios de respuesta, que brindan notificaciones y acciones correctivas para problemas de seguridad. Entonces, como puede ver aquí, si las instancias son públicas, puede detenerlas. Si un depósito es público, puede desactivarlo o hacerlo privado, etc., etc. Puedes decidir qué tipo de respondedores quieres.

Ahora, veamos esto en acción. Entonces, el escenario aquí es un depósito público y no desea que este depósito sea público. Quiere que este sea un depósito privado porque se alinea con su postura de seguridad. Entonces, primero, lo que hace Cloud Guard es suponer que este depósito se encuentra en un compartimento monitoreado por Cloud Guard.

Cloud Guard está ejecutando esta supervisión de configuración. Entonces, mira su depósito y activa una bandera que dice que este depósito en particular es público. Y lo señala como una cuestión crítica y se crea un problema. Así que piense en nuestro problema como una especie de Ticket. Entonces se crea diciendo: el cubo es público. Y, al mismo tiempo, como asigna una puntuación de seguridad, dice que es un riesgo crítico. Entonces notifica que... que es un riesgo crítico.

Y luego están los que responden, que se fijan en eso. Y dicen, ¿mi respondedor está habilitado para este tipo de problema? Y si la respuesta es sí, también puede tener funciones adicionales, como cosas como Cloud Event. Podría ir a Cloud Event, activarlo como un evento y luego podría recibir notificaciones de eso.

También puedes ir a funciones OCI, que es nuestro servicio sin servidor, y podría hacer otra cosa. Podría aflojarte o algo así. Por lo tanto, podría tener alguna otra característica incorporada. Entonces el respondedor mira eso y luego se lo entrega a un operador de Cloud Guard. Esta es una política que usted escribe y que dice: ¿Puedo solucionar el problema?

¿Tengo permiso para solucionar el problema? Una cosa interesante de Cloud Guard es que se puede automatizar todo esto. Y si la respuesta es sí, entonces responde. Y hace que el depósito sea privado. Y así es como se llega a ese riesgo crítico y la situación vuelve a ponerse verde.

Se trata de una especie de flujo de trabajo de un extremo a otro sobre cómo funciona Cloud Guard. Mucho de esto es transparente. No lo ves. Y es una excelente manera de detectar problemas automáticamente y solucionarlos.

En resumen, Cloud Guard es un servicio que entra en la categoría de Gestión de la postura de seguridad en la nube. Ayuda a monitorear e identificar posibles problemas de seguridad y luego solucionarlos. También podría solucionar automáticamente estos problemas. 

## Secirity Zones and Security Advisor

Zonas de seguridad y Consejero de Seguridad.

Bienvenido a esta lección sobre Zonas de seguridad y Asesor de seguridad.

**Zona de seguridad es para configurar una ubicación en la que no se puede desactivar la seguridad**. 

**Security Advisor** es un servicio que unifica **Security Zone, Cloud Guard y algunas otras capacidades en un todo cohesionado**. En esta lección, analizaremos ambos servicios.

Primero, veamos las zonas de seguridad. ¿Qué son las Zonas de Seguridad? Bueno, hablamos de que tienes recursos en tus compartimentos. Como puede ver aquí, tiene dos compartimentos llamados compartimento A y compartimento B. Puede designar el compartimento B como zona de seguridad. ¿Qué significa eso?

Bueno, eso significa que este compartimento en particular, una vez que se le asigna una especie de nomenclatura de Zona de Seguridad, tiene un conjunto de recetas de Zona de Seguridad. Estas no son más que sus políticas que se aplican aquí. Y cada vez que hay una violación de la política, se niega esa operación.

Entonces, ¿cómo se ve eso? ¿Qué servicios son compatibles? Bueno, hoy en día se admiten las primitivas principales, incluidas las redes, el almacenamiento, la computación y las bases de datos. ¿Qué significa eso realmente? Bueno, si especificas que la subred siempre tiene que ser privada, si creas una subred pública, esa operación será denegada. Si las reglas dicen que el cliente administra las claves de cifrado maestras, se deben utilizar en lugar de las claves de cifrado administradas por el proveedor. Y si eso se viola, se denegará la operación.

Entonces la idea es que tomes una parte de tu arrendamiento y pienses en tu propia casa. Tiene los artículos más seguros que tiene, ya sea su pasaporte, documentos, joyas o cualquier otra cosa, puede guardarlos en una bóveda segura. Hágalo a prueba de incendios, etc., para que esté protegido en caso de cualquier tipo de infracción o desastre natural.

Entonces la misma idea se aplica aquí. Al tomar su arrendamiento, no todo en su arrendamiento es súper seguro, pero algunos elementos de su arrendamiento, algunas partes, serán súper seguros. Creas una zona de seguridad. A veces, también se las conoce como zonas de máxima seguridad. Y a los recursos que se mantienen allí se les aplican una especie de políticas, de recetas. Y esas políticas no pueden violarse.

La forma más sencilla de pensar en las zonas de seguridad. El asesor de seguridad es en realidad un servicio combinado que toma la funcionalidad proporcionada por Cloud Guard y Security Zone, así como algunos de los otros servicios de seguridad, y los reúne. En cierto modo, es nuestro propio punto de vista sobre cómo se debe garantizar la seguridad. Los servicios admitidos en la actualidad son el almacenamiento de objetos, el almacenamiento de archivos, el volumen en bloque y las máquinas virtuales.

Y nuevamente, en algunos de los ejemplos de los que hablamos anteriormente, los depósitos no pueden ser públicos. Y eso puede ser aplicado por Security Advisor. El asesor de seguridad le explicará cómo crear un depósito en una zona de seguridad. Y viene con su propio conjunto de requisitos.

Tienes que usar una clave de administración de clientes y así sucesivamente. Entonces, Security Advisor seguiría los pasos necesarios para hacerlo. En una demostración, podemos ver cómo funciona. Y entonces lo entenderás un poco mejor en comparación con simplemente leer las diapositivas.

Sólo para recapitular. Estos dos nuevamente son servicios únicos. Las zonas de seguridad configuran una ubicación en la que no se puede desactivar la seguridad. Security Advisor unifica Security Zone, Cloud Guard u otras capacidades de seguridad en un todo cohesivo. Espero que encuentres útil esta lección. Gracias por ver.
