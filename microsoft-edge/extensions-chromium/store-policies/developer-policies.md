---
description: Directivas para desarrolladores del tienda de complementos de Microsoft Edge
title: Directivas para desarrolladores del tienda de complementos de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 8b3e537752e1f5e891626f8cd28cb89806295166
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643430"
---
# <a name="microsoft-edge-add-ons-store-developer-policies"></a>Directivas para desarrolladores del tienda de complementos de Microsoft Edge  

## <a name="introduction-and-objective-of-this-document"></a>Introducción y objetivo de este documento  

Gracias por su interés en desarrollar extensiones para la Microsoft Edge complementos.  Las directivas de desarrollador de la tienda de complementos de Microsoft Edge \(Directivas de desarrollador de la tienda [][MicrosoftPartnerCenter] de complementos\) se aplican a las extensiones, incluido el envío de extensiones a través del Centro de partners y la provisión de dichas extensiones a través de los complementos de Microsoft Edge.  

## <a name="principles"></a>Principios  

Algunos principios para empezar:  

*   Debe ofrecer un valor único y distinto dentro de las extensiones para Microsoft Edge.  Proporcione una razón atractiva para descargar las extensiones de la tienda de complementos Microsoft Edge \(Microsoft Edge Add-ons\).  
*   No debe engañar a nuestros usuarios conjuntos sobre lo que hace la extensión, quién la ofrece, y así sucesivamente.  
*   No debe intentar engañar a los usuarios, el sistema o el ecosistema.  No hay ningún lugar en nuestros Microsoft Edge complementos para ningún tipo de fraude; ya sea la manipulación de clasificaciones y revisión, el fraude de tarjetas de crédito u otra actividad fraudulenta.  
    
El cumplimiento de las Microsoft Edge de desarrolladores de la tienda de complementos debe ayudarte a tomar decisiones que mejoren el atractivo y el público de la extensión.  

Las extensiones son cruciales para la experiencia de cientos de millones de usuarios.  Esperamos experimentar lo que creas y estamos encantados de ayudar a entregar tus extensiones al mundo.  

## <a name="1-product-policies"></a>1. Directivas de producto  

### <a name="11-distinct-function--value-accurate-representation"></a>1.1 Función distinta & valor; Representación precisa  

La extensión y los metadatos asociados deben reflejar de forma precisa y clara el origen, la funcionalidad y las características que describa.  

#### <a name="111-extensions-must-have-a-single-purpose"></a>1.1.1 Las extensiones deben tener un único propósito  

La extensión debe tener un único propósito con funcionalidad limitada.  

#### <a name="112-describe-your-extension"></a>1.1.2 Describir la extensión  

Todos los aspectos de la extensión deben describir con precisión las funciones, características y cualquier limitación importante de la extensión, incluidos los dispositivos de entrada necesarios o compatibles.  La propuesta de valor de la extensión debe ser clara durante la primera experiencia de ejecución.  La extensión no puede usar un nombre o icono similar al de otras extensiones y no debe reclamar representar una empresa, un organismo gubernamental u otra entidad si no tiene permiso para realizar esa representación.  

#### <a name="113-functionality"></a>1.1.3 Funcionalidad  

La extensión debe ser totalmente funcional.  

#### <a name="114-search-and-discovery"></a>1.1.4 Búsqueda y detección  

Los términos de búsqueda no pueden superar los siete términos únicos y deben ser relevantes para la extensión.  

#### <a name="115-provide-appropriate-details"></a>1.1.5 Proporcionar los detalles adecuados  

Debe proporcionar detalles distintos e informativos sobre la extensión y la funcionalidad en la descripción \(metadata\) de la extensión.  La extensión debe proporcionar una experiencia de usuario valiosa y de calidad.  La extensión también debe tener una presencia activa en Microsoft Edge complementos.  

#### <a name="116-stability-and-performance"></a>1.1.6 Estabilidad y rendimiento  

La extensión no debe afectar negativamente al rendimiento o la estabilidad de Microsoft Edge.  

#### <a name="117-obfuscation"></a>1.1.7 Ofuscación  

No se permiten extensiones con código ofuscado.  Esto incluye código dentro del paquete de extensión, así como cualquier código externo o recurso obtenido de la web.  Es posible que se le pida que refactorice partes del código si no es revisable.  

