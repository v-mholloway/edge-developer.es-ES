---
description: Directivas para desarrolladores del tienda de complementos de Microsoft Edge
title: Directivas para desarrolladores del tienda de complementos de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: cc34a95e08d01ebee54581222d0eb9fefa3dc458
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343083"
---
# Directivas para desarrolladores del tienda de complementos de Microsoft Edge  

## Introducción y objetivo de este documento  

Gracias por su interés en desarrollar extensiones para la tienda de complementos de Microsoft Edge.  Las directivas de desarrollador de la tienda de complementos de Microsoft Edge \(Directivas de desarrollador de [][MicrosoftPartnerCenter] la tienda de complementos\) se aplican a las extensiones, incluido el envío de extensiones a través del Centro de partners y el aprovisionamiento de dichas extensiones a través de los complementos de Microsoft Edge.  

## Principios  

Algunos principios para empezar:  

*   Debes ofrecer un valor único y distinto dentro de las extensiones para Microsoft Edge.  Proporciona una razón atractiva para descargar las extensiones de la Tienda de complementos de Microsoft Edge \(Complementos de Microsoft Edge\).  
*   No debe confundir a nuestros usuarios conjuntos sobre lo que hace su extensión, quién la ofrece, y así sucesivamente.  
*   No debe intentar engañar a los usuarios, el sistema o el ecosistema.  No hay lugar en nuestros complementos de Microsoft Edge para ningún tipo de fraude; ya sea la manipulación de clasificaciones y revisión, el fraude con tarjetas de crédito u otra actividad fraudulenta.  
    
El cumplimiento de las directivas de desarrollador de la tienda de complementos de Microsoft Edge debe ayudarte a tomar decisiones que mejoren el atractivo y el público de tu extensión.  

Las extensiones son fundamentales para la experiencia de cientos de millones de usuarios.  Esperamos experimentar lo que creas y estamos encantados de ayudar a ofrecer tus extensiones al mundo.  

## 1. Directivas de producto  

### 1.1 Función distinta & valor; Representación precisa  

La extensión y los metadatos asociados deben reflejar de forma precisa y clara el origen, la funcionalidad y las características que describa.  

#### 1.1.1 Las extensiones deben tener un único propósito  

La extensión debe tener un único propósito con funcionalidad limitada.  

#### 1.1.2 Describir la extensión  

Todos los aspectos de la extensión deben describir con precisión las funciones, características y cualquier limitación importante de la extensión, incluidos los dispositivos de entrada necesarios o compatibles.  La propuesta de valor de la extensión debe ser clara durante la primera ejecución.  Es posible que la extensión no use un nombre o icono similar al de otras extensiones, y no debe reclamar que represente a una empresa, un organismo gubernamental u otra entidad si no tiene permiso para hacer esa representación.  

#### 1.1.3 Funcionalidad  

La extensión debe ser totalmente funcional.  

#### 1.1.4 Búsqueda y detección  

Los términos de búsqueda no pueden superar los siete términos únicos y deben ser relevantes para la extensión.  

#### 1.1.5 Proporcionar los detalles adecuados  

Debes proporcionar detalles distintos e informativos sobre la extensión y la funcionalidad en la lista \(metadata\) de la extensión.  La extensión debe proporcionar una experiencia de usuario valiosa y de calidad.  La extensión también debe tener una presencia activa en los complementos de Microsoft Edge.  

#### 1.1.6 Estabilidad y rendimiento  

La extensión no debe afectar negativamente al rendimiento o la estabilidad de Microsoft Edge.  

#### 1.1.7 Ofuscación  

No se permiten las extensiones con código ofuscado.  Esto incluye código dentro del paquete de extensión, así como cualquier código externo o recurso obtenido de la web.  Es posible que se te pida que refactorices partes del código si no se pueden revisar.  

#### 1.1.8 Modificar la configuración del explorador  

La extensión no debe, sin el consentimiento del usuario adecuado, modificar o parecer que altera, la funcionalidad o la configuración del explorador, incluidos, entre otros: el proveedor y sugerencias de búsqueda de la barra de direcciones, la página de inicio o inicio, la página de la nueva pestaña y agregar o quitar favoritos.  

Cualquier modificación de la configuración del explorador debe estar explícitamente documentada en la descripción de la extensión.  

