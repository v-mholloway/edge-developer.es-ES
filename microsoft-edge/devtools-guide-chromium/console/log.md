---
title: Introducción al registro de mensajes en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d3dbec41bc1e53b5e9001551c796e5a495dd331e
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601736"
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

> ##### Figura 1  
> Mensajes en la consola  
> ![Mensajes en la consola][ImageLogExample]  

Este tutorial está pensado para completarse en orden.  Se da por hecho que comprende los aspectos básicos del desarrollo web, como el uso de JavaScript para agregar interactividad a una página.  

## Configurar la demostración y las DevTools   

Este tutorial está diseñado para que puedas abrir la demostración y probar todos los flujos de trabajo tú mismo.  Cuando sigues físicamente, es más probable que recuerdes los flujos de trabajo más adelante.  

1.  Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplos del registro de consola** para abrirlos en una nueva pestaña.  
    
    [Ejemplos del registro de consola][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  Centre la demostración y, a continuación, pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir DevTools.  De forma predeterminada, DevTools se abre a la derecha de la demostración.  
    
    > ##### Figura 2  
    > DevTools se abre a la derecha de la demostración  
    > ! [DevTools se abre a la derecha de la demostración] [ImageDevToolsRight]  
    
    > [!TIP]
    > [Acople DevTools en la parte inferior de la ventana o desacoplelo en una ventana independiente][DevToolsCustomizePlacement].  
    
    > ##### Imagen 3  
    > DevTools acoplado a la parte inferior de la demostración  
    > ! [DevTools acoplada a la parte inferior de la demostración] [ImageDevToolsBottom]  
    
    > ##### Imagen 4  
    > Explorador en una ventana independiente  
    > ! [Explorador en una ventana independiente] [ImageDevToolsSeparateBrowse]  
    
    > ##### Imagen 5  
    > DevTools desacoplado en una ventana independiente  
    > ! [DevTools desacoplado en una ventana independiente] [ImageDevToolsSeparateDevTools]  
    
## Ver mensajes registrados desde JavaScript   

La mayoría de los mensajes que ve en la consola provienen de los programadores web que escribieron el JavaScript de la página.  El objetivo de esta sección es presentarle los diferentes tipos de mensajes que probablemente verá en la consola y explicar cómo puede registrar cada tipo de mensaje desde su propio JavaScript.  

1.  Haga clic en el botón **información de registro** de la demostración.  `Hello, Console!` se registra en la consola.
    
    > ##### Imagen 6  
    > La consola después de hacer clic en **información de registro**  
    > ! [La consola después de hacer clic en información de registro] [ImageLogInfo]  
    
1.  Junto al `Hello, Console!` mensaje en la consola, haga clic en **log. js: 2**.  El panel orígenes se abre y resalta la línea de código que causó que el mensaje se registre en la consola.  El mensaje se registró cuando se ejecutó el JavaScript de la página `console.log('Hello, Console!')` .
    
    > ##### Imagen 7  
    > DevTools abre el panel orígenes después de hacer clic en **log. js: 2**  
    > ! [DevTools abre el panel orígenes después de hacer clic en log. js: 2]. [ImageSourceLog]  
    
1.  Vuelva a la consola con uno de los siguientes flujos de trabajo:  
    
    *   Haga clic en la pestaña **consola** .  
    *   Pulse `Control` + `[` \ (Windows \) o `Command` + `[` \ (MacOS \) hasta que el panel de la consola esté en el foco.  
    *   [Abra el menú de comandos][DevToolsCommandMenu], empiece `Console` a escribir, seleccione el comando **Mostrar panel de consola** y, a continuación, presione `Enter` .  
    
1.  Haga clic en el botón **registrar ADVERTENCIA** de la demostración.  `Abandon Hope All Ye Who Enter` se registra en la consola.  Los mensajes con formato como este son advertencias.  
    
    > ##### Imagen 8  
    > La consola después de hacer clic en **Advertencia de registro**  
    > ! [La consola después de hacer clic en ADVERTENCIA de registro] [ImageConsoleLogWarning]  
    
    > [!TIP]
    > Si desea ver el código que causó un mensaje para que se registre de una determinada manera, haga clic en un script \ (como `log.js:12` \) para ver el código que causó el formato del mensaje.  

1.  Haga clic **Expand** ![ en el icono de expandir que hay ][ImageExpandIcon] delante `Abandon Hope All Ye Who Enter` .  DevTools muestra el [seguimiento][WikiStackTrace] de la pila que se dirige a la llamada.  
    
    > ##### Imagen 9  
    > Un seguimiento de pila  
    > ! [Un seguimiento de pila] [ImageStackTrace]  
    
    El seguimiento de la pila le indica que se ha llamado a una función llamada `logWarning` , que a su vez llamó a una función llamada `quoteDante` .  En otras palabras, la llamada que ocurrió en primer lugar se encuentra en la parte inferior del seguimiento de pila.  Puedes registrar los seguimientos de la pila en cualquier momento llamando a `console.trace()` .  

1.  Haga clic en **registrar error**.  Se ha registrado el siguiente mensaje de error: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### Imagen 10  
    > Un mensaje de error  
    > ! [Mensaje de error] [ImageLogError]  
    
1.  Haga clic en **tabla de registro**.  Se graba en la consola una tabla sobre artistas famosos.  
    
    > [!NOTE]
    > La `birthday` columna solo se rellena para una fila.  Consulte el código para averiguar el motivo.
    
    > ##### Imagen 11  
    > Una tabla en la consola  
    > ! [Una tabla en la consola] [ImageConsoleTable]  
    
1.  Haga clic en **grupo de registro**.  Los nombres de las cuatro tortugas famosas y de lucha contra delitos se agrupan debajo de la `Adolescent Irradiated Espionage Tortoises` etiqueta.  
    
    > ##### Imagen 12  
    > Un grupo de mensajes en la consola  
    > ! [Un grupo de mensajes en la consola] [ImageConsoleLogGroup]  
    
1.  Haga clic en **registro personalizado**.  Se graba en la consola un mensaje con un borde rojo y un fondo azul.  
    
    > ##### Imagen 13  
    > Un mensaje con formato personalizado en la consola  
    > ! [Mensaje con formato personalizado en la consola] [ImageConsoleLogCustomFormatting]  
    
La idea principal es que cuando quieras registrar mensajes en la consola desde tu código JavaScript, usas uno de los `console` métodos.  Cada método da formato a los mensajes de forma diferente.  

Hay aún más métodos de los que se han demostrado en esta sección.  En este tutorial se muestra cómo explorar el resto de los métodos.  

## Ver los mensajes registrados por el explorador   

El explorador también registra mensajes en la consola.  Esto suele ocurrir cuando hay un problema con la página.  

1.  Haga clic en **Cause 404**.  El explorador registra un `404` error de red porque el código JavaScript de la página ha intentado buscar un archivo que no existe.  
    
    > ##### Imagen 14  
    > Error 404 en la consola  
    > ! [Error 404 en la consola] [ImageConsoleLogError]  
    
1.  Haga clic en **causa del error**.  El explorador registra una no capturada `TypeError` porque el JavaScript está intentando actualizar un nodo Dom que no existe.  
    
    > ##### Imagen 15  
    > Un TypeError en la consola  
    > ! [Un TypeError en la consola] [ImageConsoleLogTypeError]  
    
1.  Haga clic en la lista desplegable **niveles de registro** y habilite la opción **detallado** si está deshabilitada.  Para obtener más información sobre el filtrado, vaya a la siguiente sección.  Tiene que hacer esto para asegurarse de que el siguiente mensaje que inicie sesión está visible.  
    
    > ##### Imagen 16  
    > Habilitar el nivel de registro **detallado**  
    > ! [Habilitar el nivel de registro detallado] [ImageVerboseLogLevel]  
    
1.  Haga clic en **causa de infracción**.  La página deja de responder durante unos segundos y, a continuación, el explorador registra el mensaje `[Violation] 'click' handler took 3000ms` en la consola.  La duración exacta puede variar.  
    
    > ##### Imagen 17  
    > Violación en la consola  
    > ! [Infracción en la consola] [ImageConsoleLogViolation]  
    
## Filtrar mensajes   

En algunas páginas verás que la consola está inundada de mensajes.  DevTools proporciona varias formas diferentes de filtrar los mensajes que no son relevantes para la tarea que está realizando.  

### Filtrar por nivel de registro   

`console`A cada método se le asigna un nivel de gravedad: `Verbose` ,, `Info` `Warning` o `Error` .  Por ejemplo, `console.log()` es un `Info` mensaje de nivel, mientras que `console.error()` es `Error` un mensaje de nivel.  

1.  Haga clic en la lista desplegable **niveles de registro** y deshabilite **errores**.  Un nivel se deshabilita cuando ya no hay una marca de verificación junto a él.  Los `Error` mensajes de nivel desaparecen.  
    
    > ##### Ilustración 18  
    > Deshabilitar `Error` el nivel de mensajes en la consola  
    > ! [Deshabilitar mensajes de nivel de error en la consola] [ImageConsoleDisablingLogError]  
    
1.  Vuelva a hacer clic en la lista desplegable **niveles de registro** y vuelva a habilitar los **errores**.  Los `Error` mensajes del nivel volverán a aparecer.  

### Filtrar por texto   

Cuando desee ver solo los mensajes que incluyan una cadena exacta, escríbala en el cuadro de texto **filtro** .  

1.  Escriba `Dave` en el cuadro de texto **filtro** .  Todos los mensajes que no incluyan la cadena `Dave` están ocultos.  También puede ver la `Adolescent Irradiated Espionage Tortoises` etiqueta.  Es un error.  
    
    > ##### Ilustración 19  
    > Filtrar cualquier mensaje que no incluya `Dave`  
    > ! [Filtrar cualquier mensaje que no incluya Dave] [ImageLogTextFiltering]  
    
1.  Eliminar `Dave` en el cuadro de texto **filtro** .  Todos los mensajes volverán a aparecer.  

### Filtrar por expresión regular   

Cuando desee mostrar todos los mensajes que incluyan un patrón de texto, en lugar de una cadena específica, use una [expresión regular][MDNRegularExpressions].  

1.  Escriba `/^[AH]/` en el cuadro de texto **filtro** .  Escriba este patrón en [Regex][|::ref1::|Main] para obtener una explicación de lo que está haciendo.  
    
    > ##### Ilustración 20  
    > Filtrar los mensajes que no coincidan con el patrón `/^[AH]/`  
    > ! [Filtrar cualquier mensaje que no coincida con un patrón] [ImageLogRegExFiltering]  
    
1.  Eliminar `/^[AH]/` en el cuadro de texto **filtro** .  Todos los mensajes volverán a verse.  

### Filtrar por origen del mensaje   

Si desea ver solo los mensajes procedentes de una dirección URL determinada, use la **barra lateral**.  

1.  Haga clic en **Mostrar la barra lateral de consola** ![ Mostrar la barra lateral ][ImageShowConsoleSidebarIcon] .  
    
    > ##### Ilustración 21  
    > La barra lateral  
    > ! [Barra lateral] [ImageConsoleSidebar]  
    
1.  Haga clic **en el** ![ icono expandir expandir ][ImageExpandIcon] situado junto al número de mensajes.  En la [figura 21](#figure-21), la cantidad de mensajes se indica como **13 mensajes**.  La **barra lateral** muestra una lista de las direcciones URL que han provocado el registro de mensajes.  Por ejemplo, se `log.js` produjeron 11 mensajes.  
    
    > ##### Ilustración 22  
    > Ver el origen de los mensajes en la barra lateral  
    > ! [Ver el origen de los mensajes en la barra lateral] [ImageConsoleSidebarLogSource]  
    
### Filtrar por mensajes de usuario   

Anteriormente, cuando se hace clic en **información de registro**, se llama a un script para `console.log('Hello, Console!')` registrar el mensaje en la consola.  Los mensajes registrados de JavaScript como este se denominan **mensajes de usuario**.  Por el contrario, cuando hace clic en la **causa 404**, el explorador registra un `Error` mensaje que indica que no se pudo encontrar el recurso solicitado.  Mensajes como los que se consideran **mensajes del explorador**.  Use la **barra lateral** para filtrar los mensajes del explorador y mostrar solo los mensajes de usuario.  

1.  Haga clic en **9 mensajes de usuario**.  Los mensajes del explorador están ocultos.  
    
    > ##### Ilustración 23  
    > Filtrar los mensajes del explorador  
    > ! [Filtrar los mensajes del explorador] [ImageConsoleLogBrowserFiltering]  
    
1.  Haga clic en **13 mensajes** para volver a mostrar todos los mensajes.  

## Usar la consola junto con cualquier otro panel   

¿Qué sucede si está editando estilos, pero necesita consultar rápidamente el registro de consola para buscar algo? Use el cajón.  

1.  Haga clic en la pestaña **elementos** .  
1.  Presione `Escape` .  Se abrirá la ficha Console del **cajón** .  Tiene todas las características del panel de la consola que ha estado usando en este tutorial.  
    
    > ##### Ilustración 24  
    > Ficha de consola en el cajón  
    > ! [Ficha de consola en el cajón] [ImageDrawerConsole]  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Ilustración 1: mensajes en la consola"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-Right-Console.msft.png "Figura 2: DevTools se abre a la derecha de la demostración"  
[ImageDevToolsBottom]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-Bottom-Console.msft.png "Ilustración 3: DevTools acoplado a la parte inferior de la demostración"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-separate-Console-Browse.msft.png "Ilustración 4: explorador en una ventana independiente"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-separate-Console-DevTools.msft.png "Ilustración 5: DevTools desacoplado en una ventana independiente"  
[ImageLogInfo]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-info.msft.png "Ilustración 6: la consola después de hacer clic en información de registro"  
[ImageSourceLog]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-sources-logjs.msft.png "Figura 7: DevTools abre el panel orígenes después de hacer clic en log. js: 2"  
[ImageConsoleLogWarning]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-warning.msft.png "Ilustración 8: la consola después de hacer clic en ADVERTENCIA de registro"  
[ImageStackTrace]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Warning-Expanded.msft.png "Ilustración 9: un seguimiento de la pila"  
[ImageLogError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-error.msft.png "Figura 10: un mensaje de error"  
[ImageConsoleTable]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Table.msft.png "ilustración 11: una tabla en la consola"  
[ImageConsoleLogGroup]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Group.msft.png "Ilustración 12: un grupo de mensajes en la consola"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Custom.msft.png "ilustración 13: un mensaje con formato personalizado en la consola"  
[ImageConsoleLogError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-404.msft.png "Ilustración 14: error 404 en la consola"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-error.msft.png "Figura 15: un TypeError en la consola"  
[ImageVerboseLogLevel]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-error-log-levels.msft.png "Figura 16: habilitar el nivel de registro detallado"  
[ImageConsoleLogViolation]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-Violation.msft.png "Ilustración 17: una infracción en la consola"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-Violation-log-levels.msft.png "ilustración 18: deshabilitar mensajes de nivel de error en la consola"  
[ImageLogTextFiltering]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-All-messages-Text-Filter.msft.png "Ilustración 19: filtrar cualquier mensaje que no incluya Dave"  
[ImageLogRegExFiltering]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-All-messages-regex-Filter.msft.png "figura 20: filtrar los mensajes que no coincidan con un patrón"  
[ImageConsoleSidebar]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-All-messages.msft.png "ilustración 21: la barra lateral"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-Expanded-All-messages.msft.png "Ilustración 22: ver el origen de los mensajes en la barra lateral"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-User-messages.msft.png "Ilustración 23: filtrar los mensajes del explorador"  
[ImageDrawerConsole]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Elements-Drawer-Console-Sidebar-All-messages.msft.png "Ilustración 24: ficha consola en el cajón"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas de desarrollador de Microsoft Edge \ (cromo \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Referencia de consola"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introducción a la creación de mensajes de registro | Intento"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExer"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Seguimiento de la pila-Wikipedia"  


> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/log) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
