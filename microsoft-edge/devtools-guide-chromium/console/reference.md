---
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601791"
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





# Referencia de consola   



Esta página es una referencia de las características relacionadas con la consola de Microsoft Edge DevTools.  Se da por supuesto que ya está familiarizado con el uso de la consola para ver mensajes registrados y ejecutar JavaScript.  Si no es así, vea empezar [a ejecutar JavaScript en la consola][DevToolsConsoleJavascript] y empezar [a registrar mensajes en la consola][DevToolsConsoleLog].  

Si busca la referencia de la API en funciones como `console.log()` vea la [referencia de API de consola][DevToolsConsoleApi].  Para consultar la referencia en funciones como, consulte la referencia de la `monitorEvents()` API de [utilidades de consola][DevToolsConsoleUtilities].  

## Abrir la consola   

Puede abrir la consola como un [Panel](#open-the-console-panel) o como una [pestaña en el cajón](#open-the-console-tab-in-the-drawer).  

### Abrir el panel de consola   

Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  

> ##### Figura 1  
> Panel de consola  
> ![Panel de consola][ImageConsolePanel]  

Para abrir el panel de consola desde el [menú de comandos][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **Panel** al lado.  

> ##### Figura 2  
> Comando para mostrar el panel de consola  
> ![Comando para mostrar el panel de consola][ImageCommandShowConsole]  

### Abrir la pestaña consola en el cajón   

Pulse `Escape` o haga clic en **personalizar y controlar DevTools** `...` y, a continuación, seleccione **Mostrar cajón de consola**.  

> ##### Imagen 3  
> Mostrar cajón de consola  
> ![Mostrar cajón de consola][ImageShowConsoleDrawer]  

El cajón aparece en la parte inferior de la ventana de DevTools, con la pestaña **consola** abierto.  

> ##### Imagen 4  
> Ficha de consola en el cajón  
> ![Ficha de consola en el cajón][ImageDrawerConsole]  

Para abrir la pestaña consola desde el [menú comando][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **alimentador** al lado.  

> ##### Imagen 5  
> Comando para mostrar la ficha de consola en el cajón  
> ![Comando para mostrar la ficha de consola en el cajón][ImageShowDrawerCommand]  

### Abrir configuración de consola   

Haga clic en configuración de consola de **configuración** ![ ][ImageSettingsButtonIcon] .  

> ##### Imagen 6  
> Configuración de la consola  
> ![Configuración de la consola][ImageConsoleSettings]  

Los vínculos siguientes explican cada configuración:  

*   [**Ocultar red**](#hide-network-messages)  
*   [**Conservar registro**](#persist-messages-across-page-loads)  
*   [**Solo el contexto seleccionado**](#filter-out-messages-from-different-contexts)  
*   [**Grupo similar**](#disable-message-grouping)  
*   [**Registro XmlHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Evaluación diligente**](#disable-eager-evaluation)  
*   [**Autocompletar desde historial**](#disable-autocomplete-from-history)  

### Abrir la barra lateral de la consola   

Haga clic en **Mostrar** la barra lateral de consola para mostrar la barra lateral ![ ][ImageShowConsoleSidebarIcon] , que es útil para filtrar.  

> ##### Imagen 7  
> Barra lateral de la consola  
> ![Barra lateral de la consola][ImageConsoleSidebar]  

## Ver mensajes   

Esta sección contiene características que cambian la presentación de los mensajes en la consola.  Vea [Ver mensajes][DevToolsConsoleViewMessages] para obtener un tutorial práctico.  

### Deshabilitar la agrupación de mensajes   

[Abra configuración de consola](#open-console-settings) y deshabilite **grupo similar** para deshabilitar el comportamiento predeterminado de agrupación de mensajes de la consola.  Para obtener un ejemplo [, consulta log XHR y solicitudes fetch](#log-xhr-and-fetch-requests) .  

### Registrar solicitudes de XHR y fetch   

[Abra configuración de consola](#open-console-settings) y habilite **log XMLHttpRequests** para registrar todas las `XMLHttpRequest` solicitudes de `Fetch` la consola a medida que se produzcan.  

> ##### Imagen 8  
> Registro `XMLHttpRequest` y `Fetch` solicitudes  
> ![Registro de solicitudes de XMLHttpRequest y fetch][ImageXhrGrouped]  

El mensaje superior de la [ilustración 8](#figure-8) muestra el comportamiento de agrupación predeterminado de la consola.  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### Conservar mensajes en la carga de la página   

De forma predeterminada, la consola se desactiva cada vez que se carga una página nueva.  Para conservar los mensajes en la carga de la página, [abra configuración de consola](#open-console-settings) y active la casilla **conservar registro** .  

### Ocultar mensajes de red   

De forma predeterminada, el explorador registra los mensajes de red en la **consola**.  Por ejemplo, el mensaje seleccionado en la [figura 9](#figure-9) representa un código de estado de `429` .  

> ##### Imagen 9  
> Un mensaje de 429 en la consola  
> ! [Un mensaje de 429 en la consola] [Image429Message]  

Para ocultar mensajes de red:  

1.  [Abra configuración de consola](#open-console-settings).  
1.  Active la casilla **ocultar red** .  

## Filtrar mensajes   

Existen muchas maneras de filtrar los mensajes en la consola.  

### Filtrar los mensajes del explorador   

[Abra la barra lateral](#open-the-console-sidebar) de la consola y haga clic en **mensajes de usuario** para mostrar solo los mensajes que proceden del JavaScript de la página.  

> ##### Imagen 10  
> Ver mensajes de usuario  
> ! [Visualización de mensajes de usuario] [ImageUserMessages]  

### Filtrar por nivel de registro   

DevTools asigna cada `console.*` método a nivel de gravedad.  Hay 4 niveles: `Verbose` ,, `Info` `Warning` y `Error` .  Por ejemplo, `console.log()` se encuentra en el `Info` grupo, mientras que `console.error()` se encuentra en el `Error` grupo.  La [referencia][DevToolsConsoleApi] de la API de consola describe el nivel de gravedad de cada método aplicable.  Cada mensaje que el explorador registra en la consola también tiene un nivel de gravedad.  Puede ocultar cualquier nivel de mensajes que no le interese.  Por ejemplo, si solo le interesan `Error` los mensajes, puede ocultar los otros 3 grupos.  

Haga clic en el menú desplegable **niveles de registro** para habilitar o deshabilitar `Verbose` , `Info` `Warning` o `Error` mensajes.  

> ##### Imagen 11  
> Lista desplegable de **niveles de registro**  
> ! [La lista desplegable de niveles de registro] [ImageLogLevels]  

También puede filtrar por nivel de registro si [abre la barra lateral de la consola](#open-the-console-sidebar) y hace clic en **errores**, **advertencias**, **información**o **detallado**.  

> ##### Imagen 12  
> Uso de la barra lateral para ver las advertencias  
> ! [Uso de la barra lateral para ver las advertencias] [ImageSidebarWarnings]  

### Filtrar mensajes por dirección URL   

Escriba `url:` seguido de una dirección URL para ver solo los mensajes que proceden de esa dirección URL.  Después de escribir `url:` DevTools, se muestran todas las direcciones URL relevantes.  Los dominios también funcionan.  Por ejemplo, si `https://example.com/a.js` y `https://example.com/b.js` están registrando mensajes, `url:https://example.com` le permite centrarse en los mensajes de estas dos secuencias de comandos.  

> ##### Imagen 13  
> Un filtro de URL  
> ! [Un filtro de URL] [ImageUrlFilter]  

Escriba `-url:` para ocultar mensajes de esa dirección URL.  Esto se conoce como un filtro de URL negativo.  

> ##### Imagen 14  
> Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la dirección URL `https://b.wal.co`  
> ! [Un filtro de URL negativo que oculta todos los mensajes que coinciden con la URL https://b.wal.co ] [ImageNegativeUrlFilter1]  

También puede mostrar los mensajes de una sola dirección URL [abriendo la barra lateral](#open-the-console-sidebar)de la consola, expandiendo la sección de **mensajes de usuario** y, a continuación, haciendo clic en la dirección URL de la secuencia de comandos que contiene los mensajes en los que desea concentrarse.  

> ##### Imagen 15  
> Ver los mensajes procedentes de `wp-ad.min.js`  
> ! [Viendo los mensajes que proceden de WP-ad. min. js] [ImageNegativeUrlFilter2]  

### Filtrar mensajes de distintos contextos   

Supongamos que tiene un anuncio \ (ad \) en la página.  El anuncio está insertado en una `<iframe>` y está generando un gran número de mensajes en la consola.  Como AD se está ejecutando en un [contexto de JavaScript](#select-javascript-context)diferente, una forma de ocultar los mensajes es [abrir la configuración de consola](#open-console-settings) y habilitar la casilla de verificación de solo el **contexto seleccionado** .  

### Filtrar mensajes que no coincidan con un modelo de expresión regular   

Escriba una expresión regular, como `/[gm][ta][mi]/` en el cuadro de texto **filtro** , para filtrar los mensajes que no coincidan con ese patrón.  DevTools comprueba si el patrón se encuentra en el texto del mensaje o en la secuencia de comandos que ha provocado el registro del mensaje.  

> ##### Imagen 16  
> Filtrar los mensajes que no coincidan `/[gm][ta][mi]/`  
> ! [Filtrar los mensajes que no coincidan con la expresión regex] [ImageRegExFilter]  

## Ejecutar JavaScript   

Esta sección contiene características relacionadas con la ejecución de JavaScript en la consola.  Consulte [ejecutar JavaScript][DevToolsConsoleOverviewJavascript] para obtener un tutorial práctico.  

### Volver a ejecutar expresiones del historial   

Presione la `Up Arrow` tecla para recorrer el historial de expresiones de JavaScript que ejecutó anteriormente en la consola.  Pulse `Enter` para volver a ejecutar la expresión.  

### Ver el valor de una expresión en tiempo real con expresiones en directo   

Si se encuentra escribiendo la misma expresión de JavaScript en la consola varias veces, es posible que le resulte más fácil crear una **expresión en vivo**.  Con **expresiones en vivo** , escriba una expresión una vez y, a continuación, ancle en la parte superior de la consola.  El valor de la expresión se actualiza casi en tiempo real.  Vea [inspeccionar valores de expresiones de JavaScript en tiempo real con expresiones en directo][DevToolsConsoleLiveExpressions].  

### Deshabilitar evaluación diligente   

Mientras escribe las expresiones de JavaScript en la consola, **evaluación diligente** muestra una vista previa del valor devuelto para esa expresión.  [Abra configuración de consola](#open-console-settings) y deshabilite la casilla **evaluación diligente** para desactivar las vistas previas de valor devuelto.  

### Deshabilitar Autocompletar desde historial   

A medida que escribe una expresión, la ventana emergente de autocompletar de la consola muestra expresiones que ejecutó anteriormente.  Estas expresiones van precedidas del `>` carácter.  [Abra configuración de consola](#open-console-settings) y deshabilite la casilla **Autocompletar del historial** para dejar de mostrar las expresiones de su historial.  

> [!NOTE]
> En la [figura 17](#figure-17), `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se han evaluado anteriormente.  

> ##### Imagen 17  
> Elemento emergente de autocompletar que muestra expresiones del historial  
> ! [El elemento emergente de Autocompletar muestra expresiones del historial] [ImageHistoryAutocomplete]  

### Seleccionar contexto de JavaScript   

De forma predeterminada, la lista desplegable de **contexto de JavaScript** se establece en **Top**, que representa el [contexto de exploración][MDNBrowsingContext] del documento principal.  

> ##### Ilustración 18  
> Lista desplegable de **contexto de JavaScript**  
> ! [La lista desplegable de contexto de JavaScript] [ImageJavascriptContext]  

Supongamos que tiene un anuncio en la página insertado en una `<iframe>` .  Para poder ajustar el DOM del anuncio, deseas ejecutar JavaScript.  En primer lugar, debe seleccionar el contexto de exploración del anuncio en la lista desplegable de **contexto de JavaScript** .  

> ##### Ilustración 19  
> Selección de un contexto de JavaScript diferente  
> ! [Seleccionando un contexto de JavaScript diferente] [ImageSelectContext]  

## Borrar la consola   

Puede usar cualquiera de los siguientes flujos de trabajo para borrar la consola:  

*   Haga clic en **Borrar** consola ![ Borrar consola ][ImageClearConsoleIcon] .  
*   Haga clic con el botón derecho en un mensaje y seleccione **Borrar consola**.  
*   Escriba `clear()` la consola y, a continuación, pulse `Enter` .  
*   Llama `console.clear()` desde el JavaScript de tu página web.  
*   Pulsa `Control` + `L` mientras la consola está en el foco.  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Ilustración 1: panel de consola"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Ilustración 2: el comando para mostrar el panel de la consola"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Ilustración 3: mostrar el cajón de consola"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Ilustración 4: la pestaña de consola en el cajón"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Ilustración 5: el comando para mostrar la pestaña de consola en el cajón"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Ilustración 6: configuración de la consola"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Ilustración 7: barra lateral de la consola"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Ilustración 8: registro de solicitudes de XMLHttpRequest y fetch"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Show-Network.msft.png "Ilustración 9: un mensaje de 429 en la consola"  
[ImageUserMessages]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-Drawer-User-messages.msft.png "Ilustración 10: ver mensajes de usuario"  
[ImageLogLevels]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-LEVEL-default-levels.msft.png "ilustración 11: la lista desplegable de niveles de registro"  
[ImageSidebarWarnings]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-Warnings.msft.png "Ilustración 12: usar la barra lateral para ver las advertencias"  
[ImageUrlFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Text.msft.png "ilustración 13: un filtro de dirección URL"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-negative-Filter-Text.msft.png "Ilustración 14: un filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la dirección URL https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Text-Specified.msft.png "Ilustración 15: ver los mensajes procedentes de WP-ad. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Regex.msft.png "Ilustración 16: filtrar los mensajes que no coincidan con la expresión regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Text-AutoFilter-History.msft.png "Ilustración 17: el elemento emergente de Autocompletar muestra las expresiones del historial"  
[ImageJavascriptContext]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-DOM-Level-Top.msft.png "ilustración 18: la lista desplegable de contexto de JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-DOM-Level-Multiple.msft.png "Ilustración 19: seleccionar un contexto de JavaScript diferente"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Ver mensajes registrados-Descripción general de la consola"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "Ejecución de JavaScript-Introducción a la consola"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Introducción a la ejecución de JavaScript en la consola"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de API de utilidades de consola"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de exploración | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
