---
description: Un tutorial sobre las características más populares relacionadas con la red en Microsoft Edge DevTools.
title: Inspeccionar la actividad de la red en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3629c2d3711716d6d4a837b29bffef4786eb6d3f
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993453"
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





# Inspeccionar la actividad de la red en Microsoft Edge DevTools   



Este es un tutorial práctico de algunas de las características de DevTools más usadas relacionadas con la inspección de la actividad de red de una página.  

Consulte [referencia de red][DevtoolsNetworkReference] si desea examinar las características en su lugar.  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## Cuándo usar el panel red   

En general, use el panel red cuando necesite asegurarse de que los recursos se van a descargar o cargar según lo esperado.  Los casos de uso más comunes para el panel red son:  

*   Asegurándote de que los recursos se carguen o descarguen realmente.  
*   Inspeccione las propiedades de un recurso individual, como los encabezados HTTP, el contenido, el tamaño, etc.  
    
Si está buscando formas de mejorar el rendimiento de la carga de páginas, **no** empiece por el panel red.  Hay muchos tipos de problemas de rendimiento de la carga que no están relacionados con la actividad de la red.  Comience con el panel auditorías porque le ofrece sugerencias específicas sobre cómo mejorar la página.  Consulte [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].  

## Abrir el panel de red   

Para sacar el máximo provecho de este tutorial, abra la demostración y pruebe las características de la página de demostración.  

