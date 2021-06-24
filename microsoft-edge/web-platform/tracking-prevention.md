---
description: En esta página se proporciona documentación sobre la característica de prevención Microsoft Edge (Chromium) de seguimiento
title: Prevención de seguimiento en Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web, prevención de seguimiento, rastreadores, cookies, almacenamiento, bloqueo de anuncios, bloqueo de rastreadores, protección de seguimiento
ms.openlocfilehash: 24c410beba34b992cf01b973e79c1247fdc26fee
ms.sourcegitcommit: b5acfd4dd7f57991d659715e4621edd786d44052
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2021
ms.locfileid: "11614638"
---
# <a name="tracking-prevention-in-microsoft-edge-chromium"></a>Prevención de seguimiento en Microsoft Edge (Chromium)  

La característica de prevención de seguimiento de Microsoft Edge protege a los usuarios del seguimiento en línea al restringir la capacidad de los rastreadores para acceder al almacenamiento basado en exploradores, así como a la red.  Se ha creado para cumplir la promesa Microsoft Edge privacidad del explorador y, [al][MicrosoftEdgeBrowserPrivacyPromise] mismo tiempo, garantizar que no haya ningún impacto de forma predeterminada en la compatibilidad de sitios web o en la viabilidad económica de la web.  

Microsoft Edge ofrece a los usuarios tres niveles de prevención de seguimiento, que se seleccionan navegando a `edge://settings/privacy` .  

![Tres opciones de prevención de seguimiento][ImageThreeSettingsTrackingPrevention]  

1.  **Básico:** el nivel menos restrictivo de prevención de seguimiento diseñado para usuarios que disfrutan de anuncios personalizados y a los que no les importa que se realice un seguimiento en la web.  Basic solo protege a los usuarios contra rastreadores malintencionados, como los rastreadores de huellas digitales y cryptominers.  
1.  **Equilibrado (predeterminado):** el nivel predeterminado de prevención de seguimiento diseñado para los usuarios que desean ver anuncios menos personalizados al tiempo que minimizan el riesgo de problemas de compatibilidad a medida que navegan por la web.  Balanced tiene como objetivo bloquear los rastreadores de sitios con los que los usuarios nunca interactúan.  
1.  **Estricto:** el nivel más restrictivo de prevención de seguimiento diseñado para usuarios que están bien negociando la compatibilidad de sitios web para obtener la máxima privacidad.  

La característica de prevención de seguimiento de Microsoft Edge está hecha de tres componentes principales que trabajan juntos para determinar si un recurso específico de un sitio web debe clasificarse como rastreador y bloquearse.  Los componentes son los siguientes:  

1.  **Clasificación:** la forma Microsoft Edge determina si una dirección URL pertenece a un rastreador.  
1.  **Aplicación:** las acciones realizadas para proteger Microsoft Edge usuarios de direcciones URL clasificadas como rastreadores.  
1.  **Mitigaciones:** los mecanismos proporcionados para garantizar que los sitios favoritos especificados por el usuario siguen funcionando, al tiempo que ofrecen una protección predeterminada segura.  

Cada uno de los componentes se explora y se explica detalladamente en esta página.  

## <a name="classification"></a>Clasificación  

El primer componente de la característica de prevención de seguimiento en Microsoft Edge es la clasificación.  Para clasificar los rastreadores en línea y agruparlos en categorías, Microsoft Edge las listas de protección [de][|::ref1::|Main] seguimiento de código [abierto][GitHubDisconnectMeTrackingProtection]disconnect .  Las listas se entregan a través del componente "Listas de protección de confianza", que se puede ver en `edge://components` .  Después de descargarlas, las listas se almacenan en el disco, donde puede usarlas para determinar si se clasifica una dirección URL determinada.  

Para determinar si el sistema de clasificación de Microsoft Edge considera que una dirección URL es un rastreador, se comprueba una serie de nombres de host, empezando por una coincidencia exacta y, a continuación, buscando coincidencias parciales para hasta cuatro etiquetas más allá del dominio de nivel superior.  

