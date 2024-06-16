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

Finalmente tenemos esta capa, que se llama detección y remediación. También se le conoce como gestión de la postura de seguridad en la nube. La idea es mejorar la postura de seguridad de una organización. Entonces