#### <a name="118-altering-browser-settings"></a>1.1.8 Modificar la configuración del Configuración  

La extensión no debe, sin el consentimiento del usuario adecuado, modificar o parece alterar la funcionalidad o la configuración del explorador, incluidas, entre otras, las sugerencias y el proveedor de búsqueda de la barra de direcciones, la página de inicio o inicio, la nueva página de pestañas y la adición o eliminación de favoritos.  

Cualquier modificación de la configuración del explorador debe documentarse explícitamente en la descripción de la extensión.  

La extensión solo puede revisar la configuración de clave para reemplazar una página web o servicio de Microsoft por la de un tercero \(por ejemplo, requerir el uso de un motor de búsqueda de terceros o establecer la página principal en una propiedad web de terceros\) si está empleado por o asociado a dicho tercero.  

### <a name="12-security"></a>1.2 Seguridad  

La extensión no debe poner en peligro ni poner en peligro la seguridad del usuario, ni la seguridad o funcionalidad del dispositivo, sistema o sistemas relacionados.  

#### <a name="121-content-security-policies"></a>1.2.1 Directivas de seguridad de contenido  

> [!NOTE]
> Si realiza cambios en la extensión más allá de la funcionalidad descrita, cualquier cambio en el código debe ser compatible con la directiva de seguridad Microsoft Edge [contenido][MicrosoftEdgeContentSecurityPolicyRemoteScript].  Por ejemplo, la extensión no debe descargar un script remoto y, posteriormente, ejecutarlo de una manera que no sea coherente con la funcionalidad descrita.  

#### <a name="122-unwanted-and-malicious-software"></a>1.2.2 Software no deseado y malintencionado  

La extensión no debe contener ni habilitar malware según los criterios de Microsoft para software [no deseado y malintencionado][MicrosoftIdentifiesMalwareUnwantedApplications].  

#### <a name="123-dependency-on-other-software"></a>1.2.3 Dependencia de otro software  

La extensión puede depender de software no integrado \(como otro producto, módulo o servicio\) para ofrecer la funcionalidad principal, siempre que revele la dependencia en la descripción.  

#### <a name="124-extensions-update"></a>Actualización de extensiones 1.2.4  

A menos que Microsoft lo permita de otro modo, las extensiones solo deben actualizarse Microsoft Edge complementos.  

### <a name="13-product-is-testable"></a>1.3 El producto es testable  

La extensión debe poder probarse.  Si no es posible probar la extensión por cualquier motivo, incluidos, entre otros, los elementos siguientes, la extensión puede fallar este requisito.  

#### <a name="131-user-credentials"></a>1.3.1 Credenciales de usuario  

Si la extensión requiere credenciales de inicio de sesión, proporcione una cuenta de demostración de trabajo con el `Notes for certification` campo.  

#### <a name="132-availability-of-services"></a>1.3.2 Disponibilidad de servicios  

Si la extensión requiere acceso a un servidor, el servidor debe ser funcional para comprobar que funciona correctamente.  

### <a name="14-usability"></a>1.4 Usabilidad  

La extensión debe cumplir Microsoft Edge estándares de almacenamiento de complementos para la facilidad de uso, incluidos, entre otros, los enumerados en las subsecciones siguientes.  

#### <a name="141-compatibility-across-platforms"></a>1.4.1 Compatibilidad entre plataformas  

La extensión debe ser compatible con Microsoft Edge todos los dispositivos y plataformas en los que se pueden descargar.  Si una extensión se descarga en un dispositivo con el que no es compatible, debe detectarlo al iniciar y mostrar un mensaje al usuario detallando los requisitos que los dispositivos deben cumplir para ser compatibles con la extensión.  

#### <a name="142-user-experience"></a>1.4.2 Experiencia de usuario  

La extensión debe iniciarse rápidamente y debe responder a la entrada del usuario.  La extensión debe continuar en ejecución y seguir respondiendo a la entrada del usuario.  La extensión debe cerrarse correctamente y no cerrarse inesperadamente.  La extensión debe controlar las excepciones y seguir respondiendo a la entrada del usuario después de controlar la excepción.  

### <a name="15-personal-information"></a>1.5 Información personal  

