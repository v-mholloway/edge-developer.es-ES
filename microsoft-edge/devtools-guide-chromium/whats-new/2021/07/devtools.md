---
description: Aplica temas de color de Visual Studio Code, depura las pérdidas de memoria del nodo DOM con la nueva herramienta Elementos desasociados, Microsoft Edge Developer Tools para Visual Studio Code ahora se integra con el flujo de trabajo del depurador de Visual Studio Code y mucho más.
title: Novedades de DevTools (Microsoft Edge 93)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: b9ce2551806aa6ec4a60eb5fbf72dfc59f7e7a8c
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893271"
---
# <a name="whats-new-in-devtools-microsoft-edge-93"></a>Novedades de DevTools (Microsoft Edge 93)

[!INCLUDE [note about What's New announcements from the Microsoft Edge DevTools team](../../includes/edge-whats-new-note.md)]


## <a name="apply-themes-from-visual-studio-code-to-devtools"></a>Aplicar temas de Visual Studio Code a DevTools

<!-- Title: Apply themes from Visual Studio Code to DevTools -->
<!-- Subtitle: You can now use some of the most popular color themes from Visual Studio Code, such as Monokai and Solarized Dark, in Microsoft Edge DevTools. -->

Además de los temas claros y oscuros existentes, Microsoft Edge DevTools ahora admite algunos de los temas de color más populares de Visual Studio Code.  Para seleccionar un tema de color, vaya a **Configuración** y, a continuación, seleccione un tema de la **lista** desplegable Tema.

:::image type="complex" source="../../media/2021/07/all-devtools-themes.msft.png" alt-text="Temas de color para DevTools" lightbox="../../media/2021/07/all-devtools-themes.msft.png":::
   Temas de color para DevTools
:::image-end:::

Los temas Visual Studio Code son:

Temas claros:
*  Luz solarizada
*  Luz silenciosa

Temas oscuros:
*  Abyss
*  Kimbie Dark
*  Monokai
*  Monokai atenuado
*  Oscuro solarizado
*  Rojo
*  Tomorrow Night Blue

Para obtener más información, vaya [a Aplicar temas de color a DevTools][CustomizeDarkTheme].


## <a name="debug-dom-node-memory-leaks-with-the-new-detached-elements-tool"></a>Depurar pérdidas de memoria de nodo DOM con la nueva herramienta Elementos desasociados

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!-- Title: Introducing the Detached Elements tool -->
<!-- Subtitle: Use the Detached Elements tool to find and fix DOM node memory leaks. -->

Un nodo DOM se considera "desasociado" cuando ya no se adjunta a ningún elemento del DOM, pero aún se conserva en la memoria Microsoft Edge. El explorador no puede recopilar el elemento porque algunos JavaScript siguen haciendo referencia al elemento aunque ya no esté en la página ni en una parte del DOM.

La nueva herramienta Elementos desasociados busca todos los elementos separados de la página y los muestra. **** Puede expandir y contraer un elemento separado para ver los nodos primarios y secundarios que también se conservan. Puede desencadenar la recolección de elementos **** no utilizados del explorador seleccionando Recopilar elementos no utilizados y validando que tiene una pérdida de memoria cuando un elemento separado no se puede recopilar. Por último, puede saltar a JavaScript que hace referencia al elemento desasociado tomando una instantánea de montón con el **botón Analizar.**

:::image type="complex" source="../../media/2021/07/detached-elements-tool.msft.png" alt-text="La herramienta Elementos desasociados" lightbox="../../media/2021/07/detached-elements-tool.msft.png":::

   La **herramienta Elementos desasociados**
:::image-end:::

Para activar este experimento, vaya a **Configuración**y active la casilla  >  **** junto a **Elementos desasociados**.

<!-- For more information, navigate to [Detached elements][ExperimentalFeaturesDetachedElements]. -->
<!-- todo: link directly to the subheading in the page, when available; test the subheading link -->


## <a name="the-visual-studio-code-debugger-now-integrates-with-the-devtools-extension"></a>El Visual Studio Code se integra ahora con la extensión DevTools

<!-- Title: While debugging, launch the DevTools extension by selecting the Inspect button -->
<!-- Subtitle: Microsoft Edge DevTools for Visual Studio Code now integrates seamlessly with the JavaScript debugging workflow in the editor. -->

Si usa la depuración de JavaScript en Visual Studio Code, ahora puede iniciar Microsoft Edge **Developer Tools for Visual Studio Code** extension seleccionando el botón **Inspeccionar.**

:::image type="complex" source="../../media/2021/07/inspect-button.msft.png" alt-text="El botón Inspeccionar de Visual Studio Code para iniciar la extensión DevTools" lightbox="../../media/2021/07/inspect-button.msft.png":::
   El **botón Inspeccionar** de Visual Studio Code para iniciar la extensión DevTools
:::image-end:::

Esta característica integra la depuración DE DOM y CSS con la depuración de JavaScript en Visual Studio Code. Si no tiene instalada la extensión DevTools, cuando **** seleccione el botón Inspeccionar, Visual Studio Code le pedirá que instale la extensión.

Otras características nuevas son:
*  Las herramientas se actualizan automáticamente al cambiar entre diferentes destinos de depuración.
*  Varias correcciones de errores.
*  Documentación más detallada de la extensión.

Para obtener más información acerca de las mejoras y correcciones, compruebe el [archivo de registro de cambios][GithubMicrosoftVscodeEdgeDevtoolsChangelog] en el `vscode-edge-devtools` repositorio.

:::image type="complex" source="../../media/2021/07/extension-integrated-debugger.msft.png" alt-text="Extensión DevTools integrada con Visual Studio Code de depurador" lightbox="../../media/2021/07/extension-integrated-debugger.msft.png":::
   Extensión DevTools integrada con Visual Studio Code de depurador
:::image-end:::

Para obtener más información, vaya [a Launching Edge DevTools from the JS Debugger workflow][GithubVscodeEdgeDevtoolsDebuggerIntegration].  Obtenga la [Microsoft Edge Developer Tools para Visual Studio Code extensión][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools].  Microsoft Visual Studio Las extensiones de código se actualizan automáticamente; para actualizar esta extensión manualmente en su lugar, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Puede presentar problemas y contribuir a la extensión en [vscode-edge-devtools GitHub repositorio][GithubMicrosoftVscodeEdgeDevtools].


## <a name="new-fluent-ui-icons-for-devtools"></a>Nuevos Fluent de interfaz de usuario para DevTools

<!-- Title: New look for buttons and menus in Microsoft Edge DevTools -->
<!-- Subtitle: DevTools has adopted Fluent UI, giving it a more modern look that better aligns with the rest of the Microsoft Edge browser. -->

Microsoft Edge DevTools ha adoptado Fluent [interfaz][FluentUI]de usuario, lo que da a los botones y menús un aspecto más moderno que se alinea mejor con el resto del Microsoft Edge navegador.

:::image type="complex" source="../../media/2021/07/fluent-ui.msft.png" alt-text="DevTools implementado con un Fluent de interfaz de usuario" lightbox="../../media/2021/07/fluent-ui.msft.png":::
   DevTools implementado con un Fluent de interfaz de usuario
:::image-end:::


## <a name="change-the-devtools-display-language-directly-from-settings"></a>Cambiar el idioma de presentación de DevTools directamente desde Configuración

<!-- Title: DevTools Settings now includes display language -->
<!-- Subtitle: You can now skip the browser settings and change the DevTools display language directly within DevTools Settings. -->

Anteriormente, para cambiar el idioma de presentación en DevTools, tenías que cambiar el idioma del explorador.  Ahora puedes cambiar fácilmente el idioma de presentación en DevTools **Configuración**, sin tener que cambiar la configuración del explorador.  Para ello, abra **Configuración**y, a continuación, en Preferencias, **** seleccione un idioma en la **lista** desplegable Idioma.

:::image type="complex" source="../../media/2021/07/settings-browser-ui-language.msft.png" alt-text="Cambiar el idioma de presentación de DevTools directamente desde DevTools **Configuración**" lightbox="../../media/2021/07/settings-browser-ui-language.msft.png":::
   Cambiar el idioma de presentación de DevTools directamente desde DevTools **Configuración**
:::image-end:::

De forma predeterminada, DevTools coincide con el idioma para mostrar del explorador.  Para obtener más información, vaya [a Cambiar la configuración de idioma de DevTools][CustomizeLocalization].  Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [2882756][CR2882756].


## <a name="copy-a-declaration-in-the-styles-pane-for-css-in-js-libraries"></a>Copiar una declaración en el panel Estilos para bibliotecas CSS-in-JS

<!-- Title: Better support for CSS-in-JS libraries -->
<!-- Subtitle: Copy a single declaration or all declarations for a style rule from the Styles pane, formatted for JavaScript. -->

Anteriormente, al usar bibliotecas CSS-in-JS, no podía copiar declaraciones CSS (una propiedad y un valor CSS) con formato para JavaScript. Tendrías que editar el CSS copiado para que coincida con la sintaxis de JavaScript.

Ahora, Microsoft Edge versión 93, puede copiar una sola declaración CSS o todas las declaraciones de una regla de estilo y pegarlas directamente en un archivo JavaScript sin tener problemas de sintaxis. Para probar esta característica:

1. En el **panel Estilos** de la **herramienta Elementos,** abra el menú contextual \(hacer clic con el botón secundario\) en una declaración de una regla de estilo.
1. Seleccione **Copiar declaración como JS** o Copiar todas las **declaraciones como JS**.
1. Pegue el CSS copiado en un archivo JavaScript en el editor de texto, como Visual Studio Code.  Por ejemplo: `'--more-link': 'lime'`.

:::image type="complex" source="../../media/2021/07/copy-declaration-as-js.msft.png" alt-text="Menú contextual para una regla de estilo, incluidos los comandos Copiar declaración como JS y Copiar todas las declaraciones como JS." lightbox="../../media/2021/07/copy-declaration-as-js.msft.png":::
   Menú contextual de una regla de estilo, incluida **la declaración Copiar como JS** y Copiar todas las **declaraciones como comandos JS**
:::image-end:::

Para obtener más información sobre cómo ver y cambiar CSS, vaya a [Referencia css][CssReference].


## <a name="easier-customization-of-user-agent-client-hints"></a>Personalización más sencilla de User-Agent sugerencias de cliente

<!-- Title: Send as many (or as few) Client Hints as you want -->
<!-- Subtitle: Updated UI for User-Agent Client Hints in Emulated Devices settings and in the Network conditions tool. -->

User-Agent sugerencias de cliente hace que la información del explorador sea más accesible que una cadena delimitada por punto y coma User-Agent y mejora la compatibilidad del sitio.  Inicialmente, User-Agent sugerencias de cliente tardaban mucho tiempo en probarse y depurarse.  Había menos control sobre las sugerencias de cliente y las sugerencias de cliente tenían que rellenarse correctamente para que el formulario funcionara.

En esta versión, hemos rediseñado la experiencia de depuración para que puedas modificar fácilmente User-Agent sugerencias de cliente a través de una interfaz de usuario con varios campos y controles independientes.  Además, ahora puede probar las sugerencias User-Agent cliente y una cadena User-Agent simultáneamente.  Ahora puedes definir User-Agent sugerencias de cliente para un dispositivo personalizado **en Configuración** o en la herramienta **Condiciones de** red.

:::image type="complex" source="../../media/2021/07/ua-client-hints-in-settings.msft.png" alt-text="Definición User-Agent sugerencias de cliente para un dispositivo personalizado en Configuración" lightbox="../../media/2021/07/ua-client-hints-in-settings.msft.png":::
   Definición User-Agent sugerencias de cliente para un dispositivo personalizado **en Configuración**
:::image-end:::

Para obtener más información acerca de cómo definir sugerencias **en Configuración**, vaya a [Establecer sugerencias][DeviceModeIndexSetUach]de cliente de agente de usuario .

También puede invalidar las sugerencias User-Agent cliente de la página actual mediante la herramienta **Condiciones de** red.

:::image type="complex" source="../../media/2021/07/ua-client-hints-in-network-conditions.msft.png" alt-text="Definición User-Agent sugerencias de cliente para un dispositivo personalizado en la herramienta Condiciones de red" lightbox="../../media/2021/07/ua-client-hints-in-network-conditions.msft.png":::
   Definición User-Agent sugerencias de cliente para un dispositivo personalizado en la **herramienta Condiciones de** red
:::image-end:::

Para obtener más información sobre cómo definir sugerencias en la **herramienta Condiciones de** red, vaya a Establecer sugerencias de cliente de agente de [usuario.][NetworkReferenceSetUach]  Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [1174299][CR1174299].


## <a name="screen-readers-now-announce-errors-warnings-and-issues-in-toolbar-and-console"></a>Ahora, los lectores de pantalla anuncian errores, advertencias y problemas en la barra de herramientas y la consola

<!-- Title: Better support for errors, warnings, and issues with assistive technology -->
<!-- Subtitle: Screen readers now correctly announce the number and the type of notification for errors, warnings, and issues in the DevTools toolbar. -->

Anteriormente, los usuarios de lectores de pantalla solo oían el número de errores, advertencias o problemas anunciados en la barra de herramientas DevTools.  No se incluyó la información adicional sobre qué tipo de notificación se anunciaba, como "Error", "Advertencia" o "Problema". Por ejemplo, si DevTools notificaba 3 errores, los lectores de pantalla simplemente anunciarían "3".

Ahora, Microsoft Edge versión 93, los lectores de pantalla anuncian correctamente el tipo y el número de notificaciones; errores, advertencias o problemas.  Por ejemplo, si DevTools informa de 3 errores y 5 advertencias, los lectores de pantalla ahora anuncian "3 errores, 5 advertencias".  Esta corrección se ha aplicado tanto a las notificaciones de la barra de herramientas DevTools como a la consola.

:::image type="complex" source="../../media/2021/07/screen-reader-errors-warnings-issues.msft.png" alt-text="Errores, advertencias y problemas de interfaz de usuario en la barra de herramientas y la consola" lightbox="../../media/2021/07/screen-reader-errors-warnings-issues.msft.png":::
   Errores, advertencias y problemas de interfaz de usuario en la barra de herramientas y la **consola**
:::image-end:::

<!-- It'd be good to have a video of this a11y fix where the text that the screen reader announces is displayed -->

Para obtener información acerca de la depuración de errores de consola, vaya [a Depurar errores notificados en consola][ConsoleConsoleDebugJavascript].  Para obtener información sobre los problemas encontrados por DevTools y las mejoras que puede realizar en una página web, vaya a Buscar y solucionar problemas [con la herramienta Problemas][IssuesIndex].  Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1223208][CR1223208].


## <a name="copy-as-powershell-in-the-network-tool-now-includes-cookies"></a>Copiar como PowerShell en la herramienta Red ahora incluye cookies

<!-- Title: Generate PowerShell commands for network requests in the Network tool -->
<!-- Subtitle: The Copy as PowerShell context menu option now correctly sets the user-agent string and cookies when generating PowerShell network requests. -->

Anteriormente, en **** la herramienta **** Red, la opción del menú contextual Copiar como PowerShell no incluyeba cookies al generar un comando de PowerShell para una solicitud de red determinada en el registro de actividad de  >  **** red. Esto significaba que el comando de PowerShell generado no podía realizar correctamente la misma solicitud de red si se requerían cookies.

Ahora, Microsoft Edge versión 93, la opción del menú contextual Copiar como **PowerShell** establece correctamente la cadena de User-Agent y las cookies observadas por DevTools.  El comando de PowerShell generado ahora puede realizar correctamente la misma solicitud de red que observó DevTools, incluso en servidores que dependen de cookies.

:::image type="complex" source="../../media/2021/07/copy-as-powershell.msft.png" alt-text="El comando Copiar como PowerShell" lightbox="../../media/2021/07/copy-as-powershell.msft.png":::
   El **comando Copiar como PowerShell**
:::image-end:::

Para obtener más información sobre el registro de actividad de red, vaya a [Referencia de análisis de red][NetworkReference].  Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [932971][CR932971].


## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge

Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]


