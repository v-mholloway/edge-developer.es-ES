---
description: Mejoras de accesibilidad, con el DevTools en otros idiomas, y mucho más.
title: Novedades de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 8f82f46cd683433a37614bcf15745e1de9f31ffb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015471"
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

# Novedades de DevTools (Microsoft Edge 80)  

## Anuncios del equipo de Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge. Compruébelos para probar nuevas características en DevTools, Visual Studio Code Extensions y mucho más.  Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].  

### Mejoras de accesibilidad para el DevTools  

El equipo de DevTools ha contribuido a 170 cambios en cromo para solucionar problemas de alto impacto en el contraste de color, el teclado y el lector de pantalla en el DevTools.  Cada desarrollador que crea la web debe poder usar el DevTools.  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   La herramienta de **rendimiento** en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla  
:::image-end:::  

¿Desea saber cómo hacer que su página web sea accesible para todos los usuarios?  Descargue [Insight Insights][AccessibilityInsights] y extensiones [Webhint][WebhintBrowserExtension] para Microsoft Edge para comenzar.  

Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíe sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#963183][CR963183] de problemas de cromo  

### Usar el DevTools en otros idiomas  

Muchos programadores usan otras herramientas de desarrollo, como StackOverflow y Visual Studio, en su idioma nativo, no solo en inglés.  Nos complace anunciar la localización de la DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:  

