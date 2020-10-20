---
description: Lista de API admitidas para usar al crear extensiones de Microsoft Edge.
title: API admitidas para las extensiones de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, API de extensión, desarrollador, desarrollo web'
ms.openlocfilehash: 868473393da6cefbf146fb7acd6c9816903bd253
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120398"
---
# API admitidas para las extensiones de Microsoft Edge

En la tabla siguiente se proporciona una lista de las API que puedes usar al crear extensiones para el explorador Microsoft Edge \ (cromo \).

| API                                   | Descripción                                            
|---------------------------------------|----------------------------------------------------------|
| [alarmas](https://developer.chrome.com/extensions/alarms) | Programe el código para que se ejecute periódicamente o a una hora determinada en el futuro. |
| [marcadores](https://developer.chrome.com/extensions/bookmarks) | Crear, organizar y manipular marcadores. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Use las acciones del explorador para colocar iconos en la barra de herramientas de Microsoft Edge. También puede usar las acciones del explorador para agregar una información sobre herramientas, un distintivo o un mensaje emergente. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Quitar los datos de navegación del perfil local de un usuario. |
| [comandos](https://developer.chrome.com/extensions/commands) | Agregue métodos abreviados de teclado que desencadenen acciones en la extensión. Por ejemplo, una acción para abrir el explorador o enviar un comando a la extensión. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | En general, la configuración de contenido le permite personalizar el comportamiento de Microsoft Edge en cada sitio, en lugar de globalmente. Cambie la configuración que controla si los sitios web pueden usar características como cookies, JavaScript y complementos. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Agregar elementos al menú contextual en Microsoft Edge. Los elementos de menú pueden aplicarse a objetos diferentes, como imágenes, hipervínculos y páginas. |
| [cookies](https://developer.chrome.com/extensions/cookies) | Consultar y modificar las cookies, y recibir notificaciones cuando cambien. |
| [depurador](https://developer.chrome.com/extensions/debugger) | Adjunte a una o más pestañas para instrumentar la interacción de la red, depurar JavaScript, cambiar el DOM, cambiar CSS, etc. Use el depurador tabId para dirigir las pestañas con sendCommand y enrutar los eventos mediante tabId de las devoluciones de llamada onEvent. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Realice acciones según el contenido de una página, sin necesidad de permiso para leer el contenido de la página. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Proporciona más privacidad bloqueando o modificando las solicitudes de red mediante la especificación de reglas declarativas. Permitir que las extensiones modifiquen las solicitudes de red sin interceptar la solicitud y ver el contenido. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Capturar el contenido de una pantalla, de ventanas individuales o de pestañas. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interactúe con la ventana inspeccionada. Por ejemplo, obtenga el identificador de tabulación de las páginas, evalúe el código, vuelva a cargar páginas u obtenga recursos en una página. |
| [DevTools. Network](https://developer.chrome.com/extensions/devtools_network) | Recupere información sobre las solicitudes de red que muestran las herramientas para desarrolladores en el panel red. |
| [DevTools.](https://developer.chrome.com/extensions/devtools.panels) | Integre tu extensión en la interfaz de usuario de la ventana herramientas de desarrollo creando tus propios paneles, accediendo a los paneles existentes o añadiendo barras laterales. |
| [descargas](https://developer.chrome.com/extensions/downloads) | Iniciar, supervisar, manipular y buscar descargas mediante programación. |
| [Enterprise. hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Obtén el fabricante y el modelo de la plataforma de hardware donde se ejecuta el explorador. Esta API solo está disponible para las extensiones instaladas por la Directiva de empresa. |
| [ceso](https://developer.chrome.com/extensions/events) | Tipos comunes usados por las API que provocan eventos que le notifican cuando se produce un evento interesante. |
| [extensiones](https://developer.chrome.com/extensions/extension) | Cualquier página de extensión puede usar las utilidades de esta API. Incluye compatibilidad para intercambiar mensajes entre las extensiones y las secuencias de comandos de contenido, que se describe en paso de mensajes. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Contiene declaraciones de tipo para las extensiones de Microsoft Edge. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Administra la configuración de la fuente en Microsoft Edge. |
| [historial](https://developer.chrome.com/extensions/history) | Interactuar con el registro del explorador de las páginas visitadas. Puede Agregar, quitar o consultar direcciones URL en el historial del explorador. Para invalidar la página del historial con su propia versión, consulte invalidar páginas. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Implemente la internacionalización en toda la aplicación o extensión. |
| [está](https://developer.chrome.com/extensions/idle) | Detectar cuándo cambia el estado de inactividad de la máquina. |
| [Administración](https://developer.chrome.com/extensions/management) | Administra la lista de extensiones instaladas o que se ejecutan. Es útil para las extensiones que anulan la página de la nueva pestaña integrada. |
| [notificaciones](https://developer.chrome.com/extensions/notifications) | Crear notificaciones enriquecidas con plantillas y mostrarlas en la bandeja del sistema. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Registrar palabras clave en la barra de direcciones de Microsoft Edge, también conocida como Omnibox. |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Agregue iconos a la barra de herramientas de Microsoft Edge, a la derecha de la barra de direcciones. Las acciones de página son acciones que se pueden realizar en la página actual y no son aplicables a todas las páginas. Las acciones de la página aparecen atenuadas cuando están inactivas. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Guardar las pestañas como archivos MHTML.|
| [permisos](https://developer.chrome.com/extensions/permissions) | Recuperar permisos declarados y opcionales en tiempo de ejecución, en lugar de en el momento de la instalación. Puede usar esta API para mostrar los permisos necesarios y aprobados a los usuarios. |
| [Inicio/Apagado](https://developer.chrome.com/extensions/power) | Invalide las características de administración de energía del sistema. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Usar eventos para consultar impresoras, sus capacidades y enviar trabajos de impresión. |
| [privacidad](https://developer.chrome.com/extensions/privacy) | Controle las características de Microsoft Edge que afectan a la privacidad de un usuario. Esta API depende del `EdgeSetting` prototipo de `types` para obtener y establecer la configuración de Microsoft Edge. |
| [servidor](https://developer.chrome.com/extensions/proxy) | Administra la configuración de proxy para Microsoft Edge. Esta API depende del `EdgeSetting` prototipo de la `types` API para obtener y establecer la configuración de proxy de Microsoft Edge. |
| [motores](https://developer.chrome.com/extensions/runtime) | Recupere la página de fondo, devuelva detalles sobre el manifiesto y escuche y responda a eventos de la aplicación o el ciclo de vida de la extensión. También puede convertir la ruta de acceso relativa de las direcciones URL a direcciones URL completas. |
| [activas](https://developer.chrome.com/extensions/sessions) | Las pestañas de consultas y restauraciones y ventanas de una sesión de exploración. |
| [almacenamiento](https://developer.chrome.com/extensions/storage) | Almacenar, recuperar y realizar el seguimiento de los cambios en los datos de usuario. |
| [System. Memory](https://developer.chrome.com/extensions/system_memory) | La `system.memory` API. |
| [System. Storage](https://developer.chrome.com/extensions/system_storage) | Consultar información sobre dispositivos de almacenamiento. También puede recibir notificaciones cuando se conectan o desasocian dispositivos de almacenamiento. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interactúe con las secuencias de medios de tabulación. |
| [pestañas](https://developer.chrome.com/extensions/tabs) | Interactúe con el sistema de pestañas del explorador para crear, modificar y reorganizar las pestañas. |
| [Sitios web](https://developer.chrome.com/extensions/topSites) | Obtenga acceso a los sitios superiores, también llamados sitios visitados, que se muestran en la página de la nueva pestaña. Estos sitios no incluyen accesos directos personalizados por el usuario. |
| [TT](https://developer.chrome.com/extensions/tts) | Reproducir texto a voz sintetizado (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implementar un motor de texto a voz (TTS) con una extensión. Las extensiones que se registran para usar esta API reciben eventos que contienen utterances que se van a hablar y otros parámetros. Después, las extensiones pueden usar cualquier tecnología Web disponible para sintetizar y enviar voz, y devolver eventos a la función de llamada para informar del estado. |
| [tipos](https://developer.chrome.com/extensions/types) | Declaraciones de tipo de Microsoft Edge. |
| [navegación en](https://developer.chrome.com/extensions/webNavigation) | Recibir notificaciones sobre el estado de las solicitudes de navegación. |
| [WebRequest](https://developer.chrome.com/extensions/webRequest) | Observar y analizar el tráfico. Interceptar, bloquear o modificar solicitudes. |
| [windows](https://developer.chrome.com/extensions/windows) | Interactúe con ventanas del explorador para crear, modificar y reorganizar ventanas en el explorador. |



## API de extensión no admitidas

Microsoft Edge no admite las siguientes API de extensión:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` -Como alternativa, puede usar `launchWebAuthFlow` para obtener un símbolo (token) de OAuth2 para autenticar a los usuarios.
* `chrome.instanceID`.


## Consideraciones adicionales para las API compatibles

* El usuario debe haber iniciado sesión en Microsoft Edge mediante una cuenta de MSA o Azure Active Directory para usar `chrome.identity.getProfileUserInfo` . Si el usuario ha iniciado sesión en Microsoft Edge mediante una cuenta local de Active Directory, la API devuelve los `null` valores de los mensajes de correo electrónico y de identificación.

* Microsoft Edge no es compatible con las extensiones que usan los pagos de la tienda web de Chrome porque usa `identity.getAuthtoken` para solicitar tokens para los usuarios que iniciaron sesión. Estos tokens se envían a la API de licencias basada en REST. 


<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/apps/external_extensions).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
