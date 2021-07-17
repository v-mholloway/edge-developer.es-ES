---
description: El botón Más herramientas, documentación en contexto para empezar a usar la extensión DevTools, mayor compatibilidad para lectores de pantalla en la consola y mucho más.
title: Novedades de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 09e1438ae7fd6547a7dd14757f54f370c9008773
ms.sourcegitcommit: 1dd6376784c394087fe2938acaa069212cf7656e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2021
ms.locfileid: "11659431"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a>Novedades de DevTools (Microsoft Edge 92)

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]

> [!TIP]
> La **conferencia de Microsoft Build 2021** fue del 25 al 27 de mayo.  Este es un vídeo de Build about the updates to DevTools: [Microsoft Edge | Estado de la plataforma:][YoutubeEdgeStateOfThePlatform] Microsoft Edge una plataforma atractiva y coherente con herramientas para desarrolladores.  A medida que nuestros exploradores heredados no sean compatibles, Edge pronto será el único explorador compatible de Microsoft en Windows 10.  Únase a nosotros para obtener información sobre lo último en la plataforma perimetral, las herramientas y las aplicaciones web.


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a>El botón Cerrar ya no está oculto cuando DevTools es estrecho

<!-- Title: DevTools is now easier to close -->
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->

En Microsoft Edge versión 91 o anterior, el botón Cerrar para cerrar DevTools no se muestra cuando la ventanilla de DevTools es estrecha. ****  En Microsoft Edge versión 92, **** el botón Cerrar de DevTools siempre está presente, independientemente del ancho de la ventanilla de DevTools.

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="El botón Cerrar DevTools ahora está presente incluso cuando la ventanilla es estrecha" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   El **botón Cerrar** DevTools ahora está presente incluso cuando la ventanilla es estrecha
:::image-end:::


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a>Agregar herramientas rápidamente con el nuevo botón Más herramientas

<!-- Title: Add tools quickly with the new More Tools button -->
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->

Hay una nueva forma de abrir más herramientas en Microsoft Edge DevTools: el **menú Más herramientas** ( ) `+` . El **menú Más herramientas** aparece en la barra de herramientas del panel principal y en la barra de herramientas del cajón. Al seleccionar una herramienta en el **menú Más herramientas,** se agrega la herramienta a la barra de herramientas.

Para reordenar las pestañas de cualquiera de las barras de herramientas, seleccione y arrastre las pestañas.

El **menú Más herramientas** estaba disponible como un experimento en Microsoft Edge versión 89 y ahora siempre está presente.

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="El botón Más herramientas de la barra de herramientas superior y la barra de herramientas del cajón" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   El **botón Más herramientas** de la barra de herramientas superior y la barra de herramientas del cajón
:::image-end:::

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menú Más herramientas" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   Menú **Más** herramientas
:::image-end:::


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a>Mejoras para activar, seleccionar y cerrar herramientas

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

Las pestañas de cada herramienta se han reformateado para reducir la posibilidad de cerrar accidentalmente una herramienta.  En cada pestaña de la barra de herramientas principal y en la barra de herramientas del cajón, agregamos:
*  Espaciado alrededor de la pestaña.
*  Espaciado alrededor del botón cerrar ( `x` ) de la ficha.
*  Color de fondo al pasar el mouse sobre la pestaña.
*  Información sobre herramientas para el botón cerrar ( `x` ) de la pestaña.
*  Contraste superior para el botón cerrar ( `x` ) de la ficha.

Por ejemplo, cuando estás **** en la herramienta **** Rendimiento y mantienes el mouse sobre la pestaña de la herramienta Red, estas mejoras ayudan a evitar el cierre accidental de la **herramienta Red.**

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Pestañas antes de reformatear" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           Pestañas antes de reformatear :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Pestañas después de la reformateado" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           Pestañas después de la reformateado :::image-end:::
    :::column-end:::
:::row-end:::

Estas mejoras son especialmente relevantes para los usuarios de DevTools localizados, en los que las pestañas pueden ser más estrechas y fáciles de cerrar accidentalmente.

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="Localized DevTools con pestañas estrechas" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   Localized DevTools con pestañas estrechas
:::image-end:::

