---
description: Tutorial sobre las características más populares relacionadas con la red en Microsoft Edge DevTools.
title: Inspeccionar la actividad de red en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a4a552fa9a45267a6ffa4a4e83e7ebc4e1817162
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439699"
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

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a>Inspeccionar la actividad de red en Microsoft Edge DevTools  

Este es un tutorial práctica de algunas de las características de DevTools más usadas relacionadas con la inspección de la actividad de red de una página.  

Si desea examinar las características, vaya a [Referencia de red][DevtoolsNetworkReference].  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a>Cuándo usar el panel Red  

En general, use el panel Red cuando necesite asegurarse de que los recursos se descargan o cargan según lo esperado.  Los casos de uso más comunes para el panel Red son:  

*   Asegurarse de que los recursos se cargan o descargan realmente.  
*   Inspeccionar las propiedades de un recurso individual, como los encabezados HTTP, el contenido, el tamaño, y así sucesivamente.  
    
Si está buscando formas de mejorar el rendimiento de carga de página, **no empiece** con la **herramienta Red.**  Hay muchos tipos de problemas de rendimiento de carga que no están relacionados con la actividad de red.  Comience con el panel Auditorías porque le ofrece sugerencias dirigidas sobre cómo mejorar la página.  Vaya a [Optimizar velocidad del sitio web][DevtoolsSpeedGetStarted].  

## <a name="open-the-network-panel"></a>Abrir el panel Red  

Para sacar el máximo partido a este tutorial, abra la demostración y pruebe las características de la página de demostración.  

1.  Abra la [Demostración de introducción][GlitchNetworkGetStarted].  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       La demostración  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  Para [abrir DevTools,][DevToolsOpen]seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  Se **abre la herramienta** Consola.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="La consola" lightbox="../media/network-glitch-console.msft.png":::
       La **consola**  
    :::image-end:::  
    
    Es posible que prefiera [acoplar DevTools a la parte inferior de la ventana][DevToolsCustomizePlacement].  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools acoplada a la parte inferior de la ventana" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools acoplada a la parte inferior de la ventana  
    :::image-end:::  
    
1.  Abra la **herramienta Red.**  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Herramienta de consola en DevTools acoplada a la parte inferior de la ventana" lightbox="../media/network-glitch-network-bottom.msft.png":::
       **Herramienta** de consola en DevTools acoplada a la parte inferior de la ventana  
    :::image-end:::  
    
En este momento, **la herramienta Red** está vacía.  DevTools solo registra la actividad de red después de abrirlo y no se ha producido ninguna actividad de red desde que abrió DevTools.  

## <a name="log-network-activity"></a>Registrar actividad de red  

Para ver la actividad de red que provoca una página:  

1.  Actualice la página web.  El panel Red registra toda la actividad de red en el **registro de red**.  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="El registro de red" lightbox="../media/network-glitch-network.msft.png":::
       El **registro de red**  
    :::image-end:::  
    
    Cada fila del registro **de red** representa un recurso.  De forma predeterminada, los recursos se enumeran cronológicamente.  El recurso superior suele ser el documento HTML principal.  El recurso inferior es lo que se solicitó por última vez.  
    
    Cada columna representa información sobre un recurso.  En la figura anterior se muestran las columnas predeterminadas.  

    *   **Estado**.  El código de estado HTTP para la respuesta.  
    *   **Tipo**.  Tipo de recurso.  
    *   **Iniciador**.  La causa de la solicitud de recurso.  CHoosing a link in the Initiator column takes you to the source code that caused the request.  
    *   **Hora**.  Duración de la solicitud.  
    *   **Cascada**.  Representación gráfica de las distintas fases de la solicitud.  Para mostrar un desglose, mantenga el mouse en una cascada.  
    
    > [!NOTE]
    > El gráfico que se encuentra encima del registro de red se denomina Información general.  No usará el gráfico Información general en este tutorial, por lo que puede ocultarlo.  Vaya a [Ocultar el panel Información general][DevtoolsReferenceHideOverview].
    