> **Ejemplo**:  
> 
> DIRECCIÓN URL: `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Nombres de host probados:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Si alguno de esos nombres de host [][|::ref2::|Main] coincide con un nombre de host en las listas de desconexión, [][GitHubDisconnectMeTrackingProtection]Microsoft Edge continúa evaluando las acciones de aplicación para evitar que se realice un seguimiento de los usuarios.  

## <a name="enforcement"></a>Cumplimiento  

Para proporcionar protección frente a acciones de seguimiento en la web, Microsoft Edge dos acciones de aplicación contra rastreadores clasificados:

*   **Restringir el acceso** al almacenamiento: si un recurso de seguimiento conocido intenta obtener acceso a cualquier almacenamiento web en el que pueda intentar conservar los datos sobre el usuario, Microsoft Edge bloqueará ese acceso.  Esto incluye restringir la capacidad de ese rastreador para obtener o establecer cookies, así como las API de almacenamiento de acceso, `IndexedDB` como y `localStorage` .  
*   **Bloquear** cargas de recursos: si se carga un recurso de seguimiento conocido en un sitio web, Microsoft Edge puede bloquear esa carga antes de que la solicitud llegue a la red según el impacto de compatibilidad de la carga y la configuración de prevención de seguimiento que haya establecido un usuario.  Las cargas bloqueadas pueden incluir scripts de seguimiento, píxeles, iframes y mucho más.  Esto evita que los datos potencialmente se envíen al dominio de seguimiento e incluso pueden mejorar los tiempos de carga y el rendimiento de la página como efecto secundario.  

Un usuario puede elegir el icono desplegable de información de página en el lado izquierdo de la barra de direcciones para averiguar qué rastreadores se bloquearon en una página específica: 

![Rastreadores bloqueados en el control desplegable de información de página][ImageBlockedTrackersPageInfoFlyout]  

La forma en que se aplican las restricciones depende del nivel de prevención de seguimiento que haya seleccionado el usuario y de las mitigaciones que se puedan aplicar.  

## <a name="mitigations"></a>Mitigaciones  

Para garantizar que la compatibilidad web se conserve tanto como sea posible, Microsoft Edge tres mitigaciones para ayudar a equilibrar las aplicaciones en situaciones específicas.  Estas son la [mitigación de la relación de organización,](#org-relationship-mitigation)la mitigación [de participación](#org-engagement-mitigation)de la organización y la [lista CompatExceptions](#the-compatexceptions-list).  

Antes de sumergirse en las mitigaciones, vale la pena definir el concepto de "Organización" o "Org" en resumen.  [Disconnect][|::ref3::|Main] también mantiene una lista denominada [entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson] en la que se definen grupos de direcciones URL que pertenecen a la misma organización o empresa primaria.  La característica de prevención de seguimiento de [](#org-relationship-mitigation) Microsoft Edge usa esta lista tanto en la mitigación de relaciones de organización como en la mitigación de [org engagement](#org-engagement-mitigation) para minimizar la aparición de problemas de compatibilidad causados por la prevención de seguimiento que afecta a las solicitudes entre organizaciones.  

### <a name="org-relationship-mitigation"></a>Mitigación de relaciones de la organización  

Varios sitios web populares mantienen sitios web y redes de entrega de contenido \(CDNs\) para servir recursos estáticos y contenido a esos sitios.  Para asegurarse de que este tipo de escenarios no se ven afectados por la prevención de seguimiento, Microsoft Edge exime a un sitio de la prevención de seguimiento cuando el sitio realiza solicitudes de terceros a otros sitios propiedad de la misma organización primaria \(como se define en la lista Desconectar [entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson]on \).  Esto se ilustra mejor con un ejemplo.  

> **Por ejemplo:**
> 
> Una organización denominada Org1 es propietaria de los dominios y , tal como se define en la lista `org1.test` `org1-cdn.test` Desconectar entities.js[en][GitHubDisconnectMeTrackingProtectionEntitiesJson].  Imagine que se clasifica como rastreador y normalmente se le aplicarían medidas de prevención `org1-cdn.test` de seguimiento.  Si un usuario visita y el sitio intenta cargar un recurso desde , Microsoft Edge no realiza ninguna acción de aplicación contra las solicitudes realizadas a aunque no sea una dirección URL de `https://org1.test` `https://org1-cdn.test` primera `org1-cdn.test` persona.  Sin embargo, si otra dirección URL que no forma parte de la organización Org1 intenta cargar ese mismo recurso, la solicitud estaría sujeta a las fuerzas de seguridad porque no forma parte de la misma organización.  
> 
> Aunque esto relaja el seguimiento de las medidas de prevención para los sitios que pertenecen a la misma organización, es poco probable que esto presente un alto riesgo de privacidad, ya que dichas organizaciones pueden determinar a qué sitios o recursos ha tenido acceso, así como a través de datos `https://org1.test` `https://org1-cdn.test` back-end internos.  