Los siguientes requisitos se aplican a las extensiones que tienen acceso a información personal.  La información personal incluye toda la información o los datos que identifican o pueden usarse para identificar a una persona, o que están asociados con dicha información o datos.  

#### <a name="151-collect-personal-information-only-when-necessary"></a>1.5.1 Recopilar información personal solo cuando sea necesario  

La extensión puede recopilar, obtener acceso, usar o transmitir información personal \(incluida la actividad de exploración web\); solo si lo requiere y solo para su uso en una característica destacada y orientada al usuario.  

#### <a name="152-maintain-a-privacy-policy"></a>1.5.2 Mantener una directiva de privacidad  

Independientemente de si la extensión tiene acceso, recopila o transmite información personal; debe proporcionar un aviso destacado de y cumplir con su directiva de privacidad si lo requiere la ley.  Su directiva de privacidad debe informar a los usuarios de la información personal a la que se ha accedido, recopilado o transmitido por su extensión, cómo se usa, almacena y protege esa información e indica los tipos de partes a las que se divulga.  La directiva de privacidad debe describir los controles que los usuarios tienen sobre el uso y el uso compartido de su información, cómo acceden a su información y debe cumplir con las leyes y normativas aplicables.  La directiva de privacidad debe mantenerse actualizada a medida que agregue nuevas características y funcionalidades a la extensión.  

Si proporcionas a Microsoft tu directiva de privacidad, aceptas permitir que Microsoft comparta dicha directiva de privacidad con los usuarios de tu extensión.  

#### <a name="153-sharing-data-with-third-parties"></a>1.5.3 Compartir datos con terceros  

Puede publicar la información personal de los usuarios de su extensión en un servicio externo o de terceros a través de la extensión o los metadatos asociados solo después de obtener el consentimiento de la suscripción de esos usuarios.  El consentimiento de participación significa que los usuarios conceden su permiso express en la interfaz de usuario de la extensión para la actividad solicitada, después de lo siguiente:  

*   Describir a los usuarios cómo se accede, usa o comparte la información e indica los tipos de partes a las que se divulga, y  
*   Proporcione a los usuarios un mecanismo en la interfaz de usuario de la extensión a través del cual tengan la opción de anular posteriormente el permiso y no participar.  
    
#### <a name="154-sharing-information-of-non-users"></a>1.5.4 Compartir información de usuarios no usuarios  

Si publica la información personal de una persona en un servicio externo o de terceros a través de la extensión o los metadatos, pero la persona cuya información se comparte no es un usuario de la extensión;  

1.  Debe obtener un consentimiento escrito explícito para publicar esa información personal.  
1.  Debe permitir que la persona cuya información se comparte retire ese consentimiento en cualquier momento.  
1.  Su directiva de privacidad debe revelar claramente que puede recopilar información personal de esta manera.  
1.  Si lo requiere la legislación aplicable, debe eliminar la información personal de cualquier persona a petición, incluidas las personas cuya información recopile de esta manera.  
1.  Si la extensión proporciona a los usuarios acceso a la información personal de otra persona, también se aplica este requisito.  
    
#### <a name="155-transmit-information-securely"></a>1.5.5 Transmitir información de forma segura  

Si la extensión recopila, almacena o transmite información personal; debe hacerlo de forma segura mediante métodos de criptografía modernos.  

#### <a name="156-highly-sensitive-information"></a>1.5.6 Información altamente confidencial  

La extensión no debe recopilar, almacenar o transmitir información personal altamente confidencial, como datos financieros o de salud, a menos que la información esté relacionada con la funcionalidad de la extensión.  La extensión también debe obtener el consentimiento expreso del usuario antes de recopilar, almacenar o transmitir dicha información.  

### <a name="16-permissions"></a>1.6 Permisos  

La extensión solo debe solicitar los permisos necesarios para funcionar.  Debe proporcionar una descripción de cómo funciona la extensión.  La extensión solo debe tener el rendimiento descrito.  Es posible que la extensión no solicite permiso para funciones que vayan más allá de las capacidades necesarias para realizar y funcionar como se ha declarado.  

### <a name="17-localization"></a>1.7 Localización  

