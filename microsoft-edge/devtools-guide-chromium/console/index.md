---
description: Una introducción a la herramienta consola dentro de Microsoft Edge Developer Tools.
title: Usar la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3f2f8c01a9bc9c4f40158f0959ba5b60e03bfb80
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483243"
---
# <a name="use-the-console"></a>Usar la consola  

La **herramienta Consola** de DevTools le ayuda con varias tareas.  La siguiente lista incluye algunas de las tareas.  

*   Descubra por qué algo no funciona en el proyecto actual y [realice un seguimiento de los problemas][DevtoolsConsoleConsoleDebugJavascript].  
*   [Obtenga información sobre el proyecto web en][DevtoolsConsoleConsoleFilters] el explorador como mensajes de registro.  
*   [Información de registro][DevtoolsConsoleConsoleLog] en scripts con fines de depuración.  
*   [Pruebe las expresiones de JavaScript][DevtoolsConsoleConsoleJavascript] en un [entorno REPL.][WikiReadEvalPrintLoop]  
*   [Interactúe con el proyecto web en el explorador][DevtoolsConsoleConsoleDomInteraction] con JavaScript.  
    
La **consola** es una excelente herramienta complementaria para usarla con otras herramientas.  La **consola** proporciona una forma eficaz de crear scripts de funcionalidad, inspeccionar y manipular la página web actual mediante JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="La herramienta Consola abierta en el panel superior" lightbox="../media/console-intro-console-main.msft.png":::
         La **herramienta Consola** abierta en el panel superior  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Consola en el panel inferior con la herramienta Elementos abierta encima de ella" lightbox="../media/console-intro-console-panel.msft.png":::
         **Consola** en el panel inferior con la **herramienta Elementos** abierta encima de ella  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

La forma más rápida de abrir directamente la **consola** es `Control` + `Shift` + `J` seleccionar \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  

## <a name="error-reports-and-console"></a>Informes de errores y consola  

**La** consola es el lugar predeterminado donde se notifican los errores de conectividad y JavaScript.  Si se produce algún error, se muestra un botón junto al icono **Configuración** en DevTools que proporciona el número de errores y advertencias.  Elija para abrir la **consola y** mostrar el problema.  Para obtener más información, vaya [a Depurar errores notificados en consola][DevtoolsConsoleConsoleDebugJavascript].  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools proporciona información detallada sobre el error en la consola" lightbox="../media/console-debug-displays-error.msft.png":::
   DevTools proporciona información detallada sobre el error en la **consola**  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a>Inspeccionar y filtrar información en la página web actual  

Al abrir DevTools en una página web, es probable que muestre un auge de la información registrada en la **consola**.  La cantidad de información se convierte en un problema cuando necesita identificar información importante.  Para ver la información importante que necesita acción, use la [herramienta Problemas][DevtoolsIssuesIndex] en DevTools.  Gran parte del ruido permanece, por lo que es una buena idea conocer las opciones automatizadas de registro y [filtro][DevtoolsConsoleConsoleFilters] en la **consola**.  

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools con una consola llena de mensajes" lightbox="../media/console-intro-noise.msft.png":::
   DevTools con una **consola llena** de mensajes  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a>Información de registro que se mostrará en la consola  

El caso de uso más popular para la **consola** es registrar información de los scripts mediante el `console.log()` método u otros métodos similares.  Para probarlo, complete las siguientes acciones.  

1.  Para abrir **consola**, `Control` + `Shift` + `J` seleccione \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  
1.  Vaya a [Ejemplos de mensajes de consola: registro, información, error][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]y advertencia, o copie y ejecute el siguiente fragmento de código en la **consola**.  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  La **consola** muestra los resultados.  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Consola llena de mensajes causados por código de demostración" lightbox="../media/console-intro-logging.msft.png":::
       **Consola** llena de mensajes causados por código de demostración  
    :::image-end:::  
    
Hay muchos métodos útiles disponibles cuando se trabaja con la **consola**.  Para obtener más información, vaya [a Registrar mensajes en la herramienta Consola][DevtoolsConsoleConsoleLog].  

## <a name="try-your-javascript-live-in-the-console"></a>Pruebe JavaScript en directo en la consola  

La **consola** no es solo un lugar para registrar información.  La **consola** es un [entorno REPL.][WikiReadEvalPrintLoop]  Al escribir cualquier JavaScript en la **consola,** el código se ejecuta inmediatamente.  Puede resultar útil probar algunas nuevas características de JavaScript o realizar algunos cálculos rápidos.  Además, obtiene todas las características que espera de un entorno de edición moderno, como la autocompleción, el resaltado de sintaxis y el historial.  Para probarlo, complete las siguientes acciones.  

