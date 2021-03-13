---
description: La herramienta Novedades es ahora Welcome, Visual Font Editor en el panel Estilos, herramientas de depuración de CSS Flexbox y mucho más.
title: Novedades de DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2722da0093b3ba6521b5190e61bb208e02a2041e
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408342"
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
# <a name="whats-new-in-devtools-microsoft-edge-89"></a>Novedades de DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a>What's New is now Welcome  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

La **herramienta Novedades** de Microsoft Edge DevTools ahora tiene una nueva apariencia y un nuevo nombre:  **Welcome**.  La **herramienta DevTools** aún muestra las últimas noticias y actualizaciones de DevTools.  Ahora también incluye vínculos a la documentación de Microsoft Edge DevTools, formas de enviar comentarios y mucho más.  Para mostrar la **herramienta De** bienvenida después de cada actualización a Microsoft Edge, seleccione la casilla situada junto a la pestaña Abrir después de cada **actualización** en el título.  Para cerrar la **herramienta De** bienvenida, elija **la X** en el lado derecho del título de la pestaña.  Si prefiere la herramienta **novedades** original, [][DevtoolsCustomizeIndexSettings]vaya a Experimentos de configuración y quite la casilla situada junto a  >  **** La pestaña Habilitar **bienvenida**.  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="La herramienta De bienvenida está resaltada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   La **herramienta De** bienvenida está resaltada  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Editor de fuentes visuales en el panel Estilos  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Cuando trabaje con fuentes en CSS, use el nuevo editor de [fuentes visual][DevtoolsInspectStylesEditFonts].  Puede definir fuentes de reserva y usar controles deslizantes para definir el grosor de fuente, el tamaño, el alto de línea y el espaciado.  El **Editor de fuentes** le ayuda a completar las siguientes acciones.  

*   Cambiar entre unidades para distintas propiedades de fuente  
*   Cambiar entre palabras clave para distintas propiedades de fuente  
*   Convertir unidades  
*   Generar código CSS preciso  
    
Para activar este experimento, vaya a [Settings][DevtoolsCustomizeIndexSettings]  >  **Experiments** y elija la casilla situada junto a **Enable new Font Editor tools within Styles pane**.  Para obtener más información, vaya a Editar estilos y configuraciones de fuentes CSS en [el panel Estilos de DevTools][DevtoolsInspectStylesEditFonts].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="El editor de fuentes visuales se resalta en el panel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   El editor **de fuentes visuales** se resalta en el panel **Estilos**  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>Herramientas de depuración de CSS Flexbox  

Las características de depuración de Flexbox están en desarrollo activo.  Para activar el experimento para las dos [][DevtoolsCustomizeIndexSettings]características siguientes, vaya a Experimentos de configuración y seleccione la casilla situada junto a Habilitar nuevas características  >  **** **de depuración de CSS Flexbox**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [1136394][CR1136394] y [1139949][CR1139949].  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>El nuevo icono de Flexbox (flex) ayuda a identificar y mostrar contenedores flex  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

En la **herramienta Elementos,** el nuevo icono de Flexbox (flex) le ayuda a identificar los contenedores de Flexbox en el código.  Elija el icono Flexbox \(flex\) para activar o desactivar el efecto de superposición que describe un contenedor de Flexbox.  Puede personalizar el color de la superposición en el **panel** Diseño, que se encuentra junto **a Styles** y **Computed**.  

:::row:::
   :::column span="":::
      Para activar y desactivar el efecto de superposición que describe el contenedor de Flexbox, elija el icono Flexbox \( `flex` \).  
   :::column-end:::
   :::column span="":::
      Puede personalizar el color de la superposición en el panel **Diseño** situado junto **a Styles** y **Computed**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Icono de Flexbox (flex) y página web resaltados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         El **icono de Flexbox** \( `flex` \) y la página web resaltados :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Las superposiciones de Flexbox resaltadas en el panel Diseño" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         Las **superposiciones de Flexbox resaltadas** en el **panel Diseño**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-gridlines-when-flexbox-layouts-change-using-css-properties"></a>Mostrar iconos de alineación y líneas de cuadrícula cuando los diseños de Flexbox cambian con propiedades CSS  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Cuando edita CSS para el diseño de Flexbox, CSS autocompleta en el panel **Estilos** ahora muestra iconos útiles junto a las propiedades relevantes de Flexbox.  Para probar esta nueva característica, abra la **herramienta Elementos** y seleccione un contenedor flexible.  A continuación, agregue o cambie una propiedad en ese contenedor en el **panel Estilos.**  