Debe encontrar la extensión para todos los idiomas que la extensión dice admitir.  El texto de la descripción de la extensión debe localizarse en cada idioma que declare.  
Si la extensión está localizada de modo que algunas características no están disponibles en una versión localizada, debe especificar claramente o mostrar los límites de localización en la descripción de la extensión. La experiencia proporcionada por una extensión debe ser razonablemente similar en todos los idiomas que admite.  

### <a name="18-financial-transactions"></a>1.8 Transacciones financieras  

Si el producto incluye compras desde el producto, suscripciones, moneda virtual, funcionalidad de facturación o captura información financiera; se aplican los requisitos de las secciones siguientes.  

#### <a name="181-paid-features"></a>1.8.1 Características de pago  

La extensión puede permitir a los usuarios consumir contenido digital o servicios comprados a través de un mecanismo o API de compra de terceros.  

Debe usar una API de compra segura de terceros para las compras de bienes o servicios físicos.  Debe usar una API de compra de terceros segura para los pagos realizados en relación con cualquier otro servicio, incluidos los juegos de azar del mundo real o las contribuciones caritativas.  

*   Si la extensión se usa para facilitar o recopilar contribuciones caritativas o para llevar a cabo un sorteo o un concurso promocional, debe hacerlo de acuerdo con la legislación aplicable.  
*   También debe especificar claramente que Microsoft no es el patrocinador o recaudador de fondos de la promoción.  
*   Las ofertas desde el producto que se venden en la extensión no deben convertirse a ninguna moneda válida legalmente \(como USD, Euro, y así sucesivamente\) ni a ningún producto o servicio físico.  
    
Los siguientes requisitos se aplican al uso de una API de compra segura de terceros:  

*   En el momento de la transacción o cuando recopila información financiera o de pago del usuario; la extensión debe identificar el proveedor de transacciones comerciales, autenticar al usuario y obtener la confirmación del usuario para la transacción.  Un proveedor de transacciones comerciales mantiene una plataforma segura para los intercambios financieros.  
*   La extensión puede ofrecer a los usuarios la capacidad de guardar esta autenticación, pero los usuarios deben tener la capacidad de requerir una autenticación en cada transacción o desactivar las transacciones dentro del producto.  
*   Si su extensión recopila información de tarjeta de crédito o usa un procesador de pagos de terceros que recopila información de tarjeta de crédito, el procesamiento de pagos debe cumplir con el estándar de seguridad de datos PCI actual \(PCI DSS\).  
    
#### <a name="182-disclosing-paid-features"></a>1.8.2 Revelar características de pago  

La extensión y los metadatos asociados deben proporcionar información sobre los tipos de compras en el producto ofrecidas y el rango de precios.  No debe engañar a los usuarios y debe tener claro la naturaleza de las promociones y ofertas del producto, incluidos el ámbito y los términos de las experiencias de prueba.  Si la extensión restringe el acceso al contenido creado por el usuario durante o después de una prueba, debe notificar a los usuarios con antelación.  Además, la extensión debe dejar claro a los usuarios que están iniciando una opción de compra en la extensión.  

### <a name="19-notifications"></a>1.9 Notificaciones  

La extensión debe respetar la configuración del sistema para las notificaciones.  Esto significa que cualquier presentación de anuncios y notificaciones a los usuarios debe ser coherente con las preferencias del usuario, independientemente de si las notificaciones las proporciona el Servicio de notificaciones push de Microsoft \(MPNS\), el servicio de notificación de inserción Windows \(WNS\) o cualquier otro servicio.  Si el usuario deshabilita las notificaciones, ya sea en un producto específico o en todo el sistema, la extensión debe permanecer funcional.  

Si el producto usa MPNS o WNS para transmitir notificaciones, debe cumplir los siguientes requisitos:  

#### <a name="191-general-guidance"></a>1.9.1 Guía general  

Las notificaciones proporcionadas a través de WNS o MPNS se consideran contenido del producto y están sujetas a todas las directivas de desarrollador del Catálogo de complementos.  

#### <a name="192-ownership-of-notifications"></a>1.9.2 Propiedad de las notificaciones  

No debe ocultar ni tratar de ocultar el origen de ninguna notificación iniciada desde la extensión.  

#### <a name="193-no-confidential-or-sensitive-information"></a>1.9.3 Sin información confidencial o confidencial  

