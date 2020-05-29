---
description: Microsoft Edge complementa las directivas para desarrolladores de catálogos.
title: Directivas para desarrolladores de catálogos de Microsoft Edge addons
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: be159491d892c176a8439393573dc23680fac377
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607436"
---
# Directivas para desarrolladores de catálogos de Microsoft Edge addons  

## Introducción y objetivo de este documento  

Agradecemos tu interés en el desarrollo de extensiones para el catálogo de complementos de Microsoft Edge.  Las directivas para desarrolladores de catálogos de addons de Microsoft Edge \ (complementos: directivas para desarrolladores de catálogos \) se aplican a las extensiones, incluido el envío de extensiones a través del [centro de Partners][MicrosoftPartnerCenter] y el suministro de estas extensiones a través de los complementos de Microsoft Edge.  

## Principios  

Algunos principios que le ayudarán a empezar:  

*   Debes ofrecer un valor único y distintivo dentro de tus extensiones para Microsoft Edge.  Proporciona una razón convincente para descargar las extensiones desde el catálogo de complementos de Microsoft Edge \ (Microsoft Edge addons \).  
*   No debe confundir a nuestros usuarios conjuntos sobre lo que hace su extensión, quién lo está ofreciendo, etc.  
*   No debe intentar hacer más atajo a los usuarios, el sistema o el ecosistema.  No hay ningún lugar en nuestros complementos de Microsoft Edge para ningún tipo de fraude; ¿Estás clasificando y revisando la manipulación, el fraude de la tarjeta de crédito u otra actividad fraudulenta?  

Adherir a estos complementos las directivas de desarrollador de catálogos le ayudarán a tomar decisiones que mejorarán el atractivo y la audiencia de su extensión.  

Las extensiones son cruciales para la experiencia de cientos de millones de usuarios.  Esperamos experimentar lo que creas y estar encantados para ayudarte a entregar tus extensiones al mundo.  

## 1. directivas de producto  

### 1,1 función DISTINCT & valor; Representación precisa  

La extensión y los metadatos asociados deben reflejar de forma precisa y clara el origen, la funcionalidad y las características que se describen.  

#### las extensiones 1.1.1 deben tener un único propósito  

La extensión debe tener un único propósito con una funcionalidad estrecha.  

#### 1.1.2 describir tu extensión  

Todos los aspectos de tu extensión deben describir con precisión las funciones, las características y cualquier limitación importante de tu extensión, incluidos los dispositivos de entrada requeridos o admitidos.  La propuesta de valor de la extensión debe ser clara durante la primera experiencia de ejecución.  La extensión no puede usar un nombre o un icono similar al de otras extensiones, y no debe reclamar que se represente a una empresa, un organismo gubernamental u otra entidad si no tiene permiso para realizar esa representación.  

#### funcionalidad de 1.1.3  

La extensión debe ser completamente funcional.  

#### 1.1.4 buscar y descubrir  

Los términos de búsqueda no pueden superar las siete condiciones únicas y deben ser pertinentes para tu extensión.  

#### 1.1.5 proporcionar los detalles adecuados  

Debes proporcionar detalles informativos y distintivos sobre la extensión y la funcionalidad de la lista \ (metadatos \) para tu extensión.  Tu extensión debe proporcionar una experiencia de usuario de calidad y de gran valor.  La extensión debe tener también una presencia activa en los complementos de Microsoft Edge.  

#### estabilidad y rendimiento de 1.1.6  

La extensión no debe tener un impacto negativo en el rendimiento o la estabilidad de Microsoft Edge.  

#### ofuscación 1.1.7  

No se permiten las extensiones con código ofuscado.  Esto incluye el código dentro del paquete de extensión, así como cualquier código externo o recurso que se obtenga de la Web.  Es posible que se le pida que refactorizar partes de su código si no es revisable.  

#### 1.1.8 modificando la configuración del explorador  

La extensión no debe, **sin el consentimiento adecuado**para el usuario, alterar o parecer alterar, funcionalidad del navegador o configuración, incluyendo, entre otras, el proveedor de búsqueda de la barra de direcciones y las sugerencias, la página de inicio o inicio, la página de la nueva pestaña, y agregar o quitar favoritos.  

Cualquier cambio en la configuración del explorador debe documentarse de forma explícita en la descripción de la extensión.  

