---
description: La herramienta Novedades ahora es Bienvenida, Editor de fuentes visuales en el panel Estilos, herramientas de depuración de CSS Flexbox y más.
title: Novedades de DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.localizationpriority: high
ms.openlocfilehash: 6d1952832c84dc159222a8aa16aa0ffe11edff34
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564933"
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

## <a name="whats-new-is-now-welcome"></a>Novedades ahora es Bienvenida  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

La herramienta **Novedades** en DevTools de Microsoft Edge ahora tiene una nueva apariencia y un nuevo nombre: **Bienvenida**.  La herramienta **Bienvenida** sigue mostrando las últimas noticias y actualizaciones de DevTools.  Ahora también incluye vínculos a la documentación de Microsoft Edge DevTools, otras formas de enviar sus comentarios y mucho más.  Para mostrar la herramienta **Bienvenida** después de cada actualización Microsoft Edge, active la casilla junto a **Abrir pestaña después de cada actualización**, debajo del título.  Para cerrar la herramienta **Bienvenida**, seleccione la **X** en la parte derecha de la pestaña de título.  Si prefiere la herramienta original **Novedades**, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y desactive la casilla junto a **Habilitar pestaña de Bienvenida**.  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="La herramienta Bienvenida está resaltada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   La herramienta **Bienvenida** está resaltada  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Editor de fuentes visuales en el panel Estilos  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Cuando trabaje con fuentes en CSS, use el nuevo [Editor de fuentes visuales][DevtoolsInspectStylesEditFonts].  Puede definir las fuentes de reserva y usar los controles deslizantes para definir el grosor, el tamaño, el alto de la línea y el espaciado de la fuente.  El **Editor de fuentes** le ayuda a completar las siguientes acciones.  

*   Cambiar entre unidades para las diferentes propiedades de la fuente  
*   Cambiar entre palabras clave para las diferentes propiedades de la fuente  
*   Convertir unidades  
*   Generar código CSS preciso  
    
Para activar este experimento, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y active la casilla junto a **Habilitar las herramientas del nuevo Editor de fuentes en el panel Estilos**.  Para obtener más información, vaya a [Editar la configuración y los estilos de fuente CSS en el panel Estilos, en DevTools][DevtoolsInspectStylesEditFonts].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="El Editor de fuentes visual está resaltado en el panel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   El **Editor de fuentes** visual está resaltado en el panel **Estilos**  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>Herramientas de depuración de CSS Flexbox  

Las características de depuración de Flexbox están en desarrollo activo.  Para activar el experimento de las dos características siguientes, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y active la casilla junto a **Habilitar las nuevas características de depuración de CSS Flexbox**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a los problemas [1136394][CR1136394] y [1139949][CR1139949].  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>El nuevo icono de Flexbox (flex) le ayuda a identificar y a visualizar los contenedores flexibles.  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

En la herramienta **Elementos**, el nuevo icono de Flexbox (flex) le ayuda a identificar los contenedores de Flexbox en el código.  Seleccione el icono de Flexbox \(flex\) para activar o desactivar el efecto de superposición que resalta al contenedor de Flexbox.  Puede personalizar el color de la superposición en el panel **Diseño**, que se encuentra junto a **Estilos** y **Calculado**.  

:::row:::
   :::column span="":::
      Para activar y desactivar el efecto de superposición que resalta al contenedor de Flexbox, seleccione el icono de Flexbox \(`flex`\).  
   :::column-end:::
   :::column span="":::
      Puede personalizar el color de la superposición en el panel **Diseño**, junto a **Estilos** y **Calculado**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Icono de Flexbox (flex) y página web resaltados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         Icono de **Flexbox** \(`flex`\) y página web resaltados :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Flexbox se superpone cuando se resalta en el panel Diseño" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         Las **superposiciones de Flexbox** se resaltan en el panel de **Diseño**.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-visual-guides-when-flexbox-layouts-change-using-css-properties"></a>Mostrar los iconos de alineación y las guías visuales cuando los diseños de Flexbox cambien mediante propiedades CSS  