También facilitamos volver a agregar una herramienta que ha cerrado agregando un menú Más herramientas [a](#add-tools-quickly-with-the-new-more-tools-button) la barra de herramientas principal y la barra de herramientas del cajón.


## <a name="better-support-for-screen-readers-in-the-console"></a>Mejor compatibilidad con lectores de pantalla en la consola

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

Antes de Microsoft Edge versión 92, en la **Consola,** las tecnologías de asistencia, como los lectores de pantalla, no anunciaban sugerencias de autocompletar ni los resultados de las expresiones evaluadas. Esto se ha corregido ahora.

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           En la **Consola,** los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian el resultado de una expresión evaluada" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           En la **consola,** ahora los lectores de pantalla anuncian el resultado de una expresión evaluada :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="source-order-viewer"></a>Visor de pedidos de origen

<!--  Title: Source Order Viewer -->
<!--  Subtitle: The new Source Order Viewer displays numbers on the webpage indicating the order of page elements in the source file, independently of how the page sections are positioned by CSS. -->

Ahora puede ver el orden de los elementos de origen sobrelaidos en la página web representada, para una mejor inspección de accesibilidad.

El orden del contenido de un documento HTML es importante para la optimización y accesibilidad del motor de búsqueda.  CSS permite a los desarrolladores crear contenido que tiene un aspecto diferente en su orden en pantalla que el orden en el documento de origen HTML.  Se trata de un problema de accesibilidad, ya que los usuarios lectores de pantalla podrían obtener una experiencia confusa.

:::image type="complex" source="../../media/2021/05/source-order-viewer.msft.png" alt-text="Al activar el Visor de pedidos de origen, se muestra el orden de los elementos del origen como superposiciones en la página" lightbox="../../media/2021/05/source-order-viewer.msft.png":::
   Al activar el **Visor de pedidos de origen,** se muestra el orden de los elementos del origen como superposiciones en la página
:::image-end:::

Para obtener más información, vaya a Probar compatibilidad [con teclado mediante el Visor de pedidos de origen](../../../accessibility/test-tab-key-source-order-viewer.md).

Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1094406][CR1094406].


## <a name="user-agent-client-hints-for-devices-in-the-network-conditions-tab"></a>User-Agent sugerencias de cliente para dispositivos en la pestaña Condiciones de red

<!--  Title: User-Agent Client Hints -->
<!--  Subtitle: Access information about a user's browser in an ergonomic way that preserves privacy. -->

User-Agent sugerencias de cliente se aplican ahora para dispositivos en el **campo Agente** de usuario de la herramienta **Condiciones de** red.  User-Agent sugerencias de cliente son una nueva expansión de la API de sugerencias de cliente que le permite tener acceso a información sobre el explorador de un usuario de una forma ergonómica que preserva la privacidad.

:::image type="complex" source="../../media/2021/05/user-agent.msft.png" alt-text="Agente de usuario" lightbox="../../media/2021/05/user-agent.msft.png":::
   Agente de usuario
:::image-end:::

Para obtener más información, vaya a [Sugerencias de cliente de agente de usuario](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints).

Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [1174299][CR1174299].


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a>Microsoft Edge Developer Tools para Visual Studio Code versión 1.1.8

El [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code tiene los siguientes cambios desde la versión anterior.  Microsoft Visual Studio Code actualiza las extensiones automáticamente.  Para actualizar manualmente a la versión 1.1.8, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]

Puede presentar problemas y contribuir a la extensión en [vscode-edge-devtools GitHub repositorio][GithubMicrosoftVscodeEdgeDevtools].

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a>Documentación e interfaz de usuario en contexto para facilitar el uso de la extensión DevTools

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->

La versión 1.1.8 de la extensión [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] ahora presenta una forma más sencilla de iniciar una nueva instancia de Microsoft Edge, presentando instrucciones, botones, vínculos y una página de documentación que le guiará.

*  Cuando selecciona el botón herramientas de **** **Microsoft Edge** en la barra de actividades de Visual Studio Code, el panel Herramientas de **Microsoft Edge:** Destinos ahora presenta texto explicativo, botones y vínculos para guiarlo, en lugar de un panel en blanco.

*  Al abrir una nueva instancia de Microsoft Edge desde dentro de Visual Studio Code, Microsoft Edge muestra ahora una página de inicio que explica cómo usar la extensión Herramientas de desarrollo, en lugar de una página en blanco.

*  El **panel herramientas Microsoft Edge:** destinos ahora tiene un botón Generar **launch.jsen** y las instrucciones, para ayudar a iniciar el proyecto para la depuración en Microsoft Edge.

Para obtener más información, vaya [a Uso de las herramientas][GithubIoDevToolsUsing].


## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]


### <a name="css-grid-editor"></a>Editor de cuadrícula CSS

Ahora puede obtener una vista previa y crear diseños de cuadrícula CSS con el nuevo editor de cuadrícula CSS.

