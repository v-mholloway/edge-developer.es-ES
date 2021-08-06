---
description: Mejoras en la accesibilidad, con DevTools en otros idiomas y mucho más.
title: Novedades de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: d633a3c21d2fbc9968914265f5e2da933075d98a49ad3b18369a797afb589c1e
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11799051"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a>Novedades de DevTools (Microsoft Edge 80)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Anuncios del equipo Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo Microsoft Edge DevTools.  Echa un vistazo a los anuncios para probar nuevas características en DevTools, Microsoft Visual Studio code extensions y mucho más.  Para mantenerse al día de todas las características más recientes [][MicrosoftEdgePreviewChannels] y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa Microsoft Edge y [síganos en Twitter][EdgeDevToolsTwitterAccount].  

### <a name="accessibility-improvements-to-the-devtools"></a>Mejoras de accesibilidad a DevTools  

El equipo de DevTools ha contribuido con 170 cambios en Chromium para solucionar problemas de contraste de color, teclado y lector de pantalla de alto impacto en DevTools.  Cada desarrollador que esté creando la web debe poder usar DevTools.  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="La herramienta Rendimiento de DevTools con las mejoras de navegación del teclado y lector de pantalla" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   La **herramienta Rendimiento** de DevTools con las mejoras de navegación del teclado y lector de pantalla  
:::image-end:::  

¿Desea obtener información sobre cómo hacer que la página web sea accesible para todos los usuarios?  Descargue [las extensiones de Ideas][AccessibilityInsights] accesibilidad [y webhint][WebhintBrowserExtension] Microsoft Edge para empezar.  

Si usas lectores de pantalla o el teclado para [][PostTweetEdgeDevTools] navegar por devTools, envía tus comentarios tuiteando o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

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
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Vaya a y establezca la marca Habilitar herramientas de `edge://flags` **desarrollo** localizadas en **Habilitado**.  También establece la **marca de experimentos de Herramientas para desarrolladores** en **Habilitado**.  Reinicie Microsoft Edge y abra DevTools.  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  Las DevTools coinciden con el idioma que usa para Microsoft Edge en `edge://settings/languages` .  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="DevTools en alemán" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   DevTools en alemán  
:::image-end:::  

