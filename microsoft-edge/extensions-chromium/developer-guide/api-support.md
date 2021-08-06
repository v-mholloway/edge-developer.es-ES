---
description: Lista de API admitidas que se deben usar al crear Microsoft Edge extensiones.
title: API admitidas para Microsoft Edge extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, api de extensión, desarrollador, desarrollo web
ms.openlocfilehash: 1a97346c1b484470b63b447b0acd34833d93e0c12481da9acc56fc7a552b0cac
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11807657"
---
# <a name="supported-apis-for-microsoft-edge-extensions"></a>API admitidas para Microsoft Edge extensiones

En la tabla siguiente se proporciona una lista de API que puede usar al crear extensiones para el explorador Microsoft Edge \(Chromium\).

| API                                   | Descripción                                            
|---------------------------------------|----------------------------------------------------------|
| [alarmas](https://developer.chrome.com/extensions/alarms) | Programar el código para que se ejecute periódicamente o en un momento especificado en el futuro. |
| [marcadores](https://developer.chrome.com/extensions/bookmarks) | Crear, organizar y manipular marcadores. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Use acciones del explorador para colocar iconos en la barra de herramientas Microsoft Edge. También puedes usar acciones del explorador para agregar una información sobre herramientas, un distintivo o un elemento emergente. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Quite los datos de exploración del perfil local de un usuario. |
| [comandos](https://developer.chrome.com/extensions/commands) | Agregue métodos abreviados de teclado que desencadene acciones en la extensión. Por ejemplo, una acción para abrir el explorador o enviar un comando a la extensión. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | En general, la configuración de contenido le permite personalizar el comportamiento de Microsoft Edge en cada sitio, en lugar de globalmente. Cambiar la configuración que controla si los sitios web pueden usar características como cookies, JavaScript y complementos. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Agregue elementos al menú contextual en Microsoft Edge. Los elementos de menú pueden aplicarse a diferentes objetos, como imágenes, hipervínculos y páginas. |
| [cookies](https://developer.chrome.com/extensions/cookies) | Consulta y modifica las cookies y recibe notificaciones cuando cambian. |
| [depurador](https://developer.chrome.com/extensions/debugger) | Adjunte a una o más pestañas a la interacción de red de instrumentos, depure JavaScript, cambie el DOM, cambie CSS, etc. Use el tabId del depurador para dirigir las pestañas con sendCommand y enrutar eventos por tabId desde las devoluciones de llamada de onEvent. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Realizar acciones según el contenido de una página, sin necesidad de permiso para leer el contenido de la página. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Proporciona más privacidad bloqueando o modificando solicitudes de red especificando reglas declarativas. Permitir que las extensiones modifiquen las solicitudes de red sin interceptar la solicitud y ver el contenido. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Captura el contenido de una pantalla, ventanas individuales o pestañas. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interactuar con la ventana inspeccionada.  Por ejemplo, obtenga el identificador de pestaña de las páginas, evalúe el código, actualice las páginas u obtenga recursos en una página. |
| [devtools.network](https://developer.chrome.com/extensions/devtools_network) | Recupere información sobre las solicitudes de red que muestra herramientas de desarrollo en el panel Red. |
| [devtools.panels](https://developer.chrome.com/extensions/devtools.panels) | Integre la extensión en la interfaz de usuario de la ventana Herramientas de desarrollo creando sus propios paneles, accediendo a los paneles existentes o agregando barras laterales. |
| [descargas](https://developer.chrome.com/extensions/downloads) | Inicie, supervise, manipule y busque descargas mediante programación. |
| [enterprise.hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Obtenga el fabricante y el modelo de la plataforma de hardware donde se ejecuta el explorador. Esta API solo está disponible para las extensiones instaladas por la directiva de empresa. |
| [eventos](https://developer.chrome.com/extensions/events) | Tipos comunes usados por las API que producen eventos para notificarle cuándo se produce un evento interesante. |
| [extensión](https://developer.chrome.com/extensions/extension) | Cualquier página de extensión puede usar las utilidades de esta API. Incluye compatibilidad para intercambiar mensajes entre extensiones y scripts de contenido, que se describe en Paso de mensajes. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Contiene declaraciones de tipo para Microsoft Edge extensiones. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Administrar la configuración de fuente en Microsoft Edge. |
| [historial](https://developer.chrome.com/extensions/history) | Interactuar con el registro del explorador de páginas visitadas. Puede agregar, quitar o consultar direcciones URL en el historial del explorador. Para invalidar la página de historial con su propia versión, vaya a Invalidar páginas. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Implementar la internacionalización en toda la aplicación o extensión. |
| [idle](https://developer.chrome.com/extensions/idle) | Detectar cuándo cambia el estado de inactividad de la máquina. |
| [administración](https://developer.chrome.com/extensions/management) | Administrar la lista de extensiones instaladas o en ejecución. Es útil para las extensiones que invalidan la página de nueva pestaña integrada. |
| [notificaciones](https://developer.chrome.com/extensions/notifications) | Crea notificaciones enriquecciones con plantillas y muestralas en la bandeja del sistema. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Registre palabras clave en la Microsoft Edge de direcciones, también conocida como omnibox. |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Agregue iconos a la barra Microsoft Edge de herramientas, a la derecha de la barra de direcciones. Las acciones de página son acciones que se pueden realizar en la página actual y no son aplicables a todas las páginas. Las acciones de página aparecen atenuadas cuando están inactivas. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Guardar pestañas como archivos MHTML.|
| [permisos](https://developer.chrome.com/extensions/permissions) | Recupere los permisos declarados opcionales en tiempo de ejecución, en lugar de en el momento de la instalación. Puede usar esta API para mostrar los permisos necesarios y aprobados para los usuarios. |
| [Inicio/Apagado](https://developer.chrome.com/extensions/power) | Invalide las características de administración de energía del sistema. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Use eventos para consultar impresoras, sus capacidades y enviar trabajos de impresión. |
| [privacidad](https://developer.chrome.com/extensions/privacy) | Controle las características Microsoft Edge que afectan a la privacidad de un usuario. Esta API depende del prototipo `EdgeSetting` de para obtener y establecer la configuración de `types` Microsoft Edge. |
| [proxy](https://developer.chrome.com/extensions/proxy) | Administrar la configuración de proxy para Microsoft Edge. Esta API depende del prototipo de la API para obtener y establecer la configuración `EdgeSetting` `types` de proxy de Microsoft Edge. |
| [tiempo de ejecución](https://developer.chrome.com/extensions/runtime) | Recupera la página en segundo plano, devuelve detalles sobre el manifiesto y escucha y responde a eventos en el ciclo de vida de la aplicación o extensión. También puede convertir la ruta de acceso relativa de las direcciones URL a direcciones URL completa. |
| [sesiones](https://developer.chrome.com/extensions/sessions) | Consultar y restaurar pestañas y ventanas desde una sesión de exploración. |
| [almacenamiento](https://developer.chrome.com/extensions/storage) | Almacenar, recuperar y realizar un seguimiento de los cambios en los datos de usuario. |
| [system.memory](https://developer.chrome.com/extensions/system_memory) | La `system.memory` API. |
| [system.storage](https://developer.chrome.com/extensions/system_storage) | Consulta información sobre dispositivos de almacenamiento. También puedes recibir notificaciones cuando los dispositivos de almacenamiento se adjuntan o se desasocian. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interactuar con secuencias multimedia de tabulación. |
| [pestañas](https://developer.chrome.com/extensions/tabs) | Interactúe con el sistema de pestañas del explorador para crear, modificar y reorganizar pestañas. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Acceda a los sitios principales, también denominados sitios más visitados, que se muestran en la nueva página de pestaña. Estos sitios no incluyen accesos directos personalizados por el usuario. |
| [tts](https://developer.chrome.com/extensions/tts) | Reproducir texto a voz sintetizado (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implementar un motor de texto a voz (TTS) con una extensión. Las extensiones que se registran para usar esta API reciben eventos que contienen expresiones que se deben hablar y otros parámetros. A continuación, las extensiones pueden usar cualquier tecnología web disponible para sintetizar y generar voz, y enviar eventos de vuelta a la función de llamada para notificar el estado. |
| [tipos](https://developer.chrome.com/extensions/types) | Escriba declaraciones para Microsoft Edge. |
| [webNavigation](https://developer.chrome.com/extensions/webNavigation) | Recibir notificaciones sobre el estado de las solicitudes de navegación. |
| [webRequest](https://developer.chrome.com/extensions/webRequest) | Observe y analice el tráfico. Interceptar, bloquear o modificar solicitudes. |
| [windows](https://developer.chrome.com/extensions/windows) | Interactuar con las ventanas del explorador para crear, modificar y reorganizar ventanas en el explorador. |



## <a name="unsupported-extension-apis"></a>API de extensión no admitidas

Microsoft Edge no admite las siguientes API de extensión:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` - Como alternativa, puede usar para `launchWebAuthFlow` capturar un token OAuth2 para autenticar usuarios.
* `chrome.instanceID`.


## <a name="additional-considerations-for-supported-apis"></a>Consideraciones adicionales para las API compatibles

* El usuario debe haber iniciado sesión Microsoft Edge una cuenta de MSA o Azure Active Directory para usar `chrome.identity.getProfileUserInfo` . Si el usuario ha iniciado sesión Microsoft Edge una cuenta de Active Directory local, la API devuelve los valores de correo electrónico `null` e identificador.

* Microsoft Edge no admite extensiones que usan pagos Chrome Web Store porque se usa para solicitar tokens para usuarios que han `identity.getAuthtoken` iniciado sesión. Estos tokens se envían a la API de licencias basada en REST. 


<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/apps/external_extensions)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
