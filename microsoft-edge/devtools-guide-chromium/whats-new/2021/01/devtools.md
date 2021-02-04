---
description: La herramienta Novedades ahora es Welcome, Visual Font Editor en el panel Estilos, herramientas de depuración css Flexbox y mucho más.
title: Novedades de DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: cfaee927d2d914cf0d816505ea2cf6b36a225d64
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313350"
---
# Novedades de DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## What's New is now Welcome  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

La **herramienta Novedades de** Microsoft Edge DevTools ahora tiene una nueva apariencia y un nuevo nombre: **Bienvenido.**  La **herramienta de** bienvenida aún muestra las últimas noticias y actualizaciones de DevTools.  Ahora también incluye vínculos a la documentación de Microsoft Edge DevTools, formas de enviar comentarios y mucho más.  Para mostrar la **herramienta de** bienvenida después de cada actualización a Microsoft Edge, seleccione la casilla situada junto a la pestaña Abrir después de cada **actualización** bajo el título.  Para cerrar la **herramienta de** bienvenida, elija la **X** en el lado derecho del título de la pestaña.  Si prefieres la **herramienta** Novedades original, ve a Experimentos de configuración y quita la casilla junto a [][DevtoolsCustomizeIndexSettings]  >  **** Habilitar **pestaña de bienvenida.**  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="La herramienta de bienvenida está resaltada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   La **herramienta de** bienvenida está resaltada  
:::image-end:::  

## Editor de fuentes visuales en el panel Estilos  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Cuando trabaje con fuentes en CSS, use el nuevo Editor de [fuentes visual.][DevtoolsInspectStylesEditFonts]  Puedes definir fuentes de reserva y usar controles deslizantes para definir el grosor, el tamaño, el alto de línea y el espaciado de la fuente.  El **Editor de** fuentes le ayuda a completar las siguientes acciones.  

*   Cambiar entre unidades para distintas propiedades de fuente  
*   Cambiar entre palabras clave para distintas propiedades de fuente  
*   Convertir unidades  
*   Generar código CSS preciso  
    
Para activar este experimento, [][DevtoolsCustomizeIndexSettings]ve a Experimentos de configuración y elige la casilla junto a Habilitar nuevas herramientas del Editor de fuentes  >  **** en el **panel Estilos.**  Para obtener más información, vaya a Editar estilos y configuraciones de fuente CSS en [el panel Estilos de DevTools][DevtoolsInspectStylesEditFonts].  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="El editor de fuentes visuales se resalta en el panel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   El editor **de fuentes visuales** se resalta en el panel **Estilos**  
:::image-end:::  

## Herramientas de depuración de CSS Flexbox  

Las características de depuración de Flexbox están en desarrollo activo.  Para activar el experimento para las dos [][DevtoolsCustomizeIndexSettings]características siguientes, ve a Experimentos de configuración y elige la casilla junto a Habilitar nuevas características  >  **** **de depuración de CSS Flexbox**.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya a Problemas [1136394][CR1136394] y [1139949][CR1139949].  

### El nuevo icono de Flexbox (flex) ayuda a identificar y mostrar contenedores flex  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

En la **herramienta Elementos,** el nuevo icono de Flexbox (flex) te ayuda a identificar contenedores de Flexbox en el código.  Elige el icono de Flexbox \(flex\) para activar o desactivar el efecto de superposición que describe un contenedor de Flexbox.  Puede personalizar el color de la superposición en **el** panel Diseño, que se encuentra junto **a Estilos** y **Calculado.**  

:::row:::
   :::column span="":::
      Para activar y desactivar el efecto de superposición que describe el contenedor de Flexbox, elija el icono Flexbox \( `flex` \).  
   :::column-end:::
   :::column span="":::
      Puede personalizar el color de la superposición en el panel **Diseño** junto **a Estilos** y **Calculado.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="El icono de Flexbox (flex) y la página web resaltados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         El **icono de Flexbox** \( `flex` \) y la página web resaltados :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Las superposiciones de Flexbox resaltadas en el panel Diseño" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         Las **superposiciones de Flexbox resaltadas** en el **panel Diseño**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Mostrar iconos de alineación y líneas de cuadrícula cuando los diseños de Flexbox cambian mediante propiedades CSS  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Al editar CSS para el diseño de Flexbox, CSS se autocompleta en el panel Estilos ahora muestra iconos útiles junto a las propiedades pertinentes de Flexbox. ****  Para probar esta nueva característica, abra la herramienta **Elementos** y seleccione un contenedor flexible.  A continuación, agregue o cambie una propiedad en ese contenedor en el **panel Estilos.**  

