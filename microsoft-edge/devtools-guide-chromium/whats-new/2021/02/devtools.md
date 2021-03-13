---
description: Compatibilidad con depuración para CSS Flexbox, presentación de actualizaciones de rendimiento en la página web, problemas de actualizaciones de herramientas y mucho más
title: Novedades de DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408587"
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

## <a name="group-tools-together-in-focus-mode"></a>Agrupar herramientas en modo de foco  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

El modo de enfoque es una interfaz experimental que permite agrupar distintas herramientas en función de sus propios escenarios de depuración.  La nueva **barra de actividades** que se muestra a la izquierda incluye grupos de herramientas predefinidos, como **Diseño** y **depuración.**  Para personalizar cada grupo de herramientas, cierre las herramientas con el icono **Cerrar** \( \) o agregue nuevas herramientas con el icono Más herramientas `X` \( **** `+` \).  

Para activar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione las casillas situadas junto a Modo de foco y Información sobre herramientas **de DevTools** y **Habilitar + menús**de pestañas de botón para abrir más herramientas.  Para obtener más información sobre esta característica o comentar con preguntas e ideas, vaya [a DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Mostrar la barra de actividades" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Mostrar la **barra de actividades**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Obtenga información sobre DevTools con información sobre herramientas informativas  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

La característica DevTools Tooltips le ayuda a obtener información sobre todas las diferentes herramientas y paneles.  Elija el icono Ayuda \( \) situado en la parte inferior de la barra de actividades para alternar la información sobre `?` herramientas en **** DevTools.  Cuando haya información sobre herramientas, mantenga el mouse sobre cada región de DevTools descrita para obtener más información sobre cómo usar la herramienta.  Para activar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione las casillas situadas junto a Modo de foco y Información sobre herramientas **de DevTools** y **Habilitar + menús**de pestañas de botón para abrir más herramientas.  Para obtener más información sobre esta característica o comentar con preguntas e ideas, vaya [a DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Elija el icono ayuda (?) de la barra de actividades para mostrar información sobre herramientas" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Elija el icono Ayuda \( `?` \) de la barra **de actividades** para mostrar información sobre herramientas  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personalizar métodos abreviados de teclado en Configuración  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Ahora puede personalizar el método abreviado de teclado para cualquier acción en DevTools.  Para editar un método abreviado de teclado, realice las siguientes acciones.  

1.  Abra DevTools y, **** a continuación, elija  >  **Métodos abreviados de configuración**.  
1.  Elija la acción que desea personalizar.  
1.  Elija la opción Editar \(![Editar icono de método abreviado de teclado](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) icono.  
1.  Seleccione las claves que desea enlazar a la acción.  
1.  Elija la marca de verificación \(![Icono de método abreviado de teclado Marca de verificación](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) icono.  
    
Para obtener más información acerca de la personalización y edición de accesos directos, vaya a [Personalizar métodos abreviados de teclado en Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personalizar los métodos abreviados de teclado en la configuración de DevTools en accesos directos con un acceso directo en modo de edición" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Personalizar los métodos abreviados de teclado en [la configuración de DevTools][DevtoolsCustomizeIndexSettings] en accesos directos con un acceso directo en modo de edición  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Microsoft Edge DevTools para Visual Studio de extensión de código 1.1.4  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

Microsoft [Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code ahora muestra un icono de favoritos junto a cada una de las instancias de DevTools.  Los mensajes de consola de Microsoft Edge ahora se muestran en **la Consola de DevTools** en **Salida** de Microsoft Visual Studio código.  Microsoft Visual Studio código actualiza las extensiones automáticamente.  Para actualizar manualmente a la versión 1.1.4, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Puede presentar problemas y contribuir a la extensión en el repositorio de GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

:::row:::
   :::column span="":::
      En la siguiente figura se muestran los mensajes de una página web de ejemplo registrada en la **herramienta consola** en Microsoft Edge.  
   :::column-end:::
   :::column span="":::
      En la siguiente figura se muestran los mismos mensajes de la página web de ejemplo registrada en la Consola **de DevTools** en **Salida** de Microsoft Visual Studio código.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Mostrar un mensaje en consola en Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Mostrar un mensaje en consola en Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Mostrar el mismo mensaje en la consola de DevTools en Salida de Microsoft Visual Studio código" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Mostrar el mismo mensaje en la consola de DevTools en Salida de Microsoft Visual Studio código  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Edición mejorada de flexbox CSS con editor de flexbox visual y varias superposiciones  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

DevTools ahora tiene herramientas de depuración de flexbox CSS dedicadas.  Si el estilo o CSS se aplica a un elemento HTML, se muestra un icono junto `display: flex` a ese elemento en la `display: inline-flex` `flex` **herramienta** Elementos.  Para mostrar \(u hide\) una superposición de flex en la página web, elija el `flex` icono.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [1166710][CR1166710] y [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Para abrir el editor **de Flexbox,** vaya al panel **Estilos** y elija el nuevo icono junto al `display: flex` estilo `display: inline-flex` or.  El editor **de Flexbox** proporciona una forma rápida de editar las propiedades de flexbox.  
   :::column-end:::
   :::column span="":::
      Además, la sección **Flexbox** del panel **Diseño** muestra todos los elementos de flexbox en la página web.  Puede alternar la superposición de cada elemento.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Herramientas de depuración de flexbox CSS" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         Herramientas de depuración de flexbox CSS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Sección Flexbox en el panel Diseño" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         **Sección Flexbox** en el **panel Diseño**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Mejoras de navegación con teclado para solicitudes de red  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Anteriormente, no podía expandir o contraer la cadena de solicitudes con las teclas de flecha del teclado en el panel **Iniciador,** a diferencia del DOM de la **herramienta** Elementos.  Cuando se selecciona una solicitud de red en la **herramienta** Red, el panel **Iniciador** muestra la cadena de solicitudes que inició la solicitud seleccionada actualmente.  

En Microsoft Edge versión 90, puede expandir o contraer la cadena de solicitudes mediante las teclas de flecha del teclado en el **panel Iniciador.**  Ahora también se resalta la solicitud de red centrada en la cadena.  Para obtener más información sobre los iniciadores en la **herramienta Red,** vaya [a Mostrar iniciadores y dependencias][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [1158276][CR1158276] y [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Elija una solicitud de red y elija el panel Iniciador" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Elija una solicitud de red y elija el **panel Iniciador**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Expandir o contraer la cadena de iniciador de solicitudes y seguir la fila resaltada" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Expandir o contraer la cadena de iniciador de solicitudes y seguir la fila resaltada  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>El filtrado en la consola es más coherente  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Mientras filtra con la barra lateral [de la][DevtoolsConsoleReferenceOpenConsoleSidebar]consola, los filtros de la lista desplegable [Niveles de][DevtoolsConsoleReferenceFilterByLogLevel] registro no están disponibles.  Anteriormente, la lista desplegable **Niveles de** registro se resaltaba al mantener el mouse sobre él, incluso mientras se seleccionaba un filtro de **la** barra lateral de la consola.  En la versión 90 de Microsoft Edge, el desplegable **Niveles** de registro ya no se resalta al mantener el mouse sobre él mientras se elige un filtro de la barra **lateral** de consola.  Para obtener más información sobre el filtrado en la **consola,** vaya a [Filtrar mensajes][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Anteriormente, si abres la barra lateral de consola y mantienes el mouse en niveles predeterminados, se resaltó." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Anteriormente, si abres la **barra** lateral de consola y mantienes el mouse en **niveles predeterminados,** se resaltó.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="A partir de Microsoft Edge 90, si eliges la barra lateral de consola y mantienes el mouse en Niveles predeterminados, no se resalta" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         A partir de Microsoft Edge 90, si eliges la barra lateral de consola y mantienes el mouse en **Niveles**predeterminados, no se resalta ****  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>La consola ahora se escape de caracteres de comilla doble  

Anteriormente, la **consola no** generaba caracteres válidos de comilla doble \( `"` \) en cadenas javascript.  A partir de la versión **** 90 de Microsoft Edge, la consola genera cadenas de JavaScript con caracteres de comilla doble de escape \( `"` \).  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="La consola genera cadenas de JavaScript con caracteres de comilla doble de escape (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   La **consola genera** cadenas de JavaScript con caracteres de comilla doble de escape \( `"` \)  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Emular la característica multimedia de gama de colores CSS  

La [consulta multimedia de gama][ChromestatusFeature5354410980933632] de colores emula el intervalo aproximado de colores admitido por el explorador y el dispositivo que estás probando.  El desplegable de **emular la** gama de colores de la característica multimedia CSS contiene espacios de color que DevTools puede emular.  Por ejemplo, para desencadenar una consulta `color-gamut: p3` multimedia, elija **color-gamut: p3** en el desplegable.  

Para emular la característica multimedia de gama de colores CSS, realice las siguientes acciones.  

1.  Abra el [menú de comandos][DevtoolsCommandMenuIndex].  
1.  Escribe `Rendering`.  
1.  Ejecute el **comando Mostrar representación.**  
1.  Vaya a **Emular la gama de colores de** la característica multimedia CSS y elija una opción.  

Para obtener más información sobre la `color-gamut` característica, vaya [a Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1073887][CR1073887].  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emular la característica multimedia de gama de colores CSS" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Emular la característica multimedia de gama de colores CSS  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Herramientas mejoradas de aplicaciones web progresivas  

#### <a name="pwa-installability-warning-in-the-console"></a>Advertencia de instalación de PWA en la consola  

La **consola** ahora muestra un mensaje de advertencia de instalación de Aplicaciones web progresivas [(PWA)][ProgressiveWebAppsIndex] más detallado con un vínculo a Mejorar la detección de compatibilidad sin conexión de [Progressive Web App][ChromeDeveloperBlogImprovedPwaOfflineDetection].  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Advertencia de instalación de PWA en la herramienta consola" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Advertencia de instalación de PWA en **la herramienta consola**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Advertencia de longitud de descripción de PWA en el panel Manifiesto

El **panel** Manifiesto ahora muestra un mensaje de advertencia si la descripción del manifiesto supera los 324 caracteres.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Advertencia truncada de descripción de PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Advertencia truncada de descripción de PWA  
:::image-end:::  

Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [965802][CR965802], [1146450][CR1146450]y [1169689][CR1169689].  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Nueva columna Espacio de direcciones remotas en la herramienta Red  

<!-- does not work in canary 90.0.813.0 -->  
La nueva **columna Espacio de direcciones remotas** muestra el espacio de direcciones IP de red de cada recurso de red.  Para mostrar la nueva columna Espacio de direcciones remotas, realice las siguientes acciones.  

1.  Vaya a la **herramienta Red.**  
1.  En la tabla Solicitudes, mantenga el mouse en la fila de encabezado y abra el menú contextual \(hacer clic con el botón secundario\).  Para obtener información sobre cómo agregar o quitar columnas de la tabla Solicitudes, vaya a [Agregar o quitar columnas.][DevtoolsNetworkReferenceAddRemoveColumns]  
1.  Elija **Espacio de direcciones remotas**.  
    
La tabla Solicitudes ahora muestra una nueva columna con el encabezado denominado **Espacio de direcciones remotas**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="En el menú contextual, elija Espacio de direcciones remotas" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         En el menú contextual, elija el **espacio de direcciones remotas**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="La tabla Solicitudes ahora muestra la columna Espacio de direcciones remotas" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         La tabla Solicitudes ahora muestra la **columna Espacio de direcciones** remotas :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Mostrar características permitidas y no permitidas en la vista Detalles del marco  

La vista Detalles del marco ahora muestra una lista de características de explorador permitidas y no [permitidas controladas][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]por la directiva de permisos .  Directiva de permisos es una API de plataforma web que permite \(o bloques\) una página web el uso de características del explorador en un marco individual o en iframes que inserta.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Características permitidas y no permitidas basadas en la directiva de permisos" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Características permitidas y no permitidas basadas en la directiva de permisos  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Nueva columna SameParty en el panel Cookies  

El **panel Cookies** de la herramienta **Aplicación** ahora muestra el atributo de `SameParty` cada cookie.  El `SameParty` atributo es un nuevo atributo booleano para indicar si una cookie se incluye en las solicitudes a los orígenes de los mismos conjuntos de [terceros][GithubPrivacycgFirstPartySets].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1161427][CR1161427].  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Columna SameParty en el panel Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   **Columna SameParty** en el **panel Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>La propiedad fn.displayName de la herramienta Consola ya está en desuso  

Anteriormente, la propiedad le permitía controlar los nombres de depuración de las funciones que se muestran en y en los seguimientos de pila `fn.displayName` `error.stack` de DevTools.  A partir de la versión 90 de Microsoft Edge, la propiedad ahora está en `fn.displayName` desuso y reemplazada por la `fn.name` propiedad.  Use el método `Object.defineProperty` estándar para definir la `fn.name` propiedad.  Para obtener más `fn.name` información, vaya [a Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1177685][CR1177685].  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Un ejemplo de la propiedad fn.name para controlar los nombres de depuración de las funciones" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Un ejemplo de la `fn.name` propiedad para controlar los nombres de depuración de las funciones  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Vista de árbol de accesibilidad completa en la herramienta Elementos  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Este experimento proporciona una **vista de árbol de accesibilidad completa** en la **herramienta** Elementos.  El [panel Accesibilidad][DevtoolsAccessibilityReferenceTheAccessibilityPane] proporciona una vista de árbol de accesibilidad parcial, que muestra la cadena antecesora directa del nodo raíz al nodo inspeccionado.  
Después de activar este experimento y volver a cargar DevTools, elija uno de los siguientes botones para cambiar la pantalla en la herramienta Elementos para todos los elementos de la página web.  

*   Para mostrar la vista de árbol de accesibilidad completa, elija la **vista Cambiar a árbol de accesibilidad.**  
*   Para mostrar la vista de árbol DOM, elija **la vista Cambiar a árbol DOM**.  
    
Para activar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione la casilla situada junto a Habilitar la vista de árbol **de accesibilidad completa en el panel Elementos**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Mostrar la vista de árbol DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Mostrar la **vista DOM**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Mostrar la vista de árbol de accesibilidad completa" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Mostrar la **vista Árbol de accesibilidad completa**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si estás en Windows, Linux o macOS, considera usar los canales de vista previa [de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "El panel Accesibilidad: referencia de accesibilidad | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nivel de registro: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filtrar mensajes: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Abra la barra lateral de la consola: referencia de consola | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalización de métodos abreviados de teclado en las herramientas de desarrollo de Microsoft Edge | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Habilitar los menús de la pestaña + botón para abrir más herramientas: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Agregar o quitar columnas: referencia de análisis de red | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Mostrar iniciadores y dependencias: referencia de análisis de red | Microsoft Docs"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Información general de Aplicaciones web progresivas en Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Extension Marketplace | Visual Studio código"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio código | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Mejora de la detección de soporte técnico sin conexión de Progressive Web App | Desarrolladores de Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "Consulta multimedia de gama de colores | Estado de la plataforma Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir la personalización de métodos abreviados de teclado o enlaces de clave | Errores de Chromium"  
[CR887173]: https://crbug.com/887173 "Problema 887173: DevTools: Inspección completa del árbol de accesibilidad | Errores de Chromium"  
[CR965802]: https://crbug.com/965802 "Problema 965802: Implementar la detección de funcionalidad sin conexión del trabajador del servicio más precisa | Errores de Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problema 1073887: DevTools: @media (color-gamut: ...) colorspace emulation | Errores de Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problema 1128885: Compatibilidad con DevTools para CORS-RFC1918 | Errores de Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problema 1146450: [Android] Implementar las instalación de la hoja inferior | Errores de Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problema 1158276: No se puede expandir o contratar el panel "Solicitar cadena de iniciador" mediante teclas de flecha en la sección "Red" de DevTools | Errores de Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Directiva de permisos] Implementar la compatibilidad de devtool para la directiva de permisos | Errores de Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problema 1160637: El foco en "Solicitar cadena de iniciador" se ve incompleto en la sección "Red" de la ventana "Herramientas de desarrollo" | Errores de Chromium"  
[CR1161427]: https://crbug.com/1161427 "Problema 1161427: &#9730; compatibilidad con la depuración de atributos de cookies sameparty en DevTools | Errores de Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problema 1166710: activar el experimento de herramientas flexbox de forma predeterminada | Errores de Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problema 1169689: La hoja inferior de instalación de PWA no debe incluir categorías | Errores de Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problema 1175699: Editor de Flexbox | Errores de Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problema 1177685: Quitar la compatibilidad con fn.displayName no estándar | Errores de Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problema 1178530: la consola no se escapa a las comillas dobles al imprimir cadenas | Errores de Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Calidad de visualización de color: la característica "color-gamut" | Borradores del editor de grupo de trabajo css"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Interfaz de usuario del modo de enfoque: MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Conjuntos de primera | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicador de directivas de permisos | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2021/02/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