<!-- links -->
[CustomizeDarkTheme]: ../../../customize/theme.md "Aplicar temas de color a DevTools | Microsoft Docs"
<!-- todo: link directly to the subheading in the page, when available; test the subheading link:
[ExperimentalFeaturesDetachedElements]: ../../../experimental-features/index.md#detached-elements "Detached elements | Microsoft Docs" -->
[CustomizeLocalization]: ../../../customize/localization.md "Cambiar la configuración de idioma de DevTools | Microsoft Docs"
[CssReference]: ../../../css/reference.md "Referencia CSS | Microsoft Docs"
[DeviceModeIndexSetUach]: ../../../device-mode/index.md#set-user-agent-client-hints "Establecer sugerencias de cliente de agente de usuario | Microsoft Docs"
[NetworkReferenceSetUach]: ../../../network/reference.md#set-user-agent-client-hints "Establecer sugerencias de cliente de agente de usuario | Microsoft Docs"
[ConsoleConsoleDebugJavascript]: ../../../console/console-debug-javascript.md "Errores de depuración notificados en la consola | Microsoft Docs"
[IssuesIndex]: ../../../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas | Microsoft Docs"
[NetworkReference]: ../../../network/reference.md "Referencia de análisis de red | Microsoft Docs"

<!-- external links -->
[FluentUI]: https://developer.microsoft.com/en-us/fluentui#/ "Fluent Ui | developer.microsoft.com"