### <a name="org-engagement-mitigation"></a>Mitigación de participación de la organización  

La mitigación de participación de la organización se creó para minimizar los riesgos de compatibilidad introducidos mediante el seguimiento de la prevención al garantizar que los sitios que pertenecen a organizaciones con las que los usuarios interactúan lo suficiente continúen funcionando según lo esperado en la web.  Hace uso [][ChromiumDesignDocsSiteEngagement] de la interacción del sitio para relajar las directivas siempre que un usuario haya establecido una relación continua \(actualmente definida por una puntuación de interacción del sitio de 4,1 o superior\) con un sitio determinado.  Esto se muestra mejor en un ejemplo:

> **Por ejemplo:**
> 
> Una organización denominada Organización social es propietaria de los `social.example` dominios y `social-videos.example` .
> 
> Se considera que los usuarios tienen una relación con la organización social si han establecido una puntuación de interacción del sitio de 4,1 o superior con cualquiera de los dominios que pertenecen a la organización social.
> 
> Si otro sitio, , incluye contenido de terceros `https://content-embedder.example` \(say an embedded video from \) from `social-videos.example` any of the domains owned by Social Org that would normally be restricted by tracking prevention enforcements, the site is exempt from tracking prevention enforcements as long as the user's site engagement score with domains owned by Social Org is maintained above the threshold.
> 
> Si un sitio no pertenece a una organización, un usuario debe establecer una puntuación de interacción del sitio de 4,1 o superior con él directamente antes de que se relajen los bloques de carga de recursos o acceso de almacenamiento impuestos por la prevención de seguimiento.

Actualmente, la mitigación de participación de la organización solo se aplica en modo equilibrado para que Microsoft Edge ofrezca las protecciones más altas posibles para los usuarios que han optado por Strict.

### <a name="the-compatexceptions-list"></a>La lista CompatExceptions  