La extensión solo puede revisar la configuración clave para reemplazar una página web o servicio de Microsoft por una de terceros \ (como, por ejemplo, requerir el uso de un motor de búsqueda de terceros o establecer la página de inicio en una propiedad Web de terceros? si usted está contratado o asociado de algún otro modo con dicho tercero.  

### seguridad de 1,2  

La extensión no debe comprometer ni poner en peligro la seguridad de los usuarios, ni la seguridad ni la funcionalidad del dispositivo, del sistema o de los sistemas relacionados.  

#### 1.2.1 directivas de seguridad de contenido  

> [!NOTE]
> Si realiza cambios en la extensión más allá de la funcionalidad descrita, cualquier cambio en el código debe ser compatible con la [Directiva de seguridad de contenido de Microsoft Edge][MicrosoftEdgeContentSecurityPolicyRemoteScript].  Ejemplo: la extensión no debe descargar un script remoto y, posteriormente, ejecutar ese script de forma que no sea coherente con la funcionalidad descrita.  

#### 1.2.2 software no deseado y malintencionado  

La extensión no debe contener ni habilitar malware según se define en los criterios de Microsoft para el [software no deseado y malintencionado][MicrosoftIdentifiesMalwareUnwantedApplications].  

#### dependencia 1.2.3 en otro software  

La extensión puede depender del software no integrado \ (como otro producto, módulo o servicio \) para ofrecer la funcionalidad principal, siempre que se divulgue la dependencia en la descripción  

#### Actualización de las extensiones de 1.2.4  

A menos que Microsoft permita lo contrario, las extensiones solo deben actualizarse a través de los complementos de Microsoft Edge.  

### el producto 1,3 se va a probar  
La extensión debe ser comprobable.  Si no es posible probar la extensión por algún motivo, incluidos, entre otros, los siguientes elementos, la extensión puede dar error en este requisito.  

#### 1.3.1 credenciales de usuario  
Si su extensión requiere credenciales de inicio de sesión, proporcione una cuenta de demostración de trabajo con el campo **notas para la certificación** .  

#### 1.3.2 disponibilidad de servicios  

Si su extensión requiere acceso a un servidor, el servidor debe ser funcional para verificar que funciona correctamente.  

### uso de 1,4  

La extensión debe cumplir con los estándares del almacén de extensiones para facilitar su uso, incluidos, entre otros, los que se enumeran en las subsecciones siguientes.  

#### 1.4.1 compatibilidad entre plataformas  

Las extensiones deben ser compatibles con Microsoft Edge en todos los dispositivos y plataformas en los que se pueden descargar.  Si se descarga una extensión en un dispositivo con el que no es compatible, debe detectarse en el lanzamiento y mostrar un mensaje al usuario en el que se detallan los requisitos que deben cumplir los dispositivos para ser compatibles con su extensión.  

#### Experiencia de usuario de 1.4.2  

La extensión debe iniciarse inmediatamente y debe continuar respondiendo a la entrada del usuario.  Las extensiones deben continuar ejecutándose y siguen respondiendo a la entrada del usuario.  Las extensiones deben cerrarse correctamente y no cerrarse inesperadamente.  La extensión debe controlar las excepciones y seguir respondiendo a la entrada del usuario una vez que se ha controlado la excepción.  

### 1,5 información personal  

Los siguientes requisitos se aplican a las extensiones que acceden a información personal.  Información personal incluye toda la información o los datos que identifican o pueden usarse para identificar a una persona o que está asociada a información o datos.  

#### 1.5.1 recopilar información personal solo cuando sea necesario  

Su extensión puede recopilar, acceder, usar o transmitir información personal \ (incluida la actividad de navegación en Internet \); solo si lo necesita y solo para usarla en una característica que se haya divulgado de cara al usuario.  

#### 1.5.2 mantener una política de privacidad  

Independientemente de si su extensión accede, recopila o transmite información personal; usted debe proporcionar una notificación destacada y cumplir con su política de privacidad Si así lo requiere la ley.  Su política de privacidad debe informar a los usuarios de la información personal a la que se tiene acceso, recopilar o transmitir mediante su extensión, cómo se usa, almacena y protege la información, e indican los tipos de partes a quienes se revela.  Su política de privacidad debe describir los controles que los usuarios tienen sobre el uso y el uso compartido de su información, la forma en que acceden a su información y deben cumplir con las leyes y normativas vigentes.  Tu política de privacidad debe estar actualizada a medida que agregues nuevas características y funcionalidades a tu extensión.  

Si proporciona a Microsoft su política de privacidad, usted acepta permitir a Microsoft compartir dicha política de privacidad con usuarios de su extensión.  

#### 1.5.3 compartir datos con terceros  

Puede publicar la información personal de los usuarios de su extensión a un servicio externo o a terceros a través de la extensión o los metadatos asociados solo después de obtener el consentimiento de aceptación de esos usuarios.  El consentimiento de aceptación significa que los usuarios otorgan su permiso expreso en la interfaz de usuario de su extensión para la actividad solicitada, después de:  

*   Describa a sus usuarios cómo se accede a la información, la utiliza o la comparte e indica los tipos de partes a quienes se revela, y  
*   Proporcionar a los usuarios un mecanismo en la interfaz de usuario de extensión a través de la cual tienen la opción de revocar el permiso y anular la suscripción.  

#### 1.5.4 información de uso compartido de no usuarios  

Si publica la información personal de una persona en un servicio externo o de terceros a través de la extensión o los metadatos, pero la persona cuya información está compartiendo no es un usuario de su extensión;  

1.  Para publicar esa información personal, debe obtener el consentimiento expreso por escrito.  
1.  Usted debe permitir que la persona cuya información se comparte retirara ese consentimiento en cualquier momento.  
1.  Su política de privacidad debe revelar claramente que puede recopilar información personal de esta manera.  
1.  Si así lo exige la legislación vigente, deberá eliminar la información personal de cualquier persona a petición, incluidas las personas cuya información usted recopile de esta manera.  
1.  Si su extensión proporciona a los usuarios acceso a la información personal de otra persona, este requisito también se aplica.  

#### 1.5.5 transmitir información de forma segura  

Si su extensión recopila, almacena o transmite información personal; debe hacerlo de manera segura usando métodos de criptografía modernos.  

#### información muy confidencial de 1.5.6  

La extensión no debe recopilar, almacenar ni transmitir información personal delicada, como la salud o los datos financieros, a menos que la información esté relacionada con la funcionalidad de su extensión.  La extensión también debe obtener consentimiento expreso para el usuario antes de recopilar, almacenar o transmitir dicha información.  

### permisos de 1,6  

La extensión solo debe solicitar los permisos necesarios para funcionar.  Debes proporcionar una descripción del funcionamiento de tu extensión.  La extensión solo debe realizarse como se describe.  La extensión no puede solicitar permiso para capacidades que van más allá de las capacidades necesarias para realizar y funcionar como se declara.  

### localización de 1,7  

Debe localizar su extensión para todos los idiomas que la extensión pretende admitir.  El texto de la descripción de la extensión debe estar localizado en cada uno de los lenguajes declarados.  
Si la extensión está localizada de modo que algunas características no estén disponibles en una versión localizada, debe indicar o mostrar claramente los límites de localización en la descripción de la extensión. La experiencia proporcionada por una extensión debe ser razonablemente similar en todos los idiomas que admita.  

### 1,8 transacciones financieras  

Si su producto incluye la compra de productos, las suscripciones, la moneda virtual, la funcionalidad de facturación o captura información financiera; se aplican los requisitos de las secciones siguientes.  

#### Características de 1.8.1 de pagar  

Tu extensión puede permitir que los usuarios consuman contenido digital o servicios adquiridos a través de una API o un mecanismo de compra de terceros.  

Debes usar una API segura de compras de terceros para las compras de bienes o servicios físicos.  Debes usar una API segura de compras de terceros para los pagos realizados en relación con otros servicios, entre ellos, el mundo real de las apuestas o las contribuciones benéficas.  

*   Si su extensión se usa para facilitar o recopilar contribuciones benéficas o para realizar un sorteo o concurso promocional, debe hacerlo de conformidad con la legislación vigente.  
*   También debes indicar claramente que Microsoft no es el recaudador ni el patrocinador de la promoción.  
*   Las ofertas de productos que se venden en su extensión no deben convertirse a ninguna moneda válida legal \ (como USD, euro, etc. \) ni a ningún producto o servicio físico.  

Los siguientes requisitos rigen para su uso de una API segura de compras de terceros:  

*   En el momento de la transacción o cuando se recopilan datos financieros o de pago del usuario; la extensión debe identificar al proveedor de transacciones de comercio, autenticar al usuario y recibir confirmación de usuario para la transacción.  Un proveedor de transacciones de comercio mantiene una plataforma segura para los intercambios financieros.  
*   Su extensión puede ofrecer a los usuarios la capacidad de guardar esta autenticación, pero los usuarios deben tener la capacidad de solicitar una autenticación en cada transacción o de desactivar las transacciones del producto.  
*   Si su extensión recopila información de la tarjeta de crédito o usa un procesador de pago de terceros que recopila información de la tarjeta de crédito, el procesamiento de pago debe cumplir con el estándar de seguridad de datos PCI actual \ (PCI DSS \).  

#### 1.8.2 características de los pagos  

La extensión y los metadatos asociados deben proporcionar información sobre los tipos de compras dentro del producto ofrecidos y la gama de precios.  Usted no debe engañar a los usuarios y debe tener claros la naturaleza de las promociones y las ofertas de los productos incluidos en el ámbito y las condiciones de las experiencias de prueba.  Si su extensión restringe el acceso al contenido creado por el usuario durante o después de una prueba, debe notificar a los usuarios por adelantado.  Además, la extensión debe dejar claro a los usuarios que inician una opción de compra en la extensión.  

### notificaciones de 1,9  

La extensión debe respetar la configuración del sistema para las notificaciones.  Esto significa que cualquier presentación de anuncios y notificaciones a los usuarios debe coincidir con las preferencias de usuario, independientemente de si las notificaciones son proporcionadas por el servicio de notificaciones push de Microsoft \ (MPNS \), el servicio de notificaciones push de Windows \ (WNS \) o cualquier otro servicio.  Si el usuario deshabilita las notificaciones, ya sea en un producto específico o en todo el sistema, la extensión debe ser funcional.  

Si tu producto usa MPNS o WNS para transmitir notificaciones, debe cumplir con los siguientes requisitos:  

#### Instrucciones generales de 1.9.1  

Las notificaciones proporcionadas a través de WNS o MPNS se consideran contenido del producto y están sujetas a todas las directivas para desarrolladores de catálogos de complementos.  

#### 1.9.2 propiedad de las notificaciones  

No debe ocultar ni intentar disfrazar el origen de las notificaciones iniciadas desde la extensión.  

#### 1.9.3 información confidencial o confidencial  

No debe incluir en una notificación ninguna información que los usuarios puedan considerar razonablemente confidencial o confidencial.  

#### 1.9.4 propósito de las notificaciones  

Las notificaciones enviadas desde la extensión deben relacionarse con esa extensión o con otras extensiones publicadas en el catálogo de complementos de Microsoft Edge y no deben incluir mensajes promocionales de ningún tipo que no estén relacionados con las extensiones.  

### 1,10 actividades de publicidad y contenido  

Para todas las actividades relacionadas con anuncios, se aplican los siguientes requisitos:  

#### 1.10.1 propósito  

El contenido principal de tu extensión no debe ser publicitario y la publicidad debe ser claramente diferenciada de otros contenidos de tu extensión.  

#### directivas y acuerdos de 1.10.2  

Todo el contenido publicitario que muestre la extensión debe adherirse a la [política de aceptación creativa de Microsoft][MicrosoftAdvertisingCreativeAcceptancePolicies].  
Si la extensión muestra anuncios, todo el contenido que se muestra debe cumplir los requisitos de publicidad del [contrato para desarrolladores de aplicaciones][MicrosoftAppDeveloperAgreement] y esta Directiva.  

#### 1.10.3 calidad de publicidad  

*   El propósito principal de tu extensión no debe ser que los usuarios puedan hacer clic en anuncios.  
*   La extensión no debe hacer nada que interfiera o disminuya la visibilidad, el valor o la calidad de los anuncios que se muestran.  

#### promociones de 1.10.4  

Si compra o crea campañas publicitarias promocionales para promocionar las extensiones a través de la funcionalidad de campaña publicitaria en el [centro asociado][MicrosoftPartnerCenter], todos los materiales de publicidad que proporcione a Microsoft, incluidas las páginas de aterrizaje asociadas, deben cumplir con la [política de especificaciones creativas de Microsoft][MicrosoftAdvertisingCreativeSpecifications] y la [política de aceptación creativa de Microsoft][MicrosoftAdvertisingCreativeAcceptancePolicies].  

#### 1.10.5 notificar a los usuarios de la cancelación de la publicidad basada en intereses  

La declaración de privacidad o las condiciones de uso deben permitir a los usuarios saber que piensa enviar información personal al proveedor de servicios de anuncios y que deben indicar a los usuarios cómo pueden optar por la publicidad basada en el interés.  

#### 1.10.6 otras pautas  

Si su extensión se dirige a niños menores de 13 años, según se define en la [ley de protección de la privacidad][FTCChildrensPrivacy]de los niños; debe notificar a Microsoft de este hecho en el [centro de Partners][MicrosoftPartnerCenter] y asegurarse de que todo el contenido que se muestra en su extensión sea adecuado para niños menores de 13 años.  

## 2 directivas de contenido  

Las siguientes directivas se aplican al contenido y los metadatos \ (incluidos el nombre del publicador, el nombre de extensión, el icono de extensión, la descripción de extensión, las capturas de pantallas, los finalizadores de extensión y las miniaturas de tráiler, y cualquier otro metadato de la extensión \) que se ofrezca para su distribución en los complementos  Contenido significa las imágenes, los sonidos, los vídeos y el texto contenido en la extensión, los mosaicos, las notificaciones, los mensajes de error o los anuncios expuestos a través de la extensión, y cualquier elemento que se envíe desde un servidor o al que se conecte la extensión.  Puesto que los complementos de extensiones y Microsoft Edge se usan en todo el mundo, estos requisitos se interpretan y aplican en el contexto de normativas regionales y culturales.  

### 2,1 requisitos de contenido para la lista de catálogos de complementos de Microsoft Edge  

Los metadatos y otros contenidos que envíes para acompañar a tu extensión no pueden contener contenido para adultos.  
Los mensajes que no cumplen los requisitos de las listas de almacenes de extensiones se rechazan o se eliminan de vez en cuando.  

### 2,2 contenido, incluidos nombres, logotipos, original y de terceros  

Todo el contenido de la extensión y los metadatos asociados debe haber sido creados originalmente por usted o con la licencia correspondiente de un titular de derechos de terceros y debe usarse solo según lo permita el titular de los derechos o de otra manera autorizada por la ley.  

### 2,3 riesgo de daño  

#### 2.3.1 requisitos  

La extensión no debe incluir ningún contenido que facilite o glamorizes las siguientes actividades del mundo real: \ (a \) Extreme o innecesaria la violencia; \ (b \) violaciones de derechos humanos; \ (c \) la creación de armas ilegales; o \ (d \) el uso de armas contra una persona, un animal o una propiedad real o personal.  

#### 2.3.2 responsabilidad  

La extensión no debe: \ (a \) supondrá un riesgo de seguridad para los usuarios finales o para cualquier otra persona o animal, y no se desprendan, heridas ni otros daños. o \ (b \) supongan un riesgo o produzcan daños en la propiedad real o personal.  Usted es el único responsable de todas las pruebas de seguridad de extensión, la adquisición de certificados y la implementación de las protecciones de características apropiadas.  Usted no debe deshabilitar ninguna característica de seguridad de la plataforma ni de comodidad y usted debe incluir todas las advertencias, los avisos y las renuncias estándar de la industria que sean necesarios en su extensión.  

### 2,4 difamatorio, difamatorios, slanderous e amenazar  

La extensión no debe contener ningún contenido difamatorio, difamatorios, slanderous o amenazante.  

### 2,5 de contenido ofensivo  

La extensión y los metadatos asociados no deben contener contenido potencialmente delicado o ofensivo.  El contenido puede considerarse confidencial u ofensivo en algunos países o regiones debido a las leyes locales o culturales.  Además, la extensión y los metadatos asociados no deben incluir contenido que se promueva contra discriminaciones, odio o violencia basándose en consideraciones de raza, étnico, nacionalidad, nacionalidad, sexo, edad, discapacidad, religión, orientación sexual, estado como veterano o miembro de cualquier otro grupo social.  

### 2,6 alcohol, tabaco y drogas  

Tu extensión no debe incluir ningún contenido que facilite o glamorizes el uso excesivo o irresponsible de alcohol o tabaco o drogas.  

### 2,7 de contenido para adultos  

La extensión no debe contener ni mostrar contenido que una persona razonable considere pornográfico o sexual Explicit.  

### 2,8 contenido, servicios y actividad prohibidos  

Tu extensión debe cumplir con las siguientes condiciones.  

*   La extensión no debe incluir contenido ni proporcionar servicios que faciliten la apuestas en línea.  El juego de azar en Internet incluye, entre otros, casinos, apuestas deportivas, loterías o juegos de habilidades que ofrecen premios de efectivo u otro valor.  
*   La extensión no debe proporcionar acceso no autorizado al contenido del sitio web, por ejemplo, mediante la elusión de las restricciones de paywalls o de inicio de sesión.  
*   La extensión no debe proporcionar, alentar ni habilitar el acceso no autorizado, la descarga ni el streaming de contenido o multimedia con derechos de propiedad intelectual.  
*   La extensión no debe tener mío cryptocurrency.  

### 2,9 actividad ilegal  

La extensión no debe incluir contenido ni funcionalidades que fomenten, faciliten o glamorizesen la actividad ilegal en el mundo real.  

### 2,10 un exceso de blasfemias y contenido inadecuado  

*   Tu extensión no debe contener blasfemias excesivas o gratuitamente.  
*   La extensión no debe contener ni mostrar contenido que una persona razonable considere obsceno.  

### 2,11 requisitos específicos de países y regiones  

El contenido que es ofensivo en cualquier país o región a los que la extensión está destinada no está permitido.  El contenido puede considerarse ofensivo en determinados países o regiones debido a las leyes locales o culturales.  Algunos ejemplos de contenido potencialmente ofensivo en ciertos países o regiones son los siguientes:  

**China**  

*   Contenido sexual prohibido  
*   Referencias de territorio o región en disputa  
*   Proporcionar o permitir el acceso a contenido o servicios ilegales en virtud de la legislación local vigente  

### 2,12 clasificaciones por edades  

#### 2.12.1 de adultos  

Al enviar la extensión al [centro de Partners][MicrosoftPartnerCenter], debe indicar si su extensión muestra el contenido que debe marcarse como "maduro".  Al determinar la clasificación de la extensión, ten en cuenta todo el contenido de la aplicación, incluido el contenido generado por el usuario y los anuncios, y el contenido que los vínculos de la extensión.  Si usted indica que su extensión no contiene ningún contenido "maduro", usted es responsable de mantener la precisión de esta calificación.  Independientemente de la clasificación dada a su extensión, aún debe cumplir con todos los requisitos de contenido de las directivas de desarrollador de complementos de Microsoft Edge.  

#### Cambio de clasificaciones de 2.12.2  

Si su extensión proporciona contenido \ (como por ejemplo, un usuario minorista, u otro contenido basado en Web \) que pueda ser adecuado para una clasificación de edad superior a la clasificación asignada, debe solicitar a los usuarios que opten por recibir dicho contenido con un filtro de contenido o iniciando sesión con una cuenta preexistente.  

### vídeos de 2,13  

Si envías un video promocional en el listado, debe seguir todas las directrices de contenido mencionadas en esta Directiva.  Si elige proporcionar un vínculo de YouTube, debe asegurarse de que los anuncios estén deshabilitados para los vídeos específicos que desea insertar.  Para obtener más información sobre cómo se habilitan y deshabilitan los anuncios en YouTube, consulte [support.Google.com/YouTube/Answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] y [support.Google.com/YouTube/Answer/132596][GoogleYoutubeAnswer132596].  

<!-- image links -->  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Relajar la directiva predeterminada: Directiva de seguridad de contenido \ (CSP \) | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Acuerdo de desarrollador de aplicaciones | Microsoft docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Cómo Microsoft identifica el malware y las aplicaciones potencialmente no deseadas | Microsoft docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Establecer los formatos de anuncio predeterminados para la ayuda de YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anuncios en vídeos insertados: ayuda de YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Privacidad de los niños: Comisión de comercio federal"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Directivas de aceptación de Creative-Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Especificaciones de creatividad-Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de socios"  
