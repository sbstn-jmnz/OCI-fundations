# Redes (Networking)

## Introducción

¿Qué es una red de nube virtual VCN? En esencia, es una red privada definida por software que se crea en Oracle Cloud. Se utiliza para una comunicación segura. Ya sean instancias que se comuniquen entre sí, instancias que se comuniquen con entornos locales o instancias que se comuniquen con otras instancias en diferentes regiones, se utilizará Virtual Cloud Network.

Como dijimos, es un servicio regional. Es altamente disponible, enormemente escalable y seguro. Y nosotros nos encargamos de estas cosas por usted. Entonces, antes de profundizar en VCN y todas las características que tiene, veamos algunas de las cosas básicas.

![image](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/6d574437-2d76-4ebc-9504-5acb35be661d)

Entonces, lo primero es que VCN tiene un espacio de direcciones. En este caso, verá que este espacio de direcciones se indica en notación **CIDR**. CIDR significa enrutamiento entre dominios sin clases (Un grupo grande de sirecciones de red). Por lo tanto, no entraremos en detalles sobre cómo se crean estas CIDR. Pero puedes leer más en la web. O puede abrir una calculadora de subred y obtener todos los detalles.

Como puede ver aquí, la VCN tiene un rango de direcciones IP. Y lo que eso significa es que tienes un rango de direcciones. Tomas ese rango. Y puedes dividirlo en redes más pequeñas que se denominan subredes. Y estas subredes son donde crearía instancias de sus instancias informáticas.

![image](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/74ae267c-ab59-4f87-8245-18dd0d9de13e)

Entonces, en este ejemplo, como puede ver, la red 10.0.0.0/16 se divide en 256 redes más pequeñas, un par de las cuales se muestran en la pantalla: la subred pública 10.0.1.0/24 y la subred privada. Y como dije, sus instancias se activan en estas subredes.

Entonces, si activa una instancia web, obtiene una dirección IP como se muestra. Si activa una instancia de base de datos, obtendrá una dirección IP: una dirección IP privada como se muestra. Y esta dirección IP se utiliza para todas las comunicaciones en el futuro. Hablando de comunicación, ¿qué diferentes mecanismos existen dentro de una VCN? En primer lugar, existe la noción de puerta de enlace a Internet (Internet Gateway). Se trata de una puerta de enlace enormemente escalable, de alta disponibilidad y que se utiliza para comunicarse con cualquier cosa en Internet.

Entonces, si tiene un servidor web que quiere comunicarse con otros sitios web a los que se puede acceder **públicamente**, usaría una puerta de enlace de Internet. Entonces, ir a Internet y regresar de Internet.

También tiene este enrutador de alta disponibilidad y escalabilidad masiva llamado puerta de enlace NAT.

Y se utiliza para proporcionar **NAT** como servicio. Entonces lo que esto significa es que el tráfico es unidireccional. Puede ir desde sus subredes privadas a Internet. Pero los usuarios de Internet no pueden usar la puerta de enlace NAT para llegar a sus instancias que se ejecutan en una subred privada. Entonces, la idea con la puerta de enlace NAT es permitir la comunicación saliente a Internet, pero bloquear las comunicaciones entrantes o las conexiones iniciadas desde Internet.

Luego tenemos otro enrutador que se llama **Service Gateway**. Y la idea es que permite que los recursos de VCN accedan a servicios públicos de OCI, como el almacenamiento de objetos, pero sin utilizar una puerta de enlace de Internet o NAT. Estos son los tres escenarios: puerta de enlace de Internet para Internet, puerta de enlace NAT también para Internet pero unidireccional y puerta de enlace de servicios para acceder a los servicios públicos de OCI, que están disponibles en Internet pero accediendo a ellos de forma segura.

Y luego la otra construcción se llama **puerta de enlace de enrutamiento dinámico**. Se trata de un enrutador virtual que proporciona una ruta para el tráfico privado entre su VCN y destinos distintos de Internet. Entonces, ¿cuáles pueden ser estos destinos? Bueno, este puede ser su entorno local.

Solo para resumir, VCN: su red definida por software, altamente escalable, segura y altamente disponible. Y tiene varios mecanismos, varios enrutadores para permitir la comunicación, ya sea a Internet o a su entorno local. Gracias por ver.

![image](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/b066b6d8-11c0-4cd4-9e0d-af61ff398487)