La extensión solo puede revisar la configuración clave para reemplazar una página web o un servicio de Microsoft por el de un tercero \(por ejemplo, requerir el uso de un motor de búsqueda de terceros o establecer la página principal en una propiedad web de terceros\) si está empleado o asociado a dicho tercero.  

### 1.2 Seguridad  

La extensión no debe poner en peligro ni poner en peligro la seguridad del usuario, ni la seguridad o la funcionalidad del dispositivo, el sistema o los sistemas relacionados.  

#### 1.2.1 Directivas de seguridad de contenido  

> [!NOTE]
> Si realiza cambios en la extensión más allá de la funcionalidad descrita, cualquier cambio en el código debe cumplir con la directiva de seguridad de contenido [de Microsoft Edge.][MicrosoftEdgeContentSecurityPolicyRemoteScript]  Por ejemplo, la extensión no debe descargar un script remoto y, posteriormente, ejecutarlo de forma que no sea coherente con la funcionalidad descrita.  

#### 1.2.2 Software no deseado y malintencionado  

La extensión no debe contener ni habilitar el malware según los criterios de Microsoft para el [software no deseado y malintencionado.][MicrosoftIdentifiesMalwareUnwantedApplications]  

#### 1.2.3 Dependencia de otro software  

La extensión puede depender de software no integrado \(como otro producto, módulo o servicio\) para ofrecer la funcionalidad principal, siempre que divulgues la dependencia en la descripción.  

#### 1.2.4 Actualización de extensiones  

A menos que Microsoft permita lo contrario, las extensiones solo deben actualizarse a través de complementos de Microsoft Edge.  

### 1.3 El producto se puede probar  

La extensión debe poder probarse.  Si no es posible probar la extensión por cualquier motivo, incluidos, entre otros, los elementos siguientes, la extensión puede no cumplir este requisito.  

#### 1.3.1 Credenciales de usuario  

Si la extensión requiere credenciales de inicio de sesión, proporcione una cuenta de demostración de trabajo con el `Notes for certification` campo.  

#### 1.3.2 Disponibilidad de servicios  

Si la extensión requiere acceso a un servidor, el servidor debe ser funcional para comprobar que funciona correctamente.  

### 1.4 Facilidad de uso  

La extensión debe cumplir con los estándares de la tienda de complementos de Microsoft Edge para su uso, incluidos, entre otros, los que se enumeran en las subsecciones siguientes.  

#### 1.4.1 Compatibilidad entre plataformas  

La extensión debe ser compatible con Microsoft Edge en todos los dispositivos y plataformas en los que se pueden descargar.  Si una extensión se descarga en un dispositivo con el que no es compatible, debe detectarla al iniciarse y mostrar un mensaje al usuario detallando los requisitos que los dispositivos deben cumplir para ser compatibles con la extensión.  

#### 1.4.2 Experiencia del usuario  

La extensión debe iniciarse rápidamente y debe responder a las entradas del usuario.  La extensión debe seguir funcionando y seguir respondiendo a las entradas del usuario.  La extensión debe cerrarse correctamente y no cerrarse inesperadamente.  La extensión debe controlar las excepciones y seguir respondiendo a la entrada del usuario después de controlar la excepción.  

### 1.5 Información personal  

Los siguientes requisitos se aplican a las extensiones que tienen acceso a información personal.  La información personal incluye toda la información o los datos que identifican o pueden usarse para identificar a una persona, o que están asociados a dicha información o datos.  

#### 1.5.1 Recopilar información personal solo cuando sea necesario  

La extensión puede recopilar, obtener acceso, usar o transmitir información personal \(incluida la actividad de exploración web\); solo si lo requiere y solo para su uso en una característica destacada y orientada al usuario.  

#### 1.5.2 Mantener una directiva de privacidad  

Independientemente de si la extensión accede, recopila o transmite información personal; debe proporcionar un aviso destacado y cumplir con su directiva de privacidad si lo requiere la ley.  Su directiva de privacidad debe informar a los usuarios de la información personal a la que se accede, recopila o transmite mediante su extensión, cómo se usa, almacena y protege esa información, e indica los tipos de partes a las que se divulga.  La directiva de privacidad debe describir los controles que los usuarios tienen sobre el uso y el uso compartido de su información, cómo acceden a su información y debe cumplir con las leyes y normativas aplicables.  La directiva de privacidad debe mantenerse actualizada a medida que agregue nuevas características y funcionalidades a la extensión.  

