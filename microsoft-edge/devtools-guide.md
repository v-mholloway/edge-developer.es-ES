---
description: Conozca las herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
title: Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/10/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
experimental: true
experiment_id: 51fe4b97-3e55-41
ms.localizationpriority: high
ms.openlocfilehash: cba59764805c0be0e9d2c57c1a3d87ca4d14943e
ms.sourcegitcommit: 1e33cd41e5afb2e6dbdc19353011ff6c2b019f9c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2020
ms.locfileid: "10866074"
---
# Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Microsoft Edge \(EdgeHTML\) DevTools está creado con [TypeScript][|::ref1::|Index], con tecnología de [Open Source][GithubMicrosoftChakracore], optimizada para los flujos de trabajo front-end modernos y ahora disponible como una [aplicación independiente de Windows 10][MicrosoftStoreEdgeDevtoolsPreview] en Microsoft Store.  

Para más información sobre las características más recientes, consulte [DevTools en la última actualización de Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Herramientas básicas  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   Microsoft Edge (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Microsoft Edge \(EdgeHTML\) DevTools incluye lo siguiente:  

*   Un [panel de elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML y CSS, inspeccionar propiedades de accesibilidad, visualizar escuchas de eventos y definir puntos de interrupción de mutación de DOM  
*   Una [consola][DevtoolsGuideEdgehtml|::ref3::|] para ver y filtrar los mensajes de registro, inspeccionar objetos de JavaScript y nodos de DOM y ejecutar JavaScript en el contexto de la ventana o marco seleccionados  
*   Un [depurador][DevtoolsGuideEdgehtml|::ref4::|] para revisar código, establecer inspecciones y puntos de interrupción, editar en vivo su código y revisar el almacenamiento web y las cachés de cookies  
*   Un panel de [red][DevtoolsGuideEdgehtml|::ref5::|] para supervisar e inspeccionar las solicitudes y respuestas de la red y de la memoria caché del explorador  
*   Un panel de [rendimiento][DevtoolsGuideEdgehtml|::ref6::|] para generar perfiles de tiempo y de los recursos del sistema necesarios para su sitio  
*   Un panel de [memoria][DevtoolsGuideEdgehtml|::ref7::|] para medir su uso de los recursos de memoria y comparar instantáneas de pila en diferentes estados del tiempo de ejecución de código.  
*   Un panel de [almacenamiento][DevtoolsGuideEdgehtml|::ref8::|] para inspeccionar y administrar su almacenamiento web, IndexedDB, cookies y datos de caché  
*   Un panel de [trabajos de servicio][DevtoolsGuideEdgehtmlServiceworkers] para administrar y depurar sus trabajos de servicio  
*   Un panel de [emulación][DevtoolsGuideEdgehtml|::ref9::|] para probar su sitio con diferentes perfiles de explorador, resoluciones de pantalla y coordenadas de ubicación GPS  

No dude en seguir enviando su [opinión y comentarios y en solicitar características](#feedback).  

> [!TIP]
> [Puede probarlo en Microsoft Edge \(EdgeHTML\) desde cualquier explorador de manera gratuita][BrowserstackEdgehtml].  
> El equipo de Microsoft Edge se asoció con [BrowserStack][BrowserstackEdgehtml] para ofrecer pruebas gratuitas en tiempo real y automatizadas en Microsoft Edge \(EdgeHTML\).  

## Aplicación de la Microsoft Store  

**Microsoft Edge \(EdgeHTML\) DevTools** se encuentra [disponible][DevtoolsGuideEdgehtmlWhatsnew] como una [aplicación independiente de Windows 10 de Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview] y se añade a la experiencia de herramientas en el explorador \(`F12`\).  Con la versión de la tienda incluye un panel **selector** que permite adjuntar a destinos de página remotos y locales abiertos, así como un diseño con fichas para facilitar el cambio entre instancias de DevTools.  

### Depuración local  

Para depurar una página a nivel local, inicie la aplicación Microsoft Edge DevTools.  El panel **local** del selector muestra todos los procesos de contenido de EdgeHTML activos, incluidas las pestañas abiertas del explorador Edge, PWA en ejecución \( procesos\) y los controles de [WebView][HostingWebview].  Seleccione el destino que desee adjuntar y abra una instancia de nueva pestaña de DevTools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Panel local de la aplicación DevTools":::
   Panel local de la aplicación DevTools
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Depuración remota  

La aplicación Microsoft Edge DevTools introduce la compatibilidad básica para la depuración de páginas en un equipo remoto mediante nuestro [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex] publicado recientemente.  Con la versión más reciente, se obtiene acceso remoto a la funcionalidad principal del depurador, elementos \ (para operaciones de solo lectura\) y paneles de [consola][DevtoolsGuideEdgehtml|::ref12::|].  La depuración remota está limitada a hosts de escritorio en ejecución de Microsoft Edge \ (EdgeHTML\) y es compatible con otros hosts EdgeHTML y dispositivos Windows 10 que disponibles en versiones futuras.  

Para empezar, consulte la sección Microsoft Edge DevTools de los documentos del [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Panel remoto de la aplicación DevTools":::
   Panel remoto de la aplicación DevTools
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Accesos directos generales  

> [!IMPORTANT]
> Todos los accesos directos han sido comprobados en la versión más reciente de Windows.  
> Si no puede usar un acceso directo, debe actualizar su copia de Windows.  

Estos accesos directos controlan la ventana principal de DevTools y deberían funcionar en todas las herramientas.  

| Acción | Acceso directo |  
|:--- |:--- |  
| Mostrar u ocultar DevTools \(se abre en el último panel visualizado\) | `F12`, `Ctrl`+`Shift`+`I` |  
| Activar o desactivar el acoplamiento \(desacoplar/inferior/derecho\) | `Ctrl`+`Shift`+`D` |  
| Abrir archivo | `Ctrl`+`P`, `Ctrl`+`O` |  
| Mostrar en el depurador el código fuente HTML no modificable | `Ctrl`+`U` |  
| Mostrar u ocultar consola en la parte inferior de cualquier otra herramienta  | `Ctrl`+`` ` `` |  
| Cambiar a elementos \(explorador DOM\) | `Ctrl`+`1` |  
| Cambiar a consola |  `Ctrl`+`2` |  
| Cambiar a depurador | `Ctrl`+`3` |  
| Cambiar a red | `Ctrl`+`4` |  
| Cambiar a rendimiento | `Ctrl`+`5` |  
| Cambiar a memoria | `Ctrl`+`6` |  
| Cambiar a emulación | `Ctrl`+`7` |  
| Documento de ayuda | `F1` |  
| Siguiente herramienta | `Ctrl`+`F6` |  
| Herramienta anterior | `Ctrl`+`Shift`+`F6` |  
| Herramienta anterior \(desde historial\) | `Ctrl`+`Shift`+`[` |  
| Siguiente herramienta \(desde historial\) | `Ctrl`+`Shift`+`]` |  
| Submarco siguiente | `F6` |  
| Submarco anterior | `Shift`+`F6` |  
| Siguiente coincidencia en el cuadro de búsqueda | `F3` |  
| Coincidencia anterior en el cuadro de búsqueda | `Shift`+`F3` |  
| Buscar en el cuadro de búsqueda | `Ctrl`+`F` |  
| Establecer el foco en la consola en la parte inferior | `Alt`+`Shift`+`I` |  
| Iniciar DevTools en la consola | `Ctrl`+`Shift`+`J` |  
| Actualizar la página. | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Si pausa la depuración en un punto de ruptura, la acción **Actualizar página** reanuda en primer lugar el tiempo de ejecución.  

## Comentarios  

Envíenos sus comentarios para ayudar a mejorar Microsoft Edge \(EdgeHTML\) DevTools.  Para ello, solo tiene que abrir las herramientas \(`F12`\) y seleccionar el botón [Enviar comentarios](#microsoft-edge-edgehtml-developer-tools).  

Únase a[Windows Insider][WindowsInsiderProgram] para obtener una vista previa de las [últimas características de DevTools][DevtoolsGuideEdgehtmlWhatsnew].  Puede utilizar la aplicación del Centro de opiniones sobre Windows para publicar y votar sugerencias y problemas generales de Windows, realizar seguimientos de los mismos y obtener soporte técnico.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Consola"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulación"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Memoria"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Red"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Rendimiento"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Trabajos de servicio"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Almacenamiento"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools en la última actualización de Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo de Microsoft Edge (EdgeHTML) DevTools"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Vista previa de Microsoft Edge DevTools - Clientes de protocolo de DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) para aplicaciones de Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicaciones web progresivas (EdgeHTML) en Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Vista previa de Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Pruebas gratuitas de explorador de Microsoft Edge | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