1.  Abra la [demostración introducción][GlitchNetworkGetStarted].  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       La demostración  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  [Abra DevTools][DevToolsOpen] presionando `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  Se abre el panel de la **consola** .  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="La consola" lightbox="../media/network-glitch-console.msft.png":::
       La **consola**  
    :::image-end:::  
    
    Es posible que prefiera [acoplar DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools acoplado en la parte inferior de la ventana" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools acoplado en la parte inferior de la ventana  
    :::image-end:::  
    
1.  Seleccione la pestaña **red** .  Se abre el panel red.  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="DevTools acoplado en la parte inferior de la ventana" lightbox="../media/network-glitch-network-bottom.msft.png":::
       DevTools acoplado en la parte inferior de la ventana  
    :::image-end:::  
    
Ahora el panel red está vacío.  DevTools solo registra la actividad de la red después de abrirla y no se ha producido ninguna actividad de red desde que abrió DevTools.  

## Registrar actividad de la red   

Para ver la actividad de red que provoca una página:  

1.  Vuelva a cargar la página.  El panel red registra toda la actividad de la red en el **registro de red**.  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="El registro de red" lightbox="../media/network-glitch-network.msft.png":::
       El **registro de red**  
    :::image-end:::  
    
    Cada fila del **registro de red** representa un recurso.  De forma predeterminada, los recursos se muestran cronológicamente.  El recurso superior suele ser el documento HTML principal.  El recurso inferior es el último que se solicitó.  
    
    Cada columna representa información acerca de un recurso.  En la ilustración anterior se muestran las columnas predeterminadas.  

    *   **Estado**.  El código de Estado HTTP para la respuesta.  
    *   **Tipo**.  El tipo de recurso.  
    *   **Iniciador**.  La causa de la solicitud de recursos.  Al seleccionar un vínculo en la columna iniciador, se le lleva al código fuente que causó la solicitud.  
    *   **Momento**.  La duración de la solicitud.  
    *   **Cascada**.  Una representación gráfica de las distintas etapas de la solicitud.  Desplace el puntero sobre una cascada para ver un desglose.  
    
    > [!NOTE]
    > El gráfico que se encuentra sobre el registro de red se denomina Descripción general.  No usará el gráfico de información general en este tutorial, por lo que puede ocultarlo.  Vea [ocultar el panel de información general][DevtoolsReferenceHideOverview].
    
1.  Después de abrir DevTools, registra la actividad de la red en el registro de red.  
    Para demostrarlo, primero mire la parte inferior del **registro de red** y tome nota mental de la última actividad.  
1.  Ahora, seleccione el botón **obtener datos** en la demostración.  
1.  Vuelva a mirar la parte inferior del **registro de red** .  Debería ver un nuevo recurso denominado `getstarted.json` .  Si selecciona el botón **obtener datos** , la página solicitará este archivo.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Un nuevo recurso en el registro de red" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Un nuevo recurso en el **registro de red**  
    :::image-end:::  
    
## Mostrar más información   

Las columnas del registro de red se pueden configurar.  Puede ocultar las columnas que no está usando.  
También hay muchas columnas que están ocultas de forma predeterminada, que pueden resultarle útiles.  

1.  Haga clic con el botón derecho en el encabezado de la tabla registro de red y seleccione **dominio**.  Ahora se muestra el dominio de cada recurso.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Habilitar la columna dominio" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Habilitar la columna dominio  
    :::image-end:::  
    
    > [!TIP]
    > Vea la dirección URL completa de un recurso colocando el puntero sobre la celda en la columna **nombre** .  
    
## Simular una conexión de red más lenta   

Es probable que la conexión de red del equipo que use para crear sitios sea más rápida que las conexiones de red de los dispositivos móviles de los usuarios.  Al limitar la página, se obtiene una idea más extensa de cuánto tarda una página en cargarse en un dispositivo móvil.  

1.  Seleccione la lista desplegable **límite** , que está establecida en **conectado** de forma predeterminada.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Habilitar límite" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Habilitar límite  
    :::image-end:::  
    
1.  Seleccione **3G lento**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Seleccionar 3G lento" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Seleccionar 3G lento  
    :::image-end:::  
    
1.  Pulse volver a **cargar** \ ( ![ volver a cargar ][ImageRefreshIcon] \) y, a continuación, seleccione **vaciar memoria caché y recargar de disco**.  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Memoria caché vacía y recarga duro" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Memoria caché vacía y recarga duro**  
    :::image-end:::  
    
    En las visitas repetidas, el explorador generalmente sirve algunos archivos de la [caché][MDNHTTPCache], lo que acelera la carga de la página.  **Vaciar la memoria caché y la recarga de disco** obliga al explorador a dirigirse a la red para todos los recursos.  Esto es útil cuando desea ver cómo experimenta un primer visitante la carga de la página.  
    
    > [!NOTE]
    > El flujo de trabajo **vacío y la recarga de disco duro** solo está disponible cuando DevTools está abierto.  
    
## Capturar capturas de pantallas   

Las capturas de pantallas le permiten ver cómo se ha enviado una página a lo largo del tiempo mientras se cargaba.  

1.  Seleccione \ ( ![ configuración ][ImageSettingsIcon] de red \) y seleccione la casilla **capturar capturas de pantallas** .
1.  Vuelva a cargar la página a través del flujo de trabajo **vacío y de recarga de disco** .  Consulte [simular una conexión más lenta](#simulate-a-slower-network-connection) si necesita un aviso sobre cómo hacerlo.  
    El panel capturas de pantallas proporciona miniaturas de la apariencia de la página en varios puntos durante el proceso de carga.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Capturas de pantallas de la carga de la página" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Capturas de pantallas de la carga de la página  
    :::image-end:::  
    
1.  Seleccionar la primera miniatura.  DevTools muestra qué actividad de la red tuvo lugar en ese momento.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="La actividad de red que se produjo durante la primera captura de pantalla" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       La actividad de red que se produjo durante la primera captura de pantalla  
    :::image-end:::  
    
1.  Seleccione \ ( ![ configuración de red ][ImageSettingsIcon] \) de nuevo y anule la selección de la casilla de verificación **capturar capturas** de pantallas para cerrar el panel capturas de pantallas.
1.  Vuelva a cargar la página.  
    
## Inspeccionar los detalles del recurso   

Seleccione un recurso para obtener más información sobre él.  Pruébelo ahora:  

1.  Seleccione `getstarted.html` .  Se muestra la pestaña **encabezados** .  Use esta pestaña para inspeccionar los encabezados HTTP.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="La pestaña encabezados" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       La pestaña **encabezados**  
    :::image-end:::  
    
1.  Seleccione la pestaña **vista previa** .  Se muestra una representación básica del HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="La ficha vista previa" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       La ficha **vista previa**  
    :::image-end:::  
    
    Esta pestaña es útil cuando una API devuelve un código de error en HTML.  Es posible que le resulte más fácil leer el código HTML representado que el código fuente HTML o cuando Inspeccione imágenes.  

1.  Seleccione la pestaña **respuesta** .  Se muestra el código fuente HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="La ficha respuesta" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       La ficha **respuesta**  
    :::image-end:::  
    
    > [!TIP]
    > Cuando se minified un archivo, al seleccionar el botón **formato** \ ( ![ formato ][ImageFormatIcon] \) en la parte inferior de la pestaña **respuesta** , se cambia el formato del contenido para mejorar la legibilidad.  
    
1.  Seleccione la pestaña **intervalos** .  Se muestra un desglose de la actividad de red de este recurso.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="La ficha intervalos" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       La ficha **intervalos**  
    :::image-end:::  
    
1.  Seleccione **cerrar** \ ( ![ cerrar ][ImageCloseIcon] \) para volver a ver el registro de red.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Botón cerrar" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Botón **cerrar**  
    :::image-end:::  
    
## Buscar encabezados y respuestas de red   

Use el panel de **búsqueda** cuando necesite buscar en los encabezados y las respuestas http de todos los recursos para una cadena determinada o una expresión normal.  

Por ejemplo, supongamos que desea comprobar que los recursos usan **directivas de caché**razonables.  

<!--TODO: add cache policies section when available  -->

1.  Seleccione **Buscar** \ ( ![ Buscar ][ImageSearchIcon] \).  El panel de búsqueda se abre a la izquierda del registro de red.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="El panel de búsqueda" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       El panel de **búsqueda**  
    :::image-end:::  
    
1.  Escriba `Cache-Control` y presione `Enter` .  El panel de búsqueda muestra todas las instancias de las `Cache-Control` que encuentra en los encabezados de recursos o en el contenido.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Resultados de la búsqueda de control de caché" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Resultados de búsqueda de  `Cache-Control`  
    :::image-end:::  
    
1.  Seleccione un resultado para ver el recurso en el que se encontró el resultado.  Si está viendo los detalles del recurso, seleccione un resultado para ir directamente a él.  Por ejemplo, si la consulta se encuentra en un encabezado, se abre la pestaña encabezados.   Si la consulta se encuentra en el contenido, se abre la pestaña **respuesta** .  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Un resultado de búsqueda resaltado en la pestaña encabezados" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Un resultado de búsqueda resaltado en la pestaña **encabezados**  
    :::image-end:::  
    
1.  Cierre el panel de búsqueda y la pestaña encabezados.  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Los botones cerrar" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Los botones **cerrar**  
    :::image-end:::  
    
## Filtrar recursos   

DevTools proporciona numerosos flujos de trabajo para filtrar recursos que no son relevantes para la tarea que está realizando.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="La barra de herramientas filtros" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   La barra de herramientas **filtros**  
:::image-end:::  

La barra de herramientas **filtros** debería estar habilitada de forma predeterminada.  De lo contrario:  

1.  Seleccione **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para mostrarlo.  
    
### Filtrar por cadena, expresión regular o propiedad   

El cuadro de texto **filtro** admite muchos tipos de filtrado diferentes.  

1.  Escriba `png` en el cuadro de texto **filtro** .  Solo se muestran los archivos que contienen el texto `png` .  En este caso, los únicos archivos que coinciden con el filtro son las imágenes PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Un filtro de cadena" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Un filtro de cadena  
    :::image-end:::  
    
1.  Escribe `/.*\.[cj]s+$/`.  DevTools filtra cualquier recurso con un nombre de archivo que no termina con un `j` o a `c` , seguido de 1 o más `s` caracteres.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Filtro de expresión regular" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Filtro de expresión regular  
    :::image-end:::  
    
1.  Escribe `-main.css`.  DevTools filtra `main.css` .  Si cualquier otro archivo coincide con el patrón, también se filtrarían.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Un filtro negativo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Un filtro negativo  
    :::image-end:::  
    
1.  Escriba `domain:cdn.glitch.com` en el cuadro de texto **filtro** .  DevTools filtra cualquier recurso con una dirección URL que no coincida con este dominio.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Un filtro de propiedad" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Un filtro de propiedad  
    :::image-end:::  
    
    Vea [filtrar solicitudes por propiedades][DevtoolsReferenceProperty] para obtener una lista completa de las propiedades que se pueden filtrar.  
    
1.  Borre el cuadro de texto de **filtro** de cualquier texto.  
    
### Filtrar por tipo de recurso   

Para centrarse en un determinado tipo de archivo, como las hojas de estilos:  

1.  Seleccione **CSS**.  Se filtran todos los demás tipos de archivo.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Mostrar solo archivos CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Mostrar solo archivos CSS  
    :::image-end:::  
    
1.  Para ver también las secuencias de comandos, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione **JS**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Mostrar solo archivos CSS y JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Mostrar solo archivos CSS y JS  
    :::image-end:::  
    
1.  Seleccione **todo** para quitar los filtros y volver a ver todos los recursos.  
    
Consulte [filtrar solicitudes][DevtoolsNetworkReferenceFilter] para otros flujos de trabajo de filtrado.  

## Solicitudes de bloqueo   

¿Cómo se ve y se comporta una página cuando algunos de los recursos de la página no están disponibles?  ¿Se produce un error completamente o aún es funcional?  Bloquear solicitudes para averiguar:  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="El menú de comandos" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       El **menú de comandos**  
    :::image-end:::  
    
1.  Escriba `block` , seleccione **Mostrar bloqueo de solicitud**y presione `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Mostrar bloqueo de solicitud" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Mostrar bloqueo de solicitud**  
    :::image-end:::  
    