Si proporcionas a Microsoft la directiva de privacidad, aceptas permitir que Microsoft comparta dicha directiva de privacidad con los usuarios de tu extensión.  

#### 1.5.3 Compartir datos con terceros  

Puede publicar la información personal de los usuarios de su extensión en un servicio externo o de terceros a través de la extensión o los metadatos asociados solo después de obtener el consentimiento para participar de esos usuarios.  El consentimiento de participación significa que los usuarios conceden su permiso explícito en la interfaz de usuario de la extensión para la actividad solicitada, después de:  

*   Describir a los usuarios cómo se accede a la información, cómo se usa o se comparte, e indicar los tipos de partes a las que se divulga, y  
*   Proporcione a los usuarios un mecanismo en la interfaz de usuario de la extensión a través del cual tengan la opción de rescindir más adelante el permiso y no participar.  
    
#### 1.5.4 Compartir información de usuarios no usuarios  

Si publica la información personal de una persona a un servicio externo o a un tercero a través de la extensión o los metadatos, pero la persona cuya información se comparte no es un usuario de su extensión;  

1.  Debe obtener su consentimiento por escrito para publicar esa información personal.  
1.  Debe permitir que la persona cuya información se comparte retire ese consentimiento en cualquier momento.  
1.  Su directiva de privacidad debe revelar claramente que puede recopilar información personal de esta manera.  
1.  Si lo requiere la legislación aplicable, debe eliminar la información personal de cualquier persona a petición, incluidas las personas cuya información recopile de esta manera.  
1.  Si la extensión proporciona a los usuarios acceso a la información personal de otra persona, también se aplica este requisito.  
    
#### 1.5.5 Transmitir información de forma segura  

Si la extensión recopila, almacena o transmite información personal; debe hacerlo de forma segura mediante el uso de métodos de criptografía modernos.  

#### 1.5.6 Información altamente confidencial  

La extensión no debe recopilar, almacenar ni transmitir información personal altamente confidencial, como datos financieros o de salud, a menos que la información esté relacionada con la funcionalidad de la extensión.  La extensión también debe obtener el consentimiento explícito del usuario antes de recopilar, almacenar o transmitir dicha información.  

### 1.6 Permisos  

La extensión solo debe solicitar los permisos necesarios para funcionar.  Debe proporcionar una descripción de cómo funciona la extensión.  La extensión solo debe tener el rendimiento descrito.  Es posible que la extensión no solicite permiso para funcionalidades que vayan más allá de las capacidades necesarias para realizar y funcionar como se ha declarado.  

### 1.7 Localización  

Debe localiza la extensión para todos los idiomas que la extensión dice admitir.  El texto de la descripción de la extensión debe localizarse en cada idioma que declares.  
Si la extensión está localizada de modo que algunas características no están disponibles en una versión localizada, debes especificar claramente o mostrar los límites de localización en la descripción de la extensión. La experiencia proporcionada por una extensión debe ser razonablemente similar en todos los idiomas que admite.  

### 1.8 Transacciones financieras  

Si el producto incluye compras desde el producto, suscripciones, moneda virtual, funcionalidad de facturación o captura información financiera; se aplican los requisitos de las secciones siguientes.  

#### 1.8.1 Características de pago  

La extensión puede permitir a los usuarios consumir contenido digital o servicios comprados a través de un mecanismo de compra de terceros o API.  

Debe usar una API de compra segura de terceros para las compras de bienes o servicios físicos.  Debe usar una API de compra de terceros segura para los pagos realizados en relación con cualquier otro servicio, incluidos los juegos de azar reales o las contribuciones caritativas.  

*   Si la extensión se usa para facilitar o recopilar contribuciones caritativas o para llevar a cabo un barrido promocional o un certamen, debes hacerlo en cumplimiento de la legislación aplicable.  
*   También debe especificar claramente que Microsoft no es el patrocinador o el patrocinador de la promoción.  
*   Las ofertas desde el producto vendidas en la extensión no deben convertirse a ninguna moneda válida legalmente \(como USD, Euro, entre otros\) ni a ningún bien físico o servicio.  
    
