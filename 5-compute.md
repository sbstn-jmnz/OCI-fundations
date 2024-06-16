# Computación

Bienvenido a este módulo sobre OCI Compute. Comencemos con una introducción. Por lo tanto, el servicio OCI Compute le proporciona máquinas virtuales y servidores bare metal para satisfacer sus requisitos informáticos y de aplicaciones. Las tres características que definen este servicio incluyen escalabilidad, alto rendimiento y precios más bajos. En las próximas diapositivas, hablaré de cada uno de ellos con un poco más de detalle.

Entonces, lo primero en el servicio OCI Compute es tener esta noción de forma flexible. ¿Qué significa? Bueno, significa que puedes elegir tus propios núcleos, tus procesadores de CPU y también puedes elegir tu propia memoria. Y como pueden ver los controles deslizantes aquí, pueden elegir una combinación de núcleos de CPU y memoria y hay una proporción allí. Pero tiene flexibilidad para elegir su propia configuración.

Literalmente, hay miles y miles de configuraciones entre las que puedes elegir. Ahora bien, ¿de qué sirve hacer esto? La utilidad de hacer esto es que puede seleccionar el tipo de máquina correcto utilizando nuestras formas flexibles.

Y en la nube existe esta noción de talla de camiseta. Entonces tienes formas pequeñas, medianas y grandes, y tu aplicación tiene que adaptarse a esas formas. Y a veces hay un aprovisionamiento excesivo o insuficiente y hay que pasar por ese doloroso proceso de cambiar los tipos de máquinas. Esperamos que con estas formas flexibles no tengas que hacer eso.

Si aún desea utilizar el enfoque tradicional, tenemos máquinas virtuales, servidores básicos y un host dedicado. Y podrías usar uno de ellos o todos. Y los servidores bare metal básicamente significan que obtienes una máquina completa, un servidor completo que está completamente dedicado a ti. Un host dedicado básicamente significa que obtienes una máquina completa y dedicada. Pero además de eso, podrías ejecutar máquinas virtuales.

¿Cuál es la diferencia entre host dedicado y máquinas virtuales? Bueno, las máquinas virtuales, como puede ver en la diapositiva aquí, son compartidas y multiinquilino, lo que significa que el host puede ejecutar máquinas virtuales de varios clientes. Tienen un fuerte aislamiento de seguridad, por lo que no tienes que preocuparte por eso. Pero algunos clientes quieren un host dedicado donde puedan ejecutar sus propias máquinas virtuales. Y las máquinas virtuales... no tienen máquinas virtuales de ningún otro cliente ejecutándose allí. Entonces esa opción también se proporciona mediante el uso de un host dedicado.

No solo esto, sino que OCI es solo uno de los dos proveedores de la nube que le ofrece opciones de procesadores. Entonces, puede ejecutar instancias basadas en AMD, puede ejecutar instancias basadas en Intel y también puede ejecutar instancias basadas en Arm; son algo realmente poderoso para la informática móvil. Los teléfonos que utiliza hoy probablemente funcionen con procesadores Arm. Ahora, Arm está llegando a los centros de datos.

Así que hoy utilizamos la familia de procesadores Ampere Altra. Las instancias Ampere A1 funcionaron muy bien en muchos casos de uso. Como puede ver en la pantalla aquí, estamos usando NGINX, un número de rendimiento de precio. Es un buen ejemplo de cargas de trabajo de alto rendimiento, como servidores web, microservicios y puertas de enlace API.

En las pruebas de Arm de NGINX como una solicitud de proxy inverso por segundo, puede ver aquí que Ampere A1, que es el procesador que tenemos, que estamos usando para Arm, tenía un rendimiento de precio un 32% mejor que el procesador AMD equivalente y un 69% mejor. rendimiento que el procesador Intel. Entonces, esto realmente habla de que nuestra industria define la capacidad de precio-rendimiento, particularmente con los procesadores Arm.

Y finalmente, en lo que respecta a los precios, el servicio implementa precios de pago por uso. Para empezar, somos un 50% más baratos que cualquier otra nube que existe. Y no solo eso, podría usar algo como máquinas virtuales interrumpibles para reducir su costo en más del 50 % con respecto a sus instancias habituales.

