---
title: Introducción a la visualización y el cambio de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601820"
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





# Introducción a la visualización y el cambio de CSS   



Complete estos tutoriales interactivos para conocer los conceptos básicos de la visualización y el cambio de las CSS de una página con Microsoft Edge DevTools.  

## Ejemplos de CSS abiertos  

1.  Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplos de CSS** para abrir en una ventana nueva.  
    
    [Ejemplos de CSS][GlitchDevToolsCssExamples]  

> [!NOTE]
> Si desea [acoplar la ventana de DevTools][DevToolsCustomizePlacement] a la derecha de la ventanilla \ (que se muestra en la [figura 1](#figure-1)\), haga clic en **personalizar y controlar DevTools** `...` .  En el menú desplegable **personalizar y controlar DevTools** , en la sección de **acoplamiento** , seleccione **acoplar a la derecha**.  
    
## Ver la CSS de un elemento   

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Haga clic con el botón derecho en el `Inspect Me!` texto y seleccione **inspeccionar**.  
    1.  En DevTools, en el panel **elementos** , en la pestaña **árbol DOM** , `Inspect Me!` se resalta el elemento.  
        
        > ##### Figura 1  
        > El elemento inspeccionado está resaltado en el **árbol DOM**  
        > ![El elemento inspeccionado está resaltado en el árbol DOM][ImageInspect]  
        
    1.  En el `Inspect Me!` elemento, busque el valor del `data-message` atributo y cópielo.  
1.  En la página, en el cuadro **de texto valor de `data-message` :** , escriba el valor.  
1.  Haga clic con el botón derecho en el `Inspect Me!` texto y seleccione **inspeccionar**.  
    
    1.  En DevTools, en el panel **elementos** , seleccione la pestaña **estilos** .  
    1.  En la pestaña **estilos** , `Inspect Me!` se resalta el elemento.  
    1.  En el `Inspect Me!` elemento, busque la `aloha` regla de clase.  
        
        > [!NOTE]
        > Verá esta regla porque se está aplicando al `Inspect Me!` elemento.  
        
    1.  En la `aloha` clase, busque el valor del `padding` estilo y cópielo.  
        
        > ##### Figura 2  
        > Las clases CSS que se aplican al elemento seleccionado, como `aloha` , se muestran en la pestaña **estilos** .  
        > ![Las clases CSS que se aplican al elemento inspeccionado se resaltan en la pestaña estilos.][ImageAloha]  
        
1.  En la página, en el cuadro **de texto valor de `padding` :** , escriba el valor.  

## Agregar una declaración CSS a un elemento   

Use la pestaña **estilos** cuando desee cambiar o agregar declaraciones CSS a un elemento.  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Haga clic con el botón derecho en el `Add A Background Color To Me!` texto y seleccione **inspeccionar**.  
1.  Haga clic `element.style` cerca de la parte superior de la pestaña **estilos** .  
1.  Escriba `background-color` y presione `Enter` .  
1.  Escriba `honeydew` y presione `Enter` .  En el **árbol DOM** , debería ver que se aplicó una declaración de estilo en línea al elemento.  

> ##### Imagen 3  
> La `background-color:honeydew` declaración se ha aplicado al elemento mediante la `element.style` sección de la pestaña **estilos** .  
> ![Agregar una declaración CSS al elemento mediante la pestaña estilos][ImageDeclaration]  

## Agregar una clase CSS a un elemento   

Use la pestaña **estilos** para ver el aspecto que tiene un elemento cuando se aplica o se quita una clase CSS de un elemento.  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Haga clic con el botón derecho en el `Add A Class To Me!` elemento y seleccione **inspeccionar**.  
1.  Haga clic en **. CLS**.  DevTools revela un cuadro de texto en el que puede Agregar clases al elemento seleccionado.  
1.  Escriba `color_me` el cuadro de texto **Agregar nueva clase** y, después, presione `Enter` .  Aparece una casilla debajo del cuadro de texto **Agregar nueva clase** , donde puede activar o desactivar la clase.  Si el `Add A Class To Me!` elemento tiene otras clases aplicadas, también podrá alternar entre aquí.  

> ##### Imagen 4  
> La `color_me` clase se ha aplicado al elemento mediante la sección **. CLS** de la pestaña **estilos** .  
> ![Aplicar la clase color_me al elemento][ImageApplyClass]  

## Agregar un PseudoState a una clase   

Use la pestaña **estilos** para aplicar de forma permanente un PseudoState CSS a un elemento.  DevTools es compatible con `:active` ,, `:focus` `:hover` , y `:visited` .  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Desplace el puntero sobre el `Hover Over Me!` texto.  Cambia el color de fondo.  
1.  Haga clic con el botón derecho en el `Hover Over Me!` texto y seleccione **inspeccionar**.  
1.  En la pestaña **estilos** , haga clic en **: HOV**.  
1.  Active la casilla **: hover** .  El color de fondo cambia como antes, aunque no esté colocando el puntero sobre el elemento.  

> ##### Imagen 5  
> Alternar el `:hover` PseudoState en un elemento  
> ![Alternar el PseudoState hover en un elemento][ImageSetHover]  

## Cambiar las dimensiones de un elemento   

Use el Diagrama interactivo del **modelo de cuadro** de la pestaña **estilos** para cambiar el ancho, alto, relleno, margen o longitud de borde de un elemento.  

> [!NOTE]
> Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.  

1.  [Abra ejemplos de CSS](#open-css-examples).  
1.  Haga clic con el botón derecho en el `Change My Margin!` elemento y seleccione **inspeccionar**.  
1.  En el diagrama de **modelo de cuadro** de la pestaña **estilos** , desplace el puntero sobre el **relleno**.  El relleno de un elemento se resalta en la ventanilla.  

    > [!NOTE]
    > Según el tamaño de la ventana de DevTools, es posible que tenga que desplazarse hasta la parte inferior de la pestaña **estilos** para ver el **modelo de cuadro**.  

1.  Haga doble clic en el margen izquierdo del **modelo de cuadro**, que tiene actualmente el valor de `-` significado que el elemento no tiene un margen izquierdo.  
1.  Escriba `100px` y presione `Enter` .  El **modelo de cuadro** tiene un valor predeterminado de píxeles, pero también acepta otros valores, como `25%` , o `10vw` .  

> ##### Imagen 6  
> Mantener el mouse sobre el relleno del elemento  
> ![Mantener el mouse sobre el relleno del elemento][ImageShowPadding]  

> ##### Imagen 7  
> Cambiar el margen izquierdo del elemento  
> ![Cambiar el margen izquierdo del elemento][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Ilustración 1: el elemento inspeccionado está resaltado en el árbol DOM"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Ilustración 2: las clases CSS que se están aplicando al elemento inspeccionado se resaltan en la pestaña estilos."  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Ilustración 3: agregar una declaración CSS al elemento mediante la pestaña estilos"  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Ilustración 4: aplicar la clase color_me al elemento"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Ilustración 5: alternar el PseudoState hover en un elemento"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Ilustración 6: mantener el mouse sobre el relleno del elemento"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Ilustración 7: cambiar el margen izquierdo del elemento"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Ejemplos de CSS: Microsoft Edge (cromo) DevTools | Intento"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
