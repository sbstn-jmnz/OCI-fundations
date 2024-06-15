# Descripción general de OCI

OCI Significa Oracle Cloud Infraestructure, es decir, la infractuctura en la nube de Oracle.

## Descripción general

Algunas de las empresas más grandes del mundo están ejecutando sus trabajo críticos en la plataforma en la nube de próxima generación de Oracle llamada Oracle Cloud Infrastructure. 

Para simplificar las cosas, dividámoslas en siete categorías principales:

Infraestructura central,
Servicios de bases de datos e inteligencia artificial,
Análisis,
Gobernanza y administración 
Servicios de desarrollo y
Servicios de aplicaciones. 

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/a23f62a2-47ed-42d9-a5e0-afd226c407b0)

Pero primero, la base de cualquier plataforma en la nube es la huella global de las regiones. Tenemos muchas regiones generalmente disponibles en el mundo, junto con soporte multinube con Microsoft Azure y una oferta híbrida diferenciada llamada Dedicated Region Cloud@Customer.

Contamos con elementos básicos sobre esta huella global: las siete categorías que acabamos de mencionar. En la parte inferior, tenemos las primitivas centrales: computación, almacenamiento y redes. Los servicios informáticos cubren máquinas virtuales, servidores real de metal, contenedores, un servicio **Kubernetes** administrado y un servicio VMware administrado.

Estos servicios sirven principalmente para realizar cálculos, ejecutar lógica y ejecutar aplicaciones. El almacenamiento en la nube incluye discos conectados a máquinas virtuales, almacenamiento de archivos, almacenamiento de objetos, almacenamiento de archivos y servicios de migración de datos. OCI ofrece una gama completa de servicios de almacenamiento para que usted almacene, acceda, gobierne y analice sus datos estructurados o no estructurados.

Las funciones de red le permiten configurar redes privadas definidas por software en Oracle Cloud. OCI proporciona el conjunto más amplio y completo de servicios de red con la mayor confiabilidad, la mayoría de las funciones de seguridad y el mayor rendimiento.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/a7362ea4-9d8d-4dd0-a17a-aeb032fa5c88)

Luego tenemos los servicios de bases de datos. Contamos con múltiples tipos de servicios de bases de datos, tanto Oracle como de código abierto.

Somos la única nube que ejecuta bases de datos autónomas y múltiples versiones de ellas, incluidos OLTP, OLAP y JSON.

OLTP: Online **Transacction** proccess.

OLAP: Online **Analitical** proccess. 

JSON: Almacenar diccionarios llave: valor

Y luego puede ejecutar bases de datos en máquinas virtuales, servidores bare metal o incluso Exadata en la nube. También puede ejecutar bases de datos de código abierto como MySQL y NoSQL en Oracle Cloud Infrastructure.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/aec7eee7-6589-40c4-ba96-8f37fe757e6b)

**EXADATA**:  Servicio automatizado de bases de datos que permite ejecutar datos con maoyr rendimiento y disponibilidad con máxima seguridad

**ETL**: Extract Transform Load. Es la operación de extraer datos desde los sistemas OLTP y guardarlos en los sitemas OLAP.

Servicios de datos e inteligencia artificial. Tenemos un servicio administrado de Apache Spark llamado flujo de datos, un servicio administrado para rastrear artefactos de datos en OCI llamado catálogo de datos y un servicio administrado para la ingesta de datos y ETL llamado integración de datos. También contamos con una plataforma de ciencia de datos administrada para modelos y entrenamiento de aprendizaje automático. También contamos con un servicio Apache Kafka administrado para casos de uso de transmisión de eventos.

En otras palabras OCI tiene todos los servicios para ciencias de datos e inteligencia artificial.

Luego tenemos los servicios de gobernanza y administración. Estos servicios incluyen seguridad, identidad y observabilidad y gestión. Contamos con características únicas, como **compartimentos**, que facilitan operativamente la gestión de entornos grandes y complejos.

La seguridad está integrada en todos los aspectos de OCI, ya sea detección o corrección automática, lo que normalmente llamamos gestión de la postura de seguridad en la nube, protección sólida de la red o cifrado de forma predeterminada. Contamos con una plataforma integrada de observabilidad y gestión con funciones como registro, análisis de registros y gestión del rendimiento de aplicaciones, y mucho más.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/e24c726e-7146-4ab0-9c9e-3359a6949827)