No debe incluir en una notificación ninguna información que los usuarios puedan considerar razonablemente confidencial o confidencial.  

#### <a name="194-purpose-of-notifications"></a>1.9.4 Propósito de las notificaciones  

Las notificaciones enviadas desde la extensión deben estar relacionadas Microsoft Edge con esa extensión o con otras extensiones que publique en un almacén de complementos y no deben incluir mensajes promocionales de ningún tipo que no estén relacionados con las extensiones.  

### <a name="110-advertising-conduct-and-content"></a>1.10 Contenido y conducta publicitaria  

Para todas las actividades relacionadas con la publicidad, se aplican los siguientes requisitos:  

#### <a name="1101-purpose"></a>1.10.1 Propósito  

El contenido principal de la extensión no debe ser publicidad y la publicidad debe distinguirse claramente de otro contenido de la extensión.  

#### <a name="1102-policies-and-agreements"></a>1.10.2 Directivas y acuerdos  

Cualquier contenido de publicidad que muestre la extensión debe cumplir con [la Directiva de aceptación creativa de Microsoft][MicrosoftAdvertisingCreativeAcceptancePolicies].  
Si la extensión muestra anuncios, todo el contenido mostrado debe cumplir los requisitos de publicidad del [Contrato][MicrosoftAppDeveloperAgreement] de desarrollador de aplicaciones y esta directiva.  

#### <a name="1103-quality-of-advertising"></a>1.10.3 Calidad de la publicidad  

*   El propósito principal de la extensión no debe ser que los usuarios puedan hacer clic en anuncios.  
*   La extensión no debe hacer nada que interfiera o disminuya la visibilidad, el valor o la calidad de los anuncios que muestra.  

#### <a name="1104-promotions"></a>1.10.4 Promociones  

Si compras o creas campañas de anuncios promocionales para promover tus extensiones a través de la funcionalidad de la campaña publicitaria en el Centro de [partners,][MicrosoftPartnerCenter]todos los materiales de anuncios que proporciones a Microsoft, incluidas las páginas de aterrizaje asociadas, deben cumplir con la Directiva de especificaciones creativas de [Microsoft][MicrosoftAdvertisingCreativeSpecifications] y la Directiva de aceptación creativa de [Microsoft][MicrosoftAdvertisingCreativeAcceptancePolicies].  

#### <a name="1105-notifying-users-of-opt-out-for-interest-based-advertising"></a>1.10.5 Notificar a los usuarios de Opt-Out para Interest-Based publicidad  

La declaración de privacidad o los términos de uso deben permitir a los usuarios saber que planea enviar información personal al proveedor de servicios de anuncios y deben saber a los usuarios cómo pueden optar por no participar en la publicidad basada en intereses.  

#### <a name="1106-other-guidelines"></a>1.10.6 Otras directrices  

Si la extensión se dirige a niños menores de 13 años, tal como se define en la Ley de protección de privacidad en línea de [los niños][FTCChildrensPrivacy]; debes notificar a Microsoft este hecho en el [Centro][MicrosoftPartnerCenter] de partners y asegurarte de que todo el contenido de anuncios que se muestra en la extensión es adecuado para los niños menores de 13 años.  

## <a name="2-content-policies"></a>2 Directivas de contenido  

Las siguientes directivas se aplican al contenido y los metadatos \(incluyendo nombre del editor, nombre de extensión, icono de extensión, descripción de extensión, capturas de pantalla de extensión, tráileres de extensión y miniaturas de tráiler, y cualquier otro metadato de extensión\) ofrecido para su distribución en Microsoft Edge Complementos.  El contenido significa las imágenes, sonidos, vídeos y texto contenidos en la extensión, los iconos, las notificaciones, los mensajes de error o los anuncios expuestos a través de la extensión, y todo lo que se entregue desde un servidor o al que se conecte la extensión.  Dado que las extensiones y Microsoft Edge complementos se usan en todo el mundo, estos requisitos se interpretan y se aplican en el contexto de las normas regionales y culturales.  

### <a name="21-content-requirements-for-microsoft-edge-addon-catalog-listing"></a>2.1 Requisitos de contenido para Microsoft Edge catálogo de complementos  