## Demo
![image](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/82f01d52-79bb-453f-b85b-99af149d8ed4)

## VCN ROUTING
Bienvenido de nuevo a esta lección sobre enrutamiento OCI. Como puede ver en este gráfico aquí, tenemos este concepto de tabla de rutas. VCN utiliza tablas de rutas para enviar tráfico fuera de VCN a Internet, a redes locales o a VCN emparejada, y analizamos cada uno de estos escenarios.

Las tablas de rutas constan de un conjunto de reglas de ruta. Cada regla especifica un bloque CIDR de destino y un destino de ruta. Piense en el destino de la ruta como el siguiente salto para el tráfico que coincide con ese bloque CIDR de destino.

Ahora, una cosa a tener en cuenta es que el enrutamiento local de VCN maneja automáticamente el tráfico dentro de la subred de VCN. Aquí verá una subred pública y una subred privada. No se necesita enrutamiento para enrutar los datos. No se necesita ninguna entrada en una tabla de rutas para enrutar esos datos entre la subred pública y la subred privada. De eso se encarga la propia VCN.

Entonces, ¿cómo funciona esto en la realidad? Como puede ver aquí, tengo una subred privada y una subred pública y le muestro la tabla de rutas solo para la subred privada solo con fines ilustrativos. Y como puede ver aquí, hay dos tipos de movimiento de datos desde la subred privada.

Estamos aprovechando la puerta de enlace NAT. Probablemente haya una base de datos ejecutándose aquí, por lo que está utilizando una puerta de enlace NAT para obtener algunos parches de Internet. Entonces puedes ver esa flecha verde que va desde la puerta de enlace NAT hasta Internet.

Y luego, la segunda parte es que está utilizando una puerta de enlace de enrutamiento dinámico. Es una especie de enrutador virtual que se utiliza para la comunicación local y pasa por el entorno local. Tal vez esté ejecutando un servidor DNS local donde la base de datos necesita resolver su DNS.

Ahora, si observa las entradas de la tabla de rutas, tenemos dos entradas allí. Hay una notación CIDR, CIDR de decisión y un destino de ruta. El primero dice 0.0.0.0/0 y va a la puerta de enlace NAT. El segundo tiene un bloque CIDR para la red local.

Entonces, ¿cómo funciona esto en la realidad? Bueno, lo que sucede es que la tabla de rutas mira tanto las rutas como la ruta que es más específica o tiene prioridad. A veces también nos referimos a la coincidencia de prefijo más larga. Entonces, si observa estos dos bloques CIDR, /16 es más grande o más específico que /0, por lo que tiene prioridad.

Primero, el tráfico pasa a través de la puerta de enlace de enrutamiento dinámico hacia su entorno local, sus servidores DNS. Y luego, el tráfico que no está destinado a su entorno local va a Internet a través de la puerta de enlace NAT y, con suerte, obtendrá un parche en este ejemplo. Esta es una ilustración muy rápida, pero con suerte le mostrará cómo funciona la tabla de rutas.

Ahora bien, también hay un escenario del que no hemos hablado antes: el **peering**. Si tiene varias redes, ¿cómo se comunican entre sí? Así que aquí hay dos escenarios posibles.

**Si las redes están dentro de la misma región OCI, pueden comunicarse entre sí a través de un mecanismo llamado peering local**. Y pueden ver aquí que tenemos este concepto de puerta de enlace de intercambio de tráfico local. Es una especie de enrutador virtual que te permite administrar esa comunicación.

Si las dos redes están en dos regiones de centros de datos OCI diferentes, entonces tenemos el mismo concepto, un concepto similar, pero ahora es un intercambio de **tráfico remoto**. Y en lugar de utilizar el emparejamiento local, ahora está utilizando puertas de **enlace de enrutamiento dinámico**. Recuerde que hablamos de puertas de enlace de enrutamiento dinámico que se utilizan para la comunicación local (on premise), cualquier cosa que no sea para Internet. Por lo tanto, este también es un caso de uso para **Dynamic Routing Gateway** que permite la comunicación entre redes en diferentes regiones.

Ahora, una cosa es que uno podría mirar esa imagen y decir: "Es genial si hay dos redes hablando entre sí dentro de una región". Es bastante sencillo utilizar algo así como una puerta de enlace de intercambio de tráfico local. ¿Qué sucede si tiene, digamos, 10 de esas VCN? O Dios no lo quiera, si tienes 300 de esas VCN, ¿cómo te vas a comunicar?