Los siguientes requisitos se aplican al uso de una API de compra segura de terceros:  

*   En el momento de la transacción o cuando se recopila información financiera o de pago del usuario; la extensión debe identificar al proveedor de transacciones comerciales, autenticar al usuario y obtener la confirmación del usuario para la transacción.  Un proveedor de transacciones comerciales mantiene una plataforma segura para los intercambios financieros.  
*   La extensión puede ofrecer a los usuarios la capacidad de guardar esta autenticación, pero los usuarios deben tener la capacidad de requerir una autenticación en cada transacción o desactivar las transacciones del producto.  
*   Si la extensión recopila información de tarjetas de crédito o usa un procesador de pagos de terceros que recopila información de tarjetas de crédito, el procesamiento de pagos debe cumplir con el estándar de seguridad de datos PCI \(PCI DSS\) actual.  
    
#### 1.8.2 Divulgación de características de pago  

La extensión y los metadatos asociados deben proporcionar información sobre los tipos de compras desde el producto ofrecidas y la gama de precios.  No debe engañar a los usuarios y debe tener claro la naturaleza de las promociones y ofertas del producto, incluido el ámbito y los términos de las experiencias de prueba.  Si la extensión restringe el acceso al contenido creado por el usuario durante o después de una prueba, debe notificar a los usuarios por adelantado.  Además, la extensión debe dejar claro a los usuarios que están iniciando una opción de compra en la extensión.  

### 1.9 Notificaciones  

La extensión debe respetar la configuración del sistema para las notificaciones.  Esto significa que cualquier presentación de anuncios y notificaciones para los usuarios debe ser coherente con las preferencias del usuario, independientemente de si las notificaciones las proporciona el servicio de notificaciones de inserción de Microsoft \(MPNS\), el servicio de notificaciones de inserción de Windows \(WNS\) o cualquier otro servicio.  Si el usuario deshabilita las notificaciones, ya sea por producto específico o por todo el sistema, la extensión debe seguir funcionando.  

Si el producto usa MPNS o WNS para transmitir notificaciones, debe cumplir los siguientes requisitos:  

#### 1.9.1 Guía general  

Las notificaciones proporcionadas a través de WNS o MPNS se consideran contenido del producto y están sujetas a todas las directivas de desarrollador del catálogo de complementos.  

#### 1.9.2 Propiedad de las notificaciones  

No debes ocultar ni intentar ocultar el origen de las notificaciones iniciadas desde la extensión.  

#### 1.9.3 Sin información confidencial o confidencial  

No debe incluir en una notificación ninguna información que los usuarios puedan considerar razonablemente confidencial o confidencial.  

#### 1.9.4 Finalidad de las notificaciones  

Las notificaciones enviadas desde la extensión deben estar relacionadas con esa extensión o con otras extensiones que publiques en la tienda de complementos de Microsoft Edge y no deben incluir mensajes promocionales de ningún tipo que no estén relacionados con las extensiones.  

### 1.10 Conducta y contenido de publicidad  

Para todas las actividades relacionadas con la publicidad, se aplican los siguientes requisitos:  

#### 1.10.1 Propósito  

El contenido principal de la extensión no debe ser publicidad y la publicidad debe distinguirse claramente de otro contenido de la extensión.  

#### 1.10.2 Directivas y acuerdos  