Basándose en los comentarios recientes de los usuarios recibidos por Microsoft, Microsoft Edge mantiene una pequeña lista de sitios \(la mayoría de los cuales se encuentran en la categoría Desconectar contenido\) que se rompían debido a la prevención de seguimiento a pesar de tener las dos mitigaciones anteriores en su lugar. Los sitios de esta lista están exentos del seguimiento de las aplicaciones de prevención.  La lista se puede encontrar en el disco en las [ubicaciones que se describen](#determining-whetherhow-a-particular-url-is-classified) a continuación.  Los usuarios pueden invalidar las entradas en él mediante la **opción Bloquear** en `edge://settings/content/cookies` .

Para evitar que esta lista avance, Microsoft está trabajando actualmente en la API Storage [Access][GitHubMsExplainersStorageAccessApi] en la base Chromium código.  La API de [Storage Access][GitHubMsExplainersStorageAccessApi] ofrece a los desarrolladores de sitios una forma de solicitar acceso de almacenamiento a los usuarios directamente, proporcionando a los usuarios más transparencia sobre cómo su configuración de privacidad está afectando a su experiencia de exploración y proporcionando controles a los desarrolladores de sitios para desbloquearse de forma rápida e intuitiva.

Después de implementar la API de access de [Storage,][GitHubMsExplainersStorageAccessApi] Microsoft dejará de usar la lista CompatExceptions y se pondrá en contacto con los sitios afectados tanto para que conozcan los problemas como para solicitar que usen la API de access de [Storage][GitHubMsExplainersStorageAccessApi] avanzando.  

## <a name="current-tracking-prevention-behavior"></a>Comportamiento de prevención de seguimiento actual  

En la tabla siguiente se muestran las acciones de aplicación y mitigaciones que se aplican a cada categoría de rastreador clasificado en Microsoft Edge.  

*   En la parte superior se encuentran las categorías de rastreadores definidas por las categorías de lista de protección de seguimiento [de desconexión.][GitHubDisconnectTrackingProtectionCategories]  
*   A lo largo del lado izquierdo se encuentran los tres niveles de prevención de seguimiento en Microsoft Edge \(Basic, Balanced y Strict\).  
*   La letra `S` indica que el acceso de almacenamiento está bloqueado.  
*   La letra indica que tanto el acceso de almacenamiento como las cargas `B` de recursos \(como las solicitudes de red\) están bloqueadas.  
*   Un guión \( \) indica que no se aplica ningún bloque a las cargas de recursos o `-` de acceso de almacenamiento.  

| | Publicidad | Análisis | Contenido | Criptomining | Huella digital | Redes sociales | Otros | Mitigación de la misma organización | Mitigación de participación de la organización |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **Básico** | - | - | - | B | B | - | - | Habilitado | N/A |  
| **Equilibrado** | S | - | S | B | B | S | S | Habilitada | Habilitada |  
| **Estricta** | B | B | S | B | B | B | B | Habilitado | Deshabilitado |  

> [!NOTE]
> La mitigación de participación de la organización no se aplica a las categorías Criptomining o Fingerprinting.  

> [!TIP]
> El modo estricto bloquea más cargas de recursos que Balanced.  El bloqueo de más cargas de recursos puede provocar que el modo Estricto parezca bloquear menos solicitudes de seguimiento que Balanced, ya que los rastreadores que hacen las solicitudes nunca se cargan.  

> [!NOTE]
> La columna Huella digital del [comportamiento de prevención de seguimiento](#current-tracking-prevention-behavior) actual hace referencia a los rastreadores que están en la lista De huellas digitales además de otra lista.  Los rastreadores que aparecen únicamente en la lista de huellas digitales se consideran huellas digitales no malintencionadas y no se bloquean.

### <a name="inprivate-behavior"></a>Comportamiento de InPrivate  

En Microsoft Edge 79, el comportamiento predeterminado era aplicar protecciones de modo estricto en InPrivate.  En Microsoft Edge 80, este comportamiento se reemplazó por un modificador que permite a los usuarios decidir si aplican protecciones de modo estricto o mantienen su configuración regular mientras `edge://settings/privacy` exploran InPrivate.  

## <a name="determining-whetherhow-a-particular-url-is-classified"></a>Determinar si se clasifica una dirección URL determinada o cómo se clasifica.  

La forma más sencilla de determinar si una dirección URL específica se clasifica como rastreador conocido es realizar los pasos siguientes.  

1.  Abra DevTools y vaya a la pestaña Consola.  
1.  Actualice la página web.  
    1.  Es posible que desee borrar **primero cookies y** otros datos del sitio para restablecer las puntuaciones de participación del sitio y garantizar una pizarra completamente limpia.  
1.  Busque los mensajes que leen `Tracking Prevention blocked access to storage for <URL>` .  
    1.  Puede expandir los mensajes para ver las direcciones URL individuales que se bloquearon.  
1.  Si necesita determinar en qué categoría se encuentra un sitio bloqueado específico, la forma más sencilla de hacerlo es buscarlo en la lista Desconectar [services.jsen][GitHubDisconnectTrackingProtectionCategories].  Las entradas están alfabéticas, por lo que desplazarse a la parte superior de un bloque de entradas de sitio permite encontrar la categoría específica de un sitio en particular.  

> [!TIP]
> Si necesita tener acceso a las listas de prevención de seguimiento almacenadas en disco, cada una puede encontrarse en una de dos ubicaciones.  
>
> **Actualizaciones basadas en componentes:** las listas que se descargan del componente "Listas de protección de confianza".  
>
> Windows: `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> macOS: `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Directorio de instalación:** las listas que se incluyen con el instalador Microsoft Edge instalación.  Si seleccionó un directorio de instalación diferente, las rutas exactas pueden ser diferentes.  
>
> Windows: `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> macOS: `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes  

La siguiente sección contiene respuestas a las preguntas más frecuentes sobre la característica de prevención de seguimiento en Microsoft Edge.  

**¿Hay alguna forma de bloquear o permitir rastreadores específicos con fines de depuración?**  

Actualmente, Microsoft Edge solo expone una opción para deshabilitar la ejecución de las aplicaciones de prevención de seguimiento en un sitio especificado.  Se tiene acceso a esta opción a través del control desplegable de información de la página o a través de la `edge://settings/privacy/trackingPreventionExceptions` página.  

Dicho esto, las **** opciones **Bloquear** y Permitir de la página pueden usarse para permitir o denegar el acceso de dominios específicos al almacenamiento, como las cookies y otros mecanismos de almacenamiento `edge://settings/content/cookies` del explorador.  Esto es útil para depurar problemas de sitio causados por el seguimiento de las aplicaciones de prevención que bloquean el acceso al almacenamiento de un sitio específico.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Privacidad: Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Site Engagement: el Chromium proyectos"  

[DisconnectMain]: https://disconnect.me "Desconectar"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.js: desconectarme/desconectar-seguimiento-protección | Github"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.js: desconectarme/desconectar-seguimiento-protección | Github"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Storage Explíquelo de la API de Access: MSEdgeExplainers/StorageAccessAPI | GitHub"
