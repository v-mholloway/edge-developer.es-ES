---
description: Familiarizarse con las herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
title: Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629507"
---
# Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Los DevTools de Microsoft Edge \ (EdgeHTML \) están creados con [TypeScript][|::ref1::|Index], con tecnología de [código abierto][GithubMicrosoftChakracore], optimizado para los flujos de trabajo front-end modernos y ahora disponibles como una [aplicación independiente de Windows 10][MicrosoftStoreEdgeDevtoolsPreview] en Microsoft Store.  

Para obtener más información sobre las características más recientes, consulte [DevTools en la actualización más reciente de Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Herramientas básicas  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   Microsoft Edge (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

La DevTools de Microsoft Edge \ (EdgeHTML \) incluye:  

*   Un panel [elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML y CSS, inspeccionar propiedades de accesibilidad, ver detectores de eventos y establecer puntos de interrupción de mutación Dom  
*   Una [consola][DevtoolsGuideEdgehtml|::ref3::|] para ver y filtrar los mensajes de registro, inspeccionar objetos de JavaScript y nodos DOM y ejecutar JavaScript en el contexto de la ventana o el marco seleccionado  
*   Un [depurador][DevtoolsGuideEdgehtml|::ref4::|] para recorrer el código, establecer relojes y puntos de interrupción, editar en vivo el código e inspeccionar el almacenamiento web y las cachés de cookies  
*   Panel de [red][DevtoolsGuideEdgehtml|::ref5::|] para supervisar e inspeccionar solicitudes y respuestas desde la red y la caché del explorador  
*   Un panel de [rendimiento][DevtoolsGuideEdgehtml|::ref6::|] para perfilar el tiempo y los recursos del sistema que necesita su sitio  
*   Panel [memoria][DevtoolsGuideEdgehtml|::ref7::|] para medir el uso de los recursos de memoria y Comparar instantáneas de montones en diferentes Estados de tiempo de ejecución de código  
*   Panel de [almacenamiento][DevtoolsGuideEdgehtml|::ref8::|] para inspeccionar y administrar el almacenamiento Web, IndexedDB, cookies y datos de la caché  
*   Un panel de [trabajo de servicios][DevtoolsGuideEdgehtmlServiceworkers] para la administración y la depuración de los trabajadores de servicios  
*   Un panel de [emulación][DevtoolsGuideEdgehtml|::ref9::|] para probar su sitio con diferentes perfiles de explorador, resoluciones de pantalla y coordenadas de ubicación GPS  

¡ Sigue enviando tus [comentarios y solicitudes de características](#feedback)!  

> [!TIP]
> [Prueba en Microsoft Edge \ (EdgeHTML \) gratis desde cualquier explorador][BrowserstackEdgehtml].  
> El equipo de Microsoft Edge se asoció con [BrowserStack][BrowserstackEdgehtml] para ofrecer pruebas gratuitas en vivo y automatizadas en Microsoft Edge \ (EdgeHTML \).  

## Aplicación de la Microsoft Store  

Los **DevTools de Microsoft Edge \ (EdgeHTML \)** [ahora están disponibles][DevtoolsGuideEdgehtmlWhatsnew] como una [aplicación independiente de Windows 10 en Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], además de la experiencia de herramientas en el explorador \ ( `F12` \).  La versión de la tienda viene con un panel de **selección** para adjuntar a destinos de página locales y remotos y un diseño con fichas para facilitar el cambio entre instancias de DevTools.  

### Depuración local  

Para depurar una página de forma local, simplemente inicia la aplicación Microsoft Edge DevTools.  El panel **local** del selector muestra todos los procesos de contenido de EdgeHTML activos, incluidas las pestañas del explorador abierto, que ejecutan [PWAs][PwasEdgehtmlIndex] \ ( `WWAHost.exe` procesos \) y los controles de [WebView][HostingWebview] .  Seleccione el destino que desea adjuntar y abra una nueva pestaña de la DevTools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Panel local de la aplicación DevTools":::
   Panel local de la aplicación DevTools
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Depuración remota  

La aplicación Microsoft Edge DevTools presenta compatibilidad básica para la depuración de páginas en un equipo remoto a través de nuestro nuevo [Protocolo de DevTools][DevtoolsProtocolEdgehtmlIndex].  Con la última versión, se obtiene acceso remoto a la funcionalidad principal en el [depurador][DevtoolsGuideEdgehtml|::ref10::|]: [los elementos][DevtoolsGuideEdgehtml|::ref11::|] \ (para las operaciones de solo lectura \) y los paneles de [consola][DevtoolsGuideEdgehtml|::ref12::|] .  La depuración remota está limitada a Microsoft Edge \ (EdgeHTML \) ejecutando hosts de escritorio, con compatibilidad para otros hosts de EdgeHTML y dispositivos Windows 10 que se publiquen en versiones futuras.  

Para comenzar, consulta la sección [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] de los documentos de [Protocolo de DevTools][DevtoolsProtocolEdgehtmlIndex] .  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Panel remoto de aplicaciones de DevTools":::
   Panel remoto de aplicaciones de DevTools
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Métodos abreviados generales  

> [!IMPORTANT]
> Todos los métodos abreviados se han verificado en la versión más reciente de Windows.  
> Si no puede usar un acceso directo, actualice su copia de Windows.  

Estos métodos abreviados controlan la ventana principal de DevTools y deben funcionar en todas las herramientas.  

| Acción | Método abreviado |  
|:--- |:--- |  
| Mostrar u ocultar DevTools \ (se abre en el panel de última vista \) | `F12`, `Ctrl`+`Shift`+`I` |  
| Activar o desactivar el acoplamiento \ (desacoplar/inferior/derecha \) | `Ctrl`+`Shift`+`D` |  
| Abrir archivo | `Ctrl`+`P`, `Ctrl`+`O` |  
| Mostrar código fuente HTML no modificable en el depurador | `Ctrl`+`U` |  
| Mostrar u ocultar consola en la parte inferior de cualquier otra herramienta  | `Ctrl`+`` ` `` |  
| Cambiar a elementos \ (explorador DOM \) | `Ctrl`+`1` |  
| Cambiar a consola |  `Ctrl`+`2` |  
| Cambiar a depurador | `Ctrl`+`3` |  
| Cambiar a red | `Ctrl`+`4` |  
| Cambiar al rendimiento | `Ctrl`+`5` |  
| Cambiar a memoria | `Ctrl`+`6` |  
| Cambiar a la emulación | `Ctrl`+`7` |  
| Documento de ayuda | `F1` |  
| Siguiente herramienta | `Ctrl`+`F6` |  
| Herramienta anterior | `Ctrl`+`Shift`+`F6` |  
| Herramienta anterior \ (desde historial \) | `Ctrl`+`Shift`+`[` |  
| Siguiente herramienta \ (desde historial \) | `Ctrl`+`Shift`+`]` |  
| Submarco siguiente | `F6` |  
| Submarco anterior | `Shift`+`F6` |  
| Coincidencia siguiente en el cuadro de búsqueda | `F3` |  
| Coincidencia anterior en el cuadro de búsqueda | `Shift`+`F3` |  
| Buscar en el cuadro de búsqueda | `Ctrl`+`F` |  
| Dar el foco a la consola en la parte inferior | `Alt`+`Shift`+`I` |  
| Iniciar DevTools a la consola | `Ctrl`+`Shift`+`J` |  
| Actualizar la página | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Si está depurando un punto de interrupción y se encuentra en pausa, la acción **actualizar la página** reanuda el tiempo de ejecución en primer lugar.  

## Comentarios  

Envíanos tus comentarios para ayudar a mejorar la DevTools de Microsoft Edge \ (EdgeHTML \).  Simplemente abre las herramientas \ ( `F12` \) y selecciona el botón [Enviar comentarios](#microsoft-edge-edgehtml-developer-tools) .  

Conviértase en un [Windows Insider][WindowsInsiderProgram] para obtener una vista previa de las [características más recientes de la DevTools][DevtoolsGuideEdgehtmlWhatsnew].  Use la aplicación Hub de comentarios de Windows para publicar, votar, realizar un seguimiento y obtener soporte técnico para sugerencias y problemas generales de Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Sola"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulación"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Memoria"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Red"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Comportamiento"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Trabajadores de servicio"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Storage"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools en la actualización más reciente de Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo Microsoft Edge (EdgeHTML) DevTools"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview-clientes de protocolo DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "Vista de WebView (EdgeHTML) para aplicaciones de Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicaciones web progresivas (EdgeHTML) en Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Vista previa de Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Prueba gratuita del explorador Microsoft Edge BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "Llena"  