Cualquier contenido de publicidad que muestre la extensión debe cumplir con la [Directiva de aceptación creadora de Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  
Si la extensión muestra anuncios, todo el contenido mostrado debe cumplir los requisitos de publicidad del Acuerdo para desarrolladores de aplicaciones [y][MicrosoftAppDeveloperAgreement] esta directiva.  

#### 1.10.3 Calidad de la publicidad  

*   El propósito principal de la extensión no debe ser que los usuarios puedan hacer clic en anuncios.  
*   La extensión no debe hacer nada que interfiera o disminuya la visibilidad, el valor o la calidad de los anuncios que muestra.  

#### 1.10.4 Promociones  

Si compras o creas campañas de anuncios promocionales para promocionar tus extensiones a través de la funcionalidad de campaña publicitaria en el Centro de [partners,][MicrosoftPartnerCenter]todos los materiales de anuncios que proporciones a Microsoft, incluidas las páginas de aterrizaje asociadas, deben cumplir con la Directiva de especificaciones creativos de [Microsoft][MicrosoftAdvertisingCreativeSpecifications] y la Directiva de aceptación creadora de [Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  

#### 1.10.5 Notificar a los usuarios Opt-Out para Interest-Based Publicidad  

La declaración de privacidad o los términos de uso deben permitir a los usuarios saber que tienes previsto enviar información personal al proveedor de servicios de anuncios y deben decir a los usuarios cómo pueden optar por no participar en la publicidad basada en intereses.  

#### 1.10.6 Otras directrices  

Si la extensión se dirige a niños menores de 13 años, tal como se define en la Ley de protección de privacidad en línea de los [niños;][FTCChildrensPrivacy] Debes notificar a Microsoft [][MicrosoftPartnerCenter] este hecho en el Centro de partners y asegurarte de que todo el contenido de anuncios que se muestra en la extensión es adecuado para los niños menores de 13 años.  

## 2 Directivas de contenido  

Las siguientes directivas se aplican al contenido y a los metadatos \(incluido el nombre del editor, el nombre de extensión, el icono de extensión, la descripción de la extensión, las capturas de pantalla de extensión, los tráileres de extensión y las miniaturas de tráiler, y cualquier otro metadato de extensión\) que se ofrece para su distribución en complementos de Microsoft Edge.  El contenido significa las imágenes, sonidos, vídeos y texto contenidos en la extensión, los iconos, las notificaciones, los mensajes de error o los anuncios expuestos a través de la extensión, y todo lo que se entregue desde un servidor o al que se conecte la extensión.  Dado que las extensiones y los complementos de Microsoft Edge se usan en todo el mundo, estos requisitos se interpretan y se aplican en el contexto de las normas regionales y culturales.  

### 2.1 Requisitos de contenido para la descripción del catálogo de complementos de Microsoft Edge  

Es posible que los metadatos y otros contenidos que envíe para que acompañen a la extensión no contengan contenido para adultos.  
Los envíos que no cumplen con los requisitos de las de listas de la tienda de complementos de Microsoft Edge se rechazan o se eliminan rápidamente.  

### 2.2 Contenido incluidos nombres, logotipos, originales y de terceros  

Todo el contenido de la extensión y los metadatos asociados deben ser creados originalmente por el usuario o con una licencia adecuada de un titular de derechos de terceros y deben usarse solo según lo permita el titular de los derechos o según lo permita la ley.  

### 2.3 Riesgo de daños  

#### 2.3.1 Requisitos  

La extensión no debe contener ningún contenido que facilite o consorice las siguientes actividades reales: \(a\) violencia extrema o gratuita; \(b\) violaciones de derechos humanos; \(c\) la creación de armas ilegales; o \(d\) el uso de armas contra una persona, individuo o propiedad real o personal.  

#### 2.3.2 Responsabilidad  

La extensión no debe: \(a\) suponer un riesgo para la seguridad, ni causar molestias, daños o cualquier otro daño a los usuarios finales o a cualquier otra persona o persona; o \(b\) suponen un riesgo o resultan en daños a la propiedad real o personal.  Eres el único responsable de todas las pruebas de seguridad de extensiones, la adquisición de certificados y la implementación de las protecciones de características adecuadas.  No debe deshabilitar ninguna característica de seguridad o comodidad de la plataforma y debe incluir todas las advertencias, avisos y avisos estándar del sector aplicables en su extensión.  

### 2.4 Defamatory, Libelous, Slanderous, and Defamatory  

La extensión no debe contener ningún contenido que sea calumnioso, calumnioso o calumnioso.  

### 2.5 Contenido ofensivo  

La extensión y los metadatos asociados no deben contener contenido potencialmente confidencial o ofensivo.  El contenido puede considerarse confidencial o ofensivo en determinados países o regiones debido a leyes locales o normas culturales.  Además, la extensión y los metadatos asociados no deben contener contenido que profiera la discriminación, el acoso o la violencia en función de las consideraciones de carrera, etnicidad, origen nacional, idioma, género, edad, discapacidad, sexo, orientación sexual, estado como un mayores o pertenencia a cualquier otro grupo social.  

### 2.6 Consumo de alcohol, tabacalera y drogas  

La extensión no debe contener ningún contenido que facilite o consorte el uso excesivo o irresponsable de consumo excesivo o irresponsable de consumo de alcohol, productos de tabacalera o drogas.  

### 2.7 Contenido para adultos  

La extensión no debe contener ni mostrar contenido que una persona razonable consideraría explícita sexual o fonográfica.  

### 2.8 Contenido, servicios y actividad prohibidos  

La extensión debe cumplir las siguientes condiciones.  

*   La extensión no debe contener contenido ni proporcionar servicios que faciliten el juego en línea.  Las partidas en línea incluyen, entre otras cosas, juegos en línea, actividades deportivas, lonjas o juegos de habilidades que ofrecen reembolsos de dinero en efectivo u otro valor.  
*   La extensión no debe proporcionar acceso no autorizado al contenido del sitio web, por ejemplo, sorteando los paneles de pago o las restricciones de inicio de sesión.  
*   La extensión no debe proporcionar, fomentar ni habilitar el acceso, descarga o transmisión no autorizados de contenido o medios protegidos por derechos de autor.  
*   La extensión no debe extraer una criptodivisa.  
    
### 2.9 Actividad ilegal  

La extensión no debe contener contenido o funcionalidad que fomente, facilite o anime actividades ilegales en el mundo real.  

### 2.10 Contenido excesivo de blasfismo e inapropiado  

*   La extensión no debe contener una blasfedad excesiva o gratuita.  
*   La extensión no debe contener ni mostrar contenido que una persona razonable considere obscenas.  
    
### 2.11 Requisitos específicos de país o región  

No se permite el contenido ofensivo en cualquier país o región al que esté destinada la extensión.  El contenido puede considerarse ofensivo en determinados países o regiones debido a leyes locales o normas culturales.  Entre los ejemplos de contenido potencialmente ofensivo en determinados países o regiones se incluyen los siguientes:  

**China**  

*   Contenido sexual prohibido  
*   Referencias a territorios o regiones en disputa  
*   Proporcionar o habilitar el acceso a contenido o servicios que no son válidos según la legislación local aplicable  
    
### 2.12 Clasificaciones por edades  

#### 2.12.1 Contenido para adultos  

Al enviar la extensión al [Centro de][MicrosoftPartnerCenter]partners, debes indicar si la extensión muestra contenido que debe marcarse como "Madurez".  Al determinar la clasificación de la extensión, ten en cuenta todo el contenido de la aplicación, incluido el contenido y los anuncios generados por el usuario, y con el contenido que vincula la extensión.  Si indicas que la extensión no contiene ningún contenido "Madurez", eres responsable de mantener la precisión de esta clasificación.  Independientemente de la clasificación que se le da a la extensión, aún debe cumplir todos los requisitos de contenido de las directivas de desarrollador de complementos de Microsoft Edge  

#### 2.12.2 Cambio de clasificación  

Si tu extensión proporciona contenido \(como generado por el usuario, comercial u otro contenido basado en web\) que puede ser adecuado para una clasificación por edades superior a la clasificación asignada, debes requerir que los usuarios opten por recibir dicho contenido mediante un filtro de contenido o iniciando sesión con una cuenta preexistida.  

### 2.13 Vídeos  

Si envías un vídeo promocional en la descripción, debe seguir todas las directrices de contenido mencionadas en esta directiva.  Si decide proporcionar un vínculo de YouTube, debe asegurarse de que los anuncios están deshabilitados para los vídeos específicos que desea insertar.  Para obtener más información sobre cómo se habilitan y deshabilitan los anuncios en YouTube, consulta [support.google.com/youtube/answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] y [support.google.com/youtube/answer/132596][GoogleYoutubeAnswer132596].  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Resalte la directiva predeterminada: Directiva de seguridad de contenido \(CSP\) | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Acuerdo para desarrolladores de aplicaciones | Microsoft Docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Cómo Microsoft identifica el malware y las aplicaciones potencialmente no deseadas | Microsoft Docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Establecer los formatos de anuncio predeterminados: Ayuda de YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anuncios en vídeos insertados: Ayuda de YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Privacidad de los niños: Comisión Federal de Comercio"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Directivas de aceptación creativos: Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Especificaciones creativos: Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  