:::row:::
   :::column span="":::
      El menú autocompletar ahora muestra iconos que indican el efecto de las propiedades de alineación, `align-content` como y `align-items` .  
   :::column-end:::
   :::column span="":::
      Además, DevTools ahora muestra una línea de guía que le ayudará a revisar mejor la `align-items` propiedad CSS.  También `gap` se admite la propiedad CSS.  En la siguiente figura, la propiedad CSS se establece en y se muestra el patrón de sombreado `gap` `gap: 12px;` para cada espacio.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menú Autocompletar resaltado para las propiedades CSS que comienzan con align-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menú Autocompletar resaltado para las propiedades CSS que empiezan por `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Espacio de Flexbox en las propiedades CSS y la página web resaltadas" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` en propiedades CSS y página web resaltadas  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Agregar herramientas rápidamente con el nuevo botón Más herramientas  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Ahora tiene una nueva forma de abrir más herramientas en Microsoft Edge DevTools.  Después de activar este experimento, el icono Más **herramientas** se muestra como signo más ( ) a la derecha `+` del panel principal.  Para mostrar una lista de otras herramientas que se agregarán al panel principal, elija el icono **Más herramientas** \( `+` \).  Para activar este experimento, vaya a [Settings][DevtoolsCustomizeIndexSettings]  >  **Experiments**y, a continuación, seleccione la casilla situada junto a Habilitar + menús de pestañas de botón **para abrir más herramientas.**  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Más herramientas resaltadas en DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Más herramientas** resaltadas en DevTools  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Las tecnologías de asistencia ahora anuncian la posición y el recuento de sugerencias de CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Cuando edita CSS, obtiene un desplegable de características.  Esta característica no estaba disponible para los usuarios de tecnologías de asistencia, ya que se anuncia en La versión 89 de Microsoft Edge.  Un usuario de tecnologías de asistencia ahora puede navegar por sugerencias CSS en el **panel Estilos.**  En Microsoft Edge versión 88 y versiones anteriores, la tecnología de asistencia anunciada como un usuario navegaba por la lista de sugerencias al editar `Suggestion` CSS en el panel **Estilos.**  En La versión 89 de Microsoft Edge, un usuario de tecnología de asistencia ahora escucha la posición y el recuento de la sugerencia actual.  Cada sugerencia se anuncia a medida que el usuario navega por la lista de sugerencias, como sugerencia 3 de 5.  Para obtener más información sobre cómo escribir CSS en DevTools, vaya a [Cambiar CSS][DevtoolsCssReferenceChangeCss].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1157329][CR1157329].  

