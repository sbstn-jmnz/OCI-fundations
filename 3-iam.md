# Identity and access management

Bienvenido a esta lección sobre Gestión de acceso e identidad de OCI. En esta lección en particular, veremos una descripción general de muy alto nivel de OCI IAM. IAM significa servicio de gestión de identidad y acceso. A veces también se lo denomina control de acceso detallado o servicio de control de acceso basado en roles.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/ac515530-9009-41ed-b04f-342f2b508e75)

Hay dos aspectos clave en este servicio. La primera se llama autenticación, o también denominada **AuthN**. Y el segundo aspecto se conoce como autorización o también conocido como **AuthZ**. La autenticación tiene que ver con la identidad o quién es alguien, mientras que la autorización tiene que ver con el permiso o lo que alguien puede hacer.

Básicamente, lo que garantiza el servicio es asegurarse de que una persona sea quien dice ser. 

Y en lo que respecta a la autorización, lo que hace el servicio es permitir que a un usuario se le **asignen uno o más roles predeterminados**, y **cada rol viene con un conjunto de permisos**. Y eso es básicamente lo que se muestra en la pantalla aquí para la autorización, qué tipo de permisos tienes.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/6c2dd038-a45a-4372-bb9a-ab1a580dc0f8)

Ahora bien, hay varios conceptos que forman parte de este servicio o varias características que forman parte de este servicio, empezando por:

- Dominios de identidad,
- Principios (principals),
- grupos,
- grupos dinámicos,
- compartimentos,
- etcétera.

  Y en lecciones posteriores, los cubriremos con más detalle.

Ahora sólo quiero hablar sobre una de esas características, que son los **Dominios de identidad**. Los dominios de identidad son básicamente, como ven en la imagen aquí, un contenedor para sus usuarios y grupos. 

Así que piense en esto como una construcción que representa una población de usuarios en OCI y las configuraciones y ajustes de seguridad asociados.

Entonces, ¿cómo funciona esto en la práctica? Bueno, lo que hacemos primero es crear un dominio de identidad y luego creamos usuarios y grupos dentro de ese dominio de identidad. Y luego redactamos políticas para esos grupos, y las políticas se limitan a una cuenta o un compartimento.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/37712ef1-8e67-4498-abf3-37901e4e8c37)

Y por supuesto, los recursos están disponibles dentro de un compartimento. Y nuevamente, el compartimiento es una especie de aislamiento lógico de los recursos. Así es como funciona todo el servicio. 

La parte que está en un cuadro aquí es el dominio de identidad. Y para los usuarios y los grupos, la autenticación se realiza mediante mecanismos comunes como el nombre de usuario y la contraseña, y las políticas es básicamente donde se proporciona este control de acceso basado en roles.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/34205064-1c1d-4743-8ae6-d7b895bb1bc5)

Entonces, colocas a estos grupos en uno de los roles predeterminados y luego asignas algunos permisos para esos roles. Así es como funciona el servicio en pocas palabras. Ahora, algo que verán en la diapositiva anterior tiene que ver con estos recursos.

Ahora, cualquier cosa que cree en la nube, todos estos objetos, ya sea un almacenamiento en bloque, una instancia informática, un almacenamiento de archivos, una base de datos, todos estos son recursos. Y si estas cosas son recursos, tiene que haber un identificador único para estos recursos. ¿Cómo vas a operar con estos recursos?

Entonces, lo que hace OCI es proporcionar su propio identificador asignado, que se llama Oracle Cloud ID, OCID. No es necesario que proporciones esto. Hacemos esto automáticamente para todos los recursos.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/3e86eaeb-1d51-431b-899d-ae968695c656)


Y la sintaxis es como se muestra en la pantalla aquí. Entonces comienza con ocid1, hay un tipo de recurso, hay un dominio, hay una región y hay una identificación única.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/a93afbb8-893f-4299-ac54-ecb97b2ff4f7)


Entonces, lo que esto significa es que ocid1 es simplemente el tipo de recurso, el dominio es básicamente un conjunto de regiones que comparten las mismas características. Entonces hay un dominio comercial, hay un dominio o ámbito (REALM) gubernamental, etcétera. El tipo de recurso es una especie de tipo de recurso. Es una instancia informática o es un dispositivo de almacenamiento en bloque, etc.

Y luego la región es básicamente el código de región aquí. Solía ​​ser un código de tres caracteres, ahora es una cadena mucho más larga. Y luego hay una identificación única aquí, que es exclusiva del recurso que crea. Entonces, ¿cuáles son algunos de los ejemplos? Bueno, su cuenta también tiene un OCID, por lo que puede ver el arrendamiento o cuenta y puede ver la sintaxis aquí comenzando con ocid1.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/f58baf34-19bb-4a9d-a7b8-c42dfab5a5b6)

Ahora, por supuesto, la cuenta está en varias regiones. Entonces no tienes un identificador de región aquí. Su dominio es ocid1 y luego está el identificador único. En el caso del volumen en bloque, verá la región, porque el volumen en bloque es específico de una región en particular. Entonces verá la clave de región aquí y luego el identificador único.

