---
description: Obtenga información sobre cómo registrar mensajes en la consola.
title: Introducción al registro de mensajes en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fb428154b00959db1627096819c565dd5dc11346
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439292"
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

# <a name="get-started-with-logging-messages-in-the-console"></a>Introducción al registro de mensajes en la consola  

En este tutorial interactivo se muestra cómo registrar y filtrar mensajes en la [consola de Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Mensajes en la **consola**  
:::image-end:::  

Este tutorial está pensado para completarse en orden.  Se supone que comprende los conceptos básicos del desarrollo web, como cómo usar JavaScript para agregar interactividad a una página.  

## <a name="set-up-the-demo-and-devtools"></a>Configurar la demostración y DevTools  

Este tutorial está diseñado para que pueda abrir la demostración y probar todos los flujos de trabajo usted mismo.  Cuando se sigue físicamente, es más probable que recuerde los flujos de trabajo más adelante.  

1.  Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y elija **Ejemplos** de registro de consola para abrir en una nueva pestaña.  
    
    [Ejemplos de registro de consola][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Centra la demostración y, a `Control` + `Shift` + `J` continuación, selecciona \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\) para abrir DevTools.  De forma predeterminada, DevTools se abre a la derecha de la demostración.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools se abre a la derecha de la demostración" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools se abre a la derecha de la demostración  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Dock DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools acoplada a la parte inferior de la demostración" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools acoplada a la parte inferior de la demostración  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Desacoplar DevTools en una ventana independiente.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Explorador en una ventana independiente" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Explorador en una ventana independiente  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Desacoplar DevTools en una ventana independiente.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desacoplada en una ventana independiente" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools desacoplada en una ventana independiente  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a>Ver mensajes registrados desde JavaScript  

La mayoría de los mensajes que se muestran en la **consola** provienen de los desarrolladores web que escribieron el JavaScript de la página.  El objetivo de esta sección es presentarle los diferentes tipos de **** mensajes que probablemente revise en la consola y explicar cómo puede registrar cada tipo de mensaje usted mismo desde su propio JavaScript.  

1.  Elija el **botón Información de** registro en la demostración.  `Hello, Console!` se registra en la consola.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="La consola después de elegir Información de registro" lightbox="../media/console-log-info.msft.png":::
       La **consola** después de elegir Información **de registro**  
    :::image-end:::  
    
1.  Junto al `Hello, Console!` mensaje de la consola, elija **log.js:2**.  El panel Orígenes se abre y resalta la línea de código que hizo que el mensaje se registrara en la consola.  El mensaje se registró cuando se ejecutó el JavaScript de la página `console.log('Hello, Console!')` .
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools abre la herramienta Orígenes después de elegir log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools abre la **herramienta Orígenes** después de elegir `log.js:2`  
    :::image-end:::  
    
1.  Vuelva a la **consola con** cualquiera de los siguientes flujos de trabajo:  
    
    *   Elija la **herramienta Consola.**  
    *   Seleccione `Control` + `[` \(Windows, Linux\) o `Command` + `[` \(macOS\) hasta que la **herramienta** Consola esté en el foco.  
    *   [Abra el menú comando][DevToolsCommandMenu], escriba , elija el comando `Console` Mostrar panel de **consola** y, a continuación, seleccione `Enter` .  
    
1.  Elija el **botón Advertencia de** registro en la demostración.  `Abandon Hope All Ye Who Enter` se registra en la **consola**.  Los mensajes con este formato son advertencias.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="La consola después de elegir Advertencia de registro" lightbox="../media/console-log-warning.msft.png":::
       La **consola** después de elegir Advertencia **de registro**  
    :::image-end:::  
    
    > [!TIP]
    > Si desea mostrar el código que provocó que un mensaje se registrara de una forma determinada, elija un script \(como \) para ver el código que hizo que el mensaje se aplicara `log.js:12` formato.  

1.  Elija el **icono Expandir** \( ![ Expandir ](../media/expand-icon.msft.png) \) delante de `Abandon Hope All Ye Who Enter` .  DevTools muestra el [seguimiento de la pila][WikiStackTrace] que conduce a la llamada.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Seguimiento de una pila" lightbox="../media/console-log-warning-expanded.msft.png":::
       Seguimiento de una pila  
    :::image-end:::  
    
    El seguimiento de la pila le está diciendo que se ejecuta una función denominada , que a su vez `logWarning` ejecuta una función denominada `quoteDante` .  En otras palabras, la solicitud que se ha producido primero se encuentra en la parte inferior del seguimiento de la pila.  Puede registrar los seguimientos de la pila en cualquier momento ejecutando `console.trace()` .  

1.  Elija **Error de registro**.  Se registra el siguiente mensaje de error: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Un mensaje de error" lightbox="../media/console-log-error.msft.png":::
       Un mensaje de error  
    :::image-end:::  
    
1.  Elija **Tabla de registro**.  Una tabla sobre los artistas famosos se registra en la **consola**.  
    
    > [!NOTE]
    > La `birthday` columna solo se rellena para una fila.  Revise el código para determinar por qué es.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Una tabla en la consola" lightbox="../media/console-log-table.msft.png":::
       Una tabla en la **consola**  
    :::image-end:::  
    
1.  Elija **Grupo de registros**.  Los nombres de 4 tortugas conocidas que luchan contra el crimen se agrupan bajo la `Adolescent Irradiated Espionage Tortoises` etiqueta.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Un grupo de mensajes en la consola" lightbox="../media/console-log-group.msft.png":::
       Un grupo de mensajes en la **consola**  
    :::image-end:::  
    
1.  Elija **Registro personalizado**.  Un mensaje con un borde rojo y un fondo azul se registra en la consola.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Un mensaje con formato personalizado en la consola" lightbox="../media/console-log-custom.msft.png":::
       Un mensaje con formato personalizado en la **consola**  
    :::image-end:::  
    
La idea principal aquí es que cuando quiera registrar mensajes en la consola desde JavaScript, use uno de los `console` métodos.  Cada método da formato a los mensajes de forma diferente.  

Hay incluso más métodos de los que se han demostrado en esta sección.  En este tutorial se muestra cómo explorar el resto de los métodos.  

## <a name="view-messages-logged-by-the-browser"></a>Ver mensajes registrados por el explorador  

El explorador también registra los mensajes en la consola.  Esto suele ocurrir cuando hay un problema con la página.  

1.  Elija **Causa 404**.  El explorador registra un código de estado HTTP de error de red porque javascript de la página intentó capturar `404` un archivo que no existe.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Error 404 en la consola" lightbox="../media/console-cause-404.msft.png":::
       Error `404` en la **consola**  
    :::image-end:::  
    
1.  Elija **Causar error**.  El explorador registra un error porque JavaScript está intentando actualizar un nodo `TypeError` DOM que no existe.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="TypeError en la consola" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` en la **consola**  
    :::image-end:::  
    
1.  Elija el **desplegable Niveles de registro** y habilite la opción **Detallado** si está deshabilitada.  Obtenga más información sobre el filtrado en la sección siguiente.  Debe hacer esto para asegurarse de que el siguiente mensaje que inicie sesión esté visible.  
    
    > [!NOTE]
    > Si el desplegable Niveles predeterminados está deshabilitado, es posible que deba cerrar la barra lateral **de la** consola.  Filtra por origen de mensaje a continuación para obtener más información acerca de la **barra lateral de** la consola.
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitar el nivel de registro detallado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Habilitar el nivel de registro detallado  
    :::image-end:::  
    
1.  Elija **Causa infracción**.  La página deja de responder durante unos segundos y, a continuación, el explorador registra el mensaje `[Violation] 'click' handler took 3000ms` en la consola.  La duración exacta puede variar.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Una infracción en la consola" lightbox="../media/console-cause-violation.msft.png":::
       Una infracción en la **consola**  
    :::image-end:::  
    
## <a name="filter-messages"></a>Filtrar mensajes  

En algunas páginas web se revisa que **la consola** se inunda de mensajes.  DevTools proporciona muchas formas diferentes de filtrar los mensajes que no son relevantes para la tarea que se está haciendo.  

### <a name="filter-by-log-level"></a>Filtrar por nivel de registro  

A `console` cada método se le asigna un nivel de gravedad: , `Verbose` , , o `Info` `Warning` `Error` .  Por ejemplo, `console.log()` es un `Info` mensaje -level, mientras `console.error()` que es un mensaje de `Error` -level.  

1.  Elija el **desplegable Niveles de registro** y deshabilite **Errores**.  Un nivel está deshabilitado cuando ya no hay una marca de verificación junto a él.  Los `Error` mensajes -level desaparecen.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Deshabilitar mensajes de nivel de error en la consola" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Deshabilitar mensajes de nivel de error en la **consola**  
    :::image-end:::  
    
1.  Vuelva a **elegir el desplegable Niveles de** registro y vuelva a habilitar **Errores**.  Los `Error` mensajes -level reaparecen.  

### <a name="filter-by-text"></a>Filtrar por texto  

Cuando solo desee ver mensajes que incluyan una cadena exacta, escriba esa cadena en el **cuadro de** texto Filtrar.  

1.  Escriba `Dave` en el cuadro **de** texto Filtrar.  Todos los mensajes que no incluyen la cadena `Dave` están ocultos.  También puede revisar la `Adolescent Irradiated Espionage Tortoises` etiqueta.  Es un error.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrar cualquier mensaje que no incluya a Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Filtrar cualquier mensaje que no incluya `Dave`  
    :::image-end:::  
    
1.  Eliminar `Dave` del cuadro **de** texto Filtro.  Todos los mensajes reaparecen.  

### <a name="filter-by-regular-expression"></a>Filtrar por expresión regular  

Cuando desee mostrar todos los mensajes que incluyen un patrón de texto, en lugar de una cadena específica, use una [expresión regular][MDNRegularExpressions].  

1.  Escriba `/^[AH]/` en el cuadro **de** texto Filtrar.  Escriba el patrón en [RegExr][|::ref1::|Main] para obtener una explicación de lo que está haciendo.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrar cualquier mensaje que no coincida con un patrón" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Filtrar cualquier mensaje que no coincida con el patrón `/^[AH]/`  
    :::image-end:::  
    
1.  Eliminar `/^[AH]/` del cuadro **de** texto Filtro.  Todos los mensajes están visibles de nuevo.  

### <a name="filter-by-message-source"></a>Filtrar por origen de mensaje  

Cuando solo desee ver los mensajes que provenían de una dirección URL determinada, use la **barra lateral**.  

1.  Elija **Mostrar barra lateral de la** consola \( Mostrar barra lateral de la consola ![ ](../media/show-console-sidebar-icon.msft.png) \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="La barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       La barra lateral  
    :::image-end:::  
    
1.  Elija el **icono Expandir** \( ![ Expandir ](../media/expand-icon.msft.png) \) junto al número de mensajes.  En la siguiente figura, el número de mensajes se indica como **13 Mensajes**.  La **barra** lateral muestra una lista de direcciones URL que provocaron que se registraron los mensajes.  Por ejemplo, `log.js` causó 11 mensajes.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Ver el origen de los mensajes en la barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Ver el origen de los mensajes en la barra lateral  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a>Filtrar por mensajes de usuario  

Anteriormente, cuando elige **Información de registro**, un script denominado para registrar el mensaje en la `console.log('Hello, Console!')` consola.  Los mensajes registrados desde JavaScript como este se **denominan mensajes de usuario**.  En cambio, al elegir **Causa 404,** el explorador registra un mensaje de nivel que indica que no se encuentra `Error` el recurso solicitado.  Mensajes como ese se consideran mensajes **del explorador**.  Usa la **barra lateral para** filtrar los mensajes del explorador y solo mostrar mensajes de usuario.  

1.  Elija **9 mensajes de usuario**.  Los mensajes del explorador están ocultos.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrado de mensajes del explorador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Filtrado de mensajes del explorador  
    :::image-end:::  
    
1.  Elija **13 Mensajes para** volver a mostrar todos los mensajes.  

## <a name="use-the-console-alongside-any-other-tools"></a>Usar la consola junto con otras herramientas  

Si está editando estilos, pero necesita comprobar rápidamente si hay algo en el registro de consola, Use the Drawer.  

1.  Elija la **herramienta** Elementos.  
1.  Seleccione `Escape` .  Se **abre la herramienta** Consola en **el** cajón.  Tiene todas las características del panel consola que ha estado usando a lo largo de este tutorial.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="La herramienta Consola en el cajón" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         La **herramienta Consola** en el **cajón**  
    :::image-end:::  
    
## <a name="see-also"></a>Consulte también  

*   Para explorar más características y flujos de trabajo relacionados con **la** interfaz de usuario de consola, vaya a Referencia [de consola][DevToolsConsoleApi].  
*   Para obtener más información sobre todos los métodos que se muestran en Ver mensajes registrados desde JavaScript y explorar los otros métodos que no se tratan en este artículo, vaya a `console` Console API [](#view-messages-logged-from-javascript) `console` [Reference][DevToolsConsoleReference].  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge \(Chromium\) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md "Referencia de consola | Microsoft Docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introducción al registro de mensajes | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Seguimiento de pila : Wikipedia"  
> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/log) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