Es posible que los metadatos y otros contenidos que envíes para que acompañen a la extensión no contengan contenido maduro.  
Los envíos que no cumplen los Microsoft Edge de listas de la tienda de complementos se rechazan o se quitan rápidamente.  

### <a name="22-content-including-names-logos-original-and-third-party"></a>2.2 Contenido incluidos nombres, logotipos, originales y de terceros  

Todo el contenido de la extensión y los metadatos asociados deben ser creados originalmente por el usuario o con licencia adecuada de un titular de derechos de terceros y deben usarse solo según lo permita el titular de los derechos o según lo permita la ley.  

### <a name="23-risk-of-harm"></a>2.3 Riesgo de daño  

#### <a name="231-requirements"></a>2.3.1 Requisitos  

La extensión no debe contener ningún contenido que facilite o glamorice las siguientes actividades del mundo real: \(a\) violencia extrema o gratuita; \(b\) violaciones de derechos humanos; \(c\) la creación de armas ilegales; o \(d\) el uso de armas contra una persona, un animal o una propiedad real o personal.  

#### <a name="232-responsibility"></a>2.3.2 Responsabilidad  

La extensión no debe: \(a\) representar un riesgo de seguridad para, ni provocar molestias, daños o cualquier otro daño para los usuarios finales o para cualquier otra persona o animal; o \(b\) suponen un riesgo de daños a la propiedad real o personal o que se den como resultado.  Usted es el único responsable de todas las pruebas de seguridad de extensión, la adquisición de certificados y la implementación de las protecciones de características adecuadas.  No debe deshabilitar ninguna característica de seguridad o comodidad de la plataforma y debe incluir todas las advertencias, avisos y declinaciones de responsabilidades legales aplicables y estándares del sector en su extensión.  

### <a name="24-defamatory-libelous-slanderous-and-threatening"></a>2.4 Difamatorio, Difamatorio, Calumnioso y Amenazante  

La extensión no debe contener contenido difamatorio, calumnioso, calumnioso o amenazante.  

### <a name="25-offensive-content"></a>2.5 Contenido ofensivo  

La extensión y los metadatos asociados no deben contener contenido potencialmente confidencial u ofensivo.  El contenido puede considerarse confidencial u ofensivo en determinados países o regiones debido a las leyes locales o las normas culturales.  Además, la extensión y los metadatos asociados no deben contener contenido que profiera discriminación, odio o violencia en función de consideraciones de raza, origen étnico, origen nacional, idioma, género, edad, discapacidad, religión, orientación sexual, condición de veterano o pertenencia a cualquier otro grupo social.  

### <a name="26-alcohol-tobacco-and-drugs"></a>2.6 Alcohol, Tabaquismo y Drogas  

La extensión no debe contener ningún contenido que facilite o glamorice el uso excesivo o irresponsable de productos o drogas de alcohol o de tabaquismo.  

### <a name="27-adult-content"></a>2.7 Contenido para adultos  

La extensión no debe contener ni mostrar contenido que una persona razonable considere pornográfica o sexualmente explícita.  

### <a name="28-prohibited-content-services-and-activity"></a>2.8 Contenido, servicios y actividad prohibidos  

La extensión debe cumplir las siguientes condiciones.  

*   La extensión no debe contener contenido ni proporcionar servicios que faciliten el juego en línea.  El juego en línea incluye, entre otros, los casinos en línea, las apuestas deportivas, las loterías o los juegos de habilidad que ofrecen premios en efectivo u otro valor.  
*   La extensión no debe proporcionar acceso no autorizado al contenido del sitio web, por ejemplo, eludiendo los paneles de pago o las restricciones de inicio de sesión.  
*   La extensión no debe proporcionar, fomentar ni habilitar el acceso no autorizado, la descarga o la transmisión de contenido o medios con derechos de autor.  
*   La extensión no debe extraer criptodivisa.  
    
### <a name="29-illegal-activity"></a>2.9 Actividad ilegal  

La extensión no debe contener contenido ni funcionalidad que fomente, facilite o glamorice la actividad ilegal en el mundo real.  

### <a name="210-excessive-profanity-and-inappropriate-content"></a>2.10 Exceso de profanidad y contenido inadecuado  