1.  Después de abrir DevTools, registra la actividad de red en el registro de red.  
    Para demostrar esto, primero mire la parte inferior **del** registro de red y tome nota mental de la última actividad.  
1.  Ahora, seleccione el **botón Obtener datos** en la demostración.  
1.  Vuelva a mirar la parte inferior del **registro de** red.  Se muestra un nuevo `getstarted.json` recurso denominado.  Para hacer que la página web solicite el archivo, elija el **botón Obtener** datos.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Un nuevo recurso en el registro de red" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Un nuevo recurso en el registro **de red**  
    :::image-end:::  
    
## <a name="show-more-information"></a>Mostrar más información  

Las columnas del registro de red se pueden configurar.  Puede ocultar columnas que no está usando.  
También hay muchas columnas ocultas de forma predeterminada que puede resultar útil.  

1.  Mantenga el mouse en el encabezado de la tabla Registro de red, abra el menú contextual \(haga clic con el botón secundario\) y elija **Dominio**.  Ahora se muestra el dominio de cada recurso.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Habilitar la columna Dominio" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Habilitar la columna Dominio  
    :::image-end:::  
    
    > [!TIP]
    > Para revisar la dirección URL completa de un recurso, mantenga el mouse en la celda de la **columna** Nombre.  
    
## <a name="simulate-a-slower-network-connection"></a>Simular una conexión de red más lenta  

La conexión de red del equipo que usa para crear sitios es probablemente más rápida que las conexiones de red de los dispositivos móviles de los usuarios.  Al limitación de la página, obtienes una mejor idea del tiempo que tarda una página en cargarse en un dispositivo móvil.  

1.  Elija el **desplegable Limitación,** que se establece en **Línea de** forma predeterminada.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Habilitar la limitación" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Habilitar la limitación  
    :::image-end:::  
    
1.  Elija **Lento 3G**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Elija Lento 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Elija Lento 3G  
    :::image-end:::  
    
1.  Presione durante mucho **tiempo Reload** \( ![ Reload \) y, a ](../media/refresh-icon.msft.png) continuación, elija **Empty Cache and Hard Reload**.  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Caché vacía y recarga dura" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Caché vacía y recarga dura**  
    :::image-end:::  
    
    En las visitas repetidas, el explorador normalmente sirve algunos archivos de la [memoria caché,][MDNHTTPCache]lo que acelera la carga de la página.  **La caché vacía y la recarga dura** fuerzan al explorador a ir a la red para todos los recursos.  Úselo para mostrar cómo un visitante por primera vez experimenta una carga de página.  
    
    > [!NOTE]
    > El **flujo de trabajo Caché vacía y Recarga** dura solo está disponible cuando DevTools está abierto.  
    
## <a name="capture-screenshots"></a>Capturar capturas de pantalla  

Las capturas de pantalla muestran cómo se ve una página web con el tiempo mientras se carga.  