En un entorno realmente complejo, ésta es una posibilidad. Esta es una realidad. Muchos clientes luchan con muchas redes. Entonces, ¿cómo se produce esa comunicación en caso de que tenga una gran cantidad de redes?

Entonces, en este caso, lo que hemos hecho es lanzar una versión más nueva de DRG. **Se llama DRG v2**. Y lo que hace es que ya no necesita mantener la conectividad punto a punto mediante una puerta de enlace de intercambio de tráfico local; en su lugar, las VCN pueden comunicarse mediante DRG. Y esta característica también le permite escalar hasta 300 VCN en un solo DRG. Si esta opción no es suficiente, siempre puedes conectar un DRG adicional a través de una conexión de peering remota. Entonces la idea es simplificar y escalar esta experiencia usando este DRG v2.

Para concluir, en esta sección analizamos el enrutamiento OCI y cómo VCN utiliza tablas de enrutamiento para enviar tráfico a la VCN, a Internet, a la red local o a una VCN emparejada. 

## Seguridad

[A] Palabras clave
Cerrar

[EFECTO DE SONIDO MUSICAL]

Entonces, dentro de VCN, existe este concepto de lista de seguridad. Piense en la lista de seguridad como reglas de firewall (cortafuegos) asociadas con una subred y aplicadas a todas las instancias dentro de la subred. Entonces, ¿qué es lo que parece? **La lista de seguridad consta de reglas que especifican el tipo de tráfico permitido dentro o fuera de la subred**. Esto se aplica a una instancia determinada, ya sea que esté hablando con otra instancia en la VCN o con un host (servidor) fuera de la VCN.

Y puedes ver un par de entradas aquí. Estas reglas pueden ser con estado o sin estado. Con estado significa que si se permite el tráfico en un puerto en particular, se permite la entrada, siempre se permite la salida de ese puerto y viceversa.

Así que puedes ver aquí un par de ejemplos. El tráfico ingresa por el puerto 80 y proviene de cualquier lugar de la web. Entonces eso es 0.0.0.0/0. Esa es la fuente. Puede estar en cualquier lugar. El protocolo es TCP. Y llega al puerto 80. Eso es tráfico web.

Y la segunda regla dice que el tráfico va de la primera subred a la segunda subred. Como ve, la fuente es la IP, el bloque CIDR para la primera subred y, en realidad, es el tráfico de salida. Entonces es la fuente de la segunda subred, la subred privada. Y el tráfico se dirige al puerto 1521. Ese es el puerto de la base de datos de Oracle.

Y puede ver que, de manera similar, para la subred privada, tiene sus propias reglas de firewall. Y en este caso, dice que debido a que es una subred privada, no desea ningún tipo de tráfico web. Entonces, la única regla aquí es el tráfico proveniente de la subred pública, del servidor web, de modo que el CIDR de origen sea 10.0.1.0/24 y el puerto sea 1521, ¿verdad? Así es como se definirían las listas de seguridad dentro de un servicio OCI VCN.

Ahora bien, también existe otro concepto, que se llama grupos de seguridad de red o **NSG**. Son construcciones muy similares a las listas de seguridad, pero la diferencia clave es que **se aplican solo a un conjunto de tarjetas de de red virtuales en una única VCN**. Y otra gran diferencia aquí es que los NSG pueden ser el origen o el destino en las reglas. Compare esto con las reglas de la lista de seguridad donde especifica un CIDR, solo un CIDR, como origen o destino.

Como pueden ver aquí en este ejemplo, el tráfico de salida, la fuente es NSG B. Ese es el NSG que está adjunto a mi base de datos. De manera similar, para el segundo grupo de seguridad de red, puede ver que la fuente es el primer grupo de seguridad de red. Ese es el GSN A.

También hay una cosa a tener en cuenta: que a medida que aprovecha los grupos de seguridad de red, debido a que se aplican a VNIC individuales, ahora podría tener dos instancias en una sola subred y pueden tener diferentes construcciones de seguridad. Entonces uno puede tener un NSG con diferentes tipos de reglas, y la otra instancia, como pueden ver, tiene un NSG; en este caso, decimos NSG C. Tiene diferentes conjuntos de reglas. ¿Bien? Por lo tanto, podría habilitar ese tipo de escenario mediante el uso de grupos de seguridad de red.