<!--  Title: Display alignment icons and visual guides for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Cuando edita CSS para su diseño de Flexbox, CSS se autocompleta en el panel **Estilos** y muestra iconos útiles junto a las propiedades relevantes de Flexbox.  Para probar esta nueva característica, abra la herramienta **Elementos** y seleccione un contenedor flexible.  Luego, agregue o cambie alguna propiedad en ese contenedor en el panel **Estilos**.  

:::row:::
   :::column span="":::
      En el menú Autocompletar ahora se muestran iconos que indican el efecto de las propiedades de alineación, como `align-content` y `align-items`.  
   :::column-end:::
   :::column span="":::
      Además, DevTools ahora muestra una línea de guía para ayudarle a revisar mejor la propiedad CSS `align-items`.  La propiedad CSS `gap` también es compatible.  En la siguiente ilustración, la propiedad CSS `gap` está establecida en `gap: 12px;` y se muestra el patrón de sombreado para cada separación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menú Autocompletar resaltado para las propiedades CSS que comienzan con alinear" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menú Autocompletar resaltado para las propiedades CSS que comienzan con `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Separación de Flexbox en las propiedades CSS y página web resaltadas" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` en las propiedades CSS y página web resaltados  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Agregar herramientas rápidamente con el nuevo botón Más herramientas  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Ahora tiene una nueva forma de abrir más herramientas en Microsoft Edge DevTools.  Después de activar este experimento, el icono **Más herramientas** se muestra como un signo más (`+`) a la derecha del panel principal.  Para mostrar una lista de otras herramientas para agregar al panel principal, seleccione el icono **Más herramientas** \(`+`\).  Para activar este experimento, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y luego, active la casilla junto a **Habilitar menús de la pestaña del botón + para abrir más herramientas**.  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Más herramientas resaltadas en DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Más herramientas** resaltadas de DevTools  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Las tecnologías de asistencia ahora anuncian la posición y el recuento de sugerencias de CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Al editar CSS, obtendrá una lista desplegable de características.  Esta característica no estaba disponible para los usuarios de tecnologías de asistencia, ya que se anuncia en la versión 89 de Microsoft Edge.  El usuario de tecnologías de asistencia ahora puede navegar por las sugerencias de CSS en el panel **Estilos**.  En la versión 88 de Microsoft Edge y en las versiones anteriores, la tecnología de asistencia anuncia `Suggestion` como un usuario que navega por la lista de sugerencias al editar CSS en el panel **Estilos**.  En la versión 89 de Microsoft Edge, el usuario de tecnologías de asistencia ahora escuchará la posición y el recuento de la sugerencia actual.  Cada sugerencia se anuncia a medida que el usuario navega por la lista de sugerencias, como Sugerencia 3 de 5.  Para obtener más información sobre cómo escribir CSS en DevTools, vaya a [Cambiar CSS][DevtoolsCssReferenceChangeCss].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1157329][CR1157329].  

Para ver un vídeo que muestra y lee en voz alta varias sugerencias con este experimento activado, vaya a [Opciones de devtools anunciadas por VoiceOver](https://youtu.be/9TcUpleEwwA) en YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Sugerencia resaltada en el panel Estilos" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   Lista `suggestion` resaltada en el panel **Estilos**.  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emular Surface Duo y Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Pruebe la apariencia de su sitio web o aplicación en los siguientes dispositivos en Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Active las **Características experimentales de la plataforma web** para acceder a la nueva [Característica para expandir la pantalla de los medios CSS][DualScreenWebCssMediaSpanning] y a la [API de JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  Vaya a `edge://flags` y cambie la marca junto a las **Características de la plataforma web experimental**.  Para ayudar a mejorar su sitio web o aplicación para dispositivos plegables y de pantalla doble, use las siguientes características al [emular el dispositivo][DevtoolsDeviceModeIndex].  

