---
description: Wavy subraya los problemas de código destacado en la herramienta Elementos, escala de tiempo de actualización del trabajador de servicio y mucho más.
title: Novedades de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 473b2537b631a77a182c04b6986051a4ce7aae03
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564822"
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

En Microsoft Edge versión 91 o posterior, si es un desarrollador de aplicación web progresiva o trabajador de servicio, puede mostrar el ciclo de vida de actualización de los trabajadores de servicio como una escala de tiempo en la herramienta **Aplicación.**  Esta característica le ayuda a comprender el tiempo que el trabajador de servicio pasa en cada una de las siguientes fases.  

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

En Microsoft Edge versión [90][DevtoolsWhatsNew202102Devtools] o anterior, si incluyó un icono que no es cuadrado **** en el **** Manifiesto de aplicación web de su PWA, la sección Manifiesto de la herramienta Aplicación muestra una advertencia en Errores y **advertencias** para cada icono que no sea cuadrado.  En Microsoft Edge versión 91 o **** posterior, la **** sección Manifiesto de la herramienta Aplicación no muestra advertencias si proporciona al menos un icono cuadrado.  Si no proporciona ningún icono cuadrado, una advertencia muestra el siguiente mensaje.  

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

Para revisar errores y advertencias en el manifiesto de la aplicación web, vaya a la **herramienta Aplicación** y elija la **sección** Manifiesto.  Los errores y advertencias se enumeran en el **encabezado Errores y advertencias.**  Para obtener más información sobre el manifiesto de aplicación web, vaya a Usar el manifiesto de aplicación [web para integrar la aplicación web progresiva en el sistema operativo][ProgressiveWebAppsWebappmanifests].  Para crear iconos para incluir en el manifiesto de la aplicación web, vaya al Generador de [imágenes de PWABuilder][PwabuilderImagegenerator].  Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya al problema [1185945][CR1185945].  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>Localized DevTools ahora es compatible con Chromium exploradores basados en aplicaciones  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

A partir [Microsoft Edge versión 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools se muestra en su propio idioma.  Muchos desarrolladores usan otras herramientas de desarrollador como StackOverflow y Visual Studio Code en su idioma nativo, no solo en inglés.  El Microsoft Edge de DevTools, el equipo de Chrome DevTools y el equipo de Google Lighthouse colaboraron para proporcionar la misma experiencia en todos los exploradores basados en Chromium web.  Para obtener más información sobre cómo usar DevTools en su idioma, vaya a [Cambiar la configuración de idioma de DevTools][DevtoolsCustomizeLocalization].  Para obtener más información acerca de la colaboración en esta característica Chromium proyecto de código abierto, vaya a [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge explorador y DevTools establecidos en japonés" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Microsoft Edge explorador y DevTools establecidos en japonés  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Usar el teclado para navegar a variables CSS  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

A partir [Microsoft Edge versión 88,][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]el panel **Estilos** muestra variables CSS y proporciona un vínculo directamente a la definición de cada variable.  En Microsoft Edge versión 91 o posterior, puede usar las teclas de flecha para navegar fácilmente a las variables CSS.  Para abrir la definición en el panel **Estilos,** mantenga el mouse en una variable y, a continuación, seleccione `Enter` .  Para obtener más información acerca de las variables CSS, vaya [a Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].  Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya al problema [1187735][CR1187735].  

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

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Uso de DevTools en otros idiomas: novedades de DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../../whats-new/2020/11/devtools.md#css-variable-definitions-in-styles-pane "Definiciones de variables CSS en el panel Estilos: novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Agrupar herramientas en modo de enfoque: novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Abra el menú Comando: ejecute comandos con el Microsoft Edge menú DevTools Command | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Cambiar la configuración de idioma de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Mejoras de service worker | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Ciclo de vida del trabajador de servicio: usar los trabajadores de servicio para administrar las solicitudes de red y las notificaciones de inserción | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Usa el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR1066604]: https://crbug.com/1066604 "Problema 1066604: DevTools: Vea detalles sobre ServiceWorker para instalar y activar eventos | Chromium errores"  
[CR1136655]: https://crbug.com/1136655 "Problema 1136655: Devtools: Localización V2 | Chromium errores"  
[CR1185945]: https://crbug.com/1185945 "Problema 1185945: La advertencia de manifiesto implica que todos los iconos deben ser cuadrados | Chromium errores"  
[CR1187735]: https://crbug.com/1187735 "Problema 1187735: Accesibilidad: MAS2.1.1: Teclado: No se puede invocar la función 'Var(..)' con el teclado | Chromium errores"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas de CSS (variables) | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Generador de imágenes | PWABuilder"  

<!--  > [!NOTE]
> Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].  
> The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen
-->
