---
description: Vista 3D, Visual Studio integración con Microsoft Edge y mucho más.
title: Novedades de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 03b17f524e9be55e1ed37147ce46b7a15fc3a17d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564962"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-81"></a>Novedades de DevTools (Microsoft Edge 81)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Anuncios del equipo Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo Microsoft Edge DevTools.  Echa un vistazo a los anuncios para probar nuevas características en DevTools, Microsoft Visual Studio code extensions y mucho más.  Para mantenerse al día de todas las características más recientes [][MicrosoftEdgePreviewChannels] y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa Microsoft Edge y [síganos en Twitter][EdgeDevToolsTwitterAccount].  

### <a name="accessibility-improvements-to-the-devtools"></a>Mejoras de accesibilidad a DevTools  

El equipo de DevTools ha contribuido con 170 cambios en Chromium para solucionar problemas de contraste de color, teclado y lector de pantalla de alto impacto en DevTools.  Cada desarrollador que esté creando la web debe poder usar DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="La herramienta Rendimiento de DevTools con las mejoras de navegación del teclado y lector de pantalla" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   La **herramienta Rendimiento** de DevTools con las mejoras de navegación del teclado y lector de pantalla  
:::image-end:::  

¿Desea obtener información sobre cómo hacer que la página web sea accesible para todos los usuarios?  Descargue las [extensiones accessibility Insights][AccessibilityInsights] y [webhint][WebhintBrowserExtension] Microsoft Edge para empezar.  