Las máquinas virtuales interrumpibles son máquinas virtuales de bajo costo y de corta duración, adecuadas para trabajos por lotes y cargas de trabajo tolerantes a fallas. Son similares a las instancias normales, pero tienen un precio un 50 % más bajo. Para que pueda utilizarlos para reducir aún más sus costos.

Para resumir, un servicio muy poderoso. Las tres características definitorias de las que hablamos son la noción de escala, la noción de mayor rendimiento, vimos un ejemplo de eso y los precios más bajos proporcionados por el servicio informático. Espero que hayas encontrado útil esta lección. Gracias por ver.

## Instancias

Bienvenido a esta lección sobre conceptos básicos de instancias. Veamos aquí algunos de los conceptos básicos de las instancias. Entonces, cuando decimos una instancia, nos referimos a un comuptador informático. Y tiene varias dependencias. Así que veámoslos.

Entonces tiene una región de Oracle Cloud aquí. Una región se compone de múltiples AD. Un AD no es más que un centro de datos, como puedes ver aquí. La primera dependencia que tiene el servicio informático o los hosts informáticos es en Virtual Cloud Network. Entonces, para poner en marcha una instancia informática, necesita una red de nube virtual. Como puede ver aquí, tiene una red dividida en porciones más pequeñas llamadas subredes. Entonces tiene una subred aquí y necesita crearla antes de poder activar un host informático.

Ahora puede activar un host informático. Es una construcción física. La creación de redes es una construcción virtual. Entonces, ¿cómo se relacionan? Dentro de un host informático, tiene una tarjeta de interfaz de red física y virtualiza esa tarjeta. Virtualizamos esa tarjeta: le damos esta NIC virtual. Y esa NIC virtual se coloca dentro de la subred, como puedes ver aquí. Y esa es la asociación para el host informático. Y de ahí proviene la IP privada para el host informático, porque cada host informático o VM que está ejecutando, o una máquina básica, tiene una dirección IP privada.

Ahora, hay otro conjunto de dependencias que tienen las instancias informáticas, y es con el volumen de inicio, el disco de inicio y los volúmenes en bloque. ¿Qué significan estos? Bueno, cada uno de estos hosts informáticos que está creando tiene un sistema operativo. Y la imagen que se utiliza para lanzar una instancia determina su sistema operativo y otro software. Entonces tienes este concepto de una imagen que proviene de este disco de almacenamiento de red llamado disco de arranque. Por lo tanto, no permanece en el host informático, sino que en realidad vive en algún lugar de la red.

Y también tienes datos, como sistemas de archivos, etcétera. Estás trabajando en las instancias informáticas. También viven en la red. Entonces están los discos de datos y los discos del sistema operativo juntos. Hay un servicio llamado servicio de volumen en bloque que el host informático utiliza para ejecutar su sistema operativo y sus discos de datos. Ahora bien, estos son almacenamiento remoto, como puedes ver aquí. Entonces, para recapitular, el plano de control de cómputo depende del plano de control de red y del plano de control de almacenamiento en bloque.

Hay una característica más que es realmente relevante cuando se habla de instancias informáticas y es la migración en vivo. Sabemos que las computadoras fallan todo el tiempo. Entonces, ¿cómo nos aseguramos de que cualquier host informático que esté ejecutando esté siempre en funcionamiento? Entonces tenemos esta característica llamada migración en vivo. Y la idea aquí es que si uno de los hosts informáticos falla, hay un problema, migraremos su VM a otro host en nuestro centro de datos y será transparente para usted. Hay múltiples opciones que usted proporciona, ya sea de participación o de exclusión voluntaria, entre las que puede elegir. Pero la idea es que migremos sus máquinas virtuales para que pueda migrar en vivo entre hosts sin reiniciar. Esto mantiene sus aplicaciones funcionando incluso durante eventos de mantenimiento. Lograr esto en sus propios centros de datos no es una tarea tan trivial, pero lo hacemos sin problemas dentro de OCI.

Para resumir, en esta lección analizamos los conceptos básicos de las dependencias del plano de control y luego hablamos sobre la migración en vivo.



