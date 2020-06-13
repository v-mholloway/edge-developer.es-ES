---
title: Introducción a cómo ver y cambiar CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 346145a7deb9e8ac951ed0578a5060da72817463
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710388"
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

# Introducción a cómo ver y cambiar CSS  

Complete estos tutoriales interactivos para conocer los conceptos básicos de la visualización y el cambio de las CSS de una página con Microsoft Edge DevTools.  

## Ejemplos de CSS abiertos  

1.  Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y seleccione **ejemplos de CSS** para abrir en una ventana nueva.  
    
    [Ejemplos de CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Si deseas [acoplar la ventana de DevTools][DevToolsCustomizePlacement] a la derecha de tu ventanilla \ (se muestra en la siguiente ilustración \), selecciona **personalizar y controla la DevTools** `...` .  En el menú desplegable **personalizar y controlar DevTools** , en la sección de **acoplamiento** , seleccione **acoplar a la derecha**.  
    
## Ver la CSS de un elemento  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Desplace el puntero sobre el `Inspect Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.  
    1.  En DevTools, en el panel **elementos** , en la pestaña **árbol DOM** , `Inspect Me!` se resalta el elemento.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="El elemento inspeccionado está resaltado en el árbol DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           Ilustración 1: el elemento inspeccionado está resaltado en el **árbol DOM**  
        :::image-end:::  
        
    1.  En el `Inspect Me!` elemento, busque el valor del `data-message` atributo y cópielo.  
1.  En la página, en el cuadro **de texto valor de `data-message` :** , escriba el valor.  
1.  Desplace el puntero sobre el `Inspect Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.  
    1.  En DevTools, en el panel **elementos** , seleccione la pestaña **estilos** .  
    1.  En la pestaña **estilos** , `Inspect Me!` se resalta el elemento.  
    1.  En el `Inspect Me!` elemento, busque la `aloha` regla de clase.  
        
        > [!NOTE]
        > Verá esta regla porque se está aplicando al `Inspect Me!` elemento.  
        
    1.  En la `aloha` clase, busque el valor del `padding` estilo y cópielo.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Las clases CSS que se aplican al elemento inspeccionado se resaltan en la pestaña estilos." lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Ilustración 2: las clases CSS que se están aplicando al elemento seleccionado, como `aloha` , se muestran en la pestaña **estilos** .  
        :::image-end:::  
        
1.  En la página, en el cuadro **de texto valor de `padding` :** , escriba el valor.  

## Agregar una declaración CSS a un elemento  

Use la pestaña **estilos** cuando desee cambiar o agregar declaraciones CSS a un elemento.  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Desplace el puntero sobre el `Add A Background Color To Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.  
1.  Seleccione `element.style` cerca de la parte superior de la pestaña **estilos** .  
1.  Escriba `background-color` y presione `Enter` .  
1.  Escriba `honeydew` y presione `Enter` .  En el **árbol DOM** , debería ver que se aplicó una declaración de estilo en línea al elemento.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Agregar una declaración CSS al elemento mediante la pestaña estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       Ilustración 3: la `background-color:honeydew` declaración se ha aplicado al elemento mediante la `element.style` sección de la pestaña **estilos** .  
    :::image-end:::  
    
## Agregar una clase CSS a un elemento  

Use la pestaña **estilos** para ver el aspecto que tiene un elemento cuando se aplica o se quita una clase CSS de un elemento.  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Desplace el puntero sobre el `Add A Class To Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.  
1.  Seleccione **. CLS**.  DevTools revela un cuadro de texto en el que puede Agregar clases al elemento seleccionado.  
1.  Escriba `color_me` el cuadro de texto **Agregar nueva clase** y, después, presione `Enter` .  Aparece una casilla debajo del cuadro de texto **Agregar nueva clase** , donde puede activar o desactivar la clase.  Si el `Add A Class To Me!` elemento tiene otras clases aplicadas, también podrá alternar entre aquí.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicar la clase color_me al elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       Ilustración 4: se ha `color_me` aplicado la clase al elemento con la sección **. CLS** de la pestaña **estilos** .  
    :::image-end:::  
    
## Agregar un PseudoState a una clase  

Use la pestaña **estilos** para aplicar de forma permanente un PseudoState CSS a un elemento.  DevTools es compatible con `:active` ,, `:focus` `:hover` , y `:visited` .  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Desplace el puntero sobre el `Hover Over Me!` texto.  Cambia el color de fondo.  
1.  Desplace el puntero sobre el `Hover Over Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.  
1.  En la pestaña **estilos** , seleccione **: HOV**.  
1.  Active la casilla **: hover** .  El color de fondo cambia como antes, aunque no esté colocando el puntero sobre el elemento.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternar el PseudoState hover en un elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Ilustración 5: alternar el `:hover` PseudoState en un elemento  
    :::image-end:::  
    
## Cambiar las dimensiones de un elemento  

Use el Diagrama interactivo del **modelo de cuadro** de la pestaña **estilos** para cambiar el ancho, alto, relleno, margen o longitud de borde de un elemento.  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Desplace el puntero sobre el `Change My Margin!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.  
1.  En el diagrama de **modelo de cuadro** de la pestaña **estilos** , desplace el puntero sobre el **relleno**.  El relleno de un elemento se resalta en la ventanilla.  

    > [!NOTE]
    > Según el tamaño de la ventana de DevTools, es posible que tenga que desplazarse hasta la parte inferior de la pestaña **estilos** para ver el **modelo de cuadro**.  

1.  Haga doble clic en el margen izquierdo del **modelo de cuadro**, que tiene actualmente el valor de `-` significado que el elemento no tiene un margen izquierdo.  
1.  Escriba `100px` y presione `Enter` .  El **modelo de cuadro** tiene un valor predeterminado de píxeles, pero también acepta otros valores, como `25%` , o `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Mantener el mouse sobre el relleno del elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Ilustración 6: mantener el mouse sobre el relleno del elemento  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Cambiar el margen izquierdo del elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Ilustración 7: cambiar el margen izquierdo del elemento  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Depurar consultas de medios  

[Las consultas de medios][MDNUsingMediaGueries] son una forma de hacer que el producto Web reaccione ante los cambios en la configuración de cada usuario.  El caso de uso más importante es proporcionar a tu producto un diseño CSS diferente según las dimensiones de la ventanilla.  El uso de diseños independientes permite un diseño de una columna para dispositivos móviles y diseños de varias columnas cuando hay más pantalla disponible.  

Si desea depurar o probar las consultas de medios definidas en su CSS, siga estos pasos.  

1.  Abra las herramientas de desarrollo y seleccione el icono de la **barra de herramientas del dispositivo de alternancia** en la parte superior izquierda o pulse `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` en MacOS \).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abrir la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Ilustración 8: abrir la barra de herramientas del dispositivo  
    :::image-end:::  
    
1.  Con la barra de herramientas dispositivo abierta, seleccione el `...` menú en la parte superior derecha y, a continuación, seleccione **Ver consultas de medios**.  Debería ver barras de colores encima de la visualización de la página que representan las diferentes consultas de medios.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrar las consultas multimedia en la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Ilustración 9: mostrar las consultas multimedia en la barra de herramientas del dispositivo  
    :::image-end:::  
    
1.  Mantenga el mouse sobre los límites de las barras para ver los valores de las diferentes consultas de medios. Seleccione cada una para cambiar el tamaño de la página web para que coincidan.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Seleccionar una consulta multimedia desde la barra de vista previa" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Ilustración 10: seleccionar una consulta multimedia desde la barra de vista previa  
    :::image-end:::  
    
1.  Para depurar consultas de elementos multimedia y abrir el archivo CSS en el `Sources` Editor; Coloque el puntero sobre cualquiera de los segmentos de la barra, abra el menú contextual \ (haga clic con el botón secundario del mouse \) y seleccione `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Mostrar consultas de medios en el editor de orígenes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Ilustración 11: revelación de consultas de medios en el editor de orígenes  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Ejemplos de CSS: Microsoft Edge (cromo) DevTools | Intento"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usar consultas multimedia | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