1.  Elija \( ![ Configuración de red ](../media/settings-icon.msft.png) \) y active la casilla Capturar **capturas de** pantalla.
1.  Actualice la página de nuevo con el **flujo de trabajo Caché vacía y Recarga dura.**  Navegue hasta [Simular una conexión más lenta](#simulate-a-slower-network-connection) si necesita un aviso sobre cómo hacerlo.  
    El panel Capturas de pantalla proporciona miniaturas del aspecto de la página en varios puntos durante el proceso de carga.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Capturas de pantalla de la carga de página" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Capturas de pantalla de la carga de página  
    :::image-end:::  
    
1.  Elija la primera miniatura.  DevTools muestra qué actividad de red se estaba produciendo en ese momento.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="La actividad de red que se estaba produciendo durante la primera captura de pantalla" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       La actividad de red que se estaba produciendo durante la primera captura de pantalla  
    :::image-end:::  
    
1.  Vuelva a elegir \( Configuración de red \) y desactive la casilla Capturar capturas de pantalla ![ para cerrar el panel Capturas de ](../media/settings-icon.msft.png) pantalla. ****
1.  Actualice la página de nuevo.  
    
## <a name="inspect-the-details-of-the-resource"></a>Inspeccionar los detalles del recurso  

Elija un recurso para obtener más información sobre él.  Pruébalo ahora:  

1.  Elija `getstarted.html` .  Se **muestra** el panel Encabezados.  Use este panel para inspeccionar los encabezados HTTP.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Panel Encabezados" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Panel **Encabezados**  
    :::image-end:::  
    
1.  Elija el panel **Vista** previa.  Se muestra una representación básica del HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="El panel Vista previa" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       El panel **Vista** previa  
    :::image-end:::  
    
    El panel es útil cuando una API devuelve un código de error en HTML.  Es posible que le resulte más fácil leer el HTML representado que el código fuente HTML, o al inspeccionar imágenes.  

1.  Elija **el** panel Respuesta.  Se muestra el código fuente HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="El panel Respuesta" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       El panel **Respuesta**  
    :::image-end:::  
    
    > [!TIP]
    > Cuando se minifica un archivo, elija el botón **Formato** \( Formato \) situado en la parte inferior del panel Respuesta para volver a aplicar formato al contenido del archivo para que sea ![ ](../media/format-icon.msft.png) legible. ****  
    
1.  Elija **** el panel Temporización.  Se muestra un desglose de la actividad de red del recurso.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="El panel Temporización" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       El panel **Temporización**  
    :::image-end:::  
    
1.  Elija **Cerrar** \( ![ Cerrar ](../media/close-icon.msft.png) \) para volver a ver el registro de red.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="El botón Cerrar" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       El **botón** Cerrar  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a>Buscar respuestas y encabezados de red  

Use el **panel** Búsqueda cuando necesite buscar en los encabezados HTTP y las respuestas de todos los recursos una determinada cadena o expresión regular.  

Por ejemplo, supongamos que desea comprobar que los recursos usan directivas de **caché razonables.**  

<!--TODO: add cache policies section when available  -->

1.  Elija **Buscar** \( ![ Buscar ](../media/search-icon.msft.png) \).  El panel Búsqueda se abre a la izquierda del registro de red.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Panel de búsqueda" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Panel **de** búsqueda  
    :::image-end:::  
    
1.  Escriba `Cache-Control` y seleccione `Enter` .  El panel Búsqueda enumera todas las instancias que encuentra `Cache-Control` en los encabezados de recursos o el contenido.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Resultados de búsqueda para Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Resultados de búsqueda de  `Cache-Control`  
    :::image-end:::  
    
1.  Elija un resultado para ver el recurso en el que se encontró el resultado.  Si está viendo los detalles del recurso, seleccione un resultado para ir directamente a él.  Por ejemplo, si la consulta se encontró en un encabezado, se abrirá el panel **Encabezados.**   Si la consulta se encontró en el contenido, se **abrirá el** panel Respuesta.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Un resultado de búsqueda resaltado en el panel Encabezados" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Un resultado de búsqueda resaltado en el panel **Encabezados**  
    :::image-end:::  
    
1.  Cierre el panel Búsqueda y el panel **Encabezados.**  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Los botones Cerrar" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Los **botones Cerrar**  
    :::image-end:::  
    
## <a name="filter-resources"></a>Filtrar recursos  

DevTools proporciona numerosos flujos de trabajo para filtrar recursos que no son relevantes para la tarea en cuestión.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="La barra de herramientas Filtros" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   La **barra de herramientas Filtros**  
:::image-end:::  

La **barra de** herramientas Filtros debe estar activada de forma predeterminada.  Si no es así:  

1.  Elija **Filter** \( ![ Filter ](../media/filter-icon.msft.png) \) para mostrarlo.  
    
### <a name="filter-by-string-regular-expression-or-property"></a>Filtrar por cadena, expresión regular o propiedad  

El **cuadro de** texto Filtrar admite muchos tipos diferentes de filtrado.  

1.  Escriba `png` en el cuadro **de** texto Filtrar.  Solo se muestran los archivos que contienen `png` el texto.  En este caso, los únicos archivos que coinciden con el filtro son las imágenes PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Un filtro de cadena" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Un filtro de cadena  
    :::image-end:::  
    
1.  Escribe `/.*\.[cj]s+$/`.  DevTools filtra cualquier recurso con un nombre de archivo que no termine con un o un seguido `j` `c` de 1 o más `s` caracteres.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Filtro de expresiones regulares" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Filtro de expresiones regulares  
    :::image-end:::  
    
1.  Escribe `-main.css`.  DevTools filtra `main.css` .  Si algún archivo coincide con el patrón, tit también se filtra.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Un filtro negativo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Un filtro negativo  
    :::image-end:::  
    
1.  Escriba `domain:cdn.glitch.com` en el cuadro **de** texto Filtrar.  DevTools filtra cualquier recurso con una dirección URL que no coincida con este dominio.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Filtro de propiedades" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Filtro de propiedades  
    :::image-end:::  
    
    Para obtener la lista completa de propiedades filtrables, vaya a [Filtrar solicitudes por propiedades][DevtoolsReferenceProperty].  
    
1.  Desactive el **cuadro de** texto Filtrar de cualquier texto.  
    
### <a name="filter-by-resource-type"></a>Filtrar por tipo de recurso  

Para centrarse en un determinado tipo de archivo, como hojas de estilos:  

1.  Elija **CSS**.  El resto de tipos de archivo se filtran.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Mostrar solo archivos CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Mostrar solo archivos CSS  
    :::image-end:::  
    
1.  Para mostrar también scripts, seleccione y mantenga presionado `Control` \(Windows, Linux\) o `Command` \(macOS\) y, a continuación, **elija JS**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Mostrar solo archivos CSS y JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Mostrar solo archivos CSS y JS  
    :::image-end:::  
    
1.  Para quitar los filtros y volver a mostrar todos los recursos, elija **All**.  
    
Para otros flujos de trabajo de filtrado, vaya [a Filtrar solicitudes][DevtoolsNetworkReferenceFilter].  

## <a name="block-requests"></a>Bloquear solicitudes  

¿Cómo se ve y se comporta una página cuando algunos de los recursos de página no están disponibles?  ¿Falla completamente o todavía es algo funcional?  Bloquear solicitudes para averiguar:  

1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Menú comando" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       Menú **comando**  
    :::image-end:::  
    
1.  Escriba `block` , elija Mostrar bloqueo de **solicitudes**y seleccione `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Mostrar bloqueo de solicitudes" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Mostrar bloqueo de solicitudes**  
    :::image-end:::  
    
1.  Elija **Agregar patrón** \( Agregar patrón ![ ](../media/add-icon.msft.png) \).  
1.  Escribe `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Bloqueo de main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Bloqueo `main.css`  
    :::image-end:::  
    
1.  Elija **Agregar**.  
1.  Actualiza la página.  Como se esperaba, el estilo de la página está ligeramente desordenado porque la hoja de estilos principal se ha bloqueado.  
    
    > [!NOTE]
    > Fila `main.css` del registro de red.  El texto rojo significa que el recurso se bloqueó.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css se ha bloqueado" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` se ha bloqueado  
    :::image-end:::  
    
1.  Anule la selección **de la casilla Habilitar bloqueo de solicitudes.**  

## <a name="conclusion"></a>Conclusión  

Enhorabuena, ha completado el tutorial.  Ahora ya sabes cómo usar la herramienta **Red** en Microsoft Edge DevTools.

Vaya a [la Referencia de red para][DevtoolsNetworkReference] descubrir más características de DevTools relacionadas con la inspección de la actividad de red.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReference]: ./reference.md "Referencia de análisis de red | Microsoft Docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Solicitudes de filtro: referencia de análisis de red | Microsoft Docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar el panel Información general: referencia de análisis de red | Microsoft Docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitudes por propiedades: referencia de análisis de red | Microsoft Docs"
[DevToolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools | Microsoft Docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspeccionar la demostración de actividad de red | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché HTTP | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
