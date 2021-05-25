---
description: Wavy subraya los problemas de código destacado en la herramienta Elementos, escala de tiempo de actualización del trabajador de servicio y mucho más.
title: Novedades de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5f499a6c9f1109f80a9d459edf94ed2226734f19
ms.sourcegitcommit: 87ba918b0910373bb645615377709bf140dc9b19
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583462"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-91"></a>Novedades de DevTools (Microsoft Edge 91)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a>Wavy subraya los problemas de código destacado y las mejoras en la herramienta Elementos  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

En la mayoría de los identificadores modernos, los subrayados ondulados debajo del texto indican errores de sintaxis.   En Microsoft Edge versión 91 o posterior, los subrayados ondulados se muestran en HTML en la vista **DOM** de la **herramienta** Elementos.  Los subrayados ondulados indican problemas de código y sugerencias relacionadas con la accesibilidad, la compatibilidad, el rendimiento, y así sucesivamente.  Para obtener más información acerca de cómo revisar y editar problemas, vaya a Buscar y solucionar problemas con la [Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

Para abrir la **herramienta Problemas** y obtener más información sobre el problema y cómo solucionarlo, complete una de las siguientes acciones.  

*   Seleccione y mantenga presionado y, a `Shift` continuación, elija cualquier subrayado ondulado.  
*   Complete las siguientes acciones.  
    1.  Mantenga el mouse sobre cualquier subrayado ondulado.  
    1.  Abra el menú contextual \(haga clic con el botón derecho\).  
    1.  Elija **Mostrar en Problemas**.  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Elija el error subrayado en la herramienta Elementos" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         Elija el error subrayado en la **herramienta** Elementos  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Mostrar detalles de error en la herramienta Problemas" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         Mostrar detalles de error en la **herramienta Problemas**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Aprenda más sobre DevTools con la información sobre herramientas informativas  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

La característica DevTools Tooltips le ayuda a obtener información sobre todas las diferentes herramientas y paneles de DevTools.  Para desactivar la información sobre herramientas, seleccione `Esc` .  Para activar información sobre herramientas, complete una de las siguientes acciones.  

*   Seleccione `Ctrl` + `Shift` + `H` \(Windows/Linux\) o `Cmd` + `Shift` + `H` \(macOS\).  
*   [Abra el menú comando y,][DevtoolsCommandMenuIndexOpenCommandMenu] a continuación, escriba `tooltips` .  
*   Elija **Personalizar y controlar DevTools** \( \) > Ayuda para alternar la información sobre herramientas de `...` ****  >  **DevTools**.  

Además, si activa el experimento Modo de enfoque y Información sobre herramientas [de DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] también puede elegir el botón Alternar la información sobre herramientas **de DevTools** \( \) en la parte inferior de la barra de `?` **actividades**.  

Para mostrar más información sobre cómo usar DevTools, active Información sobre herramientas y, a continuación, mantenga el mouse en cada región de esquema de DevTools.  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Mantenga el mouse en cualquier lugar de la región resaltada de la herramienta Problemas para mostrar más detalles" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   Mantenga el mouse en cualquier lugar de la región resaltada de la **herramienta Problemas** para mostrar más detalles  
:::image-end:::  

## <a name="service-worker-update-timeline"></a>Escala de tiempo de actualización del trabajador de servicio  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

En Microsoft Edge versión 91 o posterior, si eres desarrollador de aplicación web progresiva o trabajador de servicio, muestra el ciclo de vida de actualización de los trabajadores de servicio como una escala de tiempo en la herramienta **Aplicación.**  Esta característica le ayuda a comprender el tiempo que el trabajador de servicio pasa en cada una de las siguientes fases.  

*   **Instalar**  
*   **Esperar**  
*   **Activar**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Revisar la escala de tiempo del ciclo de actualización para el trabajador de servicio" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Revisar la **escala de** tiempo del ciclo **de actualización** para el trabajador de servicio  
:::image-end:::  

Para obtener más información sobre el ciclo de vida de los trabajadores de servicio, vaya a [El ciclo de vida del trabajador de servicio][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].  Para obtener más información acerca de las herramientas de depuración para las aplicaciones web progresivas y los trabajadores de servicio en DevTools, vaya a [Mejoras del trabajador de servicio][DevtoolsServiceWorkerIndex].  Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya al problema [1066604][CR1066604].  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Las aplicaciones web progresivas ya no muestran advertencias para iconos que no son cuadrados  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

En Microsoft Edge versión [90][DevtoolsWhatsNew202102Devtools] o anterior, si el manifiesto de aplicación web de su PWA incluía un icono que no es cuadrado, se muestra una advertencia en la sección Errores y **advertencias** para cada icono que no sea cuadrado.  En Microsoft Edge versión 91 o **** posterior, la **** sección Manifiesto de la herramienta Aplicación no muestra advertencias si proporciona al menos un icono cuadrado.  Si no proporciona ningún icono cuadrado, una advertencia muestra el siguiente mensaje.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="En Microsoft Edge versión 90 o anterior, se muestra un error para cada icono que no es cuadrado" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         En Microsoft Edge versión 90 o anterior, se muestra un error para cada icono que no es cuadrado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="En Microsoft Edge versión 91 o posterior, no se muestra ningún error al proporcionar al menos un icono cuadrado" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         En Microsoft Edge versión 91 o posterior, no se muestra ningún error al proporcionar al menos un icono cuadrado  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar errores y advertencias en el manifiesto de la aplicación web, vaya a la **herramienta Aplicación** y elija la **sección** Manifiesto.  Los errores y advertencias se enumeran en el **encabezado Errores y advertencias.**  Para obtener más información sobre el manifiesto de aplicación web, vaya a Usar el manifiesto de aplicación [web para integrar la aplicación web progresiva en el sistema operativo][ProgressiveWebAppsWebappmanifests].  Para crear iconos para incluir en el manifiesto de la aplicación web, vaya al Generador de [imágenes de PWABuilder][PwabuilderImagegenerator].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [1185945][CR1185945].  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>Localized DevTools ahora es compatible con Chromium exploradores basados en aplicaciones  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

A partir [Microsoft Edge versión 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools se muestra en su propio idioma.  Muchos desarrolladores usan otras herramientas de desarrollador como StackOverflow y Visual Studio Code en su idioma nativo, no solo en inglés.  El Microsoft Edge de DevTools, el equipo de Chrome DevTools y el equipo de Google Lighthouse colaboraron para proporcionar la misma experiencia en todos los exploradores basados en Chromium web.  Para obtener más información sobre cómo usar DevTools en su idioma, vaya a [Cambiar la configuración de idioma de DevTools][DevtoolsCustomizeLocalization].  Para obtener más información sobre la colaboración en esta característica en el proyecto de código abierto Chromium, vaya a [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge explorador y DevTools establecidos en japonés" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Microsoft Edge explorador y DevTools establecidos en japonés  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Usar el teclado para navegar a variables CSS  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

A partir [Microsoft Edge versión 88,][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]el panel **Estilos** muestra variables CSS y proporciona un vínculo directamente a la definición de cada variable.  En Microsoft Edge versión 91 o posterior, puede usar las teclas de flecha para navegar fácilmente a las variables CSS.  Para abrir la definición en el panel **Estilos,** mantenga el mouse en una variable y, a continuación, seleccione `Enter` .  Para obtener más información acerca de las variables CSS, vaya [a Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto de Chromium, vaya al problema [1187735][CR1187735].  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Variable CSS --theme-body-background resaltada en el panel Estilos" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   Variable `--theme-body-background` CSS resaltada en el **panel Estilos**  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Los problemas se ordenan automáticamente por gravedad  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

La **herramienta Problemas** muestra recomendaciones para mejorar el sitio web, incluida la accesibilidad, el rendimiento, la seguridad, entre otros. En función de sus comentarios, los problemas ahora se ordenan automáticamente por gravedad.  En cada categoría de comentarios, cada problema marcado como **error** aparece primero, seguido de cada problema marcado como advertencia **y,** a continuación, cada problema marcado como **sugerencia**.  Para ayudarle a refinar sus problemas, se planean opciones de filtro adicionales para una actualización futura.  Para obtener más información acerca de cómo revisar problemas, vaya a Buscar y solucionar problemas con la [Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="La herramienta Problemas muestra los problemas ordenados por gravedad" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   La **herramienta Problemas** muestra los problemas ordenados por gravedad  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Microsoft Edge Developer Tools for Visual Studio Code versión 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

El [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 proporciona DevTools de Microsoft Edge versión [88][DevtoolsWhatsNew202011Devtools].  Esta extensión ahora admite ARM dispositivos y ya no depende del [depurador para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extensión.  La versión 1.1.7 incluye las siguientes correcciones de errores y mejoras.  

*   Se actualizó la confiabilidad del cierre de destino.  
*   Se actualizó el panel lateral para que se actualice automáticamente al depurar los destinos que se crean o destruyen.  
*   Se agregó un nuevo menú contextual que le ofrece un acceso más rápido a la configuración de extensión y al registro de cambios más reciente.  
*   Se actualizó y simplificó la versión de la documentación de extensión, incluidas las características más nuevas.  
    
Para actualizar manualmente a la versión 1.1.7, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Puede archivar los problemas y contribuir con la extensión en el [repositorio de GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a>Visualizar ajuste de desplazamiento CSS  

Ahora puede alternar el distintivo en la herramienta Elementos para inspeccionar la alineación de ajuste de desplazamiento `scroll-snap` CSS. ****  Cuando se aplica un elemento HTML en la página web, se muestra un distintivo junto a él `scroll-snap-type` `scroll-snap` en la **herramienta** Elementos.  Elija el distintivo para activar \(or off\) la presentación de una superposición de ajuste de desplazamiento en la página web.  Para revisar una página web de ejemplo, vaya a [Scroll Acoplar Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].  En el ejemplo, los puntos se muestran en bordes de ajuste.  El puerto de desplazamiento tiene un esquema sólido mientras que los elementos de ajuste tienen contornos de guión.  El relleno de desplazamiento se rellena en verde mientras el margen de desplazamiento se rellena en naranja.  Para revisar el historial de esta característica en el Chromium de código abierto, vaya al problema [862450][CR862450].  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="Complemento de desplazamiento CSS" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   Complemento de desplazamiento CSS  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a>Nueva herramienta inspector de memoria  

Use la nueva **herramienta Inspector de** memoria para inspeccionar una memoria de `ArrayBuffer` JavaScript y Wasm.  Abra la [página web de demostración memoria en JS.][GlitchMemoryInspectorDemoJsHtml]  En la **herramienta Orígenes,** abra el `memory-write-wasm` archivo y establezca un punto de interrupción en la línea `0x03c` .  Actualice la página web.  Expanda la **sección Ámbito** en el panel del depurador.  El nuevo icono se muestra junto al valor **del búfer.**  Elirá para abrir la nueva **herramienta Inspector de** memoria.  

Para obtener más información sobre la depuración en la **herramienta Orígenes,** vaya a Usar el [panel Depurador para depurar código JavaScript][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].  Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1166577][CR1166577].  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Herramienta Inspector de memoria" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   **Herramienta inspector de** memoria  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a>Panel Nueva configuración de distintivo en la herramienta Elementos  

Ahora, usa la **configuración de distintivo en** la herramienta **Elementos** para activar \(o desactivar\) distintivos individuales.  Usa esta característica para personalizar y mantenerte centrado en distintivos importantes mientras inspeccionas páginas web.  Para mostrar el panel de configuración del distintivo en la parte superior de la **herramienta Elementos,** realice las siguientes acciones.  

1.  Mantenga el mouse sobre cualquier elemento.  
1.  Abra el menú contextual \(haga clic con el botón derecho\).  
1.  Elija **Configuración de distintivo...**.  
    
Para mostrar \(u ocultar\) los distintivos, elija \(o quitar\) la casilla situada junto al nombre del distintivo.  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Panel de configuración de distintivo en la herramienta Elementos" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   **Panel de configuración** de distintivo en la **herramienta** Elementos  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a>Vista previa de imagen mejorada con información de relación de aspecto  

Las vistas previas de imágenes en DevTools se han mejorado para mostrar más información, incluidos los siguientes detalles.  

*   Tamaño representado  
*   Relación de aspecto representado  
*   Tamaño intrínseco  
*   Relación de aspecto intrínseca  
*   Tamaño de archivo  
    
La información le ayuda a comprender mejor las imágenes y aplicar la optimización.  La información de relación de aspecto de imagen también está disponible en la **herramienta Red,** cuando se elige una vista previa de imagen.  

:::row:::
   :::column span="":::
      En la **herramienta Elementos,** la vista previa de imagen ahora muestra más información sobre la imagen.  
   :::column-end:::
   :::column span="":::
      Además, la información de relación de aspecto de imagen está disponible en la **herramienta Red,** al elegir una vista previa de imagen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Vista previa de imagen con información de relación de aspecto en la herramienta Elemento" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         Vista previa de imagen con información de relación de aspecto en la **herramienta** Elemento  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Información de relación de aspecto de imagen en la herramienta Red" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         Información de relación de aspecto de imagen en la **herramienta Red**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar el historial de esta característica en el proyecto de código abierto de Chromium, vaya a Problemas [1149832][CR1149832] y [1170656][CR1170656].  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a>Nuevas opciones para configurar codificaciones de contenido en la herramienta Condiciones de red 

En la **herramienta Red,** elija el nuevo botón **** Más condiciones de **red...** junto al menú desplegable Limitación para abrir la **herramienta Condiciones de** red.  Para probar si las respuestas del servidor están codificadas correctamente para exploradores que no admiten [gzip][GnuSoftwareGzipManual], [brotli][|::ref1::|Main]u otro `Content-Encoding` futuro, complete las siguientes acciones.  

1.  Abrir la herramienta **Condiciones de** red
1.  Vaya a **Codificaciones de contenido aceptadas**. 
1.  Quite la casilla situada junto a `Content-Encoding` la que desea probar.  
    
Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1162042][CR1162042].  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Nuevas Más condiciones de red... botón abre la herramienta Condiciones de red para configurar Content-Encoding" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   Nuevo **Botón Más condiciones de red...** abre la herramienta Condiciones **de** red para configurar `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a>Mejoras en el panel Estilos  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a>Nuevo acceso directo para mostrar el valor calculado en el panel Estilos  

Ahora, para mostrar el valor CSS calculado en el panel **Estilos,** complete las siguientes acciones.  

1.  Mantenga el mouse en una propiedad CSS.  
1.  Abra el menú contextual \(haga clic con el botón derecho\).  
1.  Elija **Ver valor calculado**.  
    
Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Problema [1076198][CR1076198].  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Nuevo acceso directo para mostrar el valor calculado" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   Nuevo acceso directo para mostrar el valor calculado  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a>Compatibilidad con la palabra clave accent-color  

La interfaz de usuario de autocompletar del panel **Estilos** ahora detecta la palabra clave CSS, que te permite especificar el color de énfal para los controles de interfaz de usuario generados `accent-color` por el elemento.  Algunos ejemplos de controles de interfaz de usuario generados por un elemento incluyen casillas o botones de radio. Para obtener más información sobre el estado de la implementación Chromium, vaya a [Característica: propiedad CSS de color énfal][ChromestatusFeature4752739957473280].  Para activar esta característica, vaya a `edge://flags#enable-experimental-web-platform-features` y establezca la casilla en **Habilitado**.  Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [1092093][CR1092093].  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="palabra clave CSS de color de acento" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` Palabra clave CSS
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a>Mostrar detalles sobre las características bloqueadas en la vista Detalles del marco  

La directiva de permisos es una API de plataforma web que ofrece a un sitio web la capacidad de permitir o bloquear el uso de características del explorador en un marco individual o en un que `iframe` inserta. Para obtener más información, vaya a [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].  Para mostrar los detalles sobre por qué se bloquea una característica, realice las siguientes acciones.  

1.  Vaya a [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].  
1.  Vaya a la **herramienta Aplicación.**  
1.  Elija un marco.  
1.  Vaya a la **sección Directiva de permisos.**  
1.  Vaya a la **propiedad Disabled Features.**  
1.  Elija **Mostrar detalles**.  
1.  Elija el icono junto a cada directiva para navegar a la solicitud de red o `iframe` que bloqueó la característica.  
    
Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Características bloqueadas en la vista Detalles del marco" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   Características bloqueadas en la vista Detalles del marco  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a>Filtrar experimentos en la configuración Experimentos  

Busca experimentos más rápido con el nuevo filtro de experimento.  Por ejemplo, para activar nuevos experimentos para problemas de código, complete las siguientes acciones.
``

1.  Vaya a **Configuración**  >  **Experiments**.  
1.  Vaya al **cuadro de texto** Filtrar.  
1.  Escriba `issues`.  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtrar experimentos en la configuración Experimentos" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   Filtrar experimentos en la **configuración Experimentos**  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a>Nueva columna De encabezado Vary en el panel Almacenamiento en caché  

Use la nueva `Vary Header` columna en el panel De **Storage** caché para mostrar los valores de encabezado [de][HttpwgSpecsRfc7231HtmlHeaderVary] respuesta HTTP Variables.  Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1186049][CR1186049].  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Variar columna de encabezado" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   Variar columna de encabezado  
:::image-end:::  

### <a name="sources-tool-improvements"></a>Mejoras de herramientas de orígenes  

#### <a name="support-for-new-javascript-features"></a>Compatibilidad con nuevas características de JavaScript  

DevTools ahora admite las nuevas comprobaciones de marca privada [a.k.a.][V8DevFeaturesPrivateBrandChecks] #foo en la característica de lenguaje JavaScript de obj.  La característica de comprobaciones de marca privada amplía el [operador in][MdnDocsWebJavascriptReferenceOperatorsIn] para admitir campos de clase [Private][V8DevFeaturesClassFieldsPrivateClassFields] en un objeto específico.  Pruébalo en las **herramientas Consola** **y** Orígenes.  Además, para inspeccionar los campos privados, realice las siguientes acciones.  

1.  Vaya al **panel del** depurador.  
1.  Vaya a la **sección Ámbito.**  
    
Para revisar el historial de esta característica en el Chromium de código abierto, vaya al problema [11374][CR11374].  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="Comprobaciones de marca privada de JavaScript" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   Comprobaciones de marca privada de JavaScript  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a>Compatibilidad mejorada para la depuración de puntos de interrupción  

Los agrupadores modernos de JavaScript como [Webpack][WebpackJsMain]y [Rollup][RollupjsMain] admiten la división de código.  Para obtener más información sobre la división de código, vaya [a División de código][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].  En Microsoft Edge versión 90 o anterior, DevTools solo establece puntos de interrupción en un único lote.  En Microsoft Edge versión 91 o posterior, DevTools establece correctamente los puntos de interrupción en varios lotes al depurar un componente compartido.  Para revisar el historial de esta característica en el proyecto de código abierto de Chromium, vaya a Problemas [1142705][CR1142705], [979000][CR979000]y [1180794][CR1180794].  

#### <a name="support-hover-preview-with-bracket-notation"></a>Compatibilidad con la vista previa activa con la notación entre corchetes  

DevTools ahora admite la vista previa activa en expresiones de miembros de JavaScript que usan `[]` la notación en la **herramienta** Orígenes.  Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1178305][CR1178305].  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Compatibilidad con la vista previa activa con notación []" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   Compatibilidad con la vista previa activa con `[]` la notación  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a>Esquema mejorado de archivos HTML  

DevTools ahora tiene mejor compatibilidad de esquema para `.html` los archivos.  En la **herramienta Orígenes,** abra el `.html` archivo.  Para activar \(o desactivar\) el esquema de código, seleccione en `Ctrl` + `Shift` + `O` Windows/Linux o `Cmd` + `Shift` + `O` en macOS.  En la siguiente figura, DevTools ahora enumera correctamente todas las funciones del esquema.  Anteriormente, DevTools solo muestra algunas de las funciones.  Para revisar el historial de esta característica en el proyecto de código abierto de Chromium, vaya a Los problemas [761019][CR761019] y [1191465][CR1191465].  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Esquema mejorado de archivos HTML" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   Esquema mejorado de archivos HTML  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a>Seguimientos de pila de errores adecuados para la depuración de Wasm  

En Microsoft Edge versión 90 o anterior, DevTools solo muestra referencias wasm genéricas en seguimientos de pila de errores.  En Microsoft Edge versión 91 o posterior, DevTools resuelve las solicitudes de función en línea y muestra la ubicación de origen en Seguimientos de pila de errores para la depuración de Wasm.  Para obtener más información sobre los seguimientos de pila de errores en **la consola,** vaya a [error][DevtoolsConsoleApiError].  

En Microsoft Edge versión 91 o posterior, DevTools resuelve las solicitudes de función en línea y muestra los seguimientos de pila de errores adecuados para la depuración de Wasm.  

:::row:::
   :::column span="":::
      En Microsoft Edge versión 90 y versiones anteriores, la ubicación de origen no se muestra en los seguimientos de la pila de errores.  Las ubicaciones de origen incluyen `dsquare` .  
   :::column-end:::
   :::column span="":::
      En Microsoft Edge versión 91 y posteriores, la ubicación de origen se muestra en los seguimientos de la pila de errores.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Seguimientos de pila de errores anteriores para la depuración de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         Seguimientos de pila de errores adecuados para la depuración de Wasm  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Seguimientos de pila de errores adecuados para la depuración de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         Seguimientos de pila de errores adecuados para la depuración de Wasm  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [1189161][CR1189161].  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Uso de DevTools en otros idiomas: novedades de DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "Definiciones de variables CSS en el panel Estilos: novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Agrupar herramientas en modo de enfoque: novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Abra el menú Comando: ejecute comandos con el Microsoft Edge menú DevTools Command | Microsoft Docs"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error: referencia de api de consola | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Cambiar la configuración de idioma de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Mejoras de service worker | Microsoft Docs"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Uso del panel Depurador para depurar código JavaScript: información general sobre la herramienta Orígenes | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Ciclo de vida del trabajador de servicio: usar los trabajadores de servicio para administrar las solicitudes de red y las notificaciones de inserción | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Usa el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Característica: propiedad CSS de color de énf | Estado de la plataforma Chrome"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Widget Accent Colors: la propiedad accent-color - Css Basic User Interface Module Level 4 | Borradores del editor de grupo de trabajo css"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR11374]: https://crbug.com/v8/11374 "Problema 11374: Implementar la comprobación de marca ergonómica para campos privados"  
[CR761019]: https://crbug.com/761019 "Problema 761019: &quot;Ir a símbolo&quot; pierde la primera función y prefiere una coincidencia peor si contiene todas las chars con tipo"  
[CR862450]: https://crbug.com/862450 "Problema 862450: [css-scroll-snap] Considere la posibilidad de agregar la característica Devtools para el complemento de desplazamiento css"  
[CR979000]: https://crbug.com/979000 "Problema 979000: Los mapas de origen con rutas de acceso de orígenes en colisión no funcionan."  
[CR1066604]: https://crbug.com/1066604 "Problema 1066604: DevTools: Vea detalles sobre ServiceWorker para instalar y activar eventos | Chromium errores"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 "Problema 1076198: [Solicitud de característica] Saltar a la propiedad calculada desde la `styles` pestaña"  
[CR1092093]: "Problema 1092093: Hacer que los controles de formularios se atenúan más al color al admitir la propiedad https://crbug.com/1092093 CSS 'accent-color'"  
[CR1136655]: https://crbug.com/1136655 "Problema 1136655: Devtools: Localización V2 | Chromium errores"  
[CR1142705]: "Problema 1142705: los puntos de interrupción dejan de funcionar cuando 2 mapas de origen apuntan al mismo archivo virtual al usar https://crbug.com/1142705 webpack"  
[CR1149832]: "Problema 1149832: Solicitud de característica: la vista previa de imagen también debe mostrar https://crbug.com/1149832 el tamaño del archivo"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Directiva de permisos] Implementar la compatibilidad de devtool para la directiva de permisos"  
[CR1162042]: https://crbug.com/1162042 "Problema 1162042: DevTools: admite la deshabilitación de gzip/brotli/jxl content-encoding"  
[CR1166577]: https://crbug.com/1166577 "Problema 1166577: ☂️ inspector de memoria lineal 1.0"  
[CR1170656]: https://crbug.com/1170656 "Problema 1170656: Mostrar relación intrínseca de aspecto"  
[CR1178305]: "Problema 1178305: El depurador no muestra el valor de propiedad de un elemento indizado cuando está https://crbug.com/1178305 activa"  
[CR1180794]: "Problema 1180794: Los puntos de interrupción no funcionan con optimización de la línea del compilador https://crbug.com/1180794 de cierre"  
[CR1185945]: "Problema 1185945: La advertencia de manifiesto implica que todos los iconos deben ser cuadrados https://crbug.com/1185945 | Chromium errores"  
[CR1186049]: https://crbug.com/1186049 "Problema 1186049: Column for Vary: header in Cache Storage viewer"  
[CR1187735]: https://crbug.com/1187735 "Issue 1187735: Accessibility: MAS2.1.1: Keyboard: Unable to invoke the 'Var(..)' function using keyboard | Chromium errores"  
[CR1189161]: https://crbug.com/1189161 "Problema 1189161: los stacktraces no se `new Error` transforman a través de ENANO"  
[CR1191465]: https://crbug.com/1191465 "Problema 1191465: Ctrl+Mayús+O roto en HTML"  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicador de directivas de permisos | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Memoria en JS | Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Memoria en Wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Desplácese Acoplar de demostración | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "Directiva de permisos de OOPIF | Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip: el programa de compresión de datos | Sistema operativo GNU"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary: protocolo de transferencia de hipertexto (HTTP/1.1): semántica y contenido | Grupo de trabajo HTTP de IETF"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Hay tres enfoques generales para la división de código disponibles: Puntos de entrada: Código dividido manualmente mediante la configuración de entrada.  Impedir duplicación: use dependencias de entrada o SplitChunksPlugin para desduplicar y dividir fragmentos.  Importaciones dinámicas: divida el código mediante llamadas de función en línea dentro de los módulos. - División de código | webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas de CSS (variables) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "en operador | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Generador de imágenes | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "Marca privada comprueba a.k.a. #foo en obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Campos de clase privada: campos de clase pública y privada | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-91) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