Cuando un elemento HTML de la página tiene o se ha aplicado, se muestra un icono de cuadrícula junto a él en la pestaña Estilos. Haga clic en el icono de cuadrícula para mostrar u ocultar el editor de cuadrícula `display: grid` `display: inline-grid` CSS. **** En el editor de cuadrículas CSS, seleccione cualquiera de los iconos (por ejemplo) para obtener una vista previa del `justify-content: space-around` diseño en la página representada.  El diseño de Flex funciona de forma similar.

:::image type="complex" source="../../media/2021/05/css-grid-editor.msft.png" alt-text="Editor de cuadrícula CSS" lightbox="../../media/2021/05/css-grid-editor.msft.png":::
   Editor de cuadrícula CSS
:::image-end:::

<!-- screenshot uses https://jec.fyi -->

Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1203241][CR1203241].


### <a name="support-for-const-redeclarations-in-the-console"></a>Compatibilidad con las declaraciones de const en la consola

La consola ahora admite la reeclaración de variables en scripts REPL independientes (por ejemplo, cuando se ejecuta una instrucción en la consola), además de las `const` `let` declaraciones existentes y `class` redeclarations.  Esta compatibilidad permite experimentar con diferentes declaraciones para `const` variables sin actualizar la página.  Anteriormente, DevTools generaba un error de sintaxis si se declaraba de nuevo un `const` enlace.

Consulte el ejemplo siguiente. `const` La nueva declaración se admite en scripts REPL independientes (consulte variable `a` ).  Tenga en cuenta que los siguientes escenarios no son compatibles con el diseño:

*  `const` No se permite la reeclaración de scripts de página en scripts REPL.
*  `const` No se permite la reeclaración dentro del mismo script REPL (consulte variable `b` ).

:::image type="complex" source="../../media/2021/05/support-for-const-redeclaration.msft.png" alt-text="Se permite la declaración de una variable const en la consola" lightbox="../../media/2021/05/support-for-const-redeclaration.msft.png":::
   Se permite la declaración de una variable const en la consola
:::image-end:::

Para obtener información sobre cómo ejecutar un solo script REPL o un script REPL de varias líneas, vaya a La consola como [un entorno JavaScript](../../../console/console-javascript.md).
    
Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1076427][CR1076427].


### <a name="new-shortcut-to-view-iframe-details"></a>Nuevo acceso directo para ver detalles de iframe

Para ver rápidamente los detalles, ahora puede hacer clic con el botón secundario en un elemento de la herramienta Elementos y, a `iframe` continuación, seleccionar Mostrar detalles de `iframe` **iframe** **** .

:::image type="complex" source="../../media/2021/05/show-iframe-details.msft.png" alt-text="Vista de detalles de iframe" lightbox="../../media/2021/05/show-iframe-details.msft.png":::
   Vista de detalles de iframe
:::image-end:::

Esto muestra los detalles acerca de `iframe` la herramienta **Aplicación.**  En la **herramienta Aplicación,** puede examinar los detalles del documento, el estado de seguridad y aislamiento, la directiva de permisos y mucho más para depurar posibles problemas.

:::image type="complex" source="../../media/2021/05/show-iframe-details-application-tool.msft.png" alt-text="Detalles del marco en la herramienta Aplicación" lightbox="../../media/2021/05/show-iframe-details-application-tool.msft.png":::
   Detalles del marco en la **herramienta Aplicación**
:::image-end:::

<!-- demo page: https://wolfib.github.io/web-demos/ esp https://wolfib.github.io/web-demos/jsIframe.html -->

Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1192084][CR1192084].


### <a name="enhanced-cors-debugging-support"></a>Compatibilidad con depuración CORS mejorada

Los errores de uso compartido de recursos entre orígenes (CORS) ahora se encuentran en la **pestaña** Problemas.  Existen varias causas potenciales de errores CORS.  Haga clic para expandir cada problema para comprender las posibles causas y soluciones.

:::image type="complex" source="../../media/2021/05/cors-debugging-support.msft.png" alt-text="Problemas de CORS en la pestaña Problemas" lightbox="../../media/2021/05/cors-debugging-support.msft.png":::
   Problemas de CORS en la pestaña Problemas
:::image-end:::

<!-- screenshot uses http://cors-errors.glitch.me -->

Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1141824][CR1141824].


### <a name="renamed-xhr-filter-to-fetchxhr"></a>Filtro XHR con nombre a Fetch\/XHR

En la **herramienta Red,** el filtro **XHR** ahora se cambia a **Fetch/XHR**. Este cambio hace que sea más claro que este filtro incluye tanto solicitudes de red `XMLHttpRequest` de API como de `Fetch` API.

:::image type="complex" source="../../media/2021/05/fetch-xhr.msft.png" alt-text="La herramienta Red ahora muestra Fetch/XHR en lugar de XHR" lightbox="../../media/2021/05/fetch-xhr.msft.png":::
   La **herramienta Red** ahora muestra **Fetch/XHR en** lugar de **XHR**
