---
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 51a85c3dad121dcb42633390de9b4e817074546e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982522"
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

Si busca la referencia de la API en funciones como `console.log()` vea la [referencia de API de consola][DevToolsConsoleApi].  Para obtener la referencia en funciones como `monitorEvents()` , consulte referencia de la [API de utilidades de consola][DevToolsConsoleUtilities].  

## Abrir la consola   

Puede abrir la consola como un [Panel](#open-the-console-panel) o como una [pestaña en el cajón](#open-the-console-tab-in-the-drawer).  

### Abrir el panel de consola   

Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Panel de consola" lightbox="../media/console-hello-console.msft.png":::
   Panel de **consola**  
:::image-end:::  

Para abrir el panel de consola desde el [menú de comandos][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **Panel** al lado.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Comando para mostrar el panel de consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   Comando para mostrar el panel de **consola**  
:::image-end:::  

### Abrir la pestaña consola en el cajón   

Pulse `Escape` o haga clic en **personalizar y controlar DevTools** \ ( `...` \) y, a continuación, seleccione **Mostrar cajón de consola**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar cajón de consola" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Mostrar cajón de consola**  
:::image-end:::  

El cajón aparece en la parte inferior de la ventana de DevTools, con la pestaña **consola** abierto.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Ficha de consola en el cajón" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Ficha de **consola** en el **cajón**  
:::image-end:::  

Para abrir la pestaña consola desde el [menú comando][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **alimentador** al lado.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Comando para mostrar la ficha de consola en el cajón" lightbox="../media/console-command-menu-show-console.msft.png":::
   Comando para mostrar la ficha de **consola** en el **cajón**  
:::image-end:::  

### Abrir configuración de consola   

Haga clic en **configuración de consola** \ ( ![ configuración de consola ][ImageSettingsButtonIcon] \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configuración de la consola" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Configuración de la consola**  
:::image-end:::  

Los vínculos siguientes explican cada configuración:  

*   [**Ocultar red**](#hide-network-messages)  
*   [**Conservar registro**](#persist-messages-across-page-loads)  
*   [**Solo el contexto seleccionado**](#filter-out-messages-from-different-contexts)  
*   [**Grupo similar**](#disable-message-grouping)  
*   [**Registro XmlHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Evaluación diligente**](#disable-eager-evaluation)  
*   [**Autocompletar desde historial**](#disable-autocomplete-from-history)  
    
### Abrir la barra lateral de la consola   

Haga clic en **Mostrar la barra** lateral de consola \ ( ![ Mostrar barra lateral ][ImageShowConsoleSidebarIcon] de consola \) para mostrar la barra lateral, que es útil para filtrar.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra lateral de la consola" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Consola** Laterales  
:::image-end:::  

## Ver mensajes   

Esta sección contiene características que cambian la presentación de los mensajes en la consola.  Vea [Ver mensajes][DevToolsConsoleViewMessages] para obtener un tutorial práctico.  

### Deshabilitar la agrupación de mensajes   

[Abra configuración de consola](#open-console-settings) y deshabilite **grupo similar** para deshabilitar el comportamiento predeterminado de agrupación de mensajes de la consola.  Para obtener un ejemplo [, consulta log XHR y solicitudes fetch](#log-xhr-and-fetch-requests) .  

### Registrar solicitudes de XHR y fetch   

[Abra configuración de consola](#open-console-settings) y habilite **log XMLHttpRequests** para registrar todas las `XMLHttpRequest` solicitudes de `Fetch` la consola a medida que se produzcan.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Registrar solicitudes de recuperación y recuperación" lightbox="../media/console-xhr-fetch.msft.png":::
   Registro `XMLHttpRequest` y `Fetch` solicitudes  
:::image-end:::  
En el mensaje superior de la figura anterior se muestra el comportamiento de agrupación predeterminado de la **consola**.  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### Conservar mensajes en la carga de la página   

De forma predeterminada, la consola se desactiva cada vez que se carga una página nueva.  Para conservar los mensajes en la carga de la página, [abra configuración de consola](#open-console-settings) y active la casilla **conservar registro** .  

### Ocultar mensajes de red   

De forma predeterminada, el explorador registra los mensajes de red en la **consola**.  En la siguiente ilustración, el mensaje seleccionado representa un código de Estado HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un mensaje de 429 en la consola" lightbox="../media/console-show-network.msft.png":::
   Un `429` mensaje en la **consola**  
:::image-end:::  
Para ocultar mensajes de red:  

1.  [Abra configuración de consola](#open-console-settings).  
1.  Active la casilla **ocultar red** .  
    
## Filtrar mensajes   

Existen muchas maneras de filtrar los mensajes en la consola.  

### Filtrar los mensajes del explorador   

[Abra la barra lateral](#open-the-console-sidebar) de la consola y haga clic en **mensajes de usuario** para mostrar solo los mensajes que proceden del JavaScript de la página.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Ver mensajes de usuario" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Ver mensajes de usuario  
:::image-end:::  

### Filtrar por nivel de registro   

DevTools asigna cada `console.*` método a nivel de gravedad.  Hay 4 niveles: `Verbose` ,, `Info` `Warning` y `Error` .  Por ejemplo, `console.log()` se encuentra en el `Info` grupo, mientras que `console.error()` se encuentra en el `Error` grupo.  La [referencia][DevToolsConsoleApi] de la API de consola describe el nivel de gravedad de cada método aplicable.  Cada mensaje que el explorador registra en la consola también tiene un nivel de gravedad.  Puede ocultar cualquier nivel de mensajes que no le interese.  Por ejemplo, si solo le interesan `Error` los mensajes, puede ocultar los otros 3 grupos.  

Haga clic en el menú desplegable **niveles de registro** para habilitar o deshabilitar `Verbose` , `Info` `Warning` o `Error` mensajes.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Lista desplegable de niveles de registro" lightbox="../media/console-log-level-default-levels.msft.png":::
   Lista desplegable de **niveles de registro**  
:::image-end:::  

También puede filtrar por nivel de registro si [abre la barra lateral de la consola](#open-the-console-sidebar) y hace clic en **errores**, **advertencias**, **información**o **detallado**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar la barra lateral para ver las advertencias" lightbox="../media/console-sidebar-warnings.msft.png":::
   Usar la barra lateral para ver las advertencias  
:::image-end:::  

### Filtrar mensajes por dirección URL   

Escriba `url:` seguido de una dirección URL para ver solo los mensajes que proceden de esa dirección URL.  Después de escribir `url:` DevTools, se muestran todas las direcciones URL relevantes.  Los dominios también funcionan.  Por ejemplo, si `https://example.com/a.js` y `https://example.com/b.js` están registrando mensajes, `url:https://example.com` le permite centrarse en los mensajes de estas dos secuencias de comandos.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Un filtro de URL" lightbox="../media/console-filter-text.msft.png":::
   Un filtro de URL  
:::image-end:::  

Escriba `-url:` para ocultar mensajes de esa dirección URL.  Esto se conoce como un filtro de URL negativo.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la https://b.wal.co dirección URL" lightbox="../media/console-negative-filter-text.msft.png":::
   Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la `https://b.wal.co` dirección URL
:::image-end:::  

También puede mostrar los mensajes de una sola dirección URL [abriendo la barra lateral](#open-the-console-sidebar)de la consola, expandiendo la sección de **mensajes de usuario** y, a continuación, haciendo clic en la dirección URL de la secuencia de comandos que contiene los mensajes en los que desea concentrarse.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Ver los mensajes que proceden de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Ver los mensajes procedentes de `wp-ad.min.js`  
:::image-end:::  

### Filtrar mensajes de distintos contextos   

Supongamos que tiene un anuncio \ (ad \) en la página.  El anuncio está insertado en una `<iframe>` y está generando un gran número de mensajes en la consola.  Como AD se está ejecutando en un [contexto de JavaScript](#select-javascript-context)diferente, una forma de ocultar los mensajes es [abrir la configuración de consola](#open-console-settings) y habilitar la casilla de verificación de solo el **contexto seleccionado** .  

### Filtrar mensajes que no coincidan con un modelo de expresión regular   

Escriba una expresión regular, como `/[gm][ta][mi]/` en el cuadro de texto **filtro** , para filtrar los mensajes que no coincidan con ese patrón.  DevTools comprueba si el patrón se encuentra en el texto del mensaje o en la secuencia de comandos que ha provocado el registro del mensaje.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar los mensajes que no coincidan con la expresión Regex" lightbox="../media/console-filter-regex.msft.png":::
   Filtrar los mensajes que no coincidan con la `/[gm][ta][mi]/` expresión Regex  
:::image-end:::  

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
> En la siguiente ilustración, `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se han evaluado anteriormente.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="El mensaje emergente de Autocompletar muestra expresiones del historial" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   El mensaje emergente de Autocompletar muestra expresiones del historial  
:::image-end:::  

### Seleccionar contexto de JavaScript   

De forma predeterminada, la lista desplegable de **contexto de JavaScript** se establece en **Top**, que representa el [contexto de exploración][MDNBrowsingContext] del documento principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Lista desplegable de contexto de JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   Lista desplegable de **contexto de JavaScript**  
:::image-end:::  

Supongamos que tiene un anuncio en la página insertado en una `<iframe>` .  Para poder ajustar el DOM del anuncio, deseas ejecutar JavaScript.  En primer lugar, debe seleccionar el contexto de exploración del anuncio en la lista desplegable de **contexto de JavaScript** .  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Seleccionar un contexto de JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   Seleccionar un contexto de JavaScript diferente  
:::image-end:::  

## Borrar la consola   

Puede usar cualquiera de los siguientes flujos de trabajo para borrar la consola:  

*   Haga clic en **Borrar consola** \ ( ![ Borrar consola ][ImageClearConsoleIcon] \).  
*   Haga clic con el botón derecho en un mensaje y seleccione **Borrar consola**.  
*   Escriba `clear()` la consola y, a continuación, pulse `Enter` .  
*   Llama `console.clear()` desde el JavaScript de tu página web.  
*   Pulsa `Control` + `L` mientras la consola está en el foco.  
    
<!--
 

  
-->  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Ver mensajes registrados-Descripción general de la consola | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de la API de consola | Microsoft docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ejecución de JavaScript-Descripción general de la consola | Microsoft docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo | Microsoft docs"  
[DevToolsConsoleLog]: ./log.md "Introducción a la creación de mensajes de registro en la consola | Microsoft docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referencia de API de utilidades de consola | Microsoft docs"  

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
