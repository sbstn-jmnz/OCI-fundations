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

Esos son los compartimentos. Es una característica única dentro de OCI. Creemos que ayuda a mantener sus arrendamientos mucho mejor organizados. Y realmente es compatible con su jerarquía y diseño de identificación actuales. 

## Dominios de identidad (identity domain)

Al igual que los compartimentos, **los dominios de identidad** son contenedores para sus usuarios, grupos y configuración de seguridad. 

Entonces, la forma en que se usa es, digamos, que tengo un compartimiento sandbox con fines de prueba. Por lo tanto, podría tener una configuración seleccionada de usuarios y grupos que participan en esta prueba y podría mantenerlos en este dominio de identidad también sandbox.

Y una vez que ya no los use, puedo eliminar todos estos subgrupos de usuarios. Es una buena manera de segregar usuarios, grupos y configuración de seguridad.

## AuthN y AuthZ

Veamos qué es un principal. Un principal es una entidad de IAM a la que se le permite interactuar con los recursos de OCI. Hay dos tipos de directores principalmente en OCI. Uno son tus usuarios. Piense en las personas que inician sesión en su consola o utilizan su CLI o usuarios de SDK, seres humanos que realmente utilizan sus recursos en la nube. Y entonces los propios recursos pueden ser directores.

Entonces, un buen ejemplo de un principal de recurso es un principal de instancia, que en realidad es una instancia que se convierte en principal, lo que significa que puede realizar llamadas API contra otros servicios OCI como el almacenamiento. También cuando hablamos de directores, tenemos grupos.

Y los grupos son básicamente una colección de usuarios que tienen el mismo tipo de requisitos de acceso a los recursos. Entonces puedes tener un grupo de administración de almacenamiento donde puedes agrupar a todos los seres humanos que son administradores de almacenamiento y así sucesivamente.

Entonces, veamos algunos de los detalles comenzando con la autenticación. A la autenticación a veces también se la denomina AuthN. Como resumimos de la lección anterior, la autenticación consiste básicamente en descubrir: ¿eres quien dices ser? Y la forma más fácil de entender esto es que todos lidiamos con esto a diario. Cuando visita un sitio web y proporciona su nombre de usuario y contraseña para acceder a parte del contenido, está siendo autenticado.

Hay otras formas de realizar la autenticación. Lo común para la nube son las claves de firma de API. Entonces, cuando realiza llamadas API, ya sea que esté usando el SDK o la CLI (terminal de comandos), debe usar las claves de firma de API que utilizan un par de claves públicas privadas para firmar estas llamadas API y autenticar estas llamadas API.

Utiliza un par de claves RSA, como puede ver aquí, con una clave pública y una privada. También existe una tercera forma de realizar la autenticación y se basa en tokens de autenticación. Y estas son cadenas de tokens generadas por Oracle. Y la idea aquí es que se pueden autenticar API de terceros, que no admiten el modelo de autenticación OCI.

Entonces, en este ejemplo, mostramos un ADW, llamando a un ADW, llamada a la API de almacén de datos autónomo donde usamos estos tokens de autenticación. Aún así se sigue su identidad. Estos tokens de autenticación se pueden utilizar para este propósito.

Ahora veamos muy rápidamente la autorización. Entonces, la autorización se ocupa de los permisos y de determinar qué permisos tienes. En OCI, la autorización se realiza a través de lo que llamamos políticas IAM. Y las políticas, piense en ellas como declaraciones legibles por humanos para definir permisos granulares. Así que aquí tienes un par de ejemplos. Y la sintaxis de las políticas es siempre algo similar.

En la siguiente diapositiva, hablaré un poco más sobre lo que significa esta afirmación. Recuerde, las pólizas se pueden adjuntar a un compartimento o a un arrendamiento. Si están vinculados a un arrendamiento, se aplica a todo lo que esté dentro de ese arrendamiento. Si se aplica a un compartimento, se aplica únicamente a los recursos dentro de ese compartimento.

```
Allow group developers to create virtual-machines in tenancy

Allow grupo security to manage virual-machines in compartment sandbox where creation-date > 01/05/2024
```

Entonces, ¿cómo se realiza AuthZ en OCI? Hablamos de políticas. ¿Cómo se ve la sintaxis? Como puede ver aquí, la sintaxis es siempre: siempre debe comenzar con un permiso. Todo está denegado por defecto. Así que realmente no es necesario escribir una declaración de denegación. Entonces dices Permitir nombre_grupo.

Un grupo es básicamente una colección de usuarios. **Por lo tanto, no puede intentar establecer políticas sobre usuarios individuales**. Siempre operas a nivel de grupo. Para hacer algo, hay un verbo. En algunos recursos, hay un tipo de recurso. Y hay una ubicación. La ubicación puede ser un arrendamiento. La ubicación puede ser un compartimento. Y puedes hacer que estas políticas sean realmente complejas agregando condiciones (where). Y nuevamente, curso de fundamentos. Así que no vamos a entrar en muchos de estos temas complejos. Pero realmente se podrían redactar políticas complejas.

Entonces, solo para darle una idea de cómo podrían verse los verbos, hay cuatro niveles de verbos. Hay una gestión. Hay un uso. Hay una lectura. Y hay una inspección. Entonces, administrar básicamente significa que puedes administrar todos los recursos. Usar básicamente significa que puedes leer. Pero no se podían hacer cosas como actualizar y eliminar, etc., etc. Y puedes leer más en la documentación.

El tipo de recurso básicamente puede ser todos los recursos, es decir, todo lo que hay en su cuenta, o pueden ser recursos informáticos, recursos de bases de datos, etc., todos los recursos que tiene. Ahora, podrían operar a nivel familiar, es decir, todas las entidades dentro de esa familia de recursos, o incluso podrían ser muy granulares. Entonces se podría decir que en computación, solo quiero que alguien opere en las instancias pero no trabaje en las imágenes de las instancias.

Entonces realmente podrías hacer eso. Así es como se redactaría una política. Hay algunas excepciones a esta regla. Hay políticas que usted escribiría para servicios y demás. Pero nuevamente, es una puntuación básica, por lo que no entraremos en esos detalles avanzados. Normalmente, así es como se haría una transición en OCI.

Para concluir, vimos cómo se realiza la autenticación en OCI, los tres mecanismos, el usuario nombre, contraseñas, claves de firma de API, tokens de autenticación. Y luego analizamos cómo se realiza la autorización en OCI a través de políticas. Las políticas son realmente poderosas. Son muy fáciles de entender y legibles por humanos. Pero al mismo tiempo, le brindan muchas capacidades avanzadas para implementar un control de acceso realmente detallado. Espero que hayas encontrado útil esta lección. Gracias por ver.