:::row:::
   :::column span="":::
      El menú Autocompletar ahora muestra iconos que indican el efecto de propiedades de alineación como `align-content` y `align-items` .  
   :::column-end:::
   :::column span="":::
      Además, DevTools ahora muestra una línea de guidación para ayudarte a revisar mejor la `align-items` propiedad CSS.  También `gap` se admite la propiedad CSS.  En la figura siguiente, la propiedad CSS se establece en y se muestra el patrón de trama `gap` `gap: 12px;` de cada intervalo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menú Autocompletar resaltado para las propiedades CSS que comienzan con align-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menú Autocompletar resaltado para las propiedades CSS que empiezan por `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Diferencia de Flexbox en propiedades CSS y página web resaltada" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` en propiedades CSS y página web resaltadas  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Agregar herramientas rápidamente con el nuevo botón Más herramientas  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Ahora tienes una nueva forma de abrir más herramientas en Microsoft Edge DevTools.  Después de activar este **** experimento, el icono Más herramientas se muestra como un signo más ( ) a la derecha `+` del panel principal.  Para mostrar una lista de otras herramientas para agregar al panel principal, elija el icono **Más** herramientas \( `+` \).  Para activar este experimento, [][DevtoolsCustomizeIndexSettings]ve a Experimentos de configuración y, a continuación, selecciona la casilla junto a Habilitar + menús de pestaña de botón  >  **** para abrir **más herramientas.**  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Más herramientas resaltadas en DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Más herramientas** resaltadas en DevTools  
:::image-end:::  

## Las tecnologías de asistencia ahora anuncian la posición y el recuento de sugerencias css  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Cuando edita CSS, obtiene un desplegable de características.  Esta característica no estaba disponible para los usuarios de tecnologías de asistencia, ya que se anuncia en la versión 89 de Microsoft Edge.  Un usuario de tecnologías de asistencia ahora puede navegar por sugerencias css en el **panel** Estilos.  En La versión 88 de Microsoft Edge y versiones anteriores, la tecnología de asistencia anunciada como un usuario navegaba por la lista de sugerencias al editar CSS en el panel `Suggestion` Estilos. ****  En la versión 89 de Microsoft Edge, un usuario de tecnología de asistencia ahora escucha la posición y el recuento de la sugerencia actual.  Cada sugerencia se anuncia a medida que el usuario navega por la lista de sugerencias, como sugerencia 3 de 5.  Para obtener más información sobre cómo escribir CSS en DevTools, vaya [a Cambiar CSS.][DevtoolsCssReferenceChangeCss]  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1157329][CR1157329].  

<!--To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.  -->  

El siguiente vínculo de vídeo muestra y lee en voz alta varias sugerencias con este experimento activado.  