Luego tenemos un montón de servicios para desarrolladores. Tenemos un servicio local administrado llamado APEX, varios otros servicios para desarrolladores y un servicio **Terraform** administrado llamado administrador de recursos. Para análisis, contamos con un servicio de análisis administrado llamado Oracle Analytics Cloud que se integra con varias soluciones de terceros.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/91340f7c-8b3a-421a-9ec3-d472445d5def)

En servicios de aplicaciones, tenemos una oferta administrada sin servidor llamada funciones y API Gateway, y un servicio de eventos para ayudarlo a crear microservicios y arquitecturas basadas en eventos. Contamos con un conjunto completo de SaaS conectado en todo su negocio, finanzas, recursos humanos, cadena de suministro, fabricación, publicidad, ventas, servicio al cliente y marketing, todo funcionando en OCI.

**SaaS**: Modelo de Software de la nube que ofrece aplicaciones finales a los usuarios a través de un navegador de internet. Por ejemplo: Mail, Correo, Zoom, Netflix, Instagram, Google Sheets, etc. 

Esa es una lista larga. Y estas siete categorías y los servicios mencionados representan sólo una pequeña fracción de los más de **80 servicios disponibles actualmente en OCI**. Afortunadamente, es rápido y fácil probar un nuevo servicio utilizando nuestra cuenta gratuita líder en la industria. Somos la primera nube que ofrece un servidor por solo **un centavo por hora** central.

Aprox $250 pesos un servidor el día entero.

Ya sea que esté comenzando con Oracle Cloud Infrastructure o migrando todo su centro de datos a él, podemos ayudarlo en su viaje hacia la nube. Eso es todo. OCI, una plataforma en la nube amplia y profunda.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/a16807b7-b51d-4c6c-a146-48ee970de33a)

## OCI Arquitectura

En esta lección, cubriremos las tópicos centrales de la arquitectura física de OCI, comenzando con las Regiones.

**Una región es un área geográfica** localizada que consta de uno o más dominios de disponibilidad. Los dominios de disponibilidad son uno o más centros de datos tolerantes a fallos ubicados dentro de una región pero conectados entre sí mediante una red de baja latencia y gran ancho de banda.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/14aa31e9-8e49-4a02-9598-e23a115643fc)

Los dominios de error son una agrupación de hardware e infraestructura dentro de un dominio de disponibilidad para proporcionar antiafinidad. Así que piense en estos como centros de datos lógicos. Lo vimos en la lección anterior. Hoy en día, OCI tiene una enorme huella geográfica en todo el mundo con múltiples regiones en todo el mundo. Y también tenemos una asociación multinube con Microsoft Azure. Y tenemos una oferta de nube híbrida diferenciada llamada Dedicated Region Cloud@Customer.

**Cloud@Coustomer**: Como una region de OCI, pero completamente privada para un cliente.

Pero antes de sumergirnos en la arquitectura física, veamos cómo se elige una región. 
Lo primero es elegir una región: **elige la región más cercana a tus usuarios** para obtener la latencia más baja y el rendimiento más alto. **Entonces ese es un criterio clave.**

El segundo criterio clave es **la residencia de los datos y los requisitos de cumplimiento**. Muchos países tienen requisitos estrictos de residencia de datos. Y hay que cumplirlas. Y entonces usted elige una región en función de estos requisitos de cumplimiento.

El tercer criterio clave es la disponibilidad del servicio. Los nuevos servicios en la nube están disponibles en función de la demanda regional, en ocasiones por razones de cumplimiento normativo y disponibilidad de recursos, y varios otros factores. Tenga en cuenta estos tres criterios a la hora de elegir una región.

Así que veamos cada uno de ellos con un poco más de detalle. 

Dominio de disponibilidad. Los dominios de disponibilidad están aislados entre sí, son tolerantes a fallos y es muy poco probable que fallen simultáneamente. Debido a que los dominios de disponibilidad no comparten infraestructura física, como energía o refrigeración o la red interna, es poco probable que una falla que afecte a un dominio de disponibilidad afecte la disponibilidad de otros.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/51f7349c-67bd-4cb2-b463-79f9a5373bd6)

Como puede ver en este gráfico, una región en particular tiene tres dominios de disponibilidad. Un dominio de disponibilidad tiene algún tipo de interrupción y no está disponible. Pero los otros dos dominios de disponibilidad todavía están en funcionamiento.