[CR1174299]: https://bugs.chromium.org/p/chromium/issues/detail?id=1174299 "Problema 1174299: Sugerencias de cliente ua se descartaron al reemplazar la cadena UA a través de la pestaña Condiciones de red de Chrome DevTools | Chromium errores"
[CR2882756]: https://chromium-review.googlesource.com/c/devtools/devtools-frontend/+/2882756 "Problema 2882756: \[l10n\] Agregar configuración para que los usuarios elijan la configuración regional de DevTools | Chromium errores"
[CR1223208]: https://bugs.chromium.org/p/chromium/issues/detail?id=1223208 "El lector de pantalla anuncia información inapropiada para los errores y advertencias en el encabezado | Chromium errores"
[CR932971]: https://bugs.chromium.org/p/chromium/issues/detail?id=932971 "932971: la pestaña Red, Copiar como Powershell == no envía cookies correctamente | Chromium errores"

[GithubVscodeEdgeDevtoolsDebuggerIntegration]: https://microsoft.github.io/vscode-edge-devtools/debugger-integration.html "Iniciar Edge DevTools desde el flujo de trabajo del depurador js: vscode-edge-devtools | GitHub"

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"
[GithubMicrosoftVscodeEdgeDevtoolsChangelog]: https://github.com/microsoft/vscode-edge-devtools/blob/main/CHANGELOG.md "Archivo Changelog: vscode-edge-devtools | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Extension Marketplace | Visual Studio Code"

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Herramientas de desarrollador para Visual Studio Code | Visual Studio Marketplace"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-xx) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).

[ ![ Creative Commons License][CCby4Image]][CCA4IL] Este trabajo se concede bajo una licencia de Creative Commons [Attribution 4.0 International License][CCA4IL].

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