:::row:::
   :::column span="":::
      Chino \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chino (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Francés: Francisco&#231;AIS
   :::column-end:::
   :::column span="":::
      Alemán-Deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italiano-Italiano
   :::column-end:::
   :::column span="":::
       &#26085;&#26412;&#35486; japonés
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Coreano:  &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Portugués-Portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Ruso:  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Español-Espa&#241;ol
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

Vaya a `edge://flags` y establezca la marca **Habilitar herramientas de desarrollo localizadas** en **habilitado**.  También establezca el marcador de **experimentos de herramientas de desarrollo** en **habilitado**.  Reinicie Microsoft Edge y abra el DevTools.  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  El DevTools coincide con el idioma que usas para Microsoft Edge en `edge://settings/languages` .  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="El DevTools en alemán" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   El DevTools en alemán  
:::image-end:::  

Si desea usar la DevTools en un idioma diferente al de los que están disponibles, [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#941561][CR941561] de problemas de cromo  

### extensión webhint de Microsoft Edge  

La extensión webhint de Microsoft Edge te permite examinar fácilmente tu página web y obtener comentarios sobre la accesibilidad, la compatibilidad de explorador, la seguridad, el rendimiento y mucho más dentro de la DevTools.  Para obtener más información, consulte [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   La pestaña **sugerencias** de la DevTools cuando está instalada la extensión de explorador webhint  
:::image-end:::  

[Prueba la extensión de explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].  Una vez que haya instalado la extensión, abra el DevTools y seleccione la pestaña sugerencias.  Desde aquí, ejecute un examen de sitios personalizable.  Visita [webhint.IO][WebhintBrowserExtension] para obtener más información.

### Vista 3D  

Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objeto de documento \ (Dom \)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z][MDNZIndex] .  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Vista 3D en el DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   **Vista 3D** en el DevTools  
:::image-end:::  

Para obtener acceso a la vista 3D, vaya a `edge://flags` y asegúrese de que el indicador **experimentos de herramientas para desarrolladores** está **habilitado**.  Reinicie Microsoft Edge y abra el DevTools.  Pulsa `F1` en la DevTools o ve a **configuración**, ve a sección **experimentos** y marca la casilla **Habilitar vista 3D** .  Ahora, pulse `Ctrl`  +  `Shift`  +  `P` , escriba en la **vista 3D** y seleccione **Mostrar vista en 3D**.  

Trabajamos en la interfaz de usuario y agregamos más funciones a la vista 3D; por lo tanto, envíanos tus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team).  

[#987787][CR987787] de problemas de cromo

### Extensiones de código de Visual Studio  

El equipo de DevTools también ha publicado algunas extensiones para [código Visual Studio][VisualStudioCode] que te permiten usar la potencia de DevTools directamente desde tu editor de texto. Consulta las siguientes extensiones.  

#### Elementos de Microsoft Edge  

Use la herramienta elementos de Visual Studio para agregar los elementos de la extensión de código de Visual Studio [Microsoft Edge (cromo)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="La herramienta elementos en Visual Studio código que usa los elementos de la extensión de Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   La herramienta **elementos** en Visual Studio código que usa los elementos de la extensión de Microsoft Edge  
:::image-end:::  

Para obtener más información, consulta [los elementos de la extensión de código de Microsoft Edge Visual Studio][VisualStudioCodeElementEdgeExtension].  

#### Depurador para Microsoft Edge  

Con el [depurador de la extensión de código de Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio, depura JavaScript ejecutándose directamente en Microsoft Edge desde el código de Visual Studio.  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="El depurador para la extensión de Microsoft Edge en Visual Studio Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   El depurador para la extensión de Microsoft Edge en Visual Studio Code  
:::image-end:::  

Para obtener más información, consulte [Cómo depurar Microsoft Edge desde código de Visual Studio][VisualStudioCodeDebuggerEdgeExtension].  

#### webhint  

La extensión de código [webhint][VisualStudioMarketplaceWebhintExtension] de Visual Studio usa `webhint` para mejorar la página web mientras estás escribiendo. Esta extensión ejecuta y notifica diagnósticos en los archivos de área de trabajo según el `webhint` análisis.  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Extensión de código webhint de Visual Studio que analiza un archivo. TSX en código de Visual Studio" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   Extensión de código webhint de Visual Studio que analiza un `.tsx` archivo en código Visual Studio  
:::image-end:::  

[Más información sobre la extensión webhint de Visual Studio Code][WebhintVisualStudioCodeExtension].  

### Integración con Visual Studio
En Visual Studio 2019 versión 16,2 o posterior, usa el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.  [Descarga Visual Studio 2019][MicrosoftVisualStudioDownloads] para probar esta característica.  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta" lightbox="../../images/2019/12/vs.msft.png":::
   Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta  
:::image-end:::  

[Lea nuestra entrada de blog para obtener información sobre cómo depurar Microsoft Edge desde Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].  

### Mensajes de la consola de prevención de seguimiento  

La prevención de seguimiento es una característica exclusiva de Microsoft Edge que le protege de ser rastreada por los sitios web que no ha visitado antes.  La configuración predeterminada de prevención de rastreo es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores maliciosos conocidos para obtener una experiencia que equilibre la compatibilidad de la privacidad y la Web.  Para obtener más información sobre la compatibilidad de su página web cuando se bloquean determinados rastreadores, también hemos añadido mensajes de advertencia en la consola cuando se bloquea un rastreador.  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   Mensajes en la **consola** cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador  
:::image-end:::  

[Obtenga más información acerca de la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web][TrackingPrevention].  

## Anuncios del proyecto de cromo  

En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 80 que se han contribuido al proyecto de código abierto.  

### Compatibilidad con las redeclaraciones Let y Class en la consola  

La **consola** ahora es compatible con las declaraciones `let` e `class` instrucciones.  La incapacidad de redeclarar fue una molestia común para los desarrolladores web que usan la consola para experimentar con el nuevo código de JavaScript.  

> [!WARNING]
> La Redeclaración de `let` una `class` instrucción or en una secuencia de comandos fuera de la consola o dentro de una sola entrada de consola sigue produciendo un `SyntaxError` .  

Por ejemplo, antes, al volver a declarar una variable local con `let` , la consola producía un error:  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="La consola en Microsoft Edge 79 que muestra que no se puede realizar la Redeclaración" lightbox="../../images/2019/12/letbefore.msft.png":::
   La **consola** en Microsoft Edge 79 que indica que se produce un error en Let de volver a declarar  
:::image-end:::  

Ahora, la consola permite la nueva declaración:  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="La consola en Microsoft Edge 80, que muestra que la Redeclaración Let se realiza correctamente" lightbox="../../images/2019/12/letafter.msft.png":::
   La **consola** en Microsoft Edge 80, que muestra que la nueva declaración se realiza correctamente  
:::image-end:::  

[#1004193][CR1004193] de problemas de cromo  

### Depuración de webassembler mejorada  

DevTools ha empezado a admitir el [estándar de depuración Dwarf][DwarfHome], lo que significa que se ha mejorado la compatibilidad para desplazarse por el código, establecer puntos de interrupción y resolver los rastros de pila en los idiomas de origen en DevTools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### Actualizaciones del panel de red  

#### Solicitar cadenas de iniciador en la ficha Initiator  

Ahora puede ver los iniciadores y las dependencias de una solicitud de red como una lista anidada.  Esto puede ayudarle a comprender por qué se solicitó un recurso o la actividad de la red que un determinado recurso \ (como un script \) ha causado.  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Una cadena de iniciador de solicitudes en la ficha Initiator" lightbox="../../images/2019/12/initiators.msft.png":::
   Una cadena de iniciador de solicitudes en la ficha **Initiator**  
:::image-end:::  

Después [de registrar la actividad de la red en el panel red][DevToolsNetworkIndex], haga clic en un recurso y, a continuación, vaya a la pestaña **iniciador** para ver la **cadena de iniciadores de solicitudes**:  

*   El **recurso inspeccionado** está en negrita.  En la captura de pantalla anterior, `ai.2.min.js` se encuentra el recurso inspeccionado.  
*   Los recursos situados por encima del recurso inspeccionado son los **iniciadores**.  En la captura de pantalla anterior, `https://www.microsoftedgeinsider.com` se trata del iniciador de `ai.2.min.js` .  En otras palabras, `https://www.microsoftedgeinsider.com` causó la solicitud de red `ai.2.min.js` .  
*   Los recursos que se encuentran debajo del recurso inspeccionado son las **dependencias**.  En la captura de pantalla anterior, `https://dc.services.visualstudio.com/v2/track` se trata de una dependencia de `ai.2.min.js` .  En otras palabras, `ai.2.min.js` causó la solicitud de red `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> También se puede tener acceso a la información del iniciador y la dependencia si se mantiene presionado `Shift` y, a continuación, coloca el puntero sobre recursos de red.  Consulte [Ver iniciadores y dependencias][DevToolsNetworkReferenceViewInitiatorsDependencies].  

[#842488][CR842488] de problemas de cromo  

#### Resaltar la solicitud de red seleccionada en la información general  

Después de hacer clic en un recurso de red para inspeccionarlo, el panel red ahora coloca un borde azul en torno a ese recurso en la **información general**.  Esto puede ayudarle a detectar si la solicitud de red se está realizando antes o después de lo esperado.  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="El panel de información general resaltando el recurso inspeccionado" lightbox="../../images/2019/12/overview.msft.png":::
   El panel de **información general** resaltando el recurso inspeccionado  
:::image-end:::  

[#988253][CR988253] de problemas de cromo  

#### Columnas URL y ruta de acceso en el panel red  

Use las nuevas columnas de **dirección URL** y **ruta de acceso** del panel **red** para ver la ruta de acceso absoluta o la dirección URL completa de cada recurso de red.  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Las nuevas columnas de dirección URL y ruta de acceso del panel red" lightbox="../../images/2019/12/columns.msft.png":::
   Las nuevas columnas de dirección URL y ruta de acceso del panel **red**  
:::image-end:::  

Haga clic con el botón secundario en el encabezado de tabla **cascada** y seleccione **ruta** o **dirección URL** para mostrar las nuevas columnas.  

[#993366][CR993366] de problemas de cromo  

#### Cadenas de agente de usuario actualizadas  

DevTools admite la configuración de una cadena de agente de usuario personalizada en la pestaña **condiciones de red** .  La cadena de agente de usuario afecta al `User-Agent` encabezado HTTP adjunto a los recursos de red y también al valor de `navigator.userAgent` .  

Las cadenas de agente de usuario predefinidas se han actualizado para reflejar las versiones modernas del explorador.  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="El menú agente de usuario en la pestaña condiciones de red" lightbox="../../images/2019/12/useragent.msft.png":::
   El menú agente de usuario en la pestaña **condiciones de red**  
:::image-end:::  

Para obtener acceso a **condiciones**de la red, [Abra el menú de comandos][DevToolsCommandMenuIndex] y ejecute el `Show Network Conditions` comando.  

> [!NOTE]
> También puede [establecer cadenas de agente de usuario en el modo de dispositivo][DevToolsDeviceModeIndex].  

[#1029031][CR1029031] de problemas de cromo  

### Actualizaciones del panel auditorías  

#### Nueva interfaz de usuario de configuración  

La interfaz de usuario de configuración tiene un diseño nuevo y con capacidad de respuesta, y las opciones de configuración de límite se han simplificado.  Para obtener más información sobre los cambios de la interfaz de usuario de regulación, consulte [regulación del panel auditorías][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="La nueva interfaz de usuario de configuración" lightbox="../../images/2019/12/start.msft.png":::
   La nueva interfaz de usuario de configuración  
:::image-end:::  

### Actualizaciones de la ficha cobertura  

#### Modos de cobertura por función o por bloque  

La [pestaña cobertura][DevToolsCoverageIndex] tiene un nuevo menú desplegable que le permite especificar si se deben recopilar datos de cobertura de código **por función** o **por bloque**.  La cobertura **por bloque** es más detallada, pero es mucho más costosa de recopilar.  De forma predeterminada, DevTools usa la cobertura de **por función** .  

> [!CAUTION]
> Es posible que vea diferencias de cobertura de código de gran tamaño en archivos HTML dependiendo de si usa **por función** o **por bloque** .  Al usar el modo **por función** , las secuencias de comandos en línea de archivos HTML se tratan como funciones.  Si se ejecuta la secuencia de comandos, DevTools marca la secuencia de comandos completa como código usado.  Solo si el script no se ejecuta, DevTools marca el script como código no usado.  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="El menú desplegable modo de cobertura" lightbox="../../images/2019/12/modes.msft.png":::
   El menú desplegable modo de cobertura  
:::image-end:::  

#### La cobertura debe iniciarse ahora al volver a cargar una página  

Se ha quitado la cobertura de código sin que se recargue la página porque los datos de cobertura eran inconfiables.  Por ejemplo, se puede notificar que una función no se usa si el tiempo de ejecución fue de larga duración y el recolector de elementos no utilizados de la V8 ha limpiado.  

[#1004203][CR1004203] de problemas de cromo  

## Descargar los canales de Microsoft Edge Preview  

Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools | Microsoft docs"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular un área de visualización móvil: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft docs"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Inspeccionar la actividad de la red en Microsoft Edge DevTools | Microsoft docs"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Ver iniciadores y dependencias: referencia de análisis de red | Microsoft docs"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Novedades de EdgeHTML | Microsoft docs"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para la extensión de código de Microsoft Edge Visual Studio | Microsoft docs"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos de la extensión de código de Microsoft Edge Visual Studio | Microsoft docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Agregue el campo Initiator a la ficha encabezados | Errores de cromo"  
[CR988253]: https://crbug.com/988253 "Error DevTools: no hay ninguna asociación entre la solicitud de red y el gráfico de escala de tiempo | Errores de cromo"  
[CR993366]: https://crbug.com/993366 "Muestra la parte ruta de la URL en la lista de solicitudes del panel red | Errores de cromo"  
[CR1004193]: https://crbug.com/1004193 "Modo de REPL para V8 | Errores de cromo"  
[CR1004203]: https://crbug.com/1004203 "Hacer la cobertura de código increíble | Errores de cromo"  
[CR1029031]: https://crbug.com/1029031 "Las cadenas UA están anticuadas | Errores de cromo" 
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Errores de cromo"
[CR941561]: https://crbug.com/941561 "Localizabilidad de la DevTools | Errores de cromo"
[CR987787]: https://crbug.com/987787 "Vista 3D de Dom | Errores de cromo"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Información de accesibilidad"  

[DwarfHome]: https://dwarfstd.org "Dwarf hogar"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools de la pantalla de auditorías de GoogleChrome/Lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos de Insider de Microsoft Edge"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Depurar JavaScript en Microsoft Edge desde Visual Studio | Blog de Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Descargar Visual Studio 2019 para Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "índice z | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Código de Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Marketplace de Visual Studio"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos de Microsoft Edge \ (cromo \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-catálogo de soluciones de Visual Studio"
[Webhint]: https://aka.ms/webhint "sugerencia"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensión de explorador webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extensión de código webhint de Visual Studio | documentación de webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Mejorar la prevención de seguimiento en la entrada de blog de Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2019/12/devtools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
