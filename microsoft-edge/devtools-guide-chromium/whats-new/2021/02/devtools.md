---
description: Compatibilidad en la depuración para CSS Flexbox, rendimiento de visualización frontal en la página web, problemas de actualizaciones de herramientas y mucho más
title: Novedades de DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.localizationpriority: high
ms.openlocfilehash: a13c344bb31cdfb7d0402132e3be82e4c330c612
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597160"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>Novedades de DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Grupo de herramientas en modo Focalizado  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

El modo Focalizado es una interfaz experimental que permite agrupar distintas herramientas en función de sus propios escenarios de depuración.  La nueva **Barra de Actividad** que se muestra a la izquierda incluye grupos de herramientas predefinidos, como **Diseño** y **Depuración**.  Para personalizar cada grupo de herramientas, cierre las herramientas con el icono **Cerrar** \(`X`\) o agregue nuevas herramientas con el icono **Más herramientas** \(`+`\).  

Para activar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione las casillas situadas junto **Modo Focalizado e Información sobre herramientas de DevTools** y **Habilitar + menús de pestañas de botón para abrir más herramientas**.  Para obtener más información sobre esta característica o dejar un comentario con preguntas e ideas, vaya a [DevTools: interfaz de usuario del Modo Focalizado][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Mostrar la Barra de Actividades" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Mostrar la **Barra de Actividades**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Aprenda más sobre DevTools con la información sobre herramientas informativas  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

La función Información de herramientas de DevTools le ayuda a obtener información sobre todo el conjunto diverso de herramientas y paneles.  Elija el icono Ayuda \(`?`\) situado en la parte inferior de la **Barra de Actividades** para alternar la información sobre herramientas de DevTools.  Cuando haya información sobre herramientas disponible, pase el ratón por encima de cada región para aprender a usar la herramienta.  Para activar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione las casillas situadas junto **Modo Focalizado e Información sobre herramientas de DevTools** y **Habilitar + menús de pestañas de botón para abrir más herramientas**.  Para obtener más información sobre esta característica o dejar un comentario con preguntas e ideas, vaya a [DevTools: interfaz de usuario del Modo Focalizado][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Elija el icono Ayuda (?) de la Barra de Actividades para mostrar información sobre herramientas" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Elija el icono Ayuda \(`?`\) de la **Barra de Actividades** para mostrar información sobre herramientas  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personalizar accesos rápidos de teclado en Configuración  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Ahora puede personalizar el acceso rápido de teclado para cualquier acción en DevTools.  Para editar un acceso rápido de teclado, siga los siguientes pasos.  

1.  Abra DevTools y, a continuación, elija **Configuración** > **Accesos rápidos**.  
1.  Elija la acción que quiere personalizar.  
1.  Elija el icono \(![Icono para editar el acceso rápido de teclado](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) Editar.  
1.  Seleccione las claves con las que quiere enlazar la acción.  
1.  Elija el icono \(![Icono de la marca de verificación del acceso rápido de teclado](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) de la marca de verificación.  
    
Para obtener más información acerca de la personalización y edición de accesos directos, vaya a [Personalizar accesos rápidos de teclado en Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personalizar los accesos rápidos de teclado en la Configuración de DevTools con un acceso directo en el modo de edición" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Personalizar los accesos rápidos de teclado en la [Configuración de DevTools][DevtoolsCustomizeIndexSettings] con un acceso directo en el modo de edición  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Actualización 1.1.4 de la extensión de Microsoft Edge DevTools para Visual Studio Code  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

La versión de extensión 1.1.4 de las [Herramientas de desarrollador de Microsoft Edge para Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] para Microsoft Visual Studio Code ahora muestra un icono de favoritos al lado de cada instancia de DevTools.  Los mensajes de consola de Microsoft Edge ahora se muestran en la **Consola de DevTools**, debajo de **Salida** de Microsoft Visual Studio Code.  Microsoft Visual Studio Code actualiza las extensiones automáticamente.  Para actualizar manualmente a la versión 1.1.4, vaya a [Actualizar extensión manualmente][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].  Puede archivar problemas y contribuir con la extensión en el repositorio de GitHub [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

:::row:::
   :::column span="":::
      En la siguiente figura se muestran los mensajes de una página web de ejemplo registrada en la herramienta **Consola** en Microsoft Edge.  
   :::column-end:::
   :::column span="":::
      En la siguiente figura se muestran los mismos mensajes de la página web de ejemplo registrada en la **Consola de DevTools** bajo **Salida** de Microsoft Visual Studio Code.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Mostrar un mensaje en la Consola en Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Mostrar un mensaje en la Consola en Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Mostrar el mismo mensaje en la Consola de DevTools debajo de Salida de Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Mostrar el mismo mensaje en la Consola de DevTools debajo de Salida de Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Mejora de la edición de CSS flexbox con un editor visual de flexbox y múltiples superposiciones  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

DevTools ahora tiene herramientas de depuración de CSS Flexbox.  Si el estilo `display: flex` o `display: inline-flex` de CSS se aplica a un elemento HTML, se muestra un icono `flex` junto a ese elemento en la herramienta **Elementos**.  Para mostrar \(u ocultar\) una superposición de flex en la página web, elija el icono `flex`.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a los problemas [1166710][CR1166710] y [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Para abrir el editor **Flexbox,** vaya al panel **Estilos** y elija el nuevo icono que aparece junto al estilo `display: flex` o `display: inline-flex`.  El editor **Flexbox** proporciona una forma rápida de editar las propiedades del flexbox.  
   :::column-end:::
   :::column span="":::
      Además, la sección **Flexbox** del panel **Diseño** muestra todos los elementos de flexbox en la página web.  Puede alternar la superposición de cada elemento.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Herramientas de depuración de CSS Flexbox" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         Herramientas de depuración de CSS Flexbox  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Sección Flexbox en el panel Diseño" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         Sección **Flexbox** en el panel **Diseño**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Mejoras de navegación con el teclado para solicitudes de red  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Antes, no se podía expandir o contraer la cadena de solicitudes con las teclas de dirección del teclado en el panel **Iniciador**, a diferencia del DOM de la herramienta**Elementos**.  Cuando se selecciona una solicitud de red en la herramienta**Red**, el panel **Iniciador** muestra la cadena de solicitudes que inició la solicitud que está seleccionada en cada momento.  

En la versión 90 de Microsoft Edge, se puede expandir o contraer la cadena de solicitudes mediante las teclas de dirección del teclado en el panel **Iniciador**.  Ahora también se resalta la solicitud de red centrada en la cadena.  Para obtener más información sobre los iniciadores de la herramienta **Red**, vaya a [Mostrar iniciadores y dependencias][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a los problemas [1158276][CR1158276] and [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Elija una solicitud de red y el panel Iniciador" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Elija una solicitud de red y el panel **Iniciador**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Expandir o contraer la cadena del iniciador de solicitudes y seguir la fila resaltada" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Expandir o contraer la cadena del iniciador de solicitudes y seguir la fila resaltada  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>El filtrado en la Consola es más coherente  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Mientras filtra con la [Barra Lateral de la Consola][DevtoolsConsoleReferenceOpenConsoleSidebar], los filtros de la lista desplegable [Niveles de registro][DevtoolsConsoleReferenceFilterByLogLevel] no están disponibles.  Antes, la lista desplegable **Niveles de registro** se resaltaba al mantener el ratón sobre ella, incluso cuando se seleccionaba un filtro de la **barra lateral de la Consola**.  En la versión 90 de Microsoft Edge, la lista desplegable **Niveles de registro** ya no se resalta al mantener el ratón sobre ella mientras se elige un filtro de la **barra lateral de consola**.  Para obtener más información sobre el filtrado en la **Consola**, vaya a [Filtrar mensajes][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Antes, si se abría la barra lateral de consola y se mantenía el ratón en los niveles predeterminados, se resaltaba." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Antes, si se abría la **barra lateral de la consola** y se mantenía el ratón en los **niveles predeterminados**, se resaltaba.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="A partir de Microsoft Edge 90, si se elije la barra lateral de la Consola y se mantiene el ratón en los niveles predeterminados, no se resalta" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         A partir de Microsoft Edge 90, si se elije la **barra lateral de la Consola** y se mantiene el ratón en los **niveles predeterminados**, no se resalta  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>La consola ahora evita los caracteres de comillas dobles  

Antes, la **Consola** no generaba caracteres válidos de comillas dobles \(`"`\) en cadenas de JavaScript.  A partir de la versión 90 de Microsoft Edge, la **Consola** genera cadenas de JavaScript con caracteres de comillas dobles de escape \(`"`\).  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="La Consola genera cadenas de JavaScript con caracteres de comilla doble de escape (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   La **Consola** genera cadenas de JavaScript con caracteres de comilla doble de escape \(`"`\)  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Emular la función multimedia de la gama de colores CSS  

La consulta de medios [gama de colores][ChromestatusFeature5354410980933632] emula el intervalo aproximado de colores admitido por el explorador y el dispositivo que estás probando.  La lista desplegable de debajo de **Emular la gama de colores de la función multimedia CSS** contiene espacios de colores que DevTools puede emular.  Por ejemplo, para desencadenar una `color-gamut: p3`consulta de medios, elija **gama de colores: p3** en la lista desplegable.  

Para emular la función multimedia de gama de colores CSS, siga los siguientes pasos.  

1.  Abra el [Menú de comandos][DevtoolsCommandMenuIndex].  
1.  Escriba `Rendering`.  
1.  Ejecute el comando **Mostrar representación**.  
1.  Vaya a **Emular la gama de colores de la función multimedia CSS** y elija una opción.  

Para obtener más información sobre esta `color-gamut` función, vaya a [Calidad de la calibración de colores: la función 'gama de colores'][CsswgDraftsMediaqueries4ColorGamut].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1073887][CR1073887].  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emular la función multimedia de la gama de colores CSS" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Emular la función multimedia de la gama de colores CSS  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Herramientas mejoradas de aplicaciones web progresivas  

#### <a name="pwa-installability-warning-in-the-console"></a>Advertencia de instalación de PWA en la Consola  

La **Consola** ahora muestra un mensaje de advertencia más detallado sobre la instalación de [aplicaciones web progresivas (PWA)][ProgressiveWebAppsIndex] con un vínculo a [Mejorar la detección de compatibilidad sin conexión de Progressive Web App][ChromeDeveloperBlogImprovedPwaOfflineDetection].  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Advertencia de instalación de PWA en la herramienta Consola" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Advertencia de instalación de PWA en la herramienta **Consola**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Advertencia de longitud de descripción de PWA en el panel Manifiesto

El panel **Manifiesto** ahora muestra un mensaje de advertencia si la descripción del manifiesto supera los 324 caracteres.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Advertencia truncada de descripción de PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Advertencia truncada de descripción de PWA  
:::image-end:::  

Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a los problemas [965802][CR965802], [1146450][CR1146450] y [1169689][CR1169689].  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Nueva columna Espacio de direcciones remotas en la herramienta Red  

<!-- does not work in canary 90.0.813.0 -->  
La nueva columna **Espacio de direcciones remotas** muestra el espacio de direcciones IP de red de cada recurso de red.  Para mostrar la nueva columna Espacio de direcciones remotas, siga los siguientes pasos.  

1.  Vaya a la herramienta **Red**.  
1.  En la tabla Solicitudes, mueva el ratón sobre la fila del encabezado y abra el menú contextual \(hacer clic con el botón derecho\).  Para obtener información sobre cómo agregar o quitar columnas de la tabla Solicitudes, vaya a [Agregar o quitar columnas][DevtoolsNetworkReferenceAddRemoveColumns].  
1.  Elija **Espacio de direcciones remotas**.  
    
La tabla Solicitudes ahora muestra una nueva columna con un encabezado denominado **Espacio de direcciones remotas**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="En el menú contextual, elija Espacio de direcciones remotas" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         En el menú contextual, elija **Espacio de direcciones remotas**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="La tabla Solicitudes ahora muestra la columna Espacio de direcciones remotas" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         La tabla Solicitudes ahora muestra la columna **Espacio de direcciones remotas** :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Mostrar características permitidas y no permitidas en la vista Detalles del marco  

La vista Detalles del marco ahora muestra una lista de características de explorador que están permitidas y no permitidas controladas por la [Directiva de permisos][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].  La Directiva de permisos es una API de plataforma web que permite \(o bloquea\) a una página web el uso de características del explorador en un marco individual o en IFrames que inserta.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Características permitidas y no permitidas basadas en la Directiva de permisos" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Características permitidas y no permitidas basadas en la Directiva de permisos  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Nueva columna SameParty en el panel de las Cookies  

El panel de las **Cookies** de la herramienta **Aplicación** ahora se muestra el atributo `SameParty` para cada cookie.  El atributo `SameParty` es un nuevo atributo booleano que permite indicar si una cookie está incluida en las solicitudes a los orígenes de los mismos [Conjuntos de primeras partes][GithubPrivacycgFirstPartySets].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1161427][CR1161427].  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Columna SameParty en el panel de las Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   Columna **SameParty** en el panel de las **Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>La propiedad fn.displayName de la herramienta Consola ya está en desuso  

Antes, la propiedad `fn.displayName` permitía controlar los nombres de depuración de las funciones que se muestran en`error.stack` y en los seguimientos de pila de DevTools.  A partir de la versión 90 de Microsoft Edge, la propiedad `fn.displayName` ahora está en desuso y es reemplazada por la propiedad `fn.name`.  Use el método estándar `Object.defineProperty` para definir la propiedad `fn.name`.  Para obtener más información sobre `fn.name`, vaya a [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1177685][CR1177685].  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Un ejemplo de la propiedad fn.name para controlar los nombres de depuración de las funciones" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Un ejemplo de la propiedad `fn.name` para controlar los nombres de depuración de las funciones  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Vista de árbol de accesibilidad completa en la herramienta Elementos  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Este experimento proporciona una **vista de árbol de accesibilidad completa** en la herramienta **Elementos**.  El panel [Accesibilidad][DevtoolsAccessibilityTab] proporciona una vista de árbol de accesibilidad parcial, que muestra la cadena directamente anterior del nodo raíz al nodo inspeccionado.  
Después de activar este experimento y volver a cargar DevTools, elija uno de los siguientes botones para cambiar la visualización en la herramienta Elementos para todos los elementos de la página web.  

*   Para mostrar la vista de árbol de accesibilidad completa, elija la **vista Cambiar a árbol de accesibilidad**.  
*   Para mostrar la vista de árbol DOM, elija la **vista Cambiar a árbol DOM**.  
    
Para activar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione la casilla situada junto a **Habilitar la vista de árbol de accesibilidad completa en el panel Elementos**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Mostrar la vista de árbol DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Mostrar la **vista de árbol DOM**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Mostrar la vista de árbol de accesibilidad completa" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Mostrar la **vista Árbol de accesibilidad completa**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityTab]: ../../../accessibility/accessibility-tab.md "Probar la accesibilidad con la pestaña Accesibilidad | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: ../../../console/reference.md#filter-by-log-level "Filtrar por nivel de registro: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: ../../../console/reference.md#filter-messages "Filtrar mensajes: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: ../../../console/reference.md#open-the-console-sidebar "Abrir la barra lateral de la consola: referencia de consola | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalización de accesos rápidos de teclado en las herramientas de desarrollo de Microsoft Edge | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: ../../../experimental-features/index.md#enable--button-tab-menus-to-open-more-tools "Habilitar + menús de las pestañas de los botones para abrir más herramientas: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../../../experimental-features/index.md#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: ../../../network/reference.md#add-or-remove-columns "Agregar o quitar columnas: referencia de análisis de red | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Mostrar iniciadores y dependencias: referencia de análisis de red | Microsoft Docs"  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Información general de aplicaciones web progresivas en Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Mejora de la detección de la compatibilidad sin conexión de la aplicación web progresiva | Desarrolladores de Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "Consulta multimedia de gama de colores | Estado de la plataforma Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir la personalización de accesos rápidos de teclado o enlaces de clave | Errores de Chromium"  
[CR887173]: https://crbug.com/887173 "Problema 887173: DevTools: Inspección completa del árbol de accesibilidad | Errores de Chromium"  
[CR965802]: https://crbug.com/965802 "Problema 965802: Implementar la detección de funcionalidad sin conexión del trabajador del servicio que precise | Errores de Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problema 1073887: DevTools: @media (gama de colores: ...) emulación de espacio de color | Errores de Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problema 1128885: Compatibilidad de DevTools para CORS-RFC1918 | Errores de Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problema 1146450: [Android] Implementar las instalaciones de la hoja inferior | Errores de Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problema 1158276: No se puede expandir o contratar el panel &quot;Solicitar cadena de iniciador&quot; mediante las teclas de dirección en la sección &quot;Red&quot; de DevTools | Errores de Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Directiva de permisos] Implementar la compatibilidad de DevTools para la directiva de permisos | Errores de Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problema 1160637: El foco en &quot;Solicitar cadena de iniciador&quot; se ve incompleto en la sección &quot;Red&quot; de la ventana &quot;Herramientas para desarrolladores&quot; | Errores de Chromium"  
[CR1161427]: https://crbug.com/1161427 "Problema 1161427: &#9730; compatibilidad con la depuración de atributos de cookies SameParty en DevTools | Errores de Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problema 1166710: activar el experimento de herramientas flexbox de forma predeterminada | Errores de Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problema 1169689: La hoja inferior de instalación de PWA no debe incluir categorías | Errores de Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problema 1175699: Editor de Flexbox | Errores de Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problema 1177685: Quitar la compatibilidad con un fn.displayName no estándar | Errores de Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problema 1178530: la consola no evita las comillas dobles al imprimir cadenas | Errores de Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Calidad de visualización de color: la característica &quot;gama de colores&quot; | Borradores del editor de grupo de trabajo CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Interfaz de usuario del modo de enfoque: MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Conjuntos de primera | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicador de directivas de permisos | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-90) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