Esperamos que este sea un par de ejemplos rápidos para mostrarle cómo funcionan los OCID. Si está trabajando en una consola de administración, no interactuará con los OCID. Pero si utiliza la CLI o el SDK (interfáz de comandos), utilizará estos OCID. Y recuerde, **Oracle genera estos identificadores únicos**. No es necesario hacer nada en lo que respecta a estos OCID.


## Compartimientos

**Los compartimentos son una característica única dentro de OCI**. Y estos son realmente poderosos, así que exploremos.

¿Qué es entonces un compartimento? **Cuando abre una cuenta en OCI, obtiene un arrendamiento** (tenancy). Ese es otro nombre elegante para una cuenta. Y también te regalamos un **Compartimento Raíz**. Así que piense en el compartimento raíz como esta construcción lógica donde puede guardar todos sus recursos en la nube.

Y luego lo que podrías hacer es crear tus propios compartimentos individuales, como ves aquí.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/b97f18bc-78a0-4948-b981-bfdc52e649c7)

Hay un compartimento de red. Hay un compartimento de almacenamiento. 

**La idea es crearlos para aislar los recursos y controlar su acceso**. 

Y podrías mantener una colección de recursos relacionados en compartimentos específicos. Entonces el recurso de red tiene recursos de red y un compartimiento de almacenamiento tiene recursos de almacenamiento.

Ahora, tenga en cuenta que el compartimento raíz, como dije antes, puede contener todos los recursos de la nube. Entonces puede ser una especie de fregadero de cocina. Podrías poner todo ahí. **Pero la mejor práctica es crear compartimentos dedicados para aislar los recursos**. Verás por qué. Déjame explicarte.

**Lo primero es que cada recurso que cree pertenece a un único compartimento.** Entonces creas una máquina virtual, por ejemplo. Va al Compartimento A. No puede ir al Compartimento B. Nuevamente, debe moverlo del Compartimento A o eliminarlo y volver a crearlo en el Compartimento B. **Tenga en cuenta que cada recurso pertenece a un solo compartimento**.

La razón por la que desea compartimentar sus recursos se muestra exactamente en esta diapositiva. La razón por la que se utilizan compartimentos en primer lugar es para controlar el acceso y el aislamiento. Entonces, la forma de hacerlo es que tiene los recursos, digamos en este caso un almacenamiento en bloque, guardado en el Compartimento A. No quiere que todos los usen. Desea que solo los utilicen los administradores de computación y de almacenamiento.

Entonces, crea esos administradores como usuarios y grupos, escribe estas políticas y ellos pueden acceder a estos recursos en este compartimento. Entonces es muy importante. No coloque todos sus recursos en el compartimento raíz. Cree compartimentos para recursos específicos, o de la forma que desee dividir sus arrendamientos, y coloque los recursos en consecuencia.

Ahora bien, ¿cómo interactúan los recursos si están en distintos compartimentos? ¿Tienen que estar todos en el mismo compartimento? Absolutamente no. Como puede ver aquí, **los recursos de un compartimento pueden interactuar con el recurso de otro compartimento**. Aquí, la red de nube virtual es... la instancia informática usa la red de nube virtual, pero están en dos compartimentos diferentes. Así que esto es totalmente compatible. Y mantiene su diseño mucho más limpio.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/53e94cf6-252a-490a-a630-bcfe20a5fc4d)

Tenga en cuenta que los recursos también se pueden mover de un compartimento a otro. Entonces, en este ejemplo, el Compartimento A tenía una máquina virtual. Podemos mover eso del Compartimento A al Compartimento B. 

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/e39ad701-44bd-4fb6-b988-527a8610746b)

Otro concepto que es muy importante comprender es que **los compartimentos son construcciones globales**, como todo en identidad. Por tanto, los recursos de varias regiones pueden estar en el mismo compartimento. Entonces, cuando vas a Phoenix, ves que existe este compartimento. Vas a Ashburn y ves el mismo compartimento.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/110c9c0b-fd14-4777-a325-fcdced01dde6)

Ahora puede escribir políticas para evitar que los usuarios accedan a recursos en una región específica. Podrías hacer eso. Pero tenga en cuenta que todos los compartimentos que cree son globales y están disponibles en todas las regiones a las que tenga acceso. Los compartimentos también se pueden anidar. Así tendrás hasta seis niveles de anidación proporcionados por compartimentos. Haría esto nuevamente porque puede imitar su diseño actual, ya sea su diseño organizacional o su jerarquía de ID. Podrías crear compartimentos anidados. Simplemente ayuda a mantener su diseño más limpio.

![imagen](https://github.com/sbstn-jmnz/OCI-fundations/assets/4334071/e351edd5-cd6e-48e9-93eb-426643a8a124)

**Y luego, finalmente, se podrían establecer cuotas y presupuestos por compartimentos**. Entonces se podría decir que, en mi compartimento particular, no se puede crear una máquina de|metal. O no puede crear un recurso de Exadata. Entonces podrías controlarlo así. Y luego también podrías crear presupuestos para compartimentos. Por lo tanto, se podría decir que, si el uso en un compartimento en particular supera los $1,000, se le marcará y se le notificará. 

[Uploading imagen.png…]()

Esos son los compartimentos. Es una característica única dentro de OCI. Creemos que ayuda a mantener sus arrendamientos mucho mejor organizados. Y realmente es compatible con su jerarquía y diseño de identificación actuales. 