1.  Seleccione **Agregar patrón** \ ( ![ Agregar patrón ][ImageAddIcon] \).  
1.  Escribe `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Bloqueo de Main. CSS" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Bugs `main.css`  
    :::image-end:::  
    
1.  Seleccione **Agregar**.  
1.  Vuelva a cargar la página.  Como se espera, el estilo de la página está ligeramente desordenado porque la hoja de estilos principal ha sido bloqueada.  
    
    > [!NOTE]
    > La `main.css` fila en el registro de red.  El texto en rojo significa que el recurso se ha bloqueado.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Main. CSS ha sido bloqueado" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` ha sido bloqueado  
    :::image-end:::  
    
1.  Anule la selección de la casilla de verificación **Activar bloqueo de solicitud** .  

## Conclusión  

Enhorabuena, ha completado el tutorial.  Ahora ya sabe cómo usar el panel **red** en el DevTools de Microsoft Edge.

<!--




-->  

Consulte la [referencia de red][DevtoolsNetworkReference] para descubrir más características de DevTools relacionadas con la inspección de la actividad de la red.  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de DevTools de Microsoft Edge | Microsoft docs"  
[DevtoolsNetworkReference]: ./reference.md "Referencia de análisis de red | Microsoft docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Solicitudes de filtro: referencia de análisis de red | Microsoft docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar el panel de información general: referencia de análisis de red | Microsoft docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitudes por propiedades-referencia de análisis de red | Microsoft docs"
[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools | Microsoft docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Comprobar actividad de la red demo | Intento"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché de HTTP | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