Para ver un vídeo que muestra y lee en voz alta varias sugerencias con este experimento activado, vaya a Voiceover anunciando opciones [de devtools](https://youtu.be/9TcUpleEwwA) en YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Sugerencia resaltada en el panel Estilos" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   La `suggestion` lista resaltada en el **panel Estilos**  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emular Surface Duo y Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Prueba la apariencia de tu sitio web o aplicación en los siguientes dispositivos de Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Activa las **características de la plataforma web experimental** para obtener acceso a la nueva característica de pantalla de medios [CSS][DualScreenWebCssMediaSpanning] y a la API [de JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  Vaya a `edge://flags` y cambie la marca junto a Características de la plataforma web **experimental.**  Para ayudar a mejorar tu sitio web o aplicación para los dispositivos de pantalla doble y plegables, usa las siguientes características [al emular el dispositivo][DevtoolsDeviceModeIndex].  

*   [Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], que es cuando aparece el sitio web \(o aplicación\) en ambas pantallas.  
*   [Representación de la costura][DualScreenIntroductionHowToWorkWithSeam], que es el espacio entre las dos pantallas.  
    
Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular la pantalla dual" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emular la pantalla dual  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2  

Microsoft [Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code tiene los siguientes cambios desde la versión anterior.  Microsoft Visual Studio código actualiza las extensiones automáticamente.  Para actualizar manualmente a la versión 1.1.2, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Se agregó un **botón Cerrar instancia** a cada elemento de la lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Versión de [Microsoft Edge DevTools][DevtoolsMain] de 84.0.522.63 a [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Depurador [incluido para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como dependencia \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Opción de configuración implementada para cambiar los temas de extensión \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Puede presentar problemas y contribuir a la extensión en el repositorio [de GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Captura de pantalla de nodo más allá de la ventanilla  

En Microsoft Edge versión 89, las capturas de pantalla de nodo son más precisas, capturando el nodo completo incluso si el contenido del nodo no está visible en la ventanilla.  En la **herramienta Elementos,** mantenga el mouse sobre un elemento, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Capturar captura de pantalla del nodo**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de pantalla de nodo resaltada en el menú contextual de la herramienta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Captura de pantalla de nodo** resaltada en el menú contextual de la **herramienta** Elementos  
:::image-end:::  

### <a name="elements-tool-updates"></a>Actualizaciones de herramientas de elementos  

#### <a name="support-forcing-the-target-css-state"></a>Compatibilidad con forzar el estado CSS :target  

Ahora puede usar DevTools para forzar la pseudo-clase CSS [:target.][MdnDocsWebCssTarget]  La pseudo-clase se desencadena cuando un elemento único \(el elemento de destino\) tiene un fragmento de `:target` `id` la dirección URL.  Por ejemplo, la `http://www.example.com/index.html#section1` dirección URL desencadena la pseudo class en un elemento HTML con `:target` `id="section1"` .  Para probar una demostración con la sección 1 resaltada, vaya a [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="La página web resaltada sin CSS forzada" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Página web resaltada sin CSS forzado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forzado y página web resaltado" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forzado y página web resaltado  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Usar elementos Duplicados para copiar elementos  

Use el nuevo **acceso directo del elemento Duplicate** para clonar un elemento.  En la **herramienta Elementos,** mantenga el mouse sobre un elemento, abra el menú contextual \(haga clic con el botón secundario\), elija **Elemento duplicado**.  Se crea un nuevo elemento en el elemento seleccionado.  Para duplicar el elemento con un método abreviado de teclado, seleccione `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) o `Shift` + `Option` + `Down Arrow` \(macOS\).  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="El elemento Duplicate se resalta en el menú contextual de un elemento de la herramienta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   El **elemento Duplicate** se resalta en el menú contextual de un elemento de la **herramienta** Elementos  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Selectores de colores para propiedades CSS personalizadas  

El **panel Estilos** ahora muestra selectores de colores para propiedades CSS personalizadas.  Para recorrer los formatos RGBA, HSLA y Hexadecimal del valor de color, mantenga presionado y `Shift` elija el selector de color.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1147016][CR1147016].  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Selectores de colores para propiedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Selectores de colores para propiedades CSS personalizadas  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a>Copiar clases y propiedades CSS  

Ahora puede copiar las propiedades CSS más rápido con algunas opciones nuevas en el menú contextual.  En la **herramienta Elementos,** elija un elemento.  Para copiar el valor, en el panel **Estilos,** mantenga el mouse en una clase CSS o una propiedad CSS, abra un menú contextual \(hacer clic con el botón secundario\) y elija la opción copiar.  

:::row:::
   :::column span="":::
      Copiar opciones para una clase CSS.  
      
      | Opción | Detalles |  
      |:--- |:--- |  
      | **Selector de copia** | Copie el nombre del selector actual. |  
      | **Regla de copia** | Copie la regla del selector actual. |  
      | **Copiar todas las declaraciones** | Copie todas las declaraciones en la regla actual, incluidas las propiedades no válidas y con prefijo. |  
   :::column-end:::
   :::column span="":::
      Copiar opciones para una propiedad CSS.  
      
      | Opción | Detalles |      
      |:--- |:--- |  
      | **Declaración de copia** | Copie la declaración de la línea actual. |  
      | **Copy (propiedad)** | Copie la propiedad de la línea actual. |  
      | **Valor de copia** | Copie el valor de la línea actual. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Copiar opciones para una clase CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Copiar opciones para una clase CSS en el menú contextual  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Opciones de copia de una propiedad CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Opciones de copia de una propiedad CSS en el menú contextual  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1152391][CR1152391].  

### <a name="cookies-updates"></a>Actualizaciones de cookies  

#### <a name="new-option-to-display-url-decoded-cookies"></a>Nueva opción para mostrar cookies descodificadas por URL  

Ahora puede optar por mostrar el valor de las cookies descodificadas por url en el **panel Cookies.**  Para mostrar la cookie descodificada, vaya al panel **** Cookies de aplicación, elija cualquier cookie de la lista y elija la casilla situada junto a Mostrar dirección URL  >  **** **descodificada.**  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opción para mostrar cookies descodificadas por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Opción para mostrar cookies descodificadas de dirección URL  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Filtrar y borrar las cookies visibles  

En Microsoft Edge versión 88 **** o anterior, la herramienta Aplicación solo proporcionaba una forma de borrar todas las cookies con **el botón Borrar todas las cookies.**  En Microsoft Edge versión 89, ahora puede elegir **Borrar cookies** filtradas para eliminar solo las cookies filtradas.  Para filtrar las cookies, vaya **a Cookies**  >  **de**aplicación y escriba el **cuadro de texto** Filtro.  Para eliminar las cookies mostradas, elija el **botón Borrar cookies filtradas.**  Para mostrar todas las demás cookies, desactive el texto del filtro.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Borrar solo las cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Borrar solo las cookies visibles  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Nueva opción para borrar cookies de terceros en el panel Almacenamiento  

DevTools ahora borra solo las cookies de origen de forma predeterminada.  Para borrar solo los datos del sitio web y las cookies de origen, vaya a **Almacenamiento**de aplicaciones y, a continuación,  >  **** elija Borrar datos **del sitio**.  

Para borrar los datos del sitio web y todas las cookies, vaya a **Almacenamiento de**  >  **aplicaciones**.  Elija la casilla junto a **incluir cookies de terceros**y, a continuación, elija Borrar datos del **sitio**.  

Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opción para borrar cookies de terceros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Opción para borrar cookies de terceros  
:::image-end:::  

### <a name="network-tool-updates"></a>Actualizaciones de herramientas de red  

#### <a name="persist-record-network-log-setting"></a>Configuración de registro de red de registro persistente  

En Microsoft Edge versión 88 o anterior, DevTools restablece la configuración registro de red **de** registro cuando se actualiza una página web.  En Microsoft Edge versión 89, DevTools ahora conserva la **configuración registro de red de** registro.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registro de registro de red" lightbox="../../media/2021/01/network-log.msft.png":::
   Registro de registro de red  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>La opción en línea ahora es Ninguna opción de limitación  

La opción de emulación de red **Online** ahora se cambia **a Sin limitación.**  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Sin opción de limitación" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Sin opción de limitación**  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Nuevas opciones de copia en la herramienta Consola, la herramienta Orígenes y el panel Estilos

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Copiar objeto en la herramienta Consola y orígenes  

Ahora puede copiar valores de objeto en las **herramientas Consola** **y** Orígenes.  La capacidad de copiar valores de objeto es útil al trabajar con objetos grandes.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [1148353][CR1148353] y [1149859][CR1149859].  

:::row:::
   :::column span="":::
      En la **herramienta Consola,** mantenga el mouse sobre un objeto, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, **elija Copiar objeto**.  
   :::column-end:::
   :::column span="":::
      En la **herramienta Orígenes,** en un punto de **** interrupción, mantenga el mouse sobre un objeto, en la ventana emergente Objeto, resalte un objeto, abra el menú contextual \(haga clic con el botón secundario en\) y, a continuación, elija **Copiar objeto**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copiar objeto en la consola" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Copiar objeto en la **consola**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copiar objeto en orígenes" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Copiar objeto en **orígenes**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Copiar nombre de archivo en el panel Estilos y herramienta Orígenes  

Ahora puede copiar un nombre de archivo mediante el menú contextual.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Problemas [1155120][CR1155120].  

:::row:::
   :::column span="":::
      En la **herramienta Orígenes,** mantenga el mouse sobre un nombre de archivo, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, **elija Copiar nombre de archivo**.  
   :::column-end:::
   :::column span="":::
      En el **panel** Estilos **** de > de la herramienta Elementos, mantenga el mouse sobre un nombre de **archivo,** abra el menú contextual \(clic con el botón derecho\) y, a continuación, elija Copiar nombre de archivo .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar nombre de archivo en Orígenes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copiar nombre de archivo en **Orígenes**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar nombre de archivo en el panel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copiar nombre de archivo en el **panel Estilos**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Actualizaciones de detalles del marco  

#### <a name="service-workers-information-in-frame-details"></a>Información de los trabajadores de servicio en Detalles del marco  

DevTools ahora enumera un trabajador de servicio dedicado en el marco primario.  En la siguiente figura, se muestran los detalles del trabajador de servicio.  Para mostrar los detalles del trabajador de servicio, vaya a **Application**  >  **Frames**  >  `top`  >  **Service Workers** y, a continuación, elija un trabajador de servicio.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Información de los trabajadores de servicio en los detalles marcos" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Información de los trabajadores** de servicio en los **detalles marcos**  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Medir información de memoria en detalles de marco  

El `performance.measureMemory()` estado de la API ahora se muestra en la sección disponibilidad de la **API.**  La nueva `performance.measureMemory()` API calcula el uso de memoria de toda la página web.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memoria" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Medir memoria  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Fotogramas eliminados en la herramienta Rendimiento  

Al analizar el rendimiento de carga **** en la [herramienta Rendimiento,][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]la sección Marcos marca ahora los fotogramas eliminados como rojos.  Para mostrar la velocidad de fotogramas, mantenga el mouse sobre un marco descartado.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Fotogramas descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Fotogramas descartados  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Nuevo cálculo de contraste de color: Algoritmo de contraste perceptual avanzado (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

El [Algoritmo de contraste perceptual avanzado (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] reemplaza la relación de contraste de directrices AAA de [AA][W3cWaiWcag21QuickrefContrastMinimum] / [][W3cWaiWcag21QuickrefContrastEnhanced] en el selector [de colores][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].  APCA es una nueva forma de calcular el contraste.  Se basa en investigaciones modernas sobre la percepción del color.  En comparación con las directrices de AA/AAA, APCA depende más del contexto.  El contraste se calcula en función de las siguientes propiedades espaciales del texto, color y contexto.  

*   Propiedades espaciales del texto que incluyen el grosor y el tamaño de fuente.  
*   Propiedades espaciales de color que incluyen contraste percibido entre texto y fondo.  
*   Propiedades espaciales del contexto que incluyen luz ambiental, entorno y propósito previsto.  
    
Para activar este experimento, [][DevtoolsCustomizeIndexSettings]vaya a Settings Experiments y seleccione la casilla situada junto a  >  **** Enable new **Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA en el selector de colores" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA en el selector de colores  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si estás en Windows, Linux o macOS, considera usar los canales de vista previa [de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Ver la relación de contraste de un elemento de texto en el selector de colores: referencia de accesibilidad | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Cambiar CSS: referencia CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalización de métodos abreviados de teclado en las herramientas de desarrollo de Microsoft Edge | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de doble pantalla y plegables: emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular una ventanilla móvil: emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Rendimiento de carga de registro: referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Editar estilos y configuraciones de fuentes CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Introducción a Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la costura: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de pantalla de medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Sección 1: demostración CSS :target para Novedades de DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementing dropdown in settings to change themes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Including Debugger for Microsoft Edge as a dependency | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Upgrading Edge DevTools version to 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Extracción 248: Agregar botones de cierre único al panel de instancias | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Seleccione características de fuente y colores de fondo para proporcionar suficiente contraste para la legibilidad | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos de confianza | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nueva versión de Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Extension Marketplace | Visual Studio código"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio código | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR978059]: https://crbug.com/978059 "Problema 978059: Eliminar las cookies al filtrarlas, eliminar todas las cookies no solo las filtradas | Errores de Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: Nueva característica | Opción De necesidad para ver el valor codificado en url en las cookies | Errores de Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problema 1003629: Capture Node ya no captura de pantalla el nodo debajo del plegado. | Errores de Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problema 1012337: Borrar datos del sitio destruye la sesión de Google en sitios que no son de Google | Errores de Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problema 1028078: Poner en línea y sin conexión entre sí en la lista | Errores de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: Solicitud de característica: DevTools debe emular dispositivos de pantalla doble y plegables | Errores de Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: Mostrar fotogramas eliminados en la escala de tiempo de las devtools | Errores de Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: ofrecer una interfaz de usuario de editor de tipografía especializada | Errores de Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: actualizar la lógica de cálculo de contraste por nueva especificación | Errores de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: información de los trabajos superficiales en la vista de árbol de marcos | Errores de Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problema 1122580: Imposible deshabilitar la grabación de red al volver a cargar | Errores de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: herramientas de la caja flexible | Errores de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: informar la disponibilidad de la API validada en la vista detalles del marco | Errores de Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: Superposición de Flexbox | Errores de Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problema 1147016: el selector de colores no se muestra en la función var(). | Errores de Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: Solicitud de característica: Copiar objeto desde la consola de devtools | Errores de Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitud de característica][Consola] agregar el objeto copy al elemento del portapapeles al menú contextual | Errores de Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problema 1150797: Agregar menú contextual Elemento duplicado en el panel Elemento | Errores de Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problema 1152391: Compatibilidad con copiar el menú contextual CSS en el panel de estilos | Errores de Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Support copy file name and line number | Errores de Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: agregar compatibilidad con la característica de estado de elemento :target in force | Errores de Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Accesibilidad - Narrador: El narrador no anuncia el recuento y la posición de las sugerencias disponibles para el código en la pestaña Estilos | Errores de Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (mejorado): cómo cumplir wcag (referencia rápida) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo): cómo cumplir wcag (referencia rápida) | W3C"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2021/01/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Marcador de posición de expansión"  
