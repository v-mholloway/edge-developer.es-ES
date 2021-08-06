---
description: Si te encuentras escribiendo las mismas expresiones de JavaScript en la consola repetidamente, prueba Live Expressions en su lugar.
title: Ver valores de expresión de JavaScript en tiempo real con live expressions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 0ac6cbe40d3bf52cfcde76554b90bc1926f555c4c031c595ce5f42c171ae8a82
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11801273"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a>Supervisar los cambios en JavaScript mediante expresiones live  

**Las expresiones live** son una excelente manera de supervisar expresiones de JavaScript que cambian mucho.    En lugar de tener muchos mensajes de consola para leer y navegar, puede anclar las expresiones de JavaScript específicas a la parte superior de la **consola**.  

## <a name="add-a-new-live-expression"></a>Agregar una nueva expresión en directo  

Para empezar, elija el **botón Crear expresión en** directo \(eye\) junto al cuadro de texto **Filter.**  Después de elegirlo, se muestra un cuadro de texto para que escriba la nueva expresión en él.  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Elija el botón Nueva expresión en directo para abrir un cuadro de texto para escribir una expresión" lightbox="../media/console-live-expressions-new.msft.png":::
    Elija el `New live expression` botón para abrir un cuadro de texto para escribir una expresión  
:::image-end:::  

**Las expresiones live** pueden ser cualquier expresión válida de JavaScript.  Para probarlo, complete las siguientes acciones.  

1.  Abra el **cuadro de texto Expresión** en directo.  
1.  Escriba `document.activeElement`.  
1.  Para guardar la expresión, complete una de las siguientes acciones.  
    *   Seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\).  
    *   Elija fuera del **cuadro de texto Expresión** en directo.  
        
La expresión ahora está en directo y se `body` muestra como resultado.  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="La expresión activa de document.activeElement muestra el cuerpo como resultado" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    Expresión en directo para `document.activeElement` muestra el cuerpo como resultado  
:::image-end:::  

Si navega por la página web, el valor cambia.  Por ejemplo, en la siguiente figura se abre el menú de búsqueda en la página web y la expresión se muestra `button.nav-bar-button.focus-visible` ahora como el valor.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Para cambiar el valor de live expression, interactúe con diferentes elementos de la página web" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    Para cambiar el valor de **live expression**, interactúe con diferentes elementos de la página web  
:::image-end:::  

Para volver a cambiar el valor, abra y elija el cuadro de texto Buscar en la página web.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Navegue a otro elemento de la página web para actualizar live expression" lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    Navegue a otro elemento de la página web para actualizar **live expression**  
:::image-end:::  

## <a name="remove-live-expressions"></a>Quitar expresiones en directo  

Una **expresión activa** está disponible siempre que la mantenga activa.  Para deshacerse de **una expresión live,** elija la `x` siguiente.  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Para quitar live expressions, elija la x junto a ella" lightbox="../media/console-live-expressions-remove.msft.png":::
    Para quitar **expresiones en directo,** elija la `x` siguiente.  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a>Reemplazar el registro de consola por expresiones en directo  

Puedes crear tantas expresiones como quieras y conservar cada una de las sesiones y ventanas del explorador.  **Las expresiones live** son una forma de reducir el ruido en el flujo de trabajo de depuración.  

Por ejemplo, desea supervisar el movimiento del mouse en la página web actual.  Navegue a [la demostración movimiento][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]del mouse de registro, abra **la consola**y mueva el mouse alrededor para mostrar los registros con mucha información.  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="La consola muestra mucha información sobre la posición del mouse" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    **La** consola muestra mucha información sobre la posición del mouse  
:::image-end:::  

La gran cantidad de información no solo ralentiza el proceso de depuración, sino que también facilita la pérdida de los cambios que desea revisar.  A medida **que la consola** muestra más mensajes y mueve el mouse, los valores que desea revisar se desplazan fuera de la pantalla.  

Para probar **Live Expressions** como alternativa, complete las siguientes acciones.  

1.  Vaya al movimiento [mouse sin la demostración de registro][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].  
1.  Crear **expresiones en directo** para y `x` `y` .  
    
Cuando se usan **expresiones**en directo, siempre se obtiene la **** información en la misma parte de la pantalla y se mantienen los registros de consola para valores que no cambian tanto.

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Mostrar la posición x e y del mouse como expresiones vivas" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    Mostrar la `x` posición y el mouse como `y` **expresiones vivas**  
:::image-end:::  

**Las expresiones live** se ejecutan exclusivamente en el equipo y no es necesario cambiar nada en el código para mostrar.  **Las expresiones en** directo son una excelente manera de asegurarse de que solo se muestra la información que desea depurar.  Además, **live expressions** te ayudan a limitar el ruido en los equipos de los usuarios.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Ejemplos de mensajes de consola: Uso de tablas | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Movimiento del mouse sin registro | GitHub"  
