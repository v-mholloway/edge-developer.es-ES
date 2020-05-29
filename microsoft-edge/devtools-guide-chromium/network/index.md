---
title: Inspeccionar la actividad de la red en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611815"
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

1.  Abra la [demostración introducción][GlitchNetworkGetStarted] .  
    
    > ##### Figura 1  
    > La demostración  
    > ![La demostración][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  [Abra DevTools][DevToolsOpen] presionando `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  Se abre el panel de la **consola** .  
    
    > ##### Figura 2  
    > La consola  
    > ! [La consola] [ImagesTutorialConsole]  
    
    Es posible que prefiera [acoplar DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].  
    
    > ##### Imagen 3  
    > DevTools acoplado en la parte inferior de la ventana  
    > ! [DevTools acoplada a la parte inferior de la ventana] [ImagesTutorialDocked]  

1.  Seleccione la pestaña **red** .  Se abre el panel red.  
    
    > ##### Imagen 4  
    > DevTools acoplado en la parte inferior de la ventana  
    > ! [DevTools acoplada a la parte inferior de la ventana] [ImagesTutorialNetwork]  

Ahora el panel red está vacío.  DevTools solo registra la actividad de la red después de abrirla y no se ha producido ninguna actividad de red desde que abrió DevTools.  

## Registrar actividad de la red   

Para ver la actividad de red que provoca una página:  

1.  Vuelva a cargar la página.  El panel red registra toda la actividad de la red en el **registro de red**.  
    
    > ##### Imagen 5  
    > El registro de red  
    > ! [El registro de red] [ImagesTutorialLog]  
    
    Cada fila del **registro de red** representa un recurso.  De forma predeterminada, los recursos se muestran cronológicamente.  El recurso superior suele ser el documento HTML principal.  El recurso inferior es el último que se solicitó.  
    
    Cada columna representa información acerca de un recurso.  En la [**figura 6**](#figure-6) se muestran las columnas predeterminadas:  

    *   **Estado**.  El código de Estado HTTP para la respuesta.  
    *   **Tipo**.  El tipo de recurso.  
    *   **Iniciador**.  La causa de la solicitud de recursos.  Al seleccionar un vínculo en la columna iniciador, se le lleva al código fuente que causó la solicitud.  
    *   **Momento**.  La duración de la solicitud.  
    *   **Cascada**.  Una representación gráfica de las distintas etapas de la solicitud.  
        Desplace el puntero sobre una cascada para ver un desglose.  
    
    > [!NOTE]
    > El gráfico que se encuentra sobre el registro de red se denomina Descripción general.  No usará el gráfico de información general en este tutorial, por lo que puede ocultarlo.  Vea [ocultar el panel de información general][DevtoolsReferenceHideOverview].
        
1.  Después de abrir DevTools, registra la actividad de la red en el registro de red.  
    Para demostrarlo, primero mire la parte inferior del **registro de red** y tome nota mental de la última actividad.  
1.  Ahora, seleccione el botón **obtener datos** en la demostración.  
1.  Vuelva a mirar la parte inferior del **registro de red** .  Debería ver un nuevo recurso denominado `getstarted.json` .  Si selecciona el botón **obtener datos** , la página solicitará este archivo.  
    
    > ##### Imagen 6  
    > Un nuevo recurso en el registro de red  
    > ! [Un nuevo recurso en el registro de red] [ImagesTutorialRuntime]  

## Mostrar más información   

Las columnas del registro de red se pueden configurar.  Puede ocultar las columnas que no está usando.  
También hay muchas columnas que están ocultas de forma predeterminada, que pueden resultarle útiles.  

1.  Haga clic con el botón derecho en el encabezado de la tabla registro de red y seleccione **dominio**.  Ahora se muestra el dominio de cada recurso.  
    
    > ##### Imagen 7  
    > Habilitar la columna dominio  
    > ! [Habilitar la columna dominio] [ImagesTutorialDomain]  
    
    > [!TIP]
    > Vea la dirección URL completa de un recurso colocando el puntero sobre la celda en la columna **nombre** .  

## Simular una conexión de red más lenta   

Es probable que la conexión de red del equipo que use para crear sitios sea más rápida que las conexiones de red de los dispositivos móviles de los usuarios.  Al limitar la página, se obtiene una idea más extensa de cuánto tarda una página en cargarse en un dispositivo móvil.  

1.  Seleccione la lista desplegable **límite** , que está establecida en **conectado** de forma predeterminada.  
    
    > ##### Imagen 8  
    > Habilitar la limitación  
    > ! [Habilitar limitación de peticiones] [ImagesTutorialThrottling]  
    
1.  Seleccione **3G lento**.  
    
    > ##### Imagen 9  
    > Selección de 3G lento  
    > ! [Seleccionando 3G lento] [ImagesTutorialSlow3G]  
    
1.  Haga **clic en volver a** cargar ![ ][ImageRefreshIcon] y, después, seleccione **vaciar caché y volver a carga**.  
    
    > ##### Imagen 10  
    > Memoria caché vacía y recarga duro  
    > ! [Caché vacía y recargada de disco duro] [ImagesTutorialHardReload]  
    
    En las visitas repetidas, el explorador generalmente sirve algunos archivos de la [caché][MDNHTTPCache] , lo que acelera la carga de la página.  **Vaciar la memoria caché y la recarga de disco** obliga al explorador a dirigirse a la red para todos los recursos.  Esto es útil cuando desea ver cómo experimenta un primer visitante la carga de la página.  
    
    > [!NOTE]
    > El flujo de trabajo **vacío y la recarga de disco duro** solo está disponible cuando DevTools está abierto.  

## Capturar capturas de pantallas   

Las capturas de pantallas le permiten ver cómo se ha enviado una página a lo largo del tiempo mientras se cargaba.  

1.  Seleccione ![ configuración de red ][ImageSettingsIcon] y seleccione la casilla **capturar capturas de pantallas** .
1.  Vuelva a cargar la página a través del flujo de trabajo **vacío y de recarga de disco** .  Consulte [simular una conexión más lenta](#simulate-a-slower-network-connection) si necesita un aviso sobre cómo hacerlo.  
    El panel capturas de pantallas proporciona miniaturas de la apariencia de la página en varios puntos durante el proceso de carga.  
    
    > ##### Imagen 11  
    > Capturas de pantallas de la carga de la página  
    > ! [Capturas de pantallas de la carga de la página] [ImagesTutorialAllScreenshots]  

1.  Seleccionar la primera miniatura.  DevTools muestra qué actividad de la red tuvo lugar en ese momento.  
    
    > ##### Imagen 12  
    > La actividad de red que se produjo durante la primera captura de pantalla  
    > ! [La actividad de red que se estaba realizando durante la primera captura de pantalla] [ImagesTutorialFirstScreenshot]  

1.  Vuelva a seleccionar ![ la configuración de red ][ImageSettingsIcon] y desactive la casilla **capturar capturas** de pantallas para cerrar el panel capturas de pantallas.
1.  Vuelva a cargar la página.  

## Inspeccionar los detalles del recurso   

Seleccione un recurso para obtener más información sobre él.  Pruébelo ahora:  

1.  Seleccione `getstarted.html` .  Se muestra la pestaña **encabezados** .  Use esta pestaña para inspeccionar los encabezados HTTP.  
    
    > ##### Imagen 13  
    > La pestaña encabezados  
    > ! [Ficha encabezados] [ImagesTutorialHeaders]  
    
1.  Seleccione la pestaña **vista previa** .  Se muestra una representación básica del HTML.  
    
    > ##### Imagen 14  
    > La ficha vista previa  
    > ! [Ficha vista previa] [ImagesTutorialPreview]  

     Esta pestaña es útil cuando una API devuelve un código de error en HTML.  Es posible que le resulte más fácil leer el código HTML representado que el código fuente HTML o cuando Inspeccione imágenes.  

1.  Seleccione la pestaña **respuesta** .  Se muestra el código fuente HTML.  
    
    > ##### Imagen 15  
    > La ficha respuesta  
    > ! [La pestaña respuesta] [ImagesTutorialResponse]  
    
    > [!TIP]
    > Cuando se minified un archivo, al seleccionar **el** ![ botón formato de formato ][ImageFormatIcon] en la parte inferior de la pestaña **respuesta** , se cambia el formato del contenido para mejorar la legibilidad.  

1.  Seleccione la pestaña **intervalos** .  Se muestra un desglose de la actividad de red de este recurso.  
    
    > ##### Imagen 16  
    > La ficha intervalos  
    > ! [Ficha intervalos] [ImagesTutorialTiming]  

1.  Seleccione **cerrar** ![ y, a continuación, ][ImageCloseIcon] vuelva a ver el registro de red.  
    
    > ##### Imagen 17  
    > Botón cerrar  
    > ! [El botón cerrar] [ImagesTutorialCloseTiming]  

## Buscar encabezados y respuestas de red   

Use el panel de **búsqueda** cuando necesite buscar en los encabezados y las respuestas http de todos los recursos para una cadena determinada o una expresión normal.  

Por ejemplo, supongamos que desea comprobar que los recursos usan **directivas de caché**razonables.  

<!--TODO: add cache policies section when available  -->

1.  Seleccione búsqueda de **búsqueda** ![ ][ImageSearchIcon] .  El panel de búsqueda se abre a la izquierda del registro de red.  
    
    > ##### Ilustración 18  
    > El panel de búsqueda  
    > ! [Panel de búsqueda] [ImagesTutorialSearch]  

1.  Escriba `Cache-Control` y presione `Enter` .  El panel de búsqueda muestra todas las instancias de las `Cache-Control` que encuentra en los encabezados de recursos o en el contenido.  
    
    > ##### Ilustración 19  
    > Resultados de búsqueda de  `Cache-Control`  
    > ! [Resultados de la búsqueda de control de caché] [ImagesTutorialResults]  

1.  Seleccione un resultado para ver el recurso en el que se encontró el resultado.  Si está viendo los detalles del recurso, seleccione un resultado para ir directamente a él.  Por ejemplo, si la consulta se encuentra en un encabezado, se abre la pestaña encabezados.   Si la consulta se encuentra en el contenido, se abre la pestaña **respuesta** .  
    
    > ##### Ilustración 20  
    > Un resultado de búsqueda resaltado en la pestaña encabezados  
    > ! [Resultado de la búsqueda resaltado en la pestaña encabezados] [ImagesTutorialCache]  
    
1.  Cierre el panel de búsqueda y la pestaña encabezados.  
    
    > ##### Ilustración 21  
    > Los botones cerrar  
    > ! [Los botones cerrar] [ImagesTutorialCloseButtons]  
    
## Filtrar recursos   

DevTools proporciona numerosos flujos de trabajo para filtrar recursos que no son relevantes para la tarea que está realizando.  

> ##### Ilustración 22  
> La barra de herramientas filtros  
> ! [La barra de herramientas filtros] [ImagesTutorialFilters]  

La barra de herramientas **filtros** debería estar habilitada de forma predeterminada.  De lo contrario:  

1.  Seleccione filtro de **filtro** ![ ][ImageFilterIcon] para mostrarlo.  

### Filtrar por cadena, expresión regular o propiedad   

El cuadro de texto **filtro** admite muchos tipos de filtrado diferentes.  

1.  Escriba `png` en el cuadro de texto **filtro** .  Solo se muestran los archivos que contienen el texto `png` .  En este caso, los únicos archivos que coinciden con el filtro son las imágenes PNG.  
    
    > ##### Ilustración 23  
    > Un filtro de cadena  
    > ! [Un filtro de cadena] [ImagesTutorialPNG]  

1.  Escribe `/.*\.[cj]s+$/`.  DevTools filtra cualquier recurso con un nombre de archivo que no termina con un `j` o a `c` , seguido de 1 o más `s` caracteres.  
    
    > ##### Ilustración 24  
    > Filtro de expresión regular  
    > ! [Un filtro de expresiones regulares] [ImagesTutorialRegEx]  
    
1.  Escribe `-main.css`.  DevTools filtra `main.css` .  Si cualquier otro archivo coincide con el patrón, también se filtrarían.  
    
    > ##### Ilustración 25  
    > Un filtro negativo  
    > ! [Un filtro negativo] [ImagesTutorialNegative]  
    
1.  Escriba `domain:cdn.glitch.com` en el cuadro de texto **filtro** .  DevTools filtra cualquier recurso con una dirección URL que no coincida con este dominio.  
    
    > ##### Ilustración 26  
    > Un filtro de propiedad  
    > ! [Un filtro de propiedad] [ImagesTutorialProperty]  

    Vea [filtrar solicitudes por propiedades][DevtoolsReferenceProperty] para obtener una lista completa de las propiedades que se pueden filtrar.  
    
    
1.  Borre el cuadro de texto de **filtro** de cualquier texto.  

### Filtrar por tipo de recurso   

Para centrarse en un determinado tipo de archivo, como las hojas de estilos:  

1.  Seleccione **CSS**.  Se filtran todos los demás tipos de archivo.  
    
    > ##### Ilustración 27  
    > Mostrar solo archivos CSS  
    > ! [Solo mostrar archivos CSS] [ImagesTutorialCSS]  
    
1.  Para ver también las secuencias de comandos, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione **JS**.  
    
    > ##### Ilustración 28  
    > Mostrar solo archivos CSS y JS  
    > ! [Solo mostrar archivos CSS y JS] [ImagesTutorialCSSJS]  
    
1.  Seleccione **todo** para quitar los filtros y volver a ver todos los recursos.  

Consulte [filtrar solicitudes][DevtoolsNetworkReferenceFilter] para otros flujos de trabajo de filtrado.  

## Solicitudes de bloqueo   

¿Cómo se ve y se comporta una página cuando algunos de los recursos de la página no están disponibles?  ¿Se produce un error completamente o aún es funcional?  Bloquear solicitudes para averiguar:  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    > ##### Ilustración 29  
    > El menú de comandos  
    > ! [El menú comando] [ImagesTutorialCommandMenu]  
    
1.  Escriba `block` , seleccione **Mostrar bloqueo de solicitud**y presione `Enter` .  
    
    > ##### Ilustración 30  
    > Mostrar bloqueo de solicitud  
    > ! [Mostrar bloqueo de solicitudes] [ImagesTutorialBlock]  

1.  Seleccione **Agregar** patrón de adición de patrón ![ ][ImageAddIcon] .  
1.  Escribe `main.css`.  
    
    > ##### Ilustración 31  
    > Bugs `main.css`  
    > ! [Bloqueo de Main. CSS] [ImagesTutorialAddBlock]  
    
1.  Seleccione **Agregar**.  
1.  Vuelva a cargar la página.  Como se espera, el estilo de la página está ligeramente desordenado porque la hoja de estilos principal ha sido bloqueada.  
    
    > [!NOTE]
    > La `main.css` fila en el registro de red.  El texto en rojo significa que el recurso se ha bloqueado.
    
    > ##### Ilustración 32  
    > `main.css` ha sido bloqueado  
    > ! [se ha bloqueado Main. CSS] [ImagesTutorialBlockedStyles]  

1.  Anule la selección de la casilla de verificación **Activar bloqueo de solicitud** .  

## Conclusión  

Enhorabuena, ha completado el tutorial.  Ahora ya sabe cómo usar el panel red en el DevTools de Microsoft Edge.






Consulte la [referencia de red][DevtoolsNetworkReference] para descubrir más características de DevTools relacionadas con la inspección de la actividad de la red.  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Ilustración 1: la demostración"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Console.msft.png "Ilustración 2: la consola"  
[ImagesTutorialDocked]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Console-Bottom.msft.png "Ilustración 3: DevTools acoplado a la parte inferior de la ventana"  
[ImagesTutorialNetwork]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Bottom.msft.png "Ilustración 4: DevTools acoplada a la parte inferior de la ventana"  
[ImagesTutorialLog]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network.msft.png "Figura 5: el registro de red"  
[ImagesTutorialRuntime]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-New-Resource.msft.png "Ilustración 6: un nuevo recurso en el registro de red"  
[ImagesTutorialDomain]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Edit-Column.msft.png "Ilustración 7: habilitar la columna dominio"  
[ImagesTutorialThrottling]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-throttling.msft.png "Ilustración 8: habilitar la limitación de peticiones"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-throttling-Slow-3G.msft.png "Ilustración 9: selección de 3G lento"  
[ImagesTutorialHardReload]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Empty-cache-and-Hard-Reset.msft.png "Figura 10: memoria caché vacía y recarga en disco"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-screenshots.msft.png "ilustración 11: capturas de pantallas de la carga de la página"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-screenshots-First.msft.png "Ilustración 12: la actividad de red que se estaba realizando durante la primera captura de pantalla"  
[ImagesTutorialHeaders]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-headers.msft.png "ilustración 13: la pestaña encabezados"  
[ImagesTutorialPreview]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Preview.msft.png "Ilustración 14: ficha vista previa"  
[ImagesTutorialResponse]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Response.msft.png "Ilustración 15: la pestaña respuesta"  
[ImagesTutorialTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Timing.msft.png "Ilustración 16: ficha intervalos"  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Close-Tabs.msft.png "Ilustración 17: botón Cerrar"  
[ImagesTutorialSearch]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-Empty.msft.png "ilustración 18: el panel de búsqueda"  
[ImagesTutorialResults]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-cache-control.msft.png "Ilustración 19: resultados de la búsqueda de control de caché"  
[ImagesTutorialCache]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-cache-control-headers-Response-headers.msft.png "figura 20: un resultado de búsqueda resaltado en la pestaña encabezados"  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-Close.msft.png "ilustración 21: los botones cerrar"  
[ImagesTutorialFilters]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Empty.msft.png "Ilustración 22: la barra de herramientas filtros"  
[ImagesTutorialPNG]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-PNG.msft.png "Ilustración 23: un filtro de cadena"  
[ImagesTutorialRegEx]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Regex.msft.png "Ilustración 24: un filtro de expresiones regulares"  
[ImagesTutorialNegative]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-negative-Statement.msft.png "Ilustración 25: un filtro negativo"  
[ImagesTutorialProperty]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Property-Value.msft.png "ilustración 26: un filtro de propiedad"  
[ImagesTutorialCSS]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-file-type-CSS.msft.png "Ilustración 27: mostrar solo archivos CSS"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-file-type-CSS-JS.msft.png "Ilustración 28: mostrar solo archivos CSS y JS"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Empty.msft.png "Ilustración 29: el menú de comandos"  
[ImagesTutorialBlock]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block.msft.png "figura 30: mostrar el bloqueo de solicitudes"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Add-pattern.msft.png "Ilustración 31: bloqueo de Main. css"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Main-CSS.msft.png "ilustración 32: Main. CSS se ha bloqueado"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Referencia de análisis de red"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Solicitudes de filtro-referencia de análisis de red"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Ocultar el panel de información general: referencia de análisis de red"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Solicitudes de filtro por propiedades-referencia de análisis de red"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspeccionar demostración actividad de red"  

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