Eso es todo. Para resumir, existen dos mecanismos para crear estas reglas de firewall en OCI VCN. **Una es una lista de seguridad y la otra son grupos de seguridad de red**. Gracias por ver.

## Balanceadores de Carga
Permítanme hablarles rápidamente sobre por qué usarían Load Balancer. Utilizaría Load Balancer para lograr alta disponibilidad y también escalabilidad.

Por lo general, la forma en que funciona Load Balancer es que también se les conoce como **Proxies inversos**, tendría un Load Balancer, al que múltiples clientes, varios clientes, podrían acceder. Y estos clientes llegarían al Load Balancer, y el Load Balancer enviaría ese tráfico a los distintos servidores. De esta manera, no solo protege los distintos servidores backend, sino que también proporciona alta disponibilidad. En caso de que un servidor backend en particular no esté disponible, la aplicación aún puede estar en funcionamiento. Y luego también proporciona escalabilidad porque si muchos clientes comienzan a utilizar Load Balancer, fácilmente podría agregar más backends o más servidores backend.

Y hay varias otras capacidades avanzadas como terminación SSL y paso a través de SSL y muchas otras funciones avanzadas. No vamos a llegar a ellos porque es un curso fundamental. Pero, con suerte, eso le dará una buena idea de lo que hace un Load Balancer; es decir, los beneficios de usar un Load Balancer.

Entonces, el primer tipo de Load Balancer que tenemos en OCI es un **Load Balancer de capa 7**. La capa 7 básicamente significa que comprende **HTTP y HTTPS**. Ese es el modelo OSI. Y luego hay varias capacidades disponibles aquí.

Entonces, lo primero es que el Load Balancer viene en dos formas diferentes. Una se llama forma flexible en la que defines el mínimo y el máximo y defines el rango. Y su Load Balancer puede lograr cualquier tipo de soporte de cualquier tipo de tráfico en ese rango particular, desde 10 Mbps hasta 8 Gbps.

El segundo tipo de forma se llama dinámica y predefine las formas. Entonces tienes micro, pequeño, mediano, grande y predefini. Y no es necesario que caliente su Load Balancer. Si el tráfico adquiere esa forma particular, el Load Balancer escala automáticamente.

Siempre puedes hacer un Load Balancer público y privado. Público significa que Load Balancer está disponible en la web. Privado significa que sus múltiples niveles, como un nivel web, pueden comunicarse con su nivel de base de datos y equilibrar el tráfico entre ellos, pero ambos niveles no tienen que ser públicos.

Un Load Balancer tiene alta disponibilidad, es altamente escalable por diseño y tiene muchas funciones avanzadas de capa 7. Se admiten elementos como el enrutamiento basado en contenido. Y hay muchas otras características de SSL, otras capacidades, de las cuales este es un curso fundamental, no vamos a entrar en eso. Pero tiene muchas características ricas.

El segundo tipo de Load Balancer que tenemos en OCI se llama **Network Load Balancer**. Y como su nombre lo especifica, Network Load Balancer opera en las capas 4, 3 y 4, por lo que comprende **TCP, UDP y también admite ICMP**. Nuevamente, al igual que HTTP Load Balancer, tiene una opción tanto pública como privada, por lo que puede crear un Network Load Balancer público o un Network Load Balancer privado. Es altamente disponible, altamente escalable y todas esas funciones son compatibles.

Ahora bien, ¿por qué utilizarías Network Load Balancer o HTTP Load Balancer? La razón principal por la que lo usarías es que es mucho más rápido que HTTP Load Balancer. Tiene una latencia mucho menor. Entonces, si el rendimiento es un criterio clave para usted, opte por **Network Load Balancer**.

Por el contrario, HTTP Load Balancer tiene un nivel de inteligencia más alto porque puede mirar los paquetes, puede inspeccionarlos y obtiene esa inteligencia. Entonces, si está buscando ese tipo de inteligencia de enrutamiento, elija **HTTP Load Balancer**.

Entonces, para resumir, OCI le proporciona un balanceador de carga de red de capa 3 y 4, así como un balanceador de carga HTTP de capa 7 con muchas funciones avanzadas.
