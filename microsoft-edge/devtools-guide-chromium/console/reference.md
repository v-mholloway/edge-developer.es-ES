---
description: Una referencia completa sobre todas las características y comportamientos relacionados con la interfaz de usuario de consola en Microsoft Edge DevTools.
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399165"
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

# <a name="console-reference"></a>Referencia de consola  

Esta página es una referencia de las características relacionadas con la consola DevTools de Microsoft Edge.  Se supone que ya está familiarizado con el uso de la consola para ver los mensajes registrados y ejecutar JavaScript.  Si no es así, vaya a Introducción a la ejecución [de JavaScript en][DevToolsConsoleJavascript] la consola y Empezar a registrar [mensajes en la consola][DevToolsConsoleLog].  

Si está buscando la referencia de API en funciones como `console.log()` , vaya a Referencia de api de [consola][DevToolsConsoleApi].  Para obtener la referencia de funciones como `monitorEvents()` , vaya a Console Utilities API [Reference][DevToolsConsoleUtilities].  

## <a name="open-the-console"></a>Abrir la consola  

Puede abrir la consola **como** una herramienta [en el panel superior](#open-the-console-tool) o como una herramienta en el [cajón](#open-the-console-tool-in-the-drawer).  

### <a name="open-the-console-tool"></a>Abrir la herramienta Consola  

Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="La herramienta Consola" lightbox="../media/console-hello-console.msft.png":::
   La **herramienta Consola**  
:::image-end:::  

Para abrir la **herramienta Consola** desde [el][DevToolsCommandMenu]menú comando, empiece a escribir y, a continuación, ejecute el comando Mostrar consola que tiene el `Console` distintivo **Panel** junto a él. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="El comando para mostrar el panel Consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   El comando para mostrar la **herramienta Consola**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Abrir la herramienta Consola en el cajón  

Seleccione `Escape` o elija Personalizar y controlar **DevTools** \( \) y, a continuación, `...` elija Mostrar **cajón de consola**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar el cajón de la consola" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Mostrar el cajón de la consola**  
:::image-end:::  

El cajón aparece en la parte inferior de la ventana DevTools, con la **herramienta Consola** abierta.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="La herramienta Consola en el cajón" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   La **herramienta Consola** en el **cajón**  
:::image-end:::  

Para abrir la **herramienta Consola** desde [el][DevToolsCommandMenu]menú comando, empiece a escribir y, a continuación, ejecute el comando Mostrar consola que tiene el distintivo `Console` **De** cajón junto **** a él.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="El comando para mostrar la herramienta **Consola** en el cajón" lightbox="../media/console-command-menu-show-console.msft.png":::
   El comando para mostrar la **herramienta Consola** en el **cajón**  
:::image-end:::  

### <a name="open-console-settings"></a>Abrir configuración de consola  

Elija **Configuración de consola** \( Icono configuración de consola ![ ][ImageSettingsButtonIcon] \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configuración de consola" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Configuración de consola**  
:::image-end:::  

Los vínculos siguientes explican cada configuración:  

*   [**Ocultar red**](#hide-network-messages)  
*   [**Conservar registro**](#persist-messages-across-page-loads)  
*   [**Solo contexto seleccionado**](#filter-out-messages-from-different-contexts)  
*   [**Group Similar**](#disable-message-grouping)  
*   [**Log XmlHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Evaluación ansiosa**](#disable-eager-evaluation)  
*   [**Autocompletar desde el historial**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a>Abrir la barra lateral de la consola  

Elija **Mostrar barra lateral de consola** \( Mostrar barra lateral de consola \) para mostrar la barra ![ ][ImageShowConsoleSidebarIcon] lateral, que es útil para filtrar.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra lateral de consola" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Consola** Barra lateral  
:::image-end:::  

## <a name="view-messages"></a>Ver mensajes  

Esta sección contiene características que cambian la forma en que se presentan los mensajes en la consola.  Para obtener un tutorial práctica, vaya a [Ver mensajes][DevToolsConsoleViewMessages].  

### <a name="disable-message-grouping"></a>Deshabilitar la agrupación de mensajes  

[Abra Configuración de la](#open-console-settings) consola y deshabilite **Grupo de forma similar** para deshabilitar el comportamiento de agrupación de mensajes predeterminado de la consola.  Para obtener un ejemplo, vaya [a Registrar XHR y Obtener solicitudes](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Registrar solicitudes XHR y Fetch  

[Abra Configuración de la](#open-console-settings) consola y **habilite Log XMLHttpRequests** para registrar todas y solicitudes `XMLHttpRequest` en la consola a medida que se `Fetch` suceden.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Registrar solicitudes XMLHttpRequest y Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   Registro `XMLHttpRequest` y `Fetch` solicitudes  
:::image-end:::  
El mensaje superior de la figura anterior muestra el comportamiento de agrupación predeterminado de la **consola**.  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Conservar mensajes entre cargas de página  

De forma predeterminada, la consola borra cada vez que se carga una página nueva.  Para conservar los mensajes en las cargas de página, [abra configuración de consola](#open-console-settings) y, a continuación, habilite la casilla **Conservar** registro.  

### <a name="hide-network-messages"></a>Ocultar mensajes de red  

De forma predeterminada, el explorador registra los mensajes de red en la **consola**.  En la siguiente figura, el mensaje seleccionado representa un código de estado HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un mensaje 429 en la consola" lightbox="../media/console-show-network.msft.png":::
   Un `429` mensaje en la **consola**  
:::image-end:::  
Para ocultar mensajes de red:  

1.  [Abra Configuración de la consola](#open-console-settings).  
1.  Active la casilla **Ocultar red.**  
    
## <a name="filter-messages"></a>Filtrar mensajes  

Hay muchas maneras de filtrar los mensajes en la consola.  

### <a name="filter-out-browser-messages"></a>Filtrar mensajes del explorador  

[Abra la barra lateral de la](#open-the-console-sidebar) consola y elija Mensajes de **usuario** para mostrar solo los mensajes que provenían del JavaScript de la página.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Ver mensajes de usuario" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Ver mensajes de usuario  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtrar por nivel de registro  

DevTools asigna a cada `console.*` método un nivel de gravedad.  Hay 4 niveles: `Verbose` , `Info` , y `Warning` `Error` .  Por ejemplo, `console.log()` está en el `Info` grupo, mientras que está en el `console.error()` `Error` grupo.  La [referencia de la API de][DevToolsConsoleApi] consola describe el nivel de gravedad de cada método aplicable.  Cada mensaje que el explorador inicia sesión en la consola también tiene un nivel de gravedad.  Puede ocultar cualquier nivel de mensajes que no le interesen.  Por ejemplo, si solo está interesado en los `Error` mensajes, puede ocultar los otros 3 grupos.  

Elija el **desplegable Niveles de registro** para habilitar o deshabilitar , o `Verbose` `Info` `Warning` `Error` mensajes.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Desplegable Niveles de registro" lightbox="../media/console-log-level-default-levels.msft.png":::
   Desplegable **Niveles de** registro  
:::image-end:::  

También puede filtrar por [](#open-the-console-sidebar) nivel de registro abriendo la barra lateral de la consola y, a continuación, haciendo clic en **Errores,** **Advertencias,** **Información**o **Verbose**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar la barra lateral para ver advertencias" lightbox="../media/console-sidebar-warnings.msft.png":::
   Usar la barra lateral para ver advertencias  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtrar mensajes por dirección URL  

Escriba `url:` seguido de una dirección URL para ver solo los mensajes que provenían de esa dirección URL.  Después de escribir `url:` DevTools, se muestran todas las direcciones URL relevantes.  Los dominios también funcionan.  Por ejemplo, si `https://example.com/a.js` y `https://example.com/b.js` están registrando mensajes, le permite `url:https://example.com` centrarse en los mensajes de estos 2 scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Un filtro de dirección URL" lightbox="../media/console-filter-text.msft.png":::
   Un filtro de dirección URL  
:::image-end:::  

Escriba `-url:` para ocultar mensajes de esa dirección URL.  Esto se denomina filtro de dirección URL negativa.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la https://b.wal.co dirección URL" lightbox="../media/console-negative-filter-text.msft.png":::
   Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la `https://b.wal.co` dirección URL
:::image-end:::  

También puede mostrar mensajes de una sola dirección URL **** abriendo la barra lateral de [consola,](#open-the-console-sidebar)expandiendo la sección Mensajes de usuario y, a continuación, haciendo clic en la dirección URL del script que contiene los mensajes en los que desea centrarse.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Ver los mensajes procedentes de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Ver los mensajes procedentes `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtrar mensajes de distintos contextos  

Suponga que tiene un anuncio \(ad\) en su página.  El anuncio está incrustado en un y está generando una gran cantidad `<iframe>` de mensajes en la consola.  Dado que el anuncio se ejecuta en un contexto de [](#open-console-settings) [JavaScript](#select-javascript-context)diferente, una forma de ocultar los mensajes es abrir la configuración de consola y activar la casilla **Solo contexto** seleccionado.  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a>Filtrar mensajes que no coinciden con un patrón de expresión regular  

Escriba una expresión regular como, por ejemplo, en el cuadro de texto Filtrar para filtrar los mensajes que no `/[gm][ta][mi]/` coincidan con ese patrón. ****  DevTools comprueba si el patrón se encuentra en el texto del mensaje o en el script que hizo que se registrara el mensaje.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar los mensajes que no coincidan con la expresión regex" lightbox="../media/console-filter-regex.msft.png":::
   Filtrar los mensajes que no coincidan con la `/[gm][ta][mi]/` expresión regex  
:::image-end:::  

## <a name="run-javascript"></a>Ejecutar JavaScript  

Esta sección contiene características relacionadas con la ejecución de JavaScript en la consola.  Para obtener un tutorial práctica, vaya a [Ejecutar JavaScript][DevToolsConsoleOverviewJavascript].  

### <a name="re-run-expressions-from-history"></a>Volver a ejecutar expresiones del historial  

Seleccione la `Up Arrow` clave para recorrer el historial de expresiones de JavaScript que ejecutó anteriormente en la consola.  Seleccione `Enter` para ejecutar esa expresión de nuevo.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Ver el valor de una expresión en tiempo real con live expressions  

Si se encuentra escribiendo la misma expresión de JavaScript en la consola repetidamente, es posible que le resulte más fácil crear **una expresión live**.  Con **Live Expressions,** escribe una expresión una vez y, a continuación, anclarla a la parte superior de la consola.  El valor de la expresión se actualiza casi en tiempo real.  Vaya a [Ver valores de expresión de JavaScript en Real-Time Con expresiones en directo][DevToolsConsoleLiveExpressions].  

### <a name="disable-eager-evaluation"></a>Deshabilitar la evaluación de Eager  

Al escribir expresiones de JavaScript en la consola, La evaluación **ansiosa** muestra una vista previa del valor devuelto para esa expresión.  [Abra Configuración de la](#open-console-settings) consola y deshabilite la casilla **Evaluación** ansiosa para desactivar las vistas previas del valor devuelto.  

### <a name="disable-autocomplete-from-history"></a>Deshabilitar la autocompletar del historial  

Al escribir una expresión, la ventana emergente autocompletar de la consola muestra las expresiones que ejecutó anteriormente.  Estas expresiones se anteponen al `>` carácter.  [Abra Configuración de consola](#open-console-settings) y deshabilite la casilla **Autocompletar desde el historial** para dejar de mostrar expresiones de su historial.  

> [!NOTE]
> En la siguiente figura, `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se evaluaron anteriormente.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="El elemento emergente autocompletar muestra expresiones del historial" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   El elemento emergente autocompletar muestra expresiones del historial  
:::image-end:::  

### <a name="select-javascript-context"></a>Seleccionar contexto de JavaScript  

De forma predeterminada, el desplegable Contexto de **JavaScript** se establece en **la parte**superior, que representa el contexto [de exploración][MDNBrowsingContext] del documento principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Desplegable Contexto de JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   Desplegable **Contexto de JavaScript**  
:::image-end:::  

Supongamos que tienes un anuncio en tu página incrustado en un `<iframe>` .  Quieres ejecutar JavaScript para ajustar el DOM del anuncio.  Primero debes seleccionar el contexto de exploración del anuncio en el desplegable **Contexto de JavaScript.**  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Elegir un contexto de JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   Elegir un contexto de JavaScript diferente  
:::image-end:::  

## <a name="clear-the-console"></a>Borrar la consola  

Puede usar cualquiera de los siguientes flujos de trabajo para borrar la consola:  

*   Elija **Borrar consola** \( Borrar consola ![ ][ImageClearConsoleIcon] \).  
*   Mantenga el mouse sobre un mensaje, abra el menú contextual \(righ-click\) y elija **Borrar consola**.  
*   Escriba `clear()` en la **Consola** y seleccione `Enter` .  
*   Ejecute `console.clear()` desde JavaScript para la página web.  
*   Seleccione `Control` + `L` mientras la **consola** está en foco.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Visualización de mensajes registrados: información general de la consola | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ejecución de JavaScript: información general de la consola | Microsoft Docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft Docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Ver valores de expresión de JavaScript en tiempo real con Live Expressions | Microsoft Docs"  
[DevToolsConsoleLog]: ./log.md "Introducción al registro de mensajes en la consola | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de exploración | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
