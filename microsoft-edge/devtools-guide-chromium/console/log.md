---
description: Obtenga información sobre cómo registrar mensajes en la consola.
title: Introducción al registro de mensajes en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2f91f1847bf5469e8106edc21553172fc06db9ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231114"
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

# Introducción al registro de mensajes en la consola  

Este tutorial interactivo le muestra cómo registrar y filtrar mensajes en la consola de [DevTools de Microsoft Edge][MicrosoftEdgeDevTools] .  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Mensajes en la **consola**  
:::image-end:::  

Este tutorial está pensado para completarse en orden.  Se da por hecho que comprende los aspectos básicos del desarrollo web, como el uso de JavaScript para agregar interactividad a una página.  

## Configurar la demostración y las DevTools  

Este tutorial está diseñado para que puedas abrir la demostración y probar todos los flujos de trabajo tú mismo.  Cuando sigues físicamente, es más probable que recuerdes los flujos de trabajo más adelante.  

1.  Espera `Control` \ (Windows, Linux \) o `Command` \ (MacOS \) y elige **ejemplos de registro de consola** para abrirlos en una nueva pestaña.  
    
    [Ejemplos del registro de consola][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Centre la demostración y, a continuación, seleccione `Control` + `Shift` + `J` \ (Windows, Linux \) o `Command` + `Option` + `J` \ (MacOS \) para abrir DevTools.  De forma predeterminada, DevTools se abre a la derecha de la demostración.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools se abre a la derecha de la demostración" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools se abre a la derecha de la demostración  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Acople DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools acoplado a la parte inferior de la demostración" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools acoplado a la parte inferior de la demostración  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Desacople DevTools en una ventana independiente][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Explorador en una ventana independiente" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Explorador en una ventana independiente  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Desacople DevTools en una ventana independiente][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desacoplado en una ventana independiente" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools desacoplado en una ventana independiente  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Ver mensajes registrados desde JavaScript  

La mayoría de los mensajes que se muestran en la **consola** provienen de los programadores web que escribieron el JavaScript de la página.  El objetivo de esta sección es presentarle los diferentes tipos de mensajes que es probable que se revisan en la **consola**y explicar cómo puede registrar cada tipo de mensaje desde su propio JavaScript.  

1.  Elija el botón **información de registro** en la demostración.  `Hello, Console!` se registra en la consola.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="La consola después de elegir la información de registro" lightbox="../media/console-log-info.msft.png":::
       La **consola** después de elegir la **información de registro**  
    :::image-end:::  
    
1.  Junto al `Hello, Console!` mensaje en la consola, elija **log.js:2**.  El panel orígenes se abre y resalta la línea de código que causó que el mensaje se registre en la consola.  El mensaje se registró cuando se ejecutó el JavaScript de la página `console.log('Hello, Console!')` .
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools abre el panel orígenes después de elegir log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools abre el panel **fuentes** después de elegir `log.js:2`  
    :::image-end:::  
    
1.  Vuelva a la **consola** con uno de los siguientes flujos de trabajo:  
    
    *   Elija la pestaña **consola** .  
    *   Seleccione `Control` + `[` \ (Windows, Linux \) o `Command` + `[` \ (MacOS \) hasta que el panel de la **consola** esté en el foco.  
    *   [Abra el menú de comandos][DevToolsCommandMenu], escriba `Console` , seleccione el comando **Mostrar panel de consola** y, a continuación, seleccione `Enter` .  
    
1.  Elija el botón **registrar ADVERTENCIA** de la demostración.  `Abandon Hope All Ye Who Enter` se registra en la **consola**.  Los mensajes con formato como este son advertencias.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="La consola después de elegir registrar ADVERTENCIA" lightbox="../media/console-log-warning.msft.png":::
       La **consola** después de elegir **registrar ADVERTENCIA**  
    :::image-end:::  
    
    > [!TIP]
    > Si desea mostrar el código que causó un mensaje para que se registre de una determinada manera, elija un script \ (como `log.js:12` \) para ver el código que causó el formato del mensaje.  

1.  Elija el icono **expandir** \ ( ![ expandir ][ImageExpandIcon] \) delante de `Abandon Hope All Ye Who Enter` .  DevTools muestra el [seguimiento][WikiStackTrace] de la pila que se dirige a la llamada.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Un seguimiento de pila" lightbox="../media/console-log-warning-expanded.msft.png":::
       Un seguimiento de pila  
    :::image-end:::  
    
    El seguimiento de la pila le indica que se ejecuta una función con nombre `logWarning` , que a su vez ejecuta una función llamada `quoteDante` .  En otras palabras, la solicitud que sucedió en primer lugar se encuentra en la parte inferior del seguimiento de pila.  Puede registrar los seguimientos de la pila en cualquier momento ejecutando `console.trace()` .  

1.  Elija **registrar error**.  Se ha registrado el siguiente mensaje de error: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Un mensaje de error" lightbox="../media/console-log-error.msft.png":::
       Un mensaje de error  
    :::image-end:::  
    
1.  Elija **tabla de registro**.  Se graba en la **consola**una tabla sobre artistas famosos.  
    
    > [!NOTE]
    > La `birthday` columna solo se rellena para una fila.  Revise el código para determinar el motivo.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Una tabla en la consola" lightbox="../media/console-log-table.msft.png":::
       Una tabla en la **consola**  
    :::image-end:::  
    
1.  Elija **grupo de registro**.  Los nombres de las cuatro tortugas famosas y de lucha contra delitos se agrupan debajo de la `Adolescent Irradiated Espionage Tortoises` etiqueta.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Un grupo de mensajes en la consola" lightbox="../media/console-log-group.msft.png":::
       Un grupo de mensajes en la **consola**  
    :::image-end:::  
    
1.  Elija **registro personalizado**.  Se graba en la consola un mensaje con un borde rojo y un fondo azul.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Un mensaje con formato personalizado en la consola" lightbox="../media/console-log-custom.msft.png":::
       Un mensaje con formato personalizado en la **consola**  
    :::image-end:::  
    
La idea principal es que cuando quieras registrar mensajes en la consola desde tu código JavaScript, usas uno de los `console` métodos.  Cada método da formato a los mensajes de forma diferente.  

Hay aún más métodos de los que se han demostrado en esta sección.  En este tutorial se muestra cómo explorar el resto de los métodos.  

## Ver los mensajes registrados por el explorador  

El explorador también registra mensajes en la consola.  Esto suele ocurrir cuando hay un problema con la página.  

1.  Elija **causa 404**.  El explorador registra un código de Estado HTTP de `404` error de red porque el JavaScript de la página ha intentado buscar un archivo que no existe.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Error 404 en la consola" lightbox="../media/console-cause-404.msft.png":::
       `404`Error en la **consola**  
    :::image-end:::  
    
1.  Elija **causar un error**.  El explorador registra una no capturada `TypeError` porque el JavaScript está intentando actualizar un nodo Dom que no existe.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Un TypeError en la consola" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` en la **consola**  
    :::image-end:::  
    
1.  Seleccione la lista desplegable **niveles de registro** y habilite la opción **detallado** si está deshabilitada.  Para obtener más información sobre el filtrado, vaya a la siguiente sección.  Tiene que hacer esto para asegurarse de que el siguiente mensaje que inicie sesión está visible.  
    
    > [!NOTE]
    > Si la lista desplegable niveles predeterminados está deshabilitado, es posible que tenga que cerrar la barra lateral de la **consola** .  Filtrar por origen del mensaje a continuación para obtener más información sobre la barra lateral de la **consola** .
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitar el nivel de registro detallado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Habilitar el nivel de registro detallado  
    :::image-end:::  
    
1.  Elija **causar infracción**.  La página deja de responder durante unos segundos y, a continuación, el explorador registra el mensaje `[Violation] 'click' handler took 3000ms` en la consola.  La duración exacta puede variar.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Violación en la consola" lightbox="../media/console-cause-violation.msft.png":::
       Violación en la **consola**  
    :::image-end:::  
    
## Filtrar mensajes  

En algunas páginas web, revise la **consola** para desbordarse de mensajes.  DevTools proporciona varias formas diferentes de filtrar los mensajes que no son relevantes para la tarea que está realizando.  

### Filtrar por nivel de registro  

`console`A cada método se le asigna un nivel de gravedad: `Verbose` ,, `Info` `Warning` o `Error` .  Por ejemplo, `console.log()` es un `Info` mensaje de nivel, mientras que `console.error()` es `Error` un mensaje de nivel.  

1.  Seleccione la lista desplegable **niveles de registro** y deshabilite **errores**.  Un nivel se deshabilita cuando ya no hay una marca de verificación junto a él.  Los `Error` mensajes de nivel desaparecen.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Deshabilitar mensajes de nivel de error en la consola" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Deshabilitar mensajes de nivel de error en la **consola**  
    :::image-end:::  
    
1.  Vuelva a seleccionar la lista desplegable **niveles de registro** y vuelva a habilitar los **errores**.  Los `Error` mensajes del nivel volverán a aparecer.  

### Filtrar por texto  

Cuando desee ver solo los mensajes que incluyan una cadena exacta, escríbala en el cuadro de texto **filtro** .  

1.  Escriba `Dave` en el cuadro de texto **filtro** .  Todos los mensajes que no incluyan la cadena `Dave` están ocultos.  También puede revisar la `Adolescent Irradiated Espionage Tortoises` etiqueta.  Es un error.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrar cualquier mensaje que no incluya Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Filtrar cualquier mensaje que no incluya `Dave`  
    :::image-end:::  
    
1.  Eliminar `Dave` en el cuadro de texto **filtro** .  Todos los mensajes volverán a aparecer.  

### Filtrar por expresión regular  

Cuando desee mostrar todos los mensajes que incluyan un patrón de texto, en lugar de una cadena específica, use una [expresión regular][MDNRegularExpressions].  

1.  Escriba `/^[AH]/` en el cuadro de texto **filtro** .  Escriba este patrón en [Regex][|::ref1::|Main] para obtener una explicación de lo que está haciendo.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrar los mensajes que no coincidan con un patrón" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Filtrar los mensajes que no coincidan con el patrón `/^[AH]/`  
    :::image-end:::  
    
1.  Eliminar `/^[AH]/` en el cuadro de texto **filtro** .  Todos los mensajes volverán a verse.  

### Filtrar por origen del mensaje  

Si desea ver solo los mensajes procedentes de una dirección URL determinada, use la **barra lateral**.  

1.  Elija **Mostrar la barra lateral de consola** \ ( ![ Mostrar barra lateral de consola ][ImageShowConsoleSidebarIcon] \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="La barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       La barra lateral  
    :::image-end:::  
    
1.  Elija el icono **expandir** \ ( ![ expandir ][ImageExpandIcon] \) junto al número de mensajes.  En la siguiente ilustración, el número de mensajes se indica como **13 mensajes**.  La **barra lateral** muestra una lista de las direcciones URL que han provocado el registro de mensajes.  Por ejemplo, se `log.js` produjeron 11 mensajes.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Ver el origen de los mensajes en la barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Ver el origen de los mensajes en la barra lateral  
    :::image-end:::  
    
### Filtrar por mensajes de usuario  

Anteriormente, al elegir **información de registro**, un script denominado para `console.log('Hello, Console!')` registrar el mensaje en la consola.  Los mensajes registrados de JavaScript como este se denominan **mensajes de usuario**.  Por el contrario, si elige la **causa de 404**, el explorador registrará un `Error` mensaje de nivel que indica que no se pudo encontrar el recurso solicitado.  Mensajes como los que se consideran **mensajes del explorador**.  Use la **barra lateral** para filtrar los mensajes del explorador y mostrar solo los mensajes de usuario.  

1.  Elija **9 mensajes de usuario**.  Los mensajes del explorador están ocultos.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrar los mensajes del explorador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Filtrar los mensajes del explorador  
    :::image-end:::  
    
1.  Elija **13 mensajes** para volver a mostrar todos los mensajes.  

## Usar la consola junto con cualquier otro panel  

¿Qué sucede si está editando estilos, pero necesita consultar rápidamente el registro de consola para buscar algo?  Use el cajón.  

1.  Elija la pestaña **elementos** .  
1.  Seleccione `Escape` .  Se abrirá la ficha **Console** del **cajón** .  Tiene todas las características del panel de la consola que ha estado usando en este tutorial.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Ficha de consola en el cajón" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         Ficha de **consola** en el **cajón**  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   Navigate to [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   Navigate to [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas de desarrollador de Microsoft Edge \ (cromo \) | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de DevTools de Microsoft Edge | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de la API de consola | Microsoft docs"  
[DevToolsConsoleReference]: ./reference.md "Referencia de consola | Microsoft docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introducción a la creación de mensajes de registro | Intento"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExer"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Seguimiento de la pila-Wikipedia"  
> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/log) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