*   [Expandir][DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices], que es cuando su sitio web \(o aplicación\) se extiende por las dos pantallas.  
*   [Representación de la unión][DualScreenIntroductionHowToWorkWithSeam], que es el espacio entre las dos pantallas.  
    
Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular la pantalla doble" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emular la pantalla doble  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>Herramientas para desarrollador de Microsoft Edge para Visual Studio Code versión 1.1.2  

La versión de extensión 1.1.2 de las [Herramientas de desarrollador de Microsoft Edge para Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] para Microsoft Visual Studio Code tiene los siguientes cambios desde la versión anterior.  Microsoft Visual Studio Code actualiza las extensiones automáticamente.  Para actualizar manualmente a la versión 1.1.2, vaya a [Actualizar extensión manualmente][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].  

*   Se agregó un botón de **Instancia de cierre** a cada elemento de la lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Cambio de [Microsoft Edge DevTools][DevtoolsIndex] de la versión 84.0.522.63 a la [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Se incluye el [Depurador para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como dependencia \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Se implementó la opción de configuración para cambiar los temas de la extensión \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Puede archivar los problemas y contribuir con la extensión en el [repositorio de GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Capturar nodo como captura de pantalla más allá de la ventanilla  

En la versión 89 de Microsoft Edge, la captura de nodos como captura de pantalla es más precisa, capturando el nodo completo incluso si su contenido no es visible en la ventanilla.  En la herramienta **Elementos**, mantenga el puntero sobre un elemento, abra el menú contextual \(clic con el botón derecho\) y seleccione **Capturar nodo como captura de pantalla**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de nodo como captura de pantalla resaltado en el menú contextual de la herramienta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Captura de nodo como captura de pantalla** resaltado en el menú contextual en la herramienta **Elementos**  
:::image-end:::  

### <a name="elements-tool-updates"></a>Actualizaciones de la herramienta Elementos  

#### <a name="support-forcing-the-target-css-state"></a>Compatibilidad para forzar el estado CSS :target  

Ahora puede usar DevTools para forzar la seudoclase CSS [:target][MdnDocsWebCssTarget].  La seudoclase `:target` se desencadena cuando un elemento único \(el elemento de destino\) tiene un `id` que coincide con un fragmento de la dirección URL.  Por ejemplo, la dirección URL `http://www.example.com/index.html#section1` activa la seudoclase `:target` en un elemento HTML con `id="section1"`.  Para probar una demostración con la sección 1 resaltada, vaya a [demostración de CSS :target][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Página web resaltada sin forzar CSS" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Página web resaltada sin forzar CSS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text="CSS :target forzado y página web resaltados" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forzado y página web resaltada  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Usar Duplicar elementos para copiar elementos  

Use el nuevo acceso directo **Duplicar elemento** para clonar un elemento.  En la herramienta **Elementos**, mantenga el puntero sobre un elemento, abra el menú contextual \(clic con el botón derecho\) y elija **Duplicar elemento**.  Se creará un nuevo elemento en el elemento seleccionado.  Para duplicar el elemento con un método abreviado de teclado, seleccione `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) o `Shift`+`Option`+`Down Arrow` \(macOS\).  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Duplicar elemento se resalta en el menú contextual de un elemento de la herramienta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   **Duplicar elemento** se resalta en el menú contextual en un elemento de la herramienta **Elementos**  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Selector de colores para las propiedades CSS personalizadas  

El panel **Estilos** ahora muestra selectores de color para las propiedades CSS personalizadas.  Para cambiar entre los formatos RGBA, HSLA y Hex del valor de color, mantenga presionado `Shift` y elija el Selector de colores.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1147016][CR1147016].  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Selector de colores para las propiedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Selector de colores para las propiedades CSS personalizadas  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a>Copiar las clases y propiedades CSS  

Ahora puede copiar las propiedades CSS más rápidamente con algunas opciones nuevas en el menú contextual.  En la herramienta **Elementos**, elija un elemento.  Para copiar el valor, en el panel **Estilos**, mantenga el puntero sobre una clase o propiedad CSS, abra un menú contextual \(clic con el botón derecho\) y elija la opción de copiar.  

:::row:::
   :::column span="":::
      Opciones de copia para una clase CSS.  
      
      | Opción | Detalles |  
      |:--- |:--- |  
      | **Selector de copia** | Copiar el nombre del selector actual. |  
      | **Copiar regla** | Copiar la regla del selector actual. |  
      | **Copiar todas las declaraciones** | Copiar todas las declaraciones en la regla actual, incluidas las propiedades no válidas y con prefijo. |  
   :::column-end:::
   :::column span="":::
      Opciones de copia para una propiedad CSS.  
      
      | Opción | Detalles |      
      |:--- |:--- |  
      | **Copiar declaración** | Copia la declaración de la línea actual. |  
      | **Copiar propiedad** | Copia la propiedad de la línea actual. |  
      | **Copiar valor** | Copiar el valor de la línea actual. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Opciones de copia para una clase CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Opciones de copia para una clase CSS en el menú contextual  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Opciones de copia para una propiedad CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Opciones de copia para una propiedad CSS en el menú contextual  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1152391][CR1152391].  

### <a name="cookies-updates"></a>Actualizaciones de cookies  

#### <a name="new-option-to-display-url-decoded-cookies"></a>Nueva opción para mostrar cookies descodificadas por URL  

Ahora puede optar por mostrar el valor de las cookies descodificadas por URL en el panel **Cookies**.  Para mostrar la cookie descodificada, vaya al panel **Aplicación** > **Cookies**, elija cualquier cookie de la lista y active la casilla junto a **Mostrar dirección URL descodificada**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opción para mostrar cookies descodificadas por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Opción para mostrar cookies descodificadas por URL  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Filtrar y borrar las cookies visibles  

En la versión 88 de Microsoft Edge o anteriores, la herramienta **Aplicación** solo proporciona una manera de borrar todas las cookies con el botón **Borrar todas las cookies**.  En la versión 89 de Microsoft Edge, ahora puede elegir **Borrar las cookies filtradas** para eliminar solo las cookies filtradas.  Para filtrar las cookies, vaya a **Aplicación** > **Cookies** y escriba en el cuadro de texto de **Filtrar**.  Para eliminar las cookies mostradas, seleccione el botón **Borrar cookies filtradas**.  Para mostrar las demás cookies, borre el texto del filtro.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Borrar solo las cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Borrar solo las cookies visibles  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Nueva opción para borrar cookies de terceros en el panel de Almacenamiento  

Ahora, DevTools solo borrará las cookies de origen de manera predeterminada.  Para borrar solo los datos del sitio web y las cookies de origen, vaya a **Aplicación** > **Almacenamiento**y luego, seleccione **Borrar los datos del sitio**.  

Para borrar los datos del sitio web y todas las cookies, vaya a **Aplicación** > **Almacenamiento**.  Active la casilla junto a **incluso las cookies de terceros** y luego, **Borrar datos del sitio**.  

Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opción para borrar las cookies de terceros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Opción para borrar las cookies de terceros  
:::image-end:::  

### <a name="network-tool-updates"></a>Actualizaciones de las herramientas de red  

#### <a name="persist-record-network-log-setting"></a>Configuración de registro de red de registro persistente  

En la versión 88 de Microsoft Edge o versiones anteriores, DevTools restablece la configuración **Registro de red de registro** cuando se actualiza una página web.  En la versión 89 de Microsoft Edge, DevTools conserva la configuración de **Registro de red de registro**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registro de red de registro" lightbox="../../media/2021/01/network-log.msft.png":::
   Registro de red de registro  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>La opción En línea ahora es la opción Sin limitación  

La opción de emulación de red **En línea** ahora se denomina **Sin limitación**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Opción Sin limitación" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   Opción **Sin limitación**  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Hay nuevas opciones de copiado en la herramienta Consola, la herramienta Orígenes y el panel Estilos

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Copiar objeto en las herramientas Consola y Orígenes  

Ahora puede copiar los valores del objeto en las herramientas **Consola** y **Orígenes**.  La capacidad de copiar los valores del objeto es útil cuando se trabaja con objetos grandes.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1148353][CR1148353] y [1149859][CR1149859].  

:::row:::
   :::column span="":::
      En la herramienta **Consola**, mantenga el puntero sobre un objeto, abra el menú contextual \(clic con el botón derecho\) y luego, seleccione **Copiar objeto**.  
   :::column-end:::
   :::column span="":::
      En la herramienta **Orígenes**, en un punto de interrupción, mantenga el puntero sobre un objeto y, en la ventana emergente del **Objeto**, resalte un objeto, abra el menú contextual \(clic con el botón derecho\) y luego, seleccione **Copiar objeto**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copiar objeto en la Consola" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Copiar objeto en la **Consola**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copiar un objeto en Orígenes" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Copiar objeto en **Orígenes**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Copiar el nombre de archivo en la herramienta Orígenes y en el panel Estilos  

Ahora puede copiar un nombre de archivo mediante el menú contextual.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1155120][CR1155120].  

:::row:::
   :::column span="":::
      En la herramienta **Orígenes**, mantenga el puntero sobre un nombre de archivo, abra el menú contextual \(clic con el botón derecho\) y después, seleccione **Copiar nombre de archivo**.  
   :::column-end:::
   :::column span="":::
      En la herramienta **Elementos** > panel **Estilos**, mantenga el puntero sobre un nombre de archivo, abra el menú contextual \(clic con el botón derecho\) y luego, seleccione **Copiar nombre del archivo**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar el nombre de archivo en Orígenes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copiar el nombre de archivo en **Orígenes**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar el nombre de archivo en el panel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copiar el nombre de archivo en el panel **Estilos**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Actualizaciones para Detalles del marco  

#### <a name="service-workers-information-in-frame-details"></a>Información de los trabajos de servicio en Detalles del marco  

DevTools ahora muestra un trabajo de servicio dedicado en el marco principal.  En la siguiente ilustración, se muestran los detalles del trabajo de servicio.  Para mostrar los detalles del trabajo de servicio, vaya a **Aplicación** > **Marcos** > `top` > **Trabajos de servicio** y después, seleccione un trabajo de servicio.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Información de los Trabajos de servicio en Detalles del marco" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   Información de los **Trabajos de servicio** en **Detalles del marco**  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Medir información de la memoria en Detalles del marco  

El estatus de la API `performance.measureMemory()` ahora se muestra en la sección **Disponibilidad de la API**.  La nueva API `performance.measureMemory()` calcula el uso de memoria de toda la página web.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memoria" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Medir memoria  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Fotogramas descartados en la herramienta Rendimiento  

Al [analizar el rendimiento de carga en la herramienta Rendimiento][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], la sección **Marcos** ahora marca los fotogramas eliminados en rojo.  Para mostrar la velocidad de fotogramas, mantenga el puntero sobre algún fotograma descartado.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Fotogramas descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Fotogramas descartados  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Nuevo cálculo de contraste de color: Algoritmo de contraste perceptual avanzado (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

El [Algoritmo de contraste perceptual avanzado (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] reemplaza la relación de contraste de las directrices [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] en el [Selector de colores][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].  APCA es la nueva forma de calcular el contraste.  Se basa en las investigaciones modernas sobre la percepción del color.  En comparación con las directrices AA/AAA, APCA depende más del contexto.  El contraste se calcula de acuerdo con las siguientes propiedades espaciales de texto, color y contexto.  

*   Propiedades espaciales del texto que incluyen el grosor y el tamaño de la fuente.  
*   Propiedades espaciales de color que incluyen contraste percibido entre el texto y el fondo.  
*   Propiedades espaciales del contexto que incluyen luz ambiental, alrededores y un propósito previsto.  
    
Para activar este experimento, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y active la casilla junto a **Habilitar el nuevo Algoritmo de contraste perceptual avanzado (APCA) para reemplazar la relación de contraste y las directrices AA/AAA anteriores**.  Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA en el Selector de colores" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA en el Selector de colores  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de versión preliminar de Microsoft Edge  

Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: ../../../accessibility/reference.md#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Ver la relación de contraste de un elemento de texto en el Selector de colores: Referencia de accesibilidad | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: ../../../css/reference.md#change-css "Cambiar CSS: Referencias CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configuración: Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalización de accesos rápidos de teclado en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices]: ../../../device-mode/dual-screen-and-foldables.md#test-on-foldable-and-dual-screen-devices "Prueba en dispositivos plegables y de doble pantalla: emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular una ventanilla móvil: Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: ../../../evaluate-performance/reference.md#record-load-performance "Registrar el rendimiento de carga: referencia del análisis de rendimiento | Microsoft Docs"  
[DevtoolsIndex]: ../../../index.md "Introducción a Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: ../../../inspect-styles/edit-fonts.md "Editar la configuración y los estilos de fuente CSS en el panel Estilos en DevTools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la unión: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de pantalla expandida para medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API de JavaScript de getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Sección 1: Demostración CSS :target para las Novedades en DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementar la lista desplegable en la configuración para cambiar los temas | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Incluir depurador para Microsoft Edge como dependencia | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Actualización de Edge DevTools a la versión 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Agregar botones de cierre único a las instancias del panel | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Seleccionar las características de la fuente y los colores de fondo para proporcionar suficiente contraste para facilitar la lectura | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos de confianza | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nuevo Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de versiones preliminares de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR978059]: https://crbug.com/978059 "Problema 978059: Eliminar las cookies al filtrarlas, eliminar todas las cookies y no solo las filtradas | Errores de Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: Solicitud de característica nueva | Se necesita la opción para ver el valor descodificado por URL en las cookies | Errores de Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problema 1003629: El nodo de captura ya no hace la captura de pantalla del nodo que está debajo del pliegue | Errores de Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problema 1012337: Borrar los datos del sitio destruye la sesión de Google en los sitios que no son de Google | Errores de Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problema 1028078: Poner los estados En línea y Sin conexión contiguamente en la lista | Errores de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: Solicitud de características: DevTools debe emular dispositivos plegables y de pantalla doble | Errores de Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: Mostrar fotogramas descartados en la línea de tiempo de devtools | Errores de Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: ofrecer un editor de tipo de letra especializado en la interfaz de usuario | Errores de Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: actualizar la lógica de cálculo de contraste por especificación | Errores de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: Información de los trabajos de Surface en la vista de árbol de marcos | Errores de Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problema 1122580: Imposible deshabilitar la grabación de red al volver a cargar | Errores de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: Herramientas de Flexbox | Errores de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: Informar la disponibilidad de la API validada en la vista de detalles del marco | Errores de Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: Superposición de Flexbox | Errores de Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problema 1147016: El Selector de colores no se muestra en la función var() | Errores de Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: Solicitud de característica: Copiar objeto desde la consola de devtools | Errores de Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitud de característica][Consola] agregar un objeto de copia al elemento del Portapapeles en el menú contextual | Errores de Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problema 1150797: Agregar el menú contextual del Elemento duplicado en el panel Elemento | Errores de Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problema 1152391: Compatibilidad para copiar el menú contextual CSS en el panel de Estilos | Errores de Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Compatibilidad para copiar el nombre de archivo y el número de línea | Errores de Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: agregar compatibilidad con :target en la característica de estado de forzar elemento | Errores de Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Accesibilidad - Narrador: El narrador no anuncia el recuento y la posición de las sugerencias disponibles para el código en la pestaña Estilos | Errores de Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung Estados Unidos"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (mejorado): Cómo cumplir los requisitos WCAG (referencia rápida) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo): Cómo cumplir los requisitos WCAG (referencia rápida) | W3C"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-89) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de una [Licencia internacional de Atribución de Creative Commons 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen

[SpanningPlaceholder]: link-t-b-d "Expandir el marcador de posición"  