:::image-end:::

Para obtener más información, vaya a:
*  [Especificación XMLHttpRequest][XhrSpecWhatwgOrg]
*  [Especificaciones de captura][FetchSpecWhatwgOrg]

Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1201398][CR1201398].


### <a name="filter-wasm-resource-type-in-the-network-tool"></a>Tipo de recurso Filter Wasm en la herramienta Red

En la **herramienta Red,** ahora puede seleccionar el nuevo filtro **Wasm** para filtrar las solicitudes de red WebAssembly.

:::image type="complex" source="../../media/2021/05/wasm-network-requests.msft.png" alt-text="Filter by Wasm" lightbox="../../media/2021/05/wasm-network-requests.msft.png":::
   Filter by Wasm
:::image-end:::

<!-- screenshot uses http://memory-inspector.glitch.me/demo-wasm.html -->

Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1103638][CR1103638].


### <a name="compute-intersections-are-now-included-in-the-performance-tool"></a>Las intersecciones de proceso ahora se incluyen en la herramienta Rendimiento

En la **herramienta Rendimiento,** DevTools ahora muestra **Intersecciones de proceso** en el gráfico de llamas. Estos cambios le ayudan a identificar eventos de observadores de intersección y a depurar la sobrecarga de rendimiento potencial de los observadores de intersección.

:::image type="complex" source="../../media/2021/05/compute-intersections-in-perf-tool.msft.png" alt-text="Calcular intersecciones en la herramienta Rendimiento" lightbox="../../media/2021/05/compute-intersections-in-perf-tool.msft.png":::
   Calcular intersecciones en la **herramienta Rendimiento**
:::image-end:::

<!-- screenshot uses https://googlechrome.github.io/samples/intersectionobserver -->

Para obtener más información sobre los observadores de intersección, vaya a Confianza es [bueno, la observación es mejor: Intersection Observer v2][WebDevIntersectionObserverV2].  Para obtener información sobre cómo usar el gráfico de llamas, vaya [a Analizar una grabación de rendimiento.][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]  Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1199137][CR1199137].


## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge

Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]


<!-- links -->
[DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]: ../../../evaluate-performance/reference.md#analyze-a-performance-recording "Analizar una grabación de rendimiento | Microsoft Docs"
<!-- external links -->
[XhrSpecWhatwgOrg]: https://xhr.spec.whatwg.org "Especificación XMLHttpRequest | WHATWG"
[FetchSpecWhatwgOrg]: https://fetch.spec.whatwg.org "Capturar especificaciones | WHATWG"

[WebDevIntersectionObserverV2]: https://web.dev/intersectionobserver-v2 "La confianza es buena, la observación es mejor: Intersection Observer v2 | web.dev"

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Uso de las herramientas | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Herramientas de desarrollador para Visual Studio Code | Visual Studio Marketplace"

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: Estado de la plataforma | YouTube"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"
[CR1094406]: https://crbug.com/1094406 "Problema 1094406: los desarrolladores desean un visor de pedidos de origen | Chromium errores"
[CR1174299]: https://crbug.com/1174299 "Problema 1174299: Sugerencias de cliente ua se descartaron al reemplazar la cadena UA a través de la pestaña Condiciones de red de Chrome DevTools | Chromium errores"
[CR1203241]: https://crbug.com/1203241 "Problema 1203241: editor de cuadrícula CSS | Chromium errores"
[CR1076427]: https://crbug.com/1076427 "Problema 1076427: DevTools Console debe admitir la nueva declaración de const | Chromium errores"
[CR1192084]: https://crbug.com/1192084 "Problema 1192084: agregar la opción &quot;Mostrar detalles del marco&quot; con el botón derecho para crear etiquetas iframe/html en la vista de elementos | Chromium errores"
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: mejorar el informe de errores de CORS en DevTools | Errores de Chromium"
[CR1201398]: https://crbug.com/1201398 "Problema 1201398: Solicitud de característica: cambiar el nombre del filtro de tipo XHR en panel de red | Chromium errores"
[CR1103638]: https://crbug.com/1103638 "Problema 1103638: Panel de red para mostrar recursos de WebAssembly | Chromium errores"
[CR1199137]: https://crbug.com/1199137 "Problema 1199137: Mostrar el costo de IntersectionObserver en el panel por | Chromium errores"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-xx) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).

[ ![ Creative Commons License][CCby4Image]][CCA4IL] Este trabajo se concede bajo una licencia de Creative Commons [Attribution 4.0 International License][CCA4IL].

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