1.  Vaya a la **consola**.  
1.  Escriba `2 + 2`.  
    
La **consola** muestra el resultado `4` en la siguiente línea.  Esta **característica de evaluación** de Eager es útil para depurar y comprobar que no está cometiendo errores en el código.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La consola muestra el resultado de 2 + 2 en directo a medida que lo escribe" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   La **consola** muestra el resultado de `2 + 2` live al escribirlo  
:::image-end:::  

Para ejecutar la expresión JavaScript en la **consola** y, opcionalmente, mostrar un resultado, seleccione `Enter` .  A continuación, puede escribir el siguiente código JavaScript que se ejecutará en la **consola**.  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ejecutar varias líneas de código JavaScript sucesivamente" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Ejecutar varias líneas de código JavaScript sucesivamente  
:::image-end:::  

De forma predeterminada, se ejecuta código JavaScript en una sola línea.  Para ejecutar una línea, escriba JavaScript y, a continuación, seleccione `Enter` .  Para evitar la limitación de una sola línea, seleccione `Shift` + `Enter` en lugar de `Enter` .  De forma similar a otras experiencias de línea de comandos, para obtener acceso a los comandos de JavaScript anteriores, seleccione `Arrow-Up` .  La característica de autocompletion de **la consola** es una excelente manera de obtener información sobre métodos desconocidos.  Para probarlo, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Escriba `doc`.  
1.  Elija `document` en el menú desplegable.  
1.  Seleccione la `tab` clave para elegirla.  
1.  Escriba `.bo`.  
1.  Seleccione `tab` para obtener `document.body` .  
1.  Escriba otro `.` para mostrar la lista completa de propiedades y métodos disponibles en el cuerpo de la página web actual.  
    
Para obtener más información acerca de todas las formas de trabajar con **la consola,** vaya [a Consola como un entorno JavaScript][DevtoolsConsoleConsoleJavascript].  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de consola de expresiones de JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **Autocompletion** de consola de expresiones de JavaScript  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a>Interactuar con la página web actual en el explorador  

La **consola** tiene acceso al [objeto Window][MdnDocsWebApiWindow] del explorador.  Puede escribir scripts que interactúen con la página web actual.  Para probarlo, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Copie y pegue el siguiente fragmento de código.  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Copiar el contenido del encabezado superior (h1) del DOM y mostrarlo en la consola" lightbox="../media/console-intro-reading-DOM.msft.png":::
   Copiar el encabezado superior \( `h1` \) contenido del DOM y mostrarlo en la **consola**  
:::image-end:::  

En lugar de solo leer desde la página web, también puede cambiarla.  Para probarlo, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Copie y pegue el siguiente fragmento de código.  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Escribir texto en el DOM en la consola" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   Escribir texto en el DOM en la **consola**  
:::image-end:::  

Ha cambiado el encabezado principal de la página web a **Rocking the Console**.  Los **métodos de utilidad de** consola facilita el acceso y la manipulación de la página web actual.  Para obtener más información, vaya a [Console Utilities API reference][DevtoolsConsoleUtilities].  Por ejemplo, para agregar un borde verde alrededor de todos los vínculos de la página web actual, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Copie y pegue el siguiente fragmento de código.  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    

:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Manipular una selección de elementos mediante la consola" lightbox="../media/console-intro-changing-styles.msft.png":::
    Manipular una selección de elementos mediante la **consola**  
:::image-end:::  

Para obtener más información sobre cómo trabajar con el DOM, vaya [a Usar la consola para interactuar con el DOM][DevtoolsConsoleConsoleDomInteraction].  

## <a name="learn-more-about-console"></a>Más información sobre la consola  

Para obtener más información acerca de **console**, vaya a [Console reference][DevtoolsConsoleReference], Console Utilities [API reference][DevtoolsConsoleUtilities]y Console [API reference][DevtoolsConsoleApi].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Errores de depuración notificados en la consola | Microsoft Docs"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use la consola para interactuar con el dom | Microsoft Docs" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrar mensajes de consola | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Consola como entorno de JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensajes en la herramienta consola | Microsoft Docs"  
[DevtoolsConsoleReference]: ./reference.md "Referencia de consola | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[DevtoolsIssuesIndex]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Ejemplos de mensajes de consola: registro, información, error y advertencia | GitHub"  

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Bucle read–eval–print | Wikipedia"  
