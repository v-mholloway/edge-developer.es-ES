---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para ver y cambiar el CSS de una página.
title: Introducción a cómo ver y cambiar CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 1ce96a83de1f02737a3f605d51cddaf6fb2e0c0a
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11892991"
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
# <a name="get-started-with-viewing-and-changing-css"></a>Introducción a cómo ver y cambiar CSS  

Complete estos tutoriales interactivos para aprender los conceptos básicos de ver y cambiar el CSS de una página mediante Microsoft Edge DevTools.  

## <a name="open-css-examples"></a>Ejemplos de CSS abiertos  

1.  Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y elija **Ejemplos de CSS** para abrirse en una nueva ventana.  
    
    [Ejemplos de CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Si desea acoplar la ventana [DevTools][DevToolsCustomizePlacement] a la derecha de la ventanilla \(se muestra en la siguiente figura\), elija Personalizar y **controlar DevTools** `...` .  En el **menú desplegable Personalizar y controlar DevTools,** en la sección Lado **dock,** elija **Acoplar a la derecha.**  
    
## <a name="view-the-css-for-an-element"></a>Ver el CSS de un elemento  

1.  [Abrir ejemplos de CSS](#open-css-examples).  
1.  Mantenga el mouse `Inspect Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
    1.  En DevTools, en la **herramienta Elementos,** en el panel Árbol **DOM,** se `Inspect Me!` resalta el elemento.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="El elemento inspeccionado se resalta en el árbol DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           El elemento inspeccionado se resalta en el **árbol DOM**  
        :::image-end:::  
        
    1.  En el `Inspect Me!` elemento, busque el valor del `data-message` atributo y cópielo.  
1.  En la página, en el **cuadro de texto Valor de `data-message` :** , escriba el valor.  
1.  Mantenga el mouse `Inspect Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
    1.  En DevTools, en la **herramienta Elementos,** seleccione el panel **Estilos.**  
    1.  En el panel **Estilos,** el `Inspect Me!` elemento está resaltado.  
    1.  En el `Inspect Me!` elemento, busque la regla `aloha` de clase.  
        
        > [!NOTE]
        > Esta regla se muestra, ya que se está aplicando al `Inspect Me!` elemento.  
        
    1.  En la `aloha` clase, busque el valor del `padding` estilo y cópielo.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Las clases CSS se aplican al elemento inspeccionado y se resaltan en el panel Estilos" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Las clases CSS se aplican al elemento seleccionado, como , se muestran `aloha` en el panel **Estilos**  
        :::image-end:::  
        
1.  En la página, en el **cuadro de texto Valor de `padding` :** , escriba el valor.  

## <a name="add-a-css-declaration-to-an-element"></a>Agregar una declaración CSS a un elemento  

Use el panel **Estilos** cuando desee cambiar o agregar declaraciones CSS a un elemento.  

> [!NOTE]
> Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.  

1.  [Abrir ejemplos de CSS](#open-css-examples).  
1.  Mantenga el mouse `Add A Background Color To Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
1.  Elija `element.style` cerca de la parte superior del panel **Estilos.**  
1.  Escriba `background-color` y seleccione `Enter` .  
1.  Escriba `honeydew` y seleccione `Enter` .  En el **árbol DOM,** se muestra una declaración de estilo en línea aplicada al elemento.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Agregar una declaración CSS al elemento mediante el panel Estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       La `background-color:honeydew` declaración se aplica al elemento mediante la sección del panel `element.style` **Estilos**  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a>Agregar una clase CSS a un elemento  

Para mostrar el aspecto de un elemento cuando se aplica o quita una clase CSS de un elemento, vaya al panel **Estilos.**  

> [!NOTE]
> Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.  

1.  [Abrir ejemplos de CSS](#open-css-examples).  
1.  Mantenga el mouse `Add A Class To Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
1.  Elija **.cls**.  DevTools muestra un cuadro de texto donde puede agregar clases al elemento seleccionado.  
1.  Escriba `color_me` en el cuadro de texto Agregar nueva **clase** y, a continuación, seleccione `Enter` .  Aparece una casilla debajo del cuadro de texto **Agregar** nueva clase, donde puede activar y desactivar la clase.  Si el elemento tiene otras clases aplicadas, también puedes alternar cada `Add A Class To Me!` una desde aquí.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicar la clase color_me al elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       La `color_me` clase se aplica al elemento mediante la sección **.cls** del panel **Estilos**  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a>Agregar un pseudoestado a una clase  

Use el panel **Estilos** para aplicar permanentemente un pseudoestado CSS a un elemento.  DevTools admite `:active` , `:focus` , y `:hover` `:visited` .  

> [!NOTE]
> Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.  

1.  [Abrir ejemplos de CSS](#open-css-examples).  
1.  Mantenga el mouse sobre el `Hover Over Me!` texto.  Cambia el color de fondo.  
1.  Mantenga el mouse `Hover Over Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
1.  En el panel **Estilos,** elija **:hov**.  
1.  Active la **casilla :hover.**  El color de fondo cambia como antes, aunque no se mantenga el mouse sobre el elemento.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternar la pseudoestación activa en un elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Alternar el `:hover` pseudostate en un elemento  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a>Cambiar las dimensiones de un elemento  

Use el **diagrama interactivo Modelo** de cuadro en el panel **Estilos** para cambiar el ancho, alto, relleno, margen o longitud de borde de un elemento.  

> [!NOTE]
> Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.  

1.  [Abrir ejemplos de CSS](#open-css-examples).  
1.  Mantenga el mouse `Change My Margin!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
1.  En el **diagrama Modelo de** cuadro del panel **Estilos,** mantenga el mouse sobre **el relleno**.  El relleno de un elemento se resalta en la ventanilla.  

    > [!NOTE]
    > Según el tamaño de la ventana DevTools, es posible que deba desplazarse hasta la parte inferior del panel **Estilos** para mostrar **el modelo de cuadro**.  

1.  Haga doble clic en el margen izquierdo del **Modelo**de cuadro , que actualmente tiene un valor que significa que el elemento `-` no tiene un margen izquierdo.  
1.  Escriba `100px` y seleccione `Enter` .  El **modelo de** cuadro tiene el valor predeterminado de píxeles, pero también acepta otros valores, como , o `25%` `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Mantenga el mouse sobre el relleno del elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Mantenga el mouse sobre el relleno del elemento  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Cambiar el margen izquierdo del elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Cambiar el margen izquierdo del elemento  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a>Depuración de consultas multimedia  

[Las consultas multimedia][MDNUsingMediaGueries] son una forma de hacer que el producto web reaccione a los cambios en las opciones de configuración de cada usuario.  El caso de uso más significativo es proporcionar al producto un diseño CSS diferente en función de las dimensiones de la ventanilla.  El uso de diseños independientes permite un diseño de una columna para dispositivos móviles y diseños de varias columnas cuando hay más estado de pantalla disponible.  

Si desea depurar o probar las consultas multimedia que definió en su CSS, siga estos pasos.  

1.  Abra las herramientas de desarrollador y seleccione el icono **de** la barra de herramientas Alternar dispositivo en la parte superior izquierda o `Ctrl` + `Shift` + `M` seleccione \( `Cmd` + `Shift` + `M` en macOS\).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abrir la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Abrir la barra de herramientas del dispositivo  
    :::image-end:::  
    
1.  Con la barra de herramientas del dispositivo abierta, seleccione el menú de la parte superior derecha y `...` elija Ver consultas **multimedia**.  Las barras de colores que se muestran encima de la página web representan las distintas consultas multimedia.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrar consultas multimedia en la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Mostrar consultas multimedia en la barra de herramientas del dispositivo  
    :::image-end:::  
    
1.  Mantenga el mouse sobre los límites de las barras para mostrar los valores de las distintas consultas multimedia.  Elija cada una para cambiar el tamaño de la página web que desea que coincida.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Elegir consulta multimedia en la barra de vista previa" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Elegir consulta multimedia en la barra de vista previa  
    :::image-end:::  
    
1.  Para depurar consultas multimedia y abrir el archivo CSS en el editor; mantenga el mouse en cualquiera de los segmentos de barra, abra el menú contextual \(hacer clic con el botón `Sources` secundario\) y seleccione `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Mostrar consultas multimedia en el Editor de orígenes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Mostrar consultas multimedia en el Editor de orígenes  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools (desacoplar, acoplar a abajo, acoplar a la izquierda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Ejemplos de CSS: Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Uso de consultas multimedia | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
