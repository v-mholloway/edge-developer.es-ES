---
description: Esta página proporciona documentación sobre la característica prevención de rastreo de Microsoft Edge (cromo)
title: Prevención de rastreo en Microsoft Edge (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidad, plataforma web, prevención de rastreo, rastreadores, cookies, almacenamiento, bloqueo de ad, bloqueo de Tracker, protección de rastreo
ms.openlocfilehash: a767e55a44c4d416b6d40ca12eb49f2c3a722010
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231161"
---
# Prevención de rastreo en Microsoft Edge (cromo)  

La característica prevención de rastreo de Microsoft Edge protege a los usuarios del seguimiento en línea al restringir la capacidad de los rastreadores de acceso al almacenamiento basado en el explorador, así como a la red.  Está diseñado para mantener la [promesa de privacidad del navegador][MicrosoftEdgeBrowserPrivacyPromise] Microsoft Edge, al mismo tiempo que se asegura de que no haya impacto de forma predeterminada en la compatibilidad de sitios web o la viabilidad económica de la Web.  

Actualmente, Microsoft Edge ofrece a los usuarios tres niveles de prevención de rastreo, que se seleccionan desplazándose a `edge://settings/privacy` .  

![Tres configuraciones de prevención de rastreo][ImageThreeSettingsTrackingPrevention]  

1.  **Básico** : el nivel menos restrictivo de prevención de rastreo diseñado para los usuarios que disfrutan de anuncios personalizados y a quienes no les importa su seguimiento en la Web.  Basic solo protege a los usuarios contra rastreadores maliciosos como, por ejemplo, rastros digitales y cryptominers.  
1.  **Equilibrado (valor predeterminado)** : el nivel predeterminado de prevención de rastreo diseñado para los usuarios que desean ver menos anuncios sobrante que les siguen por la web mientras lo examinan.  Objetivos equilibrados para bloquear los rastreadores de sitios con los que los usuarios nunca participan, minimizando el riesgo de problemas de compatibilidad en la Web.  
1.  **Estricto** : el nivel más restrictivo de prevención de rastreo diseñado para los usuarios que no son compatibles con la seguridad del sitio web para la privacidad máxima.  

La característica prevención de rastreo de Microsoft Edge está formada por tres componentes principales que funcionan conjuntamente para determinar si un recurso específico de un sitio web debe clasificarse como rastreador y bloqueado.  Los componentes son los siguientes:  

1.  **Clasificación** : la manera en que Microsoft Edge determina si una dirección URL pertenece a un rastreador.  
1.  **Aplicación** : las acciones llevadas a cabo para proteger a los usuarios de Microsoft Edge de las direcciones URL clasificadas como rastreadores.  
1.  **Mitigaciones** : los mecanismos proporcionados para garantizar que los sitios favoritos especificados por el usuario siguen funcionando, al mismo tiempo que ofrecen una protección predeterminada segura.  

Cada uno de los componentes se explora y explica detalladamente en esta página.  

## Clasificación  

El primer componente de la característica prevención de rastreo de Microsoft Edge es clasificación.  Para clasificar los seguimientos en línea y agruparlos en categorías, Microsoft Edge usa la [lista de protección][GitHubDisconnectMeTrackingProtection] [desconectar][|::ref1::|Main] el seguimiento de código fuente abierto.  Las listas se entregan a través del componente "listas de protección de confianza", que se pueden ver en `edge://components` .  Una vez descargadas, las listas se almacenan en el disco en el que puede usarlas para determinar si se clasifica una dirección URL determinada.  

Para determinar si una URL se considera un rastreador por el sistema de clasificación en Microsoft Edge, se comprueba una serie de nombres de host, empezando por una coincidencia exacta y, a continuación, comprobando si hay coincidencias parciales para un máximo de cuatro etiquetas más allá del dominio de nivel superior.  

> **Ejemplo**:  
> 
> URL `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Nombres de host probados:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Si cualquiera de esos nombres de host coincide con un nombre de host en las [listas][GitHubDisconnectMeTrackingProtection]de [desconexión][|::ref2::|Main] , Microsoft Edge continúa con la evaluación de las acciones de aplicación para impedir que se realice el seguimiento de los usuarios.  

## Cumplimiento  

Para proporcionar protección de las acciones de seguimiento en la web, Microsoft Edge toma dos acciones de cumplimiento contra los rastreadores clasificados:

*   **Restringir el acceso al almacenamiento** : Si un recurso de seguimiento conocido intenta acceder a cualquier almacenamiento web donde pueda intentar conservar datos sobre el usuario, Microsoft Edge bloquea ese acceso.  Esto incluye restringir la posibilidad de que el rastreador obtenga o establezca cookies, así como el acceso a las API de almacenamiento de información, como `IndexedDB` y `localStorage` .  
*   **Bloquear las cargas de recursos** : si se carga un recurso de seguimiento conocido en un sitio web, Microsoft Edge puede bloquear esa carga antes de que la solicitud llegue a la red según el impacto en la compatibilidad de la carga y la configuración de prevención de rastreo que un usuario haya establecido.  Las cargas bloqueadas pueden incluir secuencias de comandos de seguimiento, píxeles, iframes y mucho más.  Esto evita que los datos se envíen al dominio de seguimiento y pueden mejorar aún más los tiempos de carga y el rendimiento de la página como un efecto secundario.  

Un usuario puede hacer clic en el icono flotante de información de página en el lado izquierdo de la barra de direcciones para averiguar qué rastreadores se bloquearon en una página específica: 

![Rastreadores bloqueados en el control flotante información de página][ImageBlockedTrackersPageInfoFlyout]  

La forma en que se aplican las fuerzas depende del nivel de prevención de seguimiento que haya seleccionado el usuario y de los factores atenuantes que puedan aplicarse.  

## Factores atenuantes  

Para asegurarse de que la compatibilidad Web se mantenga todo lo posible, Microsoft Edge tiene tres factores atenuantes para ayudar a equilibrar las fuerzas en situaciones específicas.  Estas son la [mitigación](#org-relationship-mitigation)de la relación de organización, la [mitigación del compromiso](#org-engagement-mitigation)de la organización y la [lista CompatExceptions](#the-compatexceptions-list).  

Antes de profundizar en los factores atenuantes, merece la pena definir el concepto de "organización" o "org" para abreviar.  [Desconectar][|::ref3::|Main] también mantiene una lista denominada [entities.jsen][GitHubDisconnectMeTrackingProtectionEntitiesJson] que define grupos de direcciones URL que pertenecen a la misma organización o empresa principal.  La característica prevención de rastreo de Microsoft Edge usa esta lista tanto en la [mitigación](#org-relationship-mitigation) de la relación empresarial como en la [mitigación del compromiso](#org-engagement-mitigation) de la organización para minimizar la ocurrencia de problemas de compatibilidad causados por la prevención del seguimiento que afecta a las solicitudes entre organizaciones.  

### Mitigación de la relación org.  

Varios sitios web populares mantienen sitios web y redes de entrega de contenido \ (CDN \) para servir contenido y recursos estáticos a dichos sitios.  Para asegurarse de que estos tipos de escenarios no se vean afectados por la prevención de rastreo, Microsoft Edge exime de un sitio de la prevención de seguimiento cuando el sitio hace solicitudes de terceros a otros sitios que pertenecen a la misma organización principal \ (según se define en la [lista de desconexión entities.jsde][GitHubDisconnectMeTrackingProtectionEntitiesJson]\).  Esto se ilustra mejor con un ejemplo.  

> **Por ejemplo:**
> 
> Una organización llamada Org1 es propietaria de los dominios `org1.test` y `org1-cdn.test` , según se define en la [lista desconectar entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson].  Imagínese que `org1-cdn.test` está clasificado como un rastreador y que normalmente se le aplicarán las fuerzas de prevención de rastreo.  Si un usuario visita `https://org1.test` y el sitio intenta cargar un recurso de `https://org1-cdn.test` , Microsoft Edge no toma ninguna acción de aplicación en las solicitudes hechas a `org1-cdn.test` aunque no sea una dirección URL de origen.  Sin embargo, si otra dirección URL que no forma parte de la organización de Org1 intenta cargar el mismo recurso, la solicitud estaría sujeta a la aplicación de las mismas porque no forma parte de la misma organización.  
> 
> A pesar de que esto relaja las fuerzas de prevención de rastreo para los sitios que pertenecen a la misma organización, no es probable que esto presente una gran cantidad de riesgos de privacidad, ya que estas organizaciones pueden determinar los sitios/recursos a los que ha tenido acceso además de los `https://org1.test` `https://org1-cdn.test` datos internos de back-end.  

### Mitigación del compromiso de la organización  

La mitigación del compromiso de la organización se creó para minimizar los riesgos de compatibilidad introducidos por la prevención de rastreo asegurándose de que los sitios propiedad de las organizaciones con las que los usuarios se relacionan de manera suficiente siguen funcionando de la manera esperada en la Web.  Hace uso de la [implicación de sitios][ChromiumDesignDocsSiteEngagement] para relajar las fuerzas, siempre que un usuario haya establecido una relación continuada \ (definida actualmente por una puntuación de compromiso de sitio de 4,1 o superior \) con un sitio determinado.  Esto se muestra mejor en un ejemplo:

> **Por ejemplo:**
> 
> Una organización denominada social org es propietaria de los dominios `social.example` y `social-videos.example` .
> 
> Se considera que los usuarios tienen una relación con la organización social si han establecido una puntuación del compromiso de un sitio de 4,1 o más con cualquiera de los dominios que pertenecen a la organización social.
> 
> Si otro sitio, `https://content-embedder.example` incluye contenido de terceros \ (supongamos un vídeo insertado desde `social-videos.example` \) de cualquiera de los dominios de la organización social que normalmente se restringirían mediante el seguimiento de las fuerzas de prevención de rastreo, el sitio estará exento de las conversiones de prevención de rastreo, siempre y cuando la puntuación de la negociación del sitio de un usuario se mantenga por encima del umbral
> 
> Si un sitio no pertenece a una organización, un usuario debe establecer una puntuación de compromiso de sitio de 4,1 o superior con él directamente antes de que se relaja cualquier bloque de acceso/carga de recursos de almacenamiento impuesto por la prevención de seguimiento.

La mitigación del compromiso de la organización se aplica actualmente solo en modo equilibrado para que Microsoft Edge ofrezca las máximas protecciones posibles para los usuarios que hayan optado por estrictos.

### La lista de CompatExceptions  

En función de los comentarios de los usuarios recientes que recibió Microsoft, Microsoft Edge mantiene una pequeña lista de sitios \ (la mayoría de los cuales están en la categoría de contenido desconectado \) que se produjeron debido a la prevención de rastreo, a pesar de tener los dos factores atenuantes anteriores. Los sitios de esta lista están exentos del seguimiento de las fuerzas de prevención de rastreo.  La lista puede encontrarse en el disco en las [ubicaciones](#determining-whetherhow-a-particular-url-is-classified) que se describen a continuación.  Los usuarios pueden invalidar las entradas en él mediante la opción de **bloqueo** en `edge://settings/content/cookies` .

Para evitar mantener esta lista en movimiento adelante, Microsoft está trabajando actualmente en la [API de acceso de almacenamiento][GitHubMsExplainersStorageAccessApi] de la base de código de cromo.  La [API de acceso de almacenamiento][GitHubMsExplainersStorageAccessApi] proporciona a los desarrolladores de sitios una forma de solicitar acceso al almacenamiento de los usuarios directamente, lo que proporciona a los usuarios más transparencias en el modo en que su configuración de privacidad está afectando a su experiencia de navegación y ofrece a los controles de los programadores de sitios que se desbloquean de forma rápida y intuitiva.

Después de implementar la [API de acceso de almacenamiento][GitHubMsExplainersStorageAccessApi] , Microsoft dejará de usar la lista de CompatExceptions y llegará a los sitios afectados para que sean conscientes de los problemas, y para solicitarle que usen la API de acceso de [almacenamiento][GitHubMsExplainersStorageAccessApi] en adelante.  

## Comportamiento actual de prevención de rastreo  

En la tabla siguiente se muestran las acciones de aplicación y las mitigaciones que se aplican a cada categoría de seguimiento clasificado en Microsoft Edge.  

*   En la parte superior están las categorías de los rastreadores según se definen en [categorías de lista de protección de seguimiento de Disconnect][GitHubDisconnectTrackingProtectionCategories].  
*   En el lado izquierdo, encontrarás los tres niveles de prevención del seguimiento en Microsoft Edge \ (básico, equilibrado y estricto \).  
*   La letra `S` indica que el acceso al almacenamiento está bloqueado.  
*   La letra `B` indica que están bloqueados el acceso de almacenamiento y las cargas de recursos \ (como solicitudes de red \).  
*   Un guión \ ( `-` \) indica que no se aplica ningún bloque en el acceso de almacenamiento ni en las cargas de recursos.  

| | Publicidad | Análisis | Contenido | Cryptomining | Rastro digital | Redes sociales | Otros | Mitigación de la misma organización | Mitigación del compromiso de la organización |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **Básico** | - | - | - | B | B | - | - | Habilitado | N/D |  
| **Cuadrada** | S | - | S | B | B | S | S | Habilitada | Habilitada |  
| **Estricta** | B | B | S | B | B | B | B | Habilitada | Deshabilitada |  

> [!NOTE]
> La mitigación del compromiso de la organización no se aplica a las categorías Cryptomining ni rastro digital.  

> [!TIP]
> El modo estricto bloquea más cargas de recursos que equilibradas.  El bloqueo de más cargas de recursos puede dar lugar a que aparezca un modo estricto para bloquear menos solicitudes de seguimiento que el equilibrio porque los rastreadores que hacen las solicitudes nunca se cargan.  

> [!NOTE]
> La columna rastro digital en el [comportamiento de prevención de rastreo actual](#current-tracking-prevention-behavior) se refiere a los rastreadores que se encuentran en la lista de rastros digitales además de otra lista.  Los rastreadores que aparecen únicamente en la lista de rastros digitales se consideran rastros digitales no intencionados y no están bloqueados.

### Comportamiento InPrivate  

En Microsoft Edge 79, el comportamiento predeterminado era aplicar protecciones de modo estricto en InPrivate.  En Microsoft Edge 80, este comportamiento ha sido reemplazado por un modificador `edge://settings/privacy` que permite a los usuarios decidir si aplican protección de modo estricto o para mantener su configuración normal al explorar InPrivate.  

## Determinar si se clasifica una dirección URL en particular  

La forma más sencilla de determinar si una dirección URL específica se clasifica como un rastreador conocido es realizar los siguientes pasos.  

1.  Abra DevTools y vaya a la pestaña consola.  
1.  Vuelva a cargar la página.  
    1.  Es posible que desee borrar las **cookies y otros datos del sitio** para restablecer las puntuaciones del compromiso del sitio y garantizar una tableta completa completamente limpia.  
1.  Busque cualquier mensaje que lea `Tracking Prevention blocked access to storage for <URL>` .  
    1.  Puede expandir los mensajes para ver las URL individuales que se han bloqueado.  
1.  Si necesita determinar la categoría en la que se encuentra un sitio bloqueado específico, la manera más fácil de hacerlo es buscarlo en la [lista desconectar services.js][GitHubDisconnectTrackingProtectionCategories].  Las entradas se ordenan alfabéticamente, por lo que el desplazamiento hasta la parte superior de un bloque de entradas de sitio le permite buscar la categoría específica de un sitio en particular.  

> [!TIP]
> Si necesita acceder a las listas de prevención de rastreo almacenadas en el disco, cada una puede encontrarse en una de las dos ubicaciones.  
>
> **Actualizaciones basadas en componentes** : las listas que se descargan desde el componente "listas de protección de confianza"  
>
> Ventana `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> MacOS `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Directorio de instalación** : las listas que se incluyen con el instalador de Microsoft Edge.  Si seleccionó un directorio de instalación diferente, es posible que las rutas exactas sean diferentes.  
>
> Ventana `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> MacOS `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## Preguntas más frecuentes  

La siguiente sección contiene respuestas a las preguntas más frecuentes sobre la característica prevención de rastreo en Microsoft Edge.  

**¿Hay alguna forma de bloquear o permitir la depuración de determinados rastreadores?**  

Por el momento, Microsoft Edge solo expone una opción para deshabilitar la ejecución de la aplicación de prevención de seguimiento en un sitio específico.  Se obtiene acceso a esta opción a través del control flotante de información de página o de la `edge://settings/privacy/trackingPreventionExceptions` página.  

Tal como se dice, las opciones **bloquear** y **permitir** de la `edge://settings/content/cookies` página pueden usarse para permitir o denegar el acceso a los dominios específicos al almacenamiento, como las cookies y otros mecanismos de almacenamiento del explorador.  Esto resulta útil para depurar problemas del sitio causados por las fuerzas de prevención de rastreo que bloquean el acceso al almacenamiento de un sitio específico.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Privacidad-Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Compromiso de sitio: los proyectos de cromo"  

[DisconnectMain]: https://disconnect.me "Terminar"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/Disconnect-Tracking-protección | Github"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.json-disconnectme/Disconnect-Tracking | Github"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.json-disconnectme/Disconnect-Tracking | Github"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Explicación de API de acceso de almacenamiento de información: MSEdgeExplainers/StorageAccessAPI | GitHub"
