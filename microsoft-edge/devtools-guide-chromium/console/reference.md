---
description: Una referencia completa para cada característica y comportamiento de la interfaz de usuario de consola en Microsoft Edge DevTools.
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 3d823be96365b3e7ef75cbfa87068c7207a59c930af5b2364b2a032a294ba752
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803558"
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

Este artículo es una referencia de las características relacionadas con la Microsoft Edge DevTools Console.  Se supone que ya está familiarizado con el uso de la consola para ver los mensajes registrados y ejecutar JavaScript.  Si no es así, vaya a Introducción a la ejecución de [JavaScript en][DevtoolsConsoleConsoleJavascript] la consola y Empezar a registrar [mensajes en la consola][DevtoolsConsoleConsoleLog].  

Si está buscando la referencia de api en funciones como , vaya a `console.log()` Referencia de api de [consola][DevToolsConsoleApi].  Para obtener la referencia de funciones como `monitorEvents()` , vaya a Console Utilities API [Reference][DevToolsConsoleUtilities].  

## <a name="open-the-console"></a>Abrir la consola  

Puede abrir la consola **como** una herramienta [en el panel superior](#open-the-console-tool) o como una herramienta en el [cajón](#open-the-console-tool-in-the-drawer).  

### <a name="open-the-console-tool"></a>Abrir la herramienta Consola  

Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="La herramienta Consola" lightbox="../media/console-hello-console.msft.png":::
   La **herramienta Consola**  
:::image-end:::  

Para abrir la **herramienta Consola** desde [el][DevtoolsCommandMenuIndex]menú comando , escriba y, a continuación, ejecute el comando Mostrar consola que tiene el `Console` distintivo **Panel** junto a él. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Ejecute el comando para mostrar la herramienta Consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   Ejecute el comando para mostrar la **herramienta Consola**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Abrir la herramienta Consola en el cajón  

Seleccione `Esc` o elija Personalizar y controlar **DevTools** \( \) y, a continuación, `...` elija Mostrar **cajón de consola**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar el cajón de la consola" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Mostrar el cajón de la consola**  
:::image-end:::  

El cajón aparece en la parte inferior de la ventana DevTools, con la **herramienta Consola** abierta.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="La herramienta Consola en el cajón" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   La **herramienta Consola** en el **cajón**  
:::image-end:::  

Para abrir la **herramienta Consola** desde el menú [comando][DevtoolsCommandMenuIndex], escriba y, a continuación, ejecute el comando Mostrar consola que tiene el distintivo `Console` **De** cajón junto a él. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Ejecute el comando para mostrar la herramienta **Consola** en el cajón" lightbox="../media/console-command-menu-show-console.msft.png":::
   Ejecutar el comando para mostrar la **herramienta Consola** en el **cajón**  
:::image-end:::  

### <a name="open-console-settings"></a>Abra la consola Configuración  

Elija el **botón Consola Configuración** \( Icono de Configuración ![ ](../media/settings-button-icon.msft.png) \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Consola Configuración" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Consola Configuración**  
:::image-end:::  

Los vínculos siguientes explican cada configuración.  

*   [Ocultar red](#hide-network-messages)  
*   [Conservar registro](#persist-messages-across-page-loads)  
*   [Solo contexto seleccionado](#filter-out-messages-from-different-contexts)  
*   [Grupo similar](#turn-off-message-grouping)  
*   [XML de registroHttpRequests](#log-xhr-and-fetch-requests)  
*   [Evaluación ansiosa](#turn-off-eager-evaluation)  
*   [Autocompletar del historial](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a>Abrir la barra lateral de la consola  

Para mostrar la **barra lateral,** elija **Mostrar barra lateral de la** consola \( Mostrar barra lateral de la consola ![ ](../media/show-console-sidebar-icon.msft.png) \).  La **barra** lateral le ayuda a filtrar.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra lateral de consola" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Barra lateral de consola**  
:::image-end:::  

## <a name="view-messages"></a>Ver mensajes  

Esta sección contiene características que cambian la forma en que se presentan los mensajes en la consola.  Para obtener un tutorial práctica, vaya a [Ver mensajes][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].  

### <a name="turn-off-message-grouping"></a>Desactivar la agrupación de mensajes  

Para desactivar el comportamiento de agrupación de mensajes predeterminado de la **consola,** [abra consola Configuración](#open-console-settings) y elija la casilla junto a Grupo **similar**.  Para obtener un ejemplo, vaya [a Registrar XHR y Obtener solicitudes](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Registrar solicitudes XHR y Fetch  

Para registrar todas las solicitudes y todas en la consola a medida que se produce cada una de ellas, abra console Configuración y seleccione la casilla situada junto a `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**. **** [](#open-console-settings)  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Registrar solicitudes XMLHttpRequest y Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   Registro `XMLHttpRequest` y `Fetch` solicitudes  
:::image-end:::  

El mensaje superior de la figura anterior muestra el comportamiento de agrupación predeterminado de la **consola**.  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Conservar mensajes entre cargas de página  

Al cargar una nueva página web, la acción predeterminada borra la **consola**.  Para conservar los mensajes en las cargas de página, [abra Configuración](#open-console-settings) consola y seleccione la casilla situada junto a **Conservar registro**.  

### <a name="hide-network-messages"></a>Ocultar mensajes de red  

La acción predeterminada para Microsoft Edge es registra los mensajes de red en la **consola**.  En la siguiente figura, el mensaje elegido representa un código de estado HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un mensaje 429 en la consola" lightbox="../media/console-show-network.msft.png":::
   Un `429` mensaje en la **consola**  
:::image-end:::  

Para ocultar los mensajes de red, realice las siguientes acciones.  

1.  [Abra la consola Configuración](#open-console-settings).  
1.  Seleccione la casilla situada junto a **Ocultar red**.  
    
## <a name="filter-messages"></a>Filtrar mensajes  

Existen muchas formas de filtrar los mensajes en la **consola**.  

### <a name="filter-out-browser-messages"></a>Filtrar mensajes del explorador  

[Abra la barra lateral de la](#open-the-console-sidebar) consola y elija # mensajes de **usuario** para mostrar solo los mensajes que provenían del JavaScript de la página web.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Mostrar mensajes de usuario" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Mostrar mensajes de usuario  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtrar por nivel de registro  

DevTools asigna a cada `console.*` método uno de los cuatro niveles de gravedad.  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
Por ejemplo, `console.log()` está en el `Info` grupo, pero está en el `console.error()` `Error` grupo.  La [referencia de la API de][DevToolsConsoleApi] consola describe el nivel de gravedad de cada método aplicable.  Cada mensaje que el explorador inicia sesión en la consola también tiene un nivel de gravedad.  Puede ocultar cualquier nivel de mensajes que no le interesen.  Por ejemplo, si solo está interesado en los `Error` mensajes, puede ocultar los otros tres grupos.  

Para filtrar los mensajes, elija el desplegable **Niveles de** registro y `Verbose` elija , , o `Info` `Warning` `Error` .  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Desplegable Niveles de registro" lightbox="../media/console-log-level-default-levels.msft.png":::
   Desplegable **Niveles de** registro  
:::image-end:::  

Para usar el nivel de registro para filtrar, [abra](#open-the-console-sidebar) la barra lateral de la consola y, a continuación, elija **Errores**, **Advertencias,** **Información**o **Detallado**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar la barra lateral para ver advertencias" lightbox="../media/console-sidebar-warnings.msft.png":::
   Usar la barra lateral para ver advertencias  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtrar mensajes por dirección URL  

Escriba `url:` seguido de una dirección URL para ver solo los mensajes que provenían de esa dirección URL.  Después de escribir `url:` , DevTools muestra todas las direcciones URL relevantes.  Los dominios también funcionan.  Por ejemplo, si y están registrando mensajes, le permite `https://example.com/a.js` `https://example.com/b.js` `url:https://example.com` centrarse en los mensajes de estos dos scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Un filtro de dirección URL" lightbox="../media/console-filter-text.msft.png":::
   Un filtro de dirección URL  
:::image-end:::  

Para ocultar mensajes de una dirección URL, escriba `-url:` .  Es un filtro de dirección URL negativo.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la https://b.wal.co dirección URL" lightbox="../media/console-negative-filter-text.msft.png":::
   Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la `https://b.wal.co` dirección URL
:::image-end:::  

Para mostrar mensajes desde una única dirección URL, complete las siguientes acciones.  

1.  [Abra la barra lateral de la consola](#open-the-console-sidebar).  
1.  Expanda la **sección # mensajes de** usuario.  
1.  Elija la dirección URL del script que contiene los mensajes en los que desea centrarse.  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Mostrar los mensajes que provenían de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Mostrar los mensajes procedentes de `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtrar mensajes de distintos contextos  

Suponga que tiene un anuncio \(ad\) en su página web.  El anuncio está incrustado en un `<iframe>` y genera muchos mensajes en la **consola**.  Dado que el anuncio se ejecuta en un contexto [de JavaScript](#choose-javascript-context)diferente, una forma de ocultar los mensajes es abrir la consola [Configuración](#open-console-settings) y elegir la casilla junto a Solo **contexto seleccionado**.  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a>Filtrar mensajes que no coincidan con un patrón de expresión regular  

Escriba una expresión regular como, por ejemplo, en el cuadro de texto Filtrar para filtrar los mensajes que no `/[gm][ta][mi]/` coincidan con ese patrón. ****  DevTools comprueba si el patrón se encuentra en el texto del mensaje o en el script que hizo que se registrara el mensaje.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar los mensajes que no coincidan con la expresión regex" lightbox="../media/console-filter-regex.msft.png":::
   Filtrar los mensajes que no coincidan con la `/[gm][ta][mi]/` expresión regex  
:::image-end:::  

## <a name="run-javascript"></a>Ejecutar JavaScript  

Esta sección contiene características relacionadas con la ejecución de JavaScript en la **consola**.  Para obtener un tutorial práctica, vaya a [Ejecutar JavaScript][DevtoolsConsoleConsoleJavascript].  

### <a name="rerun-expressions-from-history"></a>Volver a ejecutar expresiones del historial  

Seleccione `Up Arrow` esta opción para recorrer el historial de expresiones de JavaScript que se ejecutó anteriormente en la **consola**.  Seleccione `Enter` para ejecutar esa expresión de nuevo.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Ver el valor de una expresión en tiempo real con Live Expressions  

Si se encuentra escribiendo la misma expresión de JavaScript en la **consola** repetidamente, es posible que le resulte más fácil crear **una expresión live**.  Con **live expressions**, se escribe una expresión una vez y, a continuación, se ancla a la parte superior de la **consola**.  El valor de la expresión se actualiza casi en tiempo real.  Vaya a [Ver valores de expresión de JavaScript en Real-Time Con expresiones en directo][DevToolsConsoleLiveExpressions].  

### <a name="turn-off-eager-evaluation"></a>Desactivar evaluación ansiosa  

**Eager Evaluation** muestra una vista previa del valor devuelto al escribir expresiones de JavaScript en la **consola**.  Para desactivar las vistas previas de valor devuelto, complete las siguientes acciones.  

1.  [Abra la consola Configuración](#open-console-settings).  
1.  Quite la casilla situada junto a **Evaluación ansiosa**.  
    
### <a name="turn-off-autocomplete-from-history"></a>Desactivar autocompletar del historial  

Al escribir una expresión, la ventana emergente autocompletar de la **consola** muestra las expresiones que ejecutó anteriormente.  Las expresiones están pre-pended con el `>` carácter.  Para dejar de mostrar expresiones del historial, abra [la](#open-console-settings) Configuración consola y quite la casilla junto a **Autocompletar del historial.**  

> [!NOTE]
> En la siguiente figura, `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se evaluaron anteriormente.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="El menú emergente autocompletar muestra expresiones del historial" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   El menú emergente autocompletar muestra expresiones del historial  
:::image-end:::  

### <a name="choose-javascript-context"></a>Elegir contexto de JavaScript  

La opción predeterminada para el desplegable **Contexto de JavaScript** es **la**parte superior, que representa el contexto [de exploración][MdnDocsGlossaryBrowsingContext] de la página web principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Desplegable Contexto de JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   Desplegable **Contexto de JavaScript**  
:::image-end:::  

Supongamos que tienes un anuncio en tu página web incrustado en un `<iframe>` .  Quieres ejecutar JavaScript para ajustar el DOM del anuncio.  En primer lugar, elige el contexto de exploración del anuncio en el desplegable **Contexto de JavaScript.**  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Elegir un contexto de JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   Elegir un contexto de JavaScript diferente  
:::image-end:::  

## <a name="clear-the-console"></a>Borrar la consola  

Para borrar la **consola,** complete cualquiera de los siguientes flujos de trabajo.  

*   Elija el **botón Borrar consola** \( Borrar consola ![ ](../media/clear-console-button-icon.msft.png) \).  
*   Mantenga el mouse sobre un mensaje, abra el menú contextual \(haga clic con el botón secundario\) y elija **Borrar consola**.  
*   Escriba `clear()` en la **Consola** y seleccione `Enter` .  
*   Ejecute `console.clear()` desde JavaScript para la página web.  
*   Seleccione `Control` + `L` mientras la **consola** está en foco.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensajes en la herramienta consola | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Consola como entorno de JavaScript | Microsoft Docs"  
[DevtoolsConsoleIndex]: .index.md "Use la consola | Microsoft Docs"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Inspeccionar y filtrar información en la página web | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Supervisar los cambios en JavaScript mediante expresiones live | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ejecute comandos con el menú de comandos de DevTools de Microsoft Edge | Microsoft Docs"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de exploración | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