> [!VIDEO https://youtu.be/9TcUpleEwwA]  

## Emular Surface Duo y El plegado Desaplicación de Samsung  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Prueba la apariencia de tu sitio web o aplicación en los siguientes dispositivos de Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Redoblón Desdeso][SamsungUsMobileGalaxyFold]  
    
Active las **características de la plataforma web experimental** para obtener acceso a la nueva característica de pantalla multimedia [CSS][DualScreenWebCssMediaSpanning] y obtener la API de JavaScript de [WindowsSegments.][DualScreenWebJavascriptGetwindowsegments]  Navegue hasta `edge://flags` y cambie la marca junto a las características de la plataforma web **experimental.**  Para ayudar a mejorar tu sitio web o aplicación para la pantalla doble y los dispositivos plegados, usa las siguientes características [al emular el dispositivo.][DevtoolsDeviceModeIndex]  

*   [Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], que es cuando el sitio web \(o app\) aparece en ambas pantallas.  
*   [Representación de la mosca][DualScreenIntroductionHowToWorkWithSeam], que es el espacio entre las dos pantallas.  
    
Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular la pantalla doble" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emular la pantalla doble  
:::image-end:::  

## Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2  

Microsoft [Edge Developer Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.  Microsoft Visual Studio Code actualiza las extensiones automáticamente.  Para actualizar manualmente a la versión 1.1.2, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Se agregó **un botón Cerrar instancia** a cada elemento de la lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Versión mejorada de [Microsoft Edge DevTools][DevtoolsMain] de 84.0.522.63 a [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Depurador [incluido para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como dependencia \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Opción de configuración implementada para cambiar los temas de extensión \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].  

## Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Captura de pantalla de nodo más allá de la ventanilla  

En La versión 89 de Microsoft Edge, las capturas de pantalla de nodo son más precisas, capturando el nodo completo incluso si el contenido del nodo no está visible en la ventanilla.  En la **herramienta Elementos,** mantenga el mouse sobre un elemento, abra el menú contextual \(haga clic con el botón secundario\) y elija **Captura de pantalla del nodo**.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de pantalla de nodo resaltada en el menú contextual de la herramienta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Captura de pantalla de nodo** resaltada en el menú contextual de la **herramienta** Elementos  
:::image-end:::  

### Actualizaciones de herramientas de elementos  

#### Compatibilidad con la fuerza del estado CSS :target  

Ahora puedes usar DevTools para forzar la pseudo-clase CSS [:target.][MdnDocsWebCssTarget]  La pseudo class se desencadena cuando un elemento único \(el elemento de destino\) tiene un fragmento de `:target` `id` la dirección URL.  Por ejemplo, la `http://www.example.com/index.html#section1` dirección URL desencadena la pseudo class en un elemento HTML con `:target` `id="section1"` .  Para probar una demostración con la sección 1 resaltada, vaya a [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Página web resaltada sin CSS forzada" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Página web resaltada sin CSS forzada  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forzado y página web resaltada" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forzada y página web resaltada  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Usar elementos duplicados para copiar elementos  

Usa el nuevo **acceso directo de elemento duplicado** para clonar un elemento.  En la **herramienta Elementos,** mantenga el mouse sobre un elemento, abra el menú contextual \(haga clic con el botón secundario\), elija **Duplicar elemento**.  Se crea un nuevo elemento en el elemento seleccionado.  Para duplicar el elemento con un método abreviado de teclado, selecciona `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) o `Shift` + `Option` + `Down Arrow` \(macOS\).  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="El elemento Duplicado se resalta en el menú contextual de un elemento de la herramienta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   El **elemento Duplicado** se resalta en el menú contextual de un elemento de la **herramienta** Elementos  
:::image-end:::  

#### Selectores de colores para propiedades CSS personalizadas  

El **panel Estilos** ahora muestra los selectores de color para las propiedades CSS personalizadas.  Para recorrer los formatos RGBA, HSLA y Hexadecimal del valor de color, mantenga presionado y `Shift` elija el selector de color.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1147016][CR1147016].  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Selectores de colores para propiedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Selectores de colores para propiedades CSS personalizadas  
:::image-end:::  

#### Copiar clases y propiedades CSS  

Ahora puede copiar las propiedades CSS más rápido con algunas opciones nuevas en el menú contextual.  En la **herramienta Elementos,** elija un elemento.  Para copiar el valor, en el panel Estilos, mantenga el mouse sobre una clase CSS o una propiedad CSS, abra un menú contextual \(haga clic con el botón secundario\) y elija la opción de copia. ****  

:::row:::
   :::column span="":::
      Opciones de copia para una clase CSS.  
      
      | Opción | Detalles |  
      |:--- |:--- |  
      | **Selector de copia** | Copie el nombre del selector actual. |  
      | **Regla de copia** | Copie la regla del selector actual. |  
      | **Copiar todas las declaraciones** | Copie todas las declaraciones en la regla actual, incluidas las propiedades no válidas y con prefijo. |  
   :::column-end:::
   :::column span="":::
      Opciones de copia de una propiedad CSS.  
      
      | Opción | Detalles |      
      |:--- |:--- |  
      | **Copiar declaración** | Copie la declaración de la línea actual. |  
      | **Copy (propiedad)** | Copie la propiedad de la línea actual. |  
      | **Valor de copia** | Copie el valor de la línea actual. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Opciones de copia para una clase CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Opciones de copia para una clase CSS en el menú contextual  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Opciones de copia de una propiedad CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Opciones de copia de una propiedad CSS en el menú contextual  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1152391][CR1152391].  

### Actualizaciones de cookies  

#### Nueva opción para mostrar cookies descodificadas por URL  

Ahora puede optar por mostrar el valor de cookies descodificadas por URL en el **panel Cookies.**  Para mostrar la cookie descodificada, vaya al panel **** Cookies de aplicación, elija cualquier cookie de la lista y seleccione la casilla situada junto a  >  **** Mostrar url **descodificada.**  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opción para mostrar cookies descodificadas por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Opción para mostrar cookies descodificadas de url  
:::image-end:::  

#### Filtrar y borrar las cookies visibles  

En Microsoft Edge versión 88 **** o anterior, la herramienta de aplicación solo proporcionaba una forma de borrar todas las cookies con el botón Borrar **todas las cookies.**  En La versión 89 de Microsoft Edge, ahora puede elegir Borrar **cookies** filtradas para eliminar solo las cookies filtradas.  Para filtrar las cookies, vaya **a**  >  **Cookies de**aplicación y escriba el **cuadro de texto** Filtro.  Para eliminar las cookies mostradas, elija el botón Borrar **cookies filtradas.**  Para mostrar todas las demás cookies, borre el texto del filtro.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Borrar solo las cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Borrar solo las cookies visibles  
:::image-end:::  

#### Nueva opción para borrar cookies de terceros en el panel almacenamiento  

DevTools ahora borra solo las cookies de origen de forma predeterminada.  Para borrar solo los datos del sitio **** web y las cookies de origen, vaya a Almacenamiento de aplicaciones y, a continuación,  >  **** elija Borrar datos **del sitio.**  

Para borrar los datos del sitio web y todas las cookies, vaya **a Almacenamiento de**  >  **aplicaciones.**  Seleccione la casilla situada junto a **la inclusión de cookies de**terceros y, a continuación, elija Borrar datos del **sitio.**  

Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opción para borrar cookies de terceros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Opción para borrar cookies de terceros  
:::image-end:::  

### Actualizaciones de herramientas de red  

#### Configuración de registro de red de registro de registro persistente  

En Microsoft Edge versión 88 o anterior, DevTools restablece la configuración de registro de red **de** registro cuando se actualiza una página web.  En La versión 89 de Microsoft Edge, DevTools ahora conserva la configuración de registro de **red de** registro.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registro de registro de red" lightbox="../../media/2021/01/network-log.msft.png":::
   Registro de registro de red  
:::image-end:::  

#### La opción en línea ahora no es ninguna opción de limitación  

La opción de emulación de red **Online** ahora se ha cambiado a **Sin limitación.**  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Sin opción de limitación" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Sin opción de limitación**  
:::image-end:::  

### Nuevas opciones de copia en la herramienta Consola, la herramienta Orígenes y el panel Estilos

#### Copiar objeto en la herramienta Consola y orígenes  

Ahora puede copiar los valores de objeto en las **herramientas Consola** **y** Orígenes.  La capacidad de copiar valores de objeto es útil cuando se trabaja con objetos grandes.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya a Problemas [1148353][CR1148353] y [1149859][CR1149859].  

:::row:::
   :::column span="":::
      En la **herramienta Consola,** mantenga el mouse sobre un objeto, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, **elija Copiar objeto**.  
   :::column-end:::
   :::column span="":::
      En **** la herramienta Orígenes, en un punto de **** interrupción, mantenga el mouse sobre un objeto, en la ventana emergente Objeto, resalte un objeto, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, elija **Copiar objeto**.  
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

#### Copiar el nombre de archivo en la herramienta Orígenes y en el panel Estilos  

Ahora puede copiar un nombre de archivo mediante el menú contextual.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya a Problemas [1155120][CR1155120].  

:::row:::
   :::column span="":::
      En la **herramienta Orígenes,** mantenga el mouse sobre un nombre de archivo, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, **elija Copiar nombre de archivo**.  
   :::column-end:::
   :::column span="":::
      En la **herramienta Elementos** > **panel** Estilos, mantenga el mouse sobre un nombre de archivo, abra el menú contextual \(right-click\) y, a continuación, elija Copiar nombre **de archivo**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar el nombre de archivo en Orígenes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copiar el nombre de archivo en **Orígenes**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar nombre de archivo en el panel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copiar nombre de archivo en el **panel Estilos**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Actualizaciones de detalles de Frame  

#### Información de los trabajadores de servicio en los detalles de Frame  

DevTools ahora muestra un trabajador de servicio dedicado en el marco primario.  En la figura siguiente, se muestran los detalles del trabajador del servicio.  Para mostrar los detalles del trabajador del servicio, vaya a **Trabajadores de**servicio de marcos de  >  ****  >  `top`  >  **** aplicación y, a continuación, elija un trabajador de servicio.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Información de los trabajadores de servicio en los detalles de marcos" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Información de los trabajadores** de servicio en los **detalles de marcos**  
:::image-end:::  

#### Medir la información de memoria en detalles del marco  

El `performance.measureMemory()` estado de la API ahora se muestra en la sección de disponibilidad de la **API.**  La nueva `performance.measureMemory()` API calcula el uso de memoria de toda la página web.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memoria" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Medir memoria  
:::image-end:::  

### Fotogramas descartados en la herramienta Rendimiento  

Al analizar [el rendimiento de carga en la herramienta Rendimiento,][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]la sección **Marcos** marca ahora los marcos descartados como rojo.  Para mostrar la velocidad de fotogramas, mantenga el puntero sobre un fotograma descartado.  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Fotogramas descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Fotogramas descartados  
:::image-end:::  

#### Nuevo cálculo de contraste de color: algoritmo de contraste perceptivo avanzado (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

El [algoritmo de contraste perceptual avanzado (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] reemplaza la relación de contraste de las directrices [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] en el [selector de colores.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]  APCA es una nueva forma de calcular el contraste.  Se basa en la investigación moderna sobre la percepción del color.  En comparación con las directrices AA/AAA, APCA depende más del contexto.  El contraste se calcula en función de las siguientes propiedades espaciales del texto, el color y el contexto.  

*   Propiedades espaciales del texto que incluyen el grosor y el tamaño de la fuente.  
*   Propiedades espaciales de color que incluyen contraste percibido entre texto y fondo.  
*   Propiedades espaciales de contexto que incluyen luz ambiental, entorno y propósito previsto.  
    
Para activar este experimento, [][DevtoolsCustomizeIndexSettings]ve a Experimentos de configuración y elige la casilla junto a Habilitar el nuevo algoritmo de contraste perceptual avanzado (APCA) que reemplaza la relación de contraste anterior y las directrices  >  **** **AA/AAA.**  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA en el selector de colores" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA en el selector de colores  
:::image-end:::  

## Descargar los canales de vista previa de Microsoft Edge  

Si está en Windows, Linux o macOS, considere la posibilidad de usar los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Ver la relación de contraste de un elemento de texto en el selector de colores: referencia de accesibilidad | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Cambiar CSS: referencia css | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar los métodos abreviados de teclado en las DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de doble pantalla y plegado: emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular una ventanilla móvil: emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Rendimiento de carga de registros: referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Edite la configuración y los estilos de fuente CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Introducción a las herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la seam: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de pantalla multimedia CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Sección 1: demostración css :target para novedades de DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementing dropdown in settings to change themes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Including Debugger for Microsoft Edge as a dependency | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Upgrading Edge DevTools version to 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Add single close buttons to instances panel | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Seleccione las características de fuente y los colores de fondo para proporcionar suficiente contraste para la legibilidad | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos de confianza | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nueva versión de Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Catálogo de soluciones de | Visual Studio código"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador de microsoft edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

<!--[CR174309]: https://crbug.com/174309 "Issue 174309: DevTools: Allow to customize keyboard shortcuts/key bindings | Chromium bugs"  -->  
<!--[CR772558]: https://crbug.com/772558 "Issue 772558: DevTools: Update to latest version of Lighthouse | Chromium bugs"  -->  
[CR978059]: "Problema 978059: Eliminar cookies al filtrarlas, eliminar todas las cookies no solo las filtradas https://crbug.com/978059 | Errores de Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: Nueva característica | Opción de necesidad para ver el valor descodificado de url en las cookies | Errores de Chromium"  
[CR1003629]: "Problema 1003629: Capture Node ya no captura de pantalla el nodo https://crbug.com/1003629 debajo del plegado. | Errores de Chromium"  
[CR1012337]: "Problema 1012337: Borrar datos del sitio destruye la sesión de Google en sitios que no https://crbug.com/1012337 son de Google | Errores de Chromium"  
[CR1028078]: "Problema 1028078: Poner en línea y sin conexión entre sí en la lista https://crbug.com/1028078 | Errores de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: Solicitud de característica: DevTools debe emular dispositivos de doble pantalla y | Errores de Chromium"  
<!--[CR1073909]: https://crbug.com/1073909 "Issue 1073909: BLOCKED | Chromium bugs"  -->  
[CR1075865]: "Problema 1075865: Mostrar fotogramas descartados en la escala de tiempo https://crbug.com/1075865 de las devtools | Errores de Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: ofrecer una interfaz de usuario de editor de tipo de letra especializada | Errores de Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: actualizar la lógica de cálculo de contraste por cada nueva especificación | Errores de Chromium"  
[CR1122507]: "Problema 1122507: Información de trabajo de Surface en la vista de árbol https://crbug.com/1122507 de marco | Errores de Chromium"  
[CR1122580]: "Problema 1122580: Imposible deshabilitar la grabación de red al volver https://crbug.com/1122580 a cargar | Errores de Chromium"  
<!--[CR1126824]: https://crbug.com/1126824 "Issue 1126824: ☂ Support Trust Token debugging in DevTools | Chromium bugs"  -->  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: Herramientas de Flexbox | Errores de Chromium"  
<!--[CR1137837]: https://crbug.com/1137837 "Issue 1137837: ☂ Improve Trusted Types support in DevTools | Chromium bugs"  -->  
[CR1139899]: "Problema 1139899: Notificar la disponibilidad de la API privada en la vista de detalles del https://crbug.com/1139899 marco | Errores de Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: Superposición de Flexbox | Errores de Chromium"  
<!--[CR1142804]: https://crbug.com/1142804 "Issue 1142804: Implement break-on-trusted-type-violation | Chromium bugs"  -->  
<!--[CR1144127]: https://crbug.com/1144127 "Issue 1144127: BLOCKED | Chromium bugs"  -->  
[CR1147016]: "Problema 1147016: el selector de colores no se muestra en la https://crbug.com/1147016 función var(). | Errores de Chromium"  
[CR1148353]: "Problema 1148353: Solicitud de característica: Copiar objeto desde la consola https://crbug.com/1148353 de devtools | Errores de Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitud de característica][Consola] agregar objeto de copia al elemento del Portapapeles al menú contextual | Errores de Chromium"  
[CR1150797]: "Problema 1150797: Agregar menú contextual de elemento duplicado en el panel de https://crbug.com/1150797 elementos | Errores de Chromium"  
<!--[CR1150883]: https://crbug.com/1150883 "Issue 1150883: Remove TT messages from the console but keep underlining in the sources tab | Chromium bugs"  -->  
<!--[CR1152290]: https://crbug.com/1152290 "Issue 1152290: Devtools support for QuicTransport | Chromium bugs"  -->  
[CR1152391]: "Problema 1152391: Compatibilidad con la copia del menú contextual CSS en el panel de https://crbug.com/1152391 estilos | Errores de Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Support copy file name and line number | Errores de Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: agregar compatibilidad con la característica de estado de elemento :target in force | Errores de Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Accesibilidad - Narrador: Narrador no anuncia el recuento y la posición de las sugerencias disponibles para el código en la pestaña Estilos | Errores de Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "| Samsung (Ee. UU.)"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (mejorado): cómo reunirse con WCAG (referencia rápida) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo): cómo reunirse con WCAG (referencia rápida) | W3C"  

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