*   La extensión no debe contener una profanidad excesiva o gratuita.  
*   La extensión no debe contener ni mostrar contenido que una persona razonable considere obsceno.  
    
### <a name="211-countryregion-specific-requirements"></a>2.11 Requisitos específicos de país o región  

No se permite el contenido ofensivo en cualquier país o región al que esté dirigida la extensión.  El contenido puede considerarse ofensivo en determinados países o regiones debido a las leyes locales o las normas culturales.  Algunos ejemplos de contenido potencialmente ofensivo en determinados países o regiones son los siguientes:  

**China**  

*   Contenido sexual prohibido  
*   Referencias a territorios o regiones en disputa  
*   Proporcionar o habilitar el acceso a contenido o servicios que son ilegales según la legislación local aplicable  
    
### <a name="212-age-ratings"></a>2.12 Clasificaciones por edades  

#### <a name="2121-mature-content"></a>2.12.1 Contenido maduro  

Al enviar la extensión al [Centro de partners,][MicrosoftPartnerCenter]debe indicar si la extensión muestra contenido que debe estar marcado como "Maduro".  Al determinar la clasificación de la extensión, tenga en cuenta todo el contenido de la aplicación, incluido el contenido generado por el usuario y los anuncios, y el contenido que vincula la extensión.  Si indicas que la extensión no contiene contenido "Maduro", eres responsable de mantener la precisión de esta clasificación.  Independientemente de la clasificación dada a la extensión, debe cumplir todos los requisitos de contenido de Microsoft Edge de desarrolladores de complementos  

#### <a name="2122-ratings-change"></a>2.12.2 Cambio de clasificación  

Si la extensión proporciona contenido \(como generado por el usuario, comercial u otro contenido basado en web\) que puede ser adecuado para una clasificación de antigüedad superior a la clasificación asignada, debe exigir a los usuarios que opten por recibir dicho contenido mediante un filtro de contenido o iniciando sesión con una cuenta preexistnte.  

### <a name="213-videos"></a>2.13 Vídeos  

Si envías un vídeo promocional en la descripción, debe seguir todas las directrices de contenido mencionadas en esta directiva.  Si eliges proporcionar un vínculo de YouTube, debes asegurarte de que los anuncios estén desactivados para los vídeos específicos que quieras insertar.  Para obtener más información sobre cómo activar o [][GoogleYoutubeAnswer2531367Topic7072227] desactivar anuncios en YouTube, ve a Establecer los formatos de anuncio predeterminados y [Anuncios en vídeos incrustados.][GoogleYoutubeAnswer132596]


## <a name="certification-appeal-process"></a>Proceso de apelación de certificación

Todas las extensiones deben cumplir con las directivas de almacén enumeradas anteriormente. Si la extensión ha fallado en el proceso de revisión, revise las directivas de almacén para comprender el motivo del error. Después de enviar la extensión mediante el Centro de partners, para hacer una pregunta sobre el estado de revisión o certificación de la misma, vaya a [Nueva][MicrosoftSupportSupportrequestformE7a381be9c9aFafbEd76262bc93fd9e4] solicitud de soporte técnico y complete el formulario.

### <a name="microsoft-edge-add-ons-appeal-statistics-for-fy2021"></a>Microsoft Edge Estadísticas de atractivo de complementos para FY2021

| Tipo de queja principal #1: Recurso de cumplimiento | Tipo de queja principal #2: Resultados de certificación | Otros tipos de quejas | Quejas totales | Quejas anuladas |
|:--- |:--- |
| 8 | 2 | 4 | 14 | 0 |


<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Relajación de la directiva predeterminada: directiva de seguridad de contenido \(CSP\) | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "App Developer Agreement | Microsoft Docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Cómo Identifica Microsoft malware y aplicaciones potencialmente no deseadas | Microsoft Docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Establecer los formatos de anuncio predeterminados: Ayuda de YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anuncios en vídeos incrustados: Ayuda de YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Privacidad de los niños - Comisión Federal de Comercio"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Directivas de aceptación creativas: Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Especificaciones creativas: Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  

[MicrosoftSupportSupportrequestformE7a381be9c9aFafbEd76262bc93fd9e4]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensiones Nueva solicitud de | Soporte técnico de Microsoft"