Si usas lectores de pantalla o el teclado para navegar [][PostTweetEdgeDevTools] por DevTools, envíanos tus comentarios tuiteando o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Chromium problema [#963183][CR963183]  

### <a name="using-the-devtools-in-other-languages"></a>Uso de DevTools en otros idiomas  

Muchos desarrolladores usan otras herramientas de desarrollador, como StackOverflow y Visual Studio Code, en su idioma nativo, no solo en inglés.  Estamos encantados de anunciar la localización de DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:  

:::row:::
   :::column span="":::
      Chino \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chino \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Francés : fran&#231;ais
   :::column-end:::
   :::column span="":::
      Alemán - deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italiano - italiano
   :::column-end:::
   :::column span="":::
      Japonés - &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Coreano - &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Portugués : portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Ruso – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Español - espa&#241;ol
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Las DevTools coinciden automáticamente con el idioma que usa para Microsoft Edge en `edge://settings/languages` .  

Si desea que Microsoft Edge en un idioma y devTools permanezca en inglés, seleccione en DevTools para abrir Configuración y deshabilitar Match `F1` **browser language**. [][DevtoolsCustomizeIndexSettings]  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools en alemán" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   DevTools en alemán  
:::image-end:::  

**Los mensajes** de consola no están localizados.  Solo las cadenas usadas en la interfaz de usuario de DevTools se muestran en el idioma que usa para Microsoft Edge.  

Si quieres usar DevTools en un idioma diferente al que está [disponible,][PostTweetEdgeDevTools] envíanos un tweet o elige el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Chromium problema [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>extensión webhint Microsoft Edge webhint  

La extensión webhint Microsoft Edge le permite examinar fácilmente la página web y obtener comentarios sobre accesibilidad, compatibilidad del explorador, seguridad, rendimiento y mucho más dentro de DevTools.  Leer más en [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="La herramienta Sugerencias en DevTools cuando se instala la extensión del explorador webhint" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   La **herramienta Sugerencias** en DevTools cuando se instala la extensión del explorador webhint  
:::image-end:::  

[Pruebe la extensión del explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].  Una vez instalada la extensión, abra DevTools y elija la **herramienta Sugerencias.**  Desde aquí, ejecute un examen de sitio personalizable.  Dirígete a [webhint.io][WebhintBrowserExtension] para obtener más información.  

### <a name="3d-view"></a>Vista 3D  

Use la **vista 3D** para depurar la aplicación web navegando por el modelo de objetos de documento [\(DOM\)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z.][MDNZIndex]  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="La vista 3D en DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   La vista 3D en DevTools  
:::image-end:::  

Para obtener acceso a la vista 3D, seleccione `Ctrl`  +  `Shift`  +  `P` , escriba en **Vista 3D** y **seleccione Mostrar vista 3D**.  

El Microsoft Edge está trabajando con el equipo de Chromium en la interfaz de usuario y agregando más funcionalidad a la vista 3D, por lo que envíe sus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team).  

Chromium problema [#987787][CR987787]  

### <a name="visual-studio-code-extensions"></a>Visual Studio Code de datos  

El equipo de DevTools también ha publicado algunas extensiones para [Visual Studio Code][VisualStudioCode] que le permiten usar la potencia de DevTools directamente desde el editor de texto. Consulte las extensiones siguientes:  

#### <a name="elements-for-microsoft-edge"></a>Elementos para Microsoft Edge  

Use la herramienta Elementos desde dentro de Visual Studio Code agregando la [extensión Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="La herramienta Elementos de Visual Studio Code la extensión Elements for Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   La **herramienta Elementos** de Visual Studio Code la extensión Elements for Microsoft Edge  
:::image-end:::  

Para obtener más información, consulte [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].  

#### <a name="debugger-for-microsoft-edge"></a>Depurador de Microsoft Edge  

Con la [extensión Depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depura JavaScript que se ejecuta en Microsoft Edge directamente desde Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="El depurador de Microsoft Edge de Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   El depurador de Microsoft Edge de Visual Studio Code  
:::image-end:::  

Para obtener más información, [consulte cómo depurar][VisualStudioCodeDebuggerEdgeExtension]Microsoft Edge desde Visual Studio Code .  

#### <a name="webhint"></a>webhint  

La [extensión webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code para `webhint` mejorar la página web mientras la escribe.  Esta extensión ejecuta e informa de diagnósticos en los archivos del área de trabajo en función del `webhint` análisis.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="La extensión webhint Visual Studio Code analizar un archivo .tsx en Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   La extensión webhint Visual Studio Code análisis de un `.tsx` archivo en Visual Studio Code  
:::image-end:::  

[Obtenga más información sobre la Visual Studio Code webhint][WebhintVisualStudioCodeExtension].  

### <a name="visual-studio-integration"></a>Visual Studio integración  

En Visual Studio versión 16.2 o posterior de 2019, use el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.  [Descarga Visual Studio 2019 para][MicrosoftVisualStudioDownloads] probar esta característica.  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta  
:::image-end:::  

[Obtenga más información sobre la depuración Microsoft Edge desde Visual Studio][VisualStudioIndex].  

### <a name="tracking-prevention-console-messages"></a>Seguimiento de mensajes de consola de prevención  

La prevención de seguimiento es una característica única en Microsoft Edge que le protege de que los sitios web que no ha visitado antes le realicen un seguimiento.  La configuración predeterminada de prevención de seguimiento es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores malintencionados conocidos para una experiencia que equilibra la privacidad y la compatibilidad web.  Para obtener más información sobre la compatibilidad de la página web cuando se **** bloquean determinados rastreadores, se agregaron mensajes de advertencia en la consola cuando se bloquea un rastreador.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensajes en la consola cuando la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Mensajes en la **consola cuando** la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador  
:::image-end:::  

[Obtenga más información sobre la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

Las secciones siguientes anuncian características adicionales disponibles en Microsoft Edge 81 que se contribuyeron al proyecto de código Chromium abierto.  

### <a name="moto-g4-support-in-device-mode"></a>Compatibilidad con Moto G4 en modo dispositivo  

Después [de habilitar la barra de herramientas de][DevtoolsDeviceModeIndexSimulateMobileViewport]dispositivos, simula las dimensiones de una ventanilla de Moto G4 desde la lista **Dispositivo.**  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulación de una ventanilla de Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Simulación de una ventanilla de Moto G4  
:::image-end:::  

Elija [Mostrar marco de dispositivo][DevtoolsDeviceModeIndexShowDeviceFrame] para mostrar el hardware de Moto G4 alrededor de la ventanilla.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrar el hardware de Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Mostrar el hardware de Moto G4  
:::image-end:::  

Características relacionadas:  

*   Abra el [menú comando y][DevtoolsCommandMenuIndex] ejecute el comando para realizar una captura de pantalla de la ventanilla que incluye el hardware de Moto `Capture screenshot` G4 (después de habilitar Mostrar marco de **dispositivo**).  
*   [Limita la red y la CPU para][DevtoolsDeviceModeIndexThrottleNetworkCpu] simular con mayor precisión las condiciones de navegación web de un usuario móvil.  

Chromium problema [#924693][CR924693]  

### <a name="cookie-related-updates"></a>Actualizaciones relacionadas con cookies  

#### <a name="blocked-cookies-in-the-cookies-pane"></a>Cookies bloqueadas en el panel Cookies  

El panel Cookies del panel Aplicación ahora muestra las cookies bloqueadas con un fondo amarillo.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueadas en el panel Cookies del panel Aplicación" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Cookies bloqueadas en el panel Cookies del panel Aplicación  
:::image-end:::  

Chromium problema [#1030258][CR1030258]  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a>Prioridad de cookies en el panel Cookie  

Las tablas cookies de las **herramientas de red** **y** aplicación ahora incluyen una **columna Prioridad.**  

> [!CAUTION]
> Chromium exploradores basados en cookies, como Microsoft Edge, son los únicos exploradores que admiten la prioridad de cookies.  

Chromium problema [#1026879][CR1026879]  

#### <a name="edit-all-cookie-values"></a>Editar todos los valores de cookie  

Todas las celdas de las tablas Cookie son editables ahora, excepto las celdas de la columna **Tamaño** porque esa columna representa el tamaño de red de la cookie, en bytes.  Para obtener una explicación de cada columna, vaya a [Campos][DevtoolsStorageCookiesFields].  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Edición de un valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Edición de un valor de cookie  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a>Copiar como Node.js para incluir datos de cookies  

Para obtener una expresión que incluya datos de cookies, mantenga el mouse en una solicitud de red, abra el menú contextual \(hacer clic con el botón secundario\) y elija `fetch` **Copiar**copia como  >  **Node.js capturar**.  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js captura" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Copiar como Node.js captura  
:::image-end:::  

Chromium problema [#1029826][CR1029826]  

### <a name="more-accurate-web-app-manifest-icons"></a>Iconos de manifiesto de aplicación web más precisos  

Anteriormente, el panel Manifiesto del panel Aplicación enviaba sus propias solicitudes para mostrar iconos de manifiesto de aplicación web.  DevTools ahora muestra exactamente el mismo icono de manifiesto que Microsoft Edge usa.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Iconos en el panel Manifiesto" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Iconos en el panel Manifiesto  
:::image-end:::  

Chromium problema [#985402][CR985402]  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a>Mantenga el mouse en las propiedades de contenido CSS para mostrar valores sin obtener.  

Mantenga el mouse sobre el valor de una propiedad para mostrar la versión sin obtener `content` del valor.  

Por ejemplo, en esta [demostración][CSSContentDemo] al inspeccionar el pseudo elemento se muestra una cadena de escape `p::after` en el panel **Estilos:**  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="La cadena de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   La cadena de escape  
:::image-end:::  

Cuando se mantiene el mouse en el valor, se muestra el valor sin `content` descapote.  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="El valor unescaped" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   El valor unescaped  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a>Errores de mapa de origen más detallados en la consola  

La consola ahora proporciona más detalles sobre por qué no se pudo cargar o analizar un mapa de origen.  Anteriormente, solo proporcionaba un error sin explicar lo que salió mal.  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Error de carga de mapa de origen en la consola" lightbox="../../images/2020/01/sourcemap.msft.png":::
   Error de carga de mapa de origen en la consola  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a>Configuración para deshabilitar el desplazamiento más allá del final de un archivo  

Abra [Configuración y,][DevtoolsCustomizeIndexSettings] a **** continuación, deshabilite Orígenes de preferencias Permitir el desplazamiento más allá del final del archivo para deshabilitar el comportamiento predeterminado de la interfaz de usuario que le permite desplazarse mucho más allá del final de un archivo en el  >  ****  >  **** panel Orígenes. ****  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Deshabilitar Permitir el desplazamiento más allá del final del archivo" lightbox="../../images/2020/01/settings.msft.png":::
   Deshabilitar Permitir **el desplazamiento al final del archivo en** Configuración  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="El desplazamiento más allá del final de un archivo ahora está deshabilitado en el panel Orígenes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   El desplazamiento más allá del final de un archivo ahora está deshabilitado en el panel Orígenes  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si está en Windows o macOS, considere la posibilidad de usar los canales [Microsoft Edge vista previa][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular una ventanilla móvil: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsDeviceModeIndexShowDeviceFrame]: ../../../device-mode/index.md#show-device-frame "Mostrar marco de dispositivo: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsDeviceModeIndexThrottleNetworkCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limitar la red y la CPU: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsStorageCookiesFields]: ../../../storage/cookies.md#fields "Campos: ver, editar y eliminar cookies con Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioIndex]: ../../../../visual-studio/index.md "Visual Studio | Microsoft Docs"  

[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador de Microsoft Edge Visual Studio Code extensión | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos para Microsoft Edge Visual Studio Code extensión | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos para Microsoft Edge \(Chromium\) | Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"

[TrackingPrevention]: https://blogs.windows.com/msedgedev/2019/12/03/improving-tracking-prevention-microsoft-edge-79 "Mejorar la prevención de seguimiento en Microsoft Edge de blog"

[MicrosoftEdgeInsiderAddons]: https://microsoftedge.microsoft.com/addons/detail/webhint/mlgfbihcfnkaenjpdcngdnhcpkdmcdee "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Descargar Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un Tweet"  

[CR924693]: https://crbug.com/924693 "Solicitud de característica: Agregar Moto G4 a la lista de modo de dispositivo | Chromium Errores"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Chromium Errores"  
[CR1026879]: https://crbug.com/1026879 "La pestaña Cookie de la consola de desarrollo ya no muestra prioridad | Chromium Errores"  
[CR1029826]: https://crbug.com/1029826 "pestaña de red -> derecho elegir solicitar -> copia -> copia ya que la captura no copia las cookies | Chromium Errores"  
[CR985402]: https://crbug.com/985402 "Las cadenas de error de icono de manifiesto de la aplicación web son confusas | Chromium Errores"  
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Chromium Errores"  
[CR941561]: https://crbug.com/941561 "Localizabilidad del | Chromium Errores"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Errores"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demostración de contenido CSS sin descapote"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://webwewant.fyi "La web que queremos"  
[AccessibilityInsights]: https://accessibilityinsights.io "Accessibility Insights"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "Z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[Webhint]: https://webhint.io "webhint"  

[WebhintBrowserExtension]: https://webhint.io/docs/user-guide/extensions/extension-browser "Extensión de explorador Webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://webhint.io/docs/user-guide/extensions/vscode-webhint "Webhint Visual Studio Code extensión | documentación de webhint"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-81) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  