Hablamos de dominios de falla un poco antes. ¿Qué son los dominios de falla? 
Piense en que cada dominio de disponibilidad tiene tres dominios de error. Así que piense en los dominios de falla como centros de datos lógicos dentro del dominio de disponibilidad. Como puede ver en la imagen aquí, tenemos tres dominios de disponibilidad. Y cada uno de ellos tiene tres dominios de falla.

Entonces, la idea es colocar los recursos en diferentes dominios de error. Y no comparten un único punto de falla de hardware, como servidores físicos, bastidores físicos, conmutadores en la parte superior del bastidor o unidades de distribución de energía. Puede obtener alta disponibilidad aprovechando los dominios de falla.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/311ec1ee-7856-4a3c-87ee-3026739c1960)

También aprovechamos los dominios de falla para nuestros propios servicios. Entonces, en cualquier región, los recursos en ese dominio de falla se cambian activamente en cualquier momento. Esto significa que los problemas de disponibilidad causados ​​por los procedimientos de cambio se aíslan en el nivel del dominio de error. Y además, puede controlar la ubicación de las instancias de la base de datos de su computadora en el dominio remoto en el momento del lanzamiento de la instancia. Para que pueda especificar qué dominio de error desea utilizar.

¿Cuál es entonces la regla general? La guía general es que tenemos estas construcciones, como dominios de falla y dominios de disponibilidad, para ayudarlo a evitar puntos únicos de falla. Lo hacemos por nuestra cuenta. Así que nos aseguramos de que los servidores y el conmutador de la parte superior del rack sean redundantes. Para que no tengas fallos de hardware. Por eso intentamos minimizar esos fallos de hardware tanto como sea posible.

**Punto único de falla**: Cuando un componente falla y genera la caida general del sistema quedando inoperativo.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/1da50195-1fd9-41db-a465-ad94303f043b)

Debe hacer lo mismo cuando diseñe su propia arquitectura. Así que veamos un ejemplo. Tienes una región. Tienes un dominio de disponibilidad. Y como dijimos, un AD (Availability Domain) tiene tres dominios de falla (dominos de errors). Entonces ves esos dominios de falla aquí.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/cb5017b5-b901-4c9f-9340-d5653d9d3db2)

Entonces, lo primero que debe hacer es cuando crea una aplicación, crea esta red virtual definida por software. Y luego digamos que es una aplicación muy simple. Tienes un nivel de aplicación. Tienes un nivel de base de datos. Entonces, lo primero que puede hacer es ejecutar varias copias de su aplicación.

Entonces tiene un nivel de aplicación, que se replica en todos los dominios. Y luego tienes una base de datos, que también se replica en todos los dominios de falla. ¿Por qué haces eso? Bueno, te brinda esa capa extra de **redundancia**. Entonces, algo le sucede a un dominio defectuoso y su aplicación aún está en funcionamiento.

Ahora, para pasar al siguiente paso, podría replicar el mismo diseño en otro dominio de disponibilidad. Entonces podrías tener dos copias de tu aplicación ejecutándose. Y puede tener dos copias de su base de datos ejecutándose. Ahora, una cosa que surgirá es, ¿cómo se asegura de que sus datos estén sincronizados entre estas copias?

Por lo tanto, podría utilizar varias tecnologías, como Oracle Data Guard, para asegurarse de que los datos principales y de reserva se mantengan sincronizados . Y así podrás diseñar tu arquitectura.

**Data Guard** Asegura que los datos principales y de reserva se mantengan sincronizados.

## Nube distribuida

Veamos OCI Distributed Cloud (Nube Distribuida) en esta lección. 

Un aspecto único de Oracle Cloud es el hecho de que está distribuida, lo que significa que los clientes pueden obtener los servicios de Oracle Cloud de muchas maneras diferentes. Ofrece flexibilidad y elección excepcionales.

**Nube pública normal**: Los clientes pueden obtener nuestros servicios a través de nuestras regiones de nube pública: **más de 41 regiones globales en todo el mundo** con todos los beneficios de **seguridad, confiabilidad y escalabilidad**. 

**Nube híbrida**: También pueden obtener servicios y capacidades de nube locales a través de nuestras ofertas híbridas como Exadata Cloud@Customer.

**Nube privada**: Toda la cartera de servicios de nube a través de nuestra región dedicada y nuestra nube dedicada.

**Multi Nube**: Más de un proveedor de nube y que pueden aprovechar lo mejor de los servicios de nube a través de nuestras ofertas multinube