Si quieres usar DevTools en un idioma diferente al que está [disponible,][PostTweetEdgeDevTools] envíanos un tweet o elige el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Chromium problema [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>extensión webhint Microsoft Edge webhint  

La extensión webhint Microsoft Edge le permite examinar fácilmente la página web y obtener comentarios sobre accesibilidad, compatibilidad del explorador, seguridad, rendimiento y mucho más dentro de DevTools.  Leer más en [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="La herramienta Sugerencias en DevTools cuando se instala la extensión del explorador webhint" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   La **herramienta Sugerencias** en DevTools cuando se instala la extensión del explorador webhint  
:::image-end:::  

[Pruebe la extensión del explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].  Una vez instalada la extensión, abra DevTools y elija la **herramienta Sugerencias.**  Desde aquí, ejecute un examen de sitio personalizable.  Dirígete a [webhint.io][WebhintBrowserExtension] para obtener más información.

### <a name="3d-view"></a>Vista 3D  

Use la **vista 3D** para depurar la aplicación web navegando por el modelo de objetos de documento [\(DOM\)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z.][MDNZIndex]  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="La vista 3D en DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   La **vista 3D en** DevTools  
:::image-end:::  

Para obtener acceso a la vista 3D, vaya a y asegúrese de que la marca de experimentos de `edge://flags` **Developer Tools** está establecida en **Enabled**.  Reinicie Microsoft Edge y abra DevTools.  Seleccione en la sección DevTools o abra la sección Configuración experimentos y active la casilla Habilitar vista `F1` ****  >  **** **3D.**  Ahora, seleccione `Ctrl`  +  `Shift`  +  `P` , escriba en **Vista 3D** y **seleccione Mostrar vista 3D**.  

Estamos trabajando en la interfaz de usuario y agregando más funcionalidad a la vista 3D, así que envíenos sus [comentarios.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium problema [#987787][CR987787]

### <a name="visual-studio-code-extensions"></a>Visual Studio Code de datos  

El equipo de DevTools también [][VisualStudioCode] ha publicado algunas extensiones para Visual Studio Code que le permiten usar la potencia de DevTools directamente desde el editor de texto. Consulte las siguientes extensiones.  

#### <a name="elements-for-microsoft-edge"></a>Elementos para Microsoft Edge  

Usa la herramienta Elementos desde dentro de Visual Studio Code agregando la [extensión Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="La herramienta Elementos de Visual Studio Code la extensión Elements for Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   La **herramienta Elementos** de Visual Studio Code la extensión Elements for Microsoft Edge  
:::image-end:::  

Para obtener más información, consulte [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].  

#### <a name="debugger-for-microsoft-edge"></a>Depurador de Microsoft Edge  

Con la [extensión Depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depura JavaScript que se ejecuta en Microsoft Edge directamente desde Visual Studio Code.  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="El depurador de Microsoft Edge de Visual Studio Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   El depurador de Microsoft Edge de Visual Studio Code  
:::image-end:::  

Para obtener más información, [consulte cómo depurar][VisualStudioCodeDebuggerEdgeExtension]Microsoft Edge desde Visual Studio Code .  

#### <a name="webhint"></a>webhint  

La [extensión webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code para `webhint` mejorar tu página web mientras la estás escribiendo. Esta extensión ejecuta e informa de diagnósticos en los archivos del área de trabajo en función del `webhint` análisis.  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="La extensión webhint Visual Studio Code analizar un archivo .tsx en Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   La extensión webhint Visual Studio Code análisis de un `.tsx` archivo en Visual Studio Code  
:::image-end:::  

[Obtenga más información sobre la Visual Studio Code webhint][WebhintVisualStudioCodeExtension].  

### <a name="visual-studio-integration"></a>Visual Studio integración  

En Visual Studio versión 16.2 o posterior de 2019, use el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.  [Descargue Visual Studio 2019][MicrosoftVisualStudioDownloads] para probar esta característica.  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta" lightbox="../../images/2019/12/vs.msft.png":::
   Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta  
:::image-end:::  

[Lea nuestra entrada de blog para obtener información sobre][MicrosoftVisualStudioBlogDebugJavascript]cómo depurar Microsoft Edge desde Visual Studio .  

### <a name="tracking-prevention-console-messages"></a>Seguimiento de mensajes de consola de prevención  

La prevención de seguimiento es una característica única en Microsoft Edge que impide que un sitio web le realice un seguimiento antes de visitarlo.  La configuración predeterminada de prevención de seguimiento es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores malintencionados conocidos para una experiencia que equilibra la privacidad y la compatibilidad web.  Para obtener más información sobre la compatibilidad de la página web cuando se bloquean determinados **** rastreadores, el equipo de Microsoft Edge agregó mensajes de advertencia en la consola cuando se bloquea un rastreador.  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Mensajes en la consola cuando la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   Mensajes en la **consola cuando** la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador  
:::image-end:::  

[Obtenga más información sobre la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

En las secciones siguientes se anuncian características adicionales disponibles en Microsoft Edge 80 que se contribuyeron al proyecto de código Chromium abierto.  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a>Compatibilidad con las declaraciones de let y class en la consola  

La **consola** ahora admite las declaraciones de y `let` las `class` instrucciones.  La incapacidad de volver a declarar era una molestia común para los desarrolladores web que usan la consola para experimentar con el nuevo código JavaScript.  

> [!WARNING]
> La declaración de una instrucción or en un script fuera de la consola o dentro de una sola entrada `let` `class` de consola sigue provocando un `SyntaxError` .  

Por ejemplo, anteriormente, al volver a declarar una variable local con , la `let` consola produjo un error:  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="La consola de Microsoft Edge 79 que muestra que se produce un error en la nueva declaración de let" lightbox="../../images/2019/12/letbefore.msft.png":::
   La **consola** de Microsoft Edge 79 que muestra que se produce un error en la nueva declaración de let  
:::image-end:::  

Ahora, la consola permite la nueva declaración:  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="La consola de Microsoft Edge 80 que muestra que la nueva declaración de let se realiza correctamente" lightbox="../../images/2019/12/letafter.msft.png":::
   La **consola** de Microsoft Edge 80 que muestra que la nueva declaración de let se realiza correctamente  
:::image-end:::  

Chromium problema [#1004193][CR1004193]  

### <a name="improved-webassembly-debugging"></a>Depuración de WebAssembly mejorada  

DevTools ha comenzado a admitir el estándar de depuración DEANAR, lo que significa una mayor compatibilidad para pasar por encima del código, establecer puntos de interrupción y resolver seguimientos de pila en los idiomas de origen dentro de DevTools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a>Actualizaciones del panel de red  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a>Solicitar cadenas de iniciador en el panel Iniciador  

Ahora puede ver los iniciadores y las dependencias de una solicitud de red como una lista anidada.  Esto puede ayudarle a comprender por qué se solicitó un recurso o qué actividad de red causó un determinado recurso \(como un script\).  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Una cadena de iniciador de solicitud en el panel Iniciador" lightbox="../../images/2019/12/initiators.msft.png":::
   Una cadena de iniciador de solicitud en el panel **Iniciador**  
:::image-end:::  

Después [de registrar la actividad de red en el panel][DevToolsNetworkIndex]Red, elija un recurso y, a continuación, vaya al panel Iniciador para ver la Cadena de **iniciador de solicitud**: ****  

*   El **recurso inspeccionado** es negrita.  En la captura de pantalla anterior, `ai.2.min.js` está el recurso inspeccionado.  
*   Los recursos que se encuentran encima del recurso inspeccionado son **los iniciadores**.  En la captura de pantalla anterior, `https://www.microsoftedgeinsider.com` está el iniciador de `ai.2.min.js` .  En otras palabras, `https://www.microsoftedgeinsider.com` causó la solicitud de red para `ai.2.min.js` .  
*   Los recursos debajo del recurso inspeccionado son las **dependencias**.  En la captura de pantalla anterior, `https://dc.services.visualstudio.com/v2/track` es una dependencia de `ai.2.min.js` .  En otras palabras, `ai.2.min.js` causó la solicitud de red para `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> También se puede tener acceso a la información del iniciador y la dependencia manteniendo presionado y, a `Shift` continuación, manteniendo el mouse sobre los recursos de red.  Vaya a [Ver iniciadores y dependencias][DevToolsNetworkReferenceDisplayInitiatorsDependencies].  

Chromium problema [#842488][CR842488]  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a>Resalte la solicitud de red seleccionada en información general  

Después de elegir un recurso de red para inspeccionarlo, el panel Red coloca ahora un borde azul alrededor de ese recurso en **overview**.  Esto puede ayudarle a detectar si la solicitud de red se está produciendo antes o después de lo esperado.  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="El panel Información general que resalta el recurso inspeccionado" lightbox="../../images/2019/12/overview.msft.png":::
   El **panel Información** general que resalta el recurso inspeccionado  
:::image-end:::  

Chromium problema [#988253][CR988253]  

#### <a name="url-and-path-columns-in-the-network-panel"></a>Columnas de dirección URL y ruta de acceso en el panel Red  

Use las nuevas columnas **Path** y **URL** de la **herramienta Red** para mostrar la ruta de acceso absoluta o la dirección URL completa de cada recurso de red.  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Las nuevas columnas Ruta de acceso y dirección URL en el panel Red" lightbox="../../images/2019/12/columns.msft.png":::
   Las nuevas columnas Ruta de acceso y DIRECCIÓN URL de la **herramienta Red**  
:::image-end:::  

Para mostrar las nuevas columnas, mantenga el mouse en el encabezado de la tabla **Cascada,** abra el menú contextual \(righ-click\) y elija **Ruta** de acceso o **dirección URL**.  

Chromium problema [#993366][CR993366]  

#### <a name="updated-user-agent-strings"></a>Cadenas User-Agent actualizadas  

DevTools admite la configuración de una cadena User-Agent a través del panel **Condiciones de** red.  La User-Agent la cadena afecta al encabezado HTTP adjunto a los recursos de red `User-Agent` y también al valor de `navigator.userAgent` .  

Las cadenas User-Agent se han actualizado para reflejar las versiones modernas del explorador.  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Menú Agente de usuario en el panel Condiciones de red" lightbox="../../images/2019/12/useragent.msft.png":::
   Menú Agente de usuario en el panel **Condiciones de red**  
:::image-end:::  

Para obtener **acceso a las condiciones de**red, abra el menú [comando][DevToolsCommandMenuIndex] y ejecute el `Show Network Conditions` comando.  

> [!NOTE]
> También puedes establecer [cadenas User-Agent en modo dispositivo][DevToolsDeviceModeIndex].  

Chromium problema [#1029031][CR1029031]  

### <a name="audits-panel-updates"></a>Actualizaciones del panel Auditorías  

#### <a name="new-configuration-ui"></a>Nueva interfaz de usuario de configuración  

La interfaz de usuario de configuración tiene un diseño nuevo y dinámico y se han simplificado las opciones de configuración de limitación.  Para obtener más información sobre los cambios de la interfaz de usuario de limitación, vaya a [Limitación del panel auditorías][GitHubGoogleChromeDevToolsAuditsPanelThrottling].  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="La nueva interfaz de usuario de configuración" lightbox="../../images/2019/12/start.msft.png":::
   La nueva interfaz de usuario de configuración  
:::image-end:::  

### <a name="coverage-tool-updates"></a>Actualizaciones de la herramienta de cobertura  

#### <a name="per-function-or-per-block-coverage-modes"></a>Modos de cobertura por función o por bloque  

La [herramienta Cobertura][DevToolsCoverageIndex] tiene un nuevo menú desplegable que le permite especificar si los datos de cobertura de código deben recopilarse por **función** o **por bloque**.  **La cobertura por** bloque es más detallada, pero también mucho más costosa de recopilar.  DevTools usa **la cobertura por** función de forma predeterminada ahora.  

> [!CAUTION]
> Es posible que observe grandes diferencias de cobertura de código en los archivos HTML en función de si usa **por función** o por **modo de** bloque.  Cuando se **usa por modo** de función, los scripts en línea en archivos HTML se tratan como funciones.  Si el script se ejecuta en absoluto, DevTools marca todo el script como código usado.  Solo si el script no se ejecuta en absoluto, DevTools marca el script como código no usado.  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Menú desplegable del modo de cobertura" lightbox="../../images/2019/12/modes.msft.png":::
   Menú desplegable del modo de cobertura  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a>La cobertura debe iniciarse ahora mediante una actualización de página  

Se ha quitado la cobertura de código de alternar sin una actualización de página porque los datos de cobertura no son confiables.  Por ejemplo, una función puede ser notificada como no usada si el tiempo de ejecución estaba hace mucho tiempo y el recolector de elementos no utilizados V8 la ha limpiado.  

Chromium problema [#1004203][CR1004203]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si está en Windows o macOS, considere la posibilidad de usar los canales [Microsoft Edge vista previa][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Busque código JavaScript y CSS sin usar con la herramienta Cobertura en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular una ventanilla móvil: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkIndex]: ../../../network/index.md "Inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Mostrar iniciadores y dependencias: referencia de análisis de red | Microsoft Docs"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador de Microsoft Edge Visual Studio Code extensión | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos para Microsoft Edge Visual Studio Code extensión | Microsoft Docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Agregue el campo Iniciador a la pestaña Encabezados | Chromium Errores"  
[CR988253]: https://crbug.com/988253 "Bug DevTools: ninguna asociación entre la solicitud de red y la escala de tiempo Graph | Chromium Errores"  
[CR993366]: https://crbug.com/993366 "Muestre la parte de ruta de acceso de la dirección URL en la lista de solicitudes de panel de red | Chromium Errores"  
[CR1004193]: https://crbug.com/1004193 "Modo REPL para V8 | Chromium Errores"  
[CR1004203]: https://crbug.com/1004203 "Hacer que la cobertura de código sea | Chromium Errores"  
[CR1029031]: https://crbug.com/1029031 "Las cadenas UA se están volviendo obsoletas | Chromium Errores" 
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Chromium Errores"
[CR941561]: https://crbug.com/941561 "Localizabilidad del | Chromium Errores"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Errores"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Accesibilidad Ideas"  

[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Limitación del panel de auditorías de DevTools: GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Vista previa de canales"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Depurar JavaScript en Microsoft Edge desde Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Descargar Visual Studio 2019 para Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "Z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge: Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint: Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensión de explorador Webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Code extensión | documentación de webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Mejorar la prevención de seguimiento en Microsoft Edge de blog"
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-80) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