En esta lección, analizaremos la **nube híbrida** y la **multinube** con mucho más detalle.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/1a41925e-c608-4d2b-94d8-a855394bc2e3)

### Nube híbrida.

La primera oferta que tenemos es la **Región Dedicada Cloud@Customer**, que son nuestras regiones privadas aisladas. 

Luego tenemos un servicio, que se llama **Oracle Cloud VMware Solution**. Y aquí lo que hacemos es proporcionar un entorno basado en VMware en OCI mediante el cual puede **migrar máquinas virtuales locales a la nube** sin problemas.

Luego tenemos la **base de datos autónoma en Exadata Cloud@Customer**. Y la idea aquí es que todas las capacidades avanzadas de base de datos autónoma estén disponibles en su propio entorno local. Y finalmente, tenemos una oferta llamada **Roving Edge Infrastructure**, que es básicamente un servidor portátil, optimizado para computación y almacenamiento, que ha sido reforzado para **operar en entornos remotos y austeros**. Y esto es bueno para casos de uso en los que desea procesar datos y realizar cálculos en lugares remotos y desconectados (Edge: borde).

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/2579ad9e-6f1d-49ba-9efa-6752118eaccf)

Veamos la región dedicada Cloud@Customer con un poco más de detalle. Bueno, esta oferta proporciona todos los **más de 100 servicios de nube pública de OCI en una región de nube independiente y autónoma en la ubicación física que usted elija**. En el centro de datos de su elección. Esta región puede desconectarse completamente de la red exterior. Los clientes pueden empezar poco a poco y escalar hasta más de **450 racks** muy rápidamente.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/e4e761b6-295c-4dbc-aa6f-3c60af94f0e4)

Oracle instalará, operará, brindará soporte y actualizará a cada región dedicada de la misma manera que mantenemos las regiones de nube pública en todo el mundo. Hay dos casos de uso. 

**Uno es que la residencia de datos cumpla con sus requisitos de gobernanza, cumplimiento normativo y privacidad de datos para datos confidenciales**. 

Y también **se puede utilizar para ejecutar aplicaciones sensibles a la latencia**. Estas son algunas de nuestras ofertas de nube híbrida, incluida la región dedicada Cloud@Customer.


Cambiemos de rumbo y veamos algunas de nuestras **ofertas multinube**. Entonces, lo primero aquí es esta OCI Azure Interconnect que se lanzó en 2019. Entonces, la idea aquí es que **Oracle y Microsoft tienen una interconexión privada entre ellos**. Y hoy tenemos 12 regiones en todo el mundo, como pueden ver en esta diapositiva, donde esta interconexión está disponible.

Y si... esta es una **interconexión privada**, lo que significa que la **latencia es muy baja**, **menos de 2 milisegundos de latencia**. Y el precio de esta oferta se basa únicamente en los puertos y los circuitos que usted proporciona en ambos lados, y no hay ningún cargo por el ancho de banda (entrante o saliente) consumido. Entonces, el caso de uso aquí sería ejecutar una base de datos en Oracle, ejecutar aplicaciones aquí en Azure y ejecutarlas sin problemas debido a esta baja latencia privada para la interconexión privada.

Luego, en 2022, llevamos esta oferta un nivel más alto y creamos esta base de datos Oracle: lanzamos este servicio de base de datos Oracle para Azure. Y la idea aquí es que sea un servicio administrado por Oracle para que los clientes de Azure proporcionen acceso y operen Servicios de Base de Datos Oracle (Servicios de Base de Datos en OCI con una experiencia familiar similar a la de Azure).

Entonces, con solo unos pocos clics, los clientes pueden conectar su suscripción de Azure al arrendamiento de OCI y el servicio configura automáticamente todo lo necesario para vincular los dos entornos de nube. **Entonces, la principal diferencia entre esto y la interconexión OCI Azure es, como pueden ver aquí, la parte de interconexión, no es necesario implementarla manualmente**. El servicio lo automatiza. Por lo tanto, esto requiere un enfoque basado en servicios en comparación con un enfoque manual de configuración de la interconexión.

Y, por último, el servicio también envía métricas, registros y eventos para la base de datos OCI que usted suministra a las herramientas de Azure. Entonces obtienes esta telemetría y monitoreo unificados donde puedes ver todos los paneles y todos los servicios que están disponibles.

