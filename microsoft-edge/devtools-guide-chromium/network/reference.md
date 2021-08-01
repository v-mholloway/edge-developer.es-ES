---
description: Una referencia completa de las Microsoft Edge del panel DevTools Network.
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 93916c2ea65f9500ae0bf8a7a6e59caf45893bc1
ms.sourcegitcommit: 57f52b3edb34b8eb5389b746ff0970f7fd3b9a82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/31/2021
ms.locfileid: "11710768"
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
# <a name="network-analysis-reference"></a>Referencia de análisis de red  

Descubra nuevas formas de analizar cómo se carga la página en esta referencia completa de las Microsoft Edge de análisis de red de DevTools.  

## <a name="record-network-requests"></a>Registrar solicitudes de red  

De forma predeterminada, DevTools registra todas las solicitudes de red en la **herramienta Red,** siempre y cuando DevTools esté abierto.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panel Red" lightbox="../media/network-network-panel.msft.png":::
   La **herramienta Red**  
:::image-end:::  

### <a name="stop-recording-network-requests"></a>Detener la grabación de solicitudes de red  

Para detener la grabación de solicitudes, siga estos pasos.  

1.  En la **herramienta Red,** elija **Detener registro de red de grabación** \( Detener registro de red de grabación ![ ](../media/record-on-icon.msft.png) \).  Se vuelve gris para indicar que DevTools ya no está grabando solicitudes.  
1.  Seleccione `Control` + `E` \(Windows, Linux\) o `Command` + `E` \(macOS\) mientras la **herramienta Red** está en el foco.  

### <a name="clear-requests"></a>Borrar solicitudes  

Elija **Borrar** \( Borrar \) en la herramienta Red para borrar todas las ![ solicitudes de la tabla ](../media/clear-requests-icon.msft.png) Solicitudes. ****  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="El botón Borrar" lightbox="../media/network-network-clear-button.msft.png":::
   El **botón Borrar**  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a>Guardar solicitudes en cargas de página  

Para guardar las solicitudes en cargas de página, en la **herramienta Red,** active la casilla **Conservar registro.**  DevTools guarda todas las solicitudes hasta que deshabilita **Conservar registro**.  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="La casilla Conservar registro" lightbox="../media/network-network-preserve-log.msft.png":::
   La **casilla Conservar registro**  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a>Capturar capturas de pantalla durante la carga de página  

Captura capturas de pantalla para analizar las pantallas de los usuarios a la espera de que se cargue la página.  

Para habilitar capturas de pantalla, elija **Configuración de red**y, en la herramienta **Red,** active la **casilla Capturar capturas de** pantalla.  

Actualice la página mientras la **herramienta Red** está en el foco para capturar capturas de pantalla.  

Después de capturar una captura de pantalla, interactúas con ella de las siguientes maneras.  

*   Mantenga el mouse en una captura de pantalla para mostrar el punto en el que se capturó esa captura de pantalla.  Se muestra una línea amarilla en el **panel Información** general.  
*   Elige la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de capturar la captura de pantalla.  
*   Haz doble clic en una miniatura para ampliarla.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Mantener el mouse en una captura de pantalla" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Mantener el mouse en una captura de pantalla  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a>Cambiar el comportamiento de carga  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a>Emular a un visitante por primera vez deshabilitando la memoria caché del explorador  

Para emular el modo en que un usuario por primera vez experimenta su sitio, active la casilla **Deshabilitar caché.**  DevTools deshabilita la memoria caché del explorador.  Esta característica emula con mayor precisión la experiencia de un usuario por primera vez, ya que las solicitudes se sirven desde la memoria caché del explorador en las visitas repetidas.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Casilla Deshabilitar caché" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Casilla **Deshabilitar caché**  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a>Deshabilitar la memoria caché del explorador desde el cajón de condiciones de red  

Si desea deshabilitar la memoria caché mientras trabaja en otros paneles de DevTools, use el cajón Condiciones de red.  

1.  Abra el **cajón Condiciones de** red.  
1.  Active \(or off\) la casilla **Deshabilitar caché.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a>Borrar manualmente la memoria caché del explorador  

Para borrar manualmente la memoria caché del explorador en cualquier momento, abra el menú contextual \(hacer clic con el botón secundario\) en cualquier lugar de la tabla Solicitudes y elija Borrar caché **del explorador**.  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Elegir Borrar caché del explorador" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Elegir **Borrar caché del explorador**  
:::image-end:::  

### <a name="emulate-offline"></a>Emular sin conexión  

Una nueva clase de aplicaciones web, denominada [Progressive Web Apps][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores del servicio.**  Puede resultar útil simular rápidamente un dispositivo que no tiene conexión de datos al compilar este tipo de aplicación.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Elija el **menú desplegable En** línea, busque en **Preestablecidos**y elija **Sin** conexión para simular una experiencia de red sin conexión.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menú desplegable Sin conexión" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Menú **desplegable Sin** conexión  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a>Emular conexiones de red lentas  

Emular velocidades 3G, rápidas 3G y otras velocidades de conexión desde el **menú** desplegable En línea.  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menú desplegable Limitación" lightbox="../media/network-network-throttling-menu.msft.png":::
   Menú **desplegable Limitación**  
:::image-end:::  

Puede elegir entre diferentes presets, como Slow 3G o Fast 3G.  Para agregar sus propios ajustes preestablecidos personalizados, abra el menú Limitación y elija **Agregar**  >  **personalizado**.  

DevTools muestra un icono de advertencia junto a la **herramienta Red** para recordarle que la limitación está habilitada.  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a>Emular conexiones de red lentas desde el cajón de condiciones de red  

Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón Condiciones de red.  

1.  Abra el **cajón Condiciones de** red.  
1.  Elija la velocidad de conexión en el menú **Limitación.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a>Borrar manualmente las cookies del explorador  

Para borrar manualmente las cookies del explorador en cualquier momento, mantenga el mouse en cualquier lugar de la tabla Solicitudes, abra el menú contextual \(hacer clic con el botón secundario en\) y elija **Borrar cookies del explorador**.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Elegir Borrar cookies del explorador" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Elegir **Borrar cookies del explorador**  
:::image-end:::  

### <a name="override-the-user-agent"></a>Invalidar el agente de usuario  

Para invalidar manualmente el agente de usuario, siga estos pasos.  

1.  Abra el **cajón Condiciones de** red.  
1.  Desactive la **casilla Seleccionar automáticamente.**  
1.  Elija una opción de agente de usuario en el menú o escriba un agente de usuario personalizado en el cuadro de texto.  

## <a name="set-user-agent-client-hints"></a>Establecer sugerencias de cliente de agente de usuario

Si el sitio usa sugerencias de cliente de agente de [usuario,](../../web-platform/user-agent-guidance.md)use el panel **Condiciones** de red para proporcionar sugerencias de cliente de agente de usuario diferentes.

1. Abra el **menú contextual** (haga clic con el botón secundario) y elija **Inspeccionar**.
1. Elija **Condiciones de**  >  **red**.
1. En el panel Agente de usuario desactive la casilla **Usar explorador predeterminado** y, a continuación, elija Sugerencias de cliente de agente de **usuario.**

    :::image type="complex" source="images/network-conditions-user-agent-client-hints.msft.png" alt-text="Establecer sugerencias de cliente de agente de usuario" lightbox="images/network-conditions-user-agent-client-hints.msft.png":::
        Establecer sugerencias de cliente de agente de usuario  
    :::image-end::: 

1. Acepte el valor predeterminado de **Custom...** o elija un explorador y un dispositivo predefinidos en la lista desplegable.
1. Para cualquiera de las opciones, establezca las sugerencias del cliente del agente de usuario de la siguiente manera.
    * **Marca** y **versión** como *Edge* y *92*. Elija **+ Agregar marca** para agregar varios pares de marca y versión.
    * **Versión completa del explorador** como *92.0.1111.0*.
    * **Plataforma** y **versión** como *Windows* *y 10.0*.
    * **Arquitectura** como *x86*.
    * **Modelo de dispositivos** como *Galaxy Nexus*.

    > [!NOTE]
    > Establezca o cambie cualquiera de las sugerencias de cliente del agente de usuario. No hay valores necesarios.

1. Selecciona **Actualización**. 
1. Para comprobar los cambios, elija **Consola** y escriba `navigator.userAgentData` . Expanda los resultados según sea necesario para ver los cambios en los datos del agente de usuario.

También puede establecer sugerencias de cliente de agente de usuario en [Emular dispositivos móviles en Microsoft Edge](../device-mode/index.md).  

## <a name="filter-requests"></a>Solicitudes de filtro  

### <a name="filter-requests-by-properties"></a>Filtrar solicitudes por propiedades  

Use el **cuadro de** texto Filtrar para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.  

Si no se muestra el cuadro de texto, es probable que el panel **Filtros** esté oculto.  
Para obtener más información, vaya [a Ocultar el panel Filtros](#hide-the-filters-pane).  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Cuadro de texto Filtrar" lightbox="../media/network-network-filters-textbox.msft.png":::
   Cuadro **de texto** Filtrar  
:::image-end:::  

Puede usar varias propiedades simultáneamente separando cada propiedad con un espacio.  Por ejemplo, `mime-type:image/png larger-than:1K` muestra todos los PNG de más de 1 kilobyte.  Los filtros multi-propiedad son equivalentes a `AND` las operaciones.  `OR` actualmente no se admiten operaciones.  

Lista completa de propiedades admitidas.  

| Propiedad | Detalles |  
|:--- | :--- |  
| `domain` | Solo mostrar recursos del dominio especificado.  Puede usar un carácter comodín \( `*` \) para incluir varios dominios.  Por ejemplo, `*.com` muestra recursos de todos los nombres de dominio que terminan en `.com` .  DevTools rellena el menú desplegable de autocompletar con todos los dominios que se encuentran. |  
| `has-response-header` | Muestra los recursos que contienen el encabezado de respuesta HTTP especificado.  DevTools rellena el desplegable de autocompletar con todos los encabezados de respuesta que se encuentran. |  
| `is` | Se `is:running` usa para buscar `WebSocket` recursos. |  
| `larger-than` | Muestra recursos que son mayores que el tamaño especificado, en bytes.  Establecer un valor de `1000` equivale a establecer un valor de `1k` . |  
| `method` | Muestra los recursos que se recuperaron a través de un tipo de método HTTP especificado.  DevTools rellena el desplegable con todos los métodos HTTP que se encuentran. |  
| `mime-type` | Muestra recursos de un tipo MIME especificado.  DevTools rellena el desplegable con todos los tipos MIME que se encuentran. |  
| `mixed-content` | Mostrar todos los recursos de contenido combinado \( \) o solo los que se muestran `mixed-content:all` actualmente \( `mixed-content:displayed` \). |  
| `scheme` | Muestra los recursos recuperados a través de HTTP sin protección \( `scheme:http` \) o HTTPS protegido \( `scheme:https` \). |  
| `set-cookie-domain` | Muestra recursos que tienen un `Set-Cookie` encabezado con un atributo que coincide con el valor `Domain` especificado.  DevTools rellena el autocompletar con todos los dominios de cookie que se encuentran. |  
| `set-cookie-name` | Muestra recursos que tienen un `Set-Cookie` encabezado con un nombre que coincide con el valor especificado.  DevTools rellena el autocompletar con todos los nombres de cookie que se encuentran. |  
| `set-cookie-value` | Muestra recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.  DevTools rellena el autocompletar con todos los valores de cookie que se encuentran. |  
| `status-code` | Muestra recursos que coinciden con el código de estado HTTP específico.  DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que se encuentran. |  

### <a name="filter-requests-by-type"></a>Filtrar solicitudes por tipo  

Para filtrar las solicitudes por tipo de solicitud, elija uno de los botones siguientes en la **herramienta Red.**  

:::row:::
   :::column span="1":::
      **XHR**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **JS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **CSS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Img**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Multimedia**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Fuente**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Doc**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **WS**  
   :::column-end:::
   :::column span="2":::
      WebSocket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Manifiesto**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Otros**  
   :::column-end:::
   :::column span="2":::
      Cualquier otro tipo que no aparezca.  
   :::column-end:::
:::row-end:::  

Si los botones no se muestran, el **panel Filtros** puede estar oculto.  
Para obtener más información, vaya [a Ocultar el panel Filtros](#hide-the-filters-pane).  

Para habilitar varios filtros de tipo simultáneamente, mantenga presionado `Control` \(Windows, Linux\) o `Command` \(macOS\) y, a continuación, elija.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Usar los filtros De tipo para mostrar recursos JS, CSS y Document" lightbox="../media/network-network-type-filters.msft.png":::
   Usar los filtros De tipo para mostrar recursos JS, CSS y Document  
:::image-end:::  

### <a name="filter-requests-by-time"></a>Filtrar solicitudes por tiempo  

Elija y arrastre a la izquierda o a la derecha en **el** panel Información general para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.  El filtro es inclusivo.  Se muestra cualquier solicitud que estuvo activa durante el tiempo resaltado.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrar las solicitudes que estaban inactivas alrededor de 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   Filtrar las solicitudes que estaban inactivas alrededor de 300 ms  
:::image-end:::  

### <a name="hide-data-urls"></a>Ocultar direcciones URL de datos  

[Las direcciones URL de datos][MDNHTTPDataURIs] son archivos pequeños incrustados en otros documentos.  Cualquier solicitud que se muestra en la tabla Solicitudes que comienza por `data:` es una dirección URL de datos.  

Para ocultar las solicitudes, desactive la casilla Ocultar direcciones **URL de** datos.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Casilla Ocultar direcciones URL de datos" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Casilla **Ocultar direcciones URL de datos**  
:::image-end:::  

## <a name="sort-requests"></a>Ordenar solicitudes  

De forma predeterminada, las solicitudes de la tabla Solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla con otros criterios.  

### <a name="sort-by-column"></a>Ordenar por columna  

Elija el encabezado de cualquier columna de las solicitudes para ordenar las solicitudes por esa columna.  

### <a name="sort-by-activity-phase"></a>Ordenar por fase de actividad  

Para cambiar el modo en que la cascada ordena las solicitudes, mantenga el mouse en el encabezado de la tabla Solicitudes, abra el menú contextual \(hacer clic con el botón secundario\), mantenga el mouse en **Cascada**y elija una de las siguientes opciones.  

:::row:::
   :::column span="1":::
      **Hora de inicio**  
   :::column-end:::
   :::column span="2":::
      La primera solicitud que se inició está en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tiempo de respuesta**  
   :::column-end:::
   :::column span="2":::
      La primera solicitud que se inició la descarga está en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Hora de finalización**  
   :::column-end:::
   :::column span="2":::
      La primera solicitud que ha finalizado está en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Duración total**  
   :::column-end:::
   :::column span="2":::
      La solicitud con la configuración de conexión más corta y la solicitud o respuesta está en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Latencia**  
   :::column-end:::
   :::column span="2":::
      La solicitud que ha esperado más tiempo para obtener una respuesta está en la parte superior.  
   :::column-end:::
:::row-end:::  

Estas descripciones suponen que cada opción respectiva se clasifica de más corta a más larga.  Elija el encabezado de la columna **Cascada** para invertir el orden.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Ordenar la cascada por duración total" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Ordenar la cascada por duración total \(La parte más ligera de cada barra es el tiempo invertido en espera y la parte más oscura es el tiempo invertido en descargar bytes\)  
:::image-end:::  

## <a name="analyze-requests"></a>Analizar solicitudes  

Mientras DevTools está abierto, registra todas las solicitudes en la **herramienta Red.**  
Use el panel Red para analizar las solicitudes.  

### <a name="display-a-log-of-requests"></a>Mostrar un registro de solicitudes  

Use la tabla Solicitudes para mostrar un registro de todas las solicitudes realizadas mientras devTools se han abierto.  Para mostrar más información sobre cada elemento, elija o mantenga el mouse en las solicitudes.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="La tabla Solicitudes" lightbox="../media/network-network-requests-table.msft.png":::
   La tabla Solicitudes  
:::image-end:::  

La tabla Solicitudes muestra las siguientes columnas de forma predeterminada.  

:::row:::
   :::column span="1":::
      **Nombre**  
   :::column-end:::
   :::column span="2":::
      Nombre de archivo o identificador del recurso.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Estado**  
   :::column-end:::
   :::column span="2":::
      El código de estado HTTP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tipo**  
   :::column-end:::
   :::column span="2":::
      Tipo MIME del recurso solicitado.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Iniciador**  
   :::column-end:::
   :::column span="2":::
      Los siguientes objetos o procesos inician solicitudes.  
      
      *   **Analizador**  El analizador HTML para Microsoft Edge.  
      *   **Redirigir**  Redireccionamiento HTTP.  
      *   **Script**  Una función JavaScript.  
      *   **Otros**  Otro proceso o acción, como navegar a una página mediante un vínculo o escribir una dirección URL en la barra de direcciones.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tamaño**  
   :::column-end:::
   :::column span="2":::
      El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, según lo entregado por el servidor.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tiempo**  
   :::column-end:::
   :::column span="2":::
      La duración total, desde el inicio de la solicitud hasta la recepción del byte final en la respuesta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Cascada](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Un desglose visual de la actividad de cada solicitud.  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a>Agregar o quitar columnas  

Mantenga el mouse en el encabezado de la tabla Solicitudes, abra el menú contextual \(hacer clic con el botón secundario\) y elija una opción para ocultarla o mostrarla.  Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Agregar una columna a la tabla Solicitudes" lightbox="../media/network-network-requests-add-column.msft.png":::
   Agregar una columna a la tabla Solicitudes  
:::image-end:::  

#### <a name="add-custom-columns"></a>Agregar columnas personalizadas  

Para agregar una columna personalizada a la tabla Solicitudes, mantenga el mouse en el encabezado de la **** tabla Solicitudes, abra el menú contextual \(clic con el botón derecho\) y elija Encabezados de respuesta Administrar columnas de  >  **encabezado**.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Agregar una columna personalizada a la tabla Solicitudes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Agregar una columna personalizada a la tabla Solicitudes  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a>Mostrar la relación de tiempo de las solicitudes  

Use la cascada para mostrar las relaciones de tiempo de las solicitudes.  
La organización predeterminada de la cascada usa la hora de inicio de las solicitudes.  
Por lo tanto, las solicitudes que están más lejos de la izquierda se iniciaron antes que las solicitudes que están más lejos de la derecha.  

Para revisar las distintas formas de ordenar la cascada, vaya a [Ordenar por fase de actividad](#sort-by-activity-phase).  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="La columna Cascada del panel Solicitudes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   La columna Cascada del **panel Solicitudes**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <a name="display-a-preview-of-a-response-body"></a>Mostrar una vista previa de un cuerpo de respuesta  

Para mostrar una vista previa de un cuerpo de respuesta, siga estos pasos.  

1.  Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.  
1.  Elija el panel **Vista** previa.  

La pestaña Vista previa es principalmente útil para mostrar imágenes.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="El panel Vista previa" lightbox="../media/network-network-resources-preview.msft.png":::
   El panel **Vista** previa  
:::image-end:::  

### <a name="display-a-response-body"></a>Mostrar un cuerpo de respuesta  

Para mostrar el cuerpo de la respuesta a una solicitud, siga estos pasos.  

1.  Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.  
1.  Elija **el** panel Respuesta.  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="El panel Respuesta" lightbox="../media/network-network-resources-response.msft.png":::
   El panel **Respuesta**  
:::image-end:::  

### <a name="display-http-headers"></a>Mostrar encabezados HTTP  

Para mostrar datos de encabezado HTTP sobre una solicitud, siga estos pasos.  

1.  Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.  
1.  Elija el panel **Encabezados.**  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Panel Encabezados" lightbox="../media/network-resources-headers.msft.png":::
   Panel **Encabezados**  
:::image-end:::  

#### <a name="display-http-header-source"></a>Mostrar origen de encabezado HTTP  

De forma predeterminada, el panel **Encabezados** muestra los nombres de encabezado alfabéticamente.  Para mostrar los nombres de encabezado HTTP en el orden recibido, siga estos pasos.  

1.  Abra el panel **Encabezados** para la solicitud que le interese.  Para obtener más información, vaya [a Mostrar encabezados HTTP](#display-http-headers).  
1.  Elija **ver origen**, junto a la sección Encabezado de **solicitud** o Encabezado **de** respuesta.  

### <a name="display-query-string-parameters"></a>Mostrar parámetros de cadena de consulta  

Para mostrar los parámetros de cadena de consulta de una dirección URL en un formato legible, siga estos pasos.  

1.  Abra el panel **Encabezados** para la solicitud que le interese.  Para obtener más información, vaya [a Mostrar encabezados HTTP](#display-http-headers).  
1.  Vaya a la **sección Parámetros de cadena de** consulta.  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Sección Parámetros de cadena de consulta" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Sección **Parámetros de cadena de** consulta  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a>Mostrar origen de parámetros de cadena de consulta  

Para mostrar el origen del parámetro de cadena de consulta de una solicitud, siga estos pasos.  

1.  Vaya a la sección Parámetros de cadena de consulta.  Para obtener más información, vaya [a Mostrar parámetros de cadena de consulta](#display-query-string-parameters).  
1.  Elija **ver origen**.  

#### <a name="display-url-encoded-query-string-parameters"></a>Mostrar parámetros de cadena de consulta con codificación URL  

Para mostrar parámetros de cadena de consulta en un formato legible, pero con codificaciones conservadas, siga estos pasos.  

1.  Vaya a la sección Parámetros de cadena de consulta.  Para obtener más información, vaya [a Mostrar parámetros de cadena de consulta](#display-query-string-parameters).  
1.  Elija **ver dirección URL codificada**.  

### <a name="display-cookies"></a>Mostrar cookies  

Para mostrar las cookies enviadas en el encabezado HTTP de una solicitud, siga estos pasos.  

1.  Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.  
1.  Elija el **panel Cookies.**  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="El panel Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   El panel Cookies  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a>Mostrar el desglose de tiempo de una solicitud  

Para mostrar el desglose de tiempo de una solicitud, siga estos pasos.  

1.  Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.  
1.  Elija **** el panel Temporización.  

Para obtener una forma más rápida de obtener acceso a los datos, vaya [a Vista previa de un desglose de tiempo.](#preview-a-timing-breakdown)  

Para obtener más información acerca de cada una de las fases que se pueden mostrar en el **panel** Temporización, vaya a Fases de desglose de [tiempo explicadas.](#timing-breakdown-phases-explained)  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="El panel Temporización" lightbox="../media/network-network-resources-timing.msft.png":::
   El panel **Temporización**  
:::image-end:::  

Más información sobre cada una de las fases.  

Para obtener más información acerca del acceso a la pantalla, vaya a Mostrar desglose [de tiempo.](#display-the-timing-breakdown-of-a-request)  

#### <a name="preview-a-timing-breakdown"></a>Obtener una vista previa de un desglose de tiempo  

Para mostrar una vista previa del desglose de tiempo de una solicitud, en la columna **Cascada** de la tabla Solicitudes, mantenga el mouse sobre la entrada de la solicitud.  

Para obtener más información acerca de cómo obtener acceso a los datos sin mantener el mouse, vaya [a Mostrar el desglose de tiempo de una solicitud](#display-the-timing-breakdown-of-a-request).  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> vista previa del desglose de tiempo de una solicitud" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Obtener una vista previa del desglose de tiempo de una solicitud  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a>Fases de desglose de tiempo explicadas  

Más información sobre cada una de las fases que se pueden mostrar en el panel **De tiempo.**  

:::row:::
   :::column span="1":::
      **Cola**  
   :::column-end:::
   :::column span="2":::
      El explorador pone en cola las solicitudes cuando se cumple cualquiera de las siguientes opciones.  
      
      *   Existen solicitudes de mayor prioridad.  
      *   Seis conexiones TCP están abiertas para el mismo origen, que es el límite.  Solo se aplica a HTTP/1.0 y HTTP/1.1.  
      *   El explorador asigna brevemente espacio en la memoria caché de disco.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Detenido**  
   :::column-end:::
   :::column span="2":::
      La solicitud se detiene por cualquiera de los motivos descritos en **Queueing**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Búsqueda DNS**  
   :::column-end:::
   :::column span="2":::
      El explorador está resolviendo la dirección IP de la solicitud.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Conexión inicial**  
   :::column-end:::
   :::column span="2":::
      El explorador establece una conexión que incluye protocolos de enlace TCP, reintentos TCP y negocia una capa de socket seguro.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Negociación de proxy**  
   :::column-end:::
   :::column span="2":::
      El explorador está negociando la solicitud con un [servidor proxy.][WikiProxyServer]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Solicitud enviada**  
   :::column-end:::
   :::column span="2":::
      Se envía la solicitud.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Preparación de ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      El explorador está iniciando el trabajador del servicio.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Solicitud a ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      La solicitud se envía al trabajador del servicio.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Waiting \(TTFB\)**  
   :::column-end:::
   :::column span="2":::
      El explorador está esperando el primer byte de una respuesta.  TTFB significa Time To First Byte.  Este tiempo incluye un recorrido de ida y vuelta de latencia y el tiempo que el servidor tardó en preparar la respuesta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Descarga de contenido**  
   :::column-end:::
   :::column span="2":::
      El explorador recibe la respuesta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Recepción de inserción**  
   :::column-end:::
   :::column span="2":::
      El explorador está recibiendo datos para esta respuesta a través de HTTP/2 Server Push.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Inserción de lectura**  
   :::column-end:::
   :::column span="2":::
      El explorador está leyendo los datos locales recibidos anteriormente.  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a>Mostrar iniciadores y dependencias  

Para mostrar los iniciadores y las dependencias de una solicitud, mantenga y mantenga el mouse sobre la solicitud `Shift` en la tabla Solicitudes.  Colores de DevTools: los iniciadores se muestran en verde y las dependencias se muestran en rojo.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Mostrar los iniciadores y las dependencias de una solicitud" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Mostrar los iniciadores y las dependencias de una solicitud  
:::image-end:::  

Cuando la tabla Solicitudes se ordena cronológicamente, si mantiene el mouse en una línea, la línea anterior muestra una solicitud verde.  La solicitud verde es el iniciador de la dependencia.  Si se muestra otra solicitud verde en la línea anterior, esa solicitud superior es el iniciador del iniciador.  Etcétera.  

### <a name="display-load-events"></a>Mostrar eventos de carga  

DevTools muestra el tiempo de los `DOMContentLoaded` eventos y en varios lugares de la herramienta `load` **Red.**  El `DOMContentLoaded` evento tiene un color azul y el evento es `load` rojo.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Ubicaciones de los eventos DOMContentLoaded y load en el panel Red" lightbox="../media/network-network-requests-load-events.msft.png":::
   Ubicaciones de los `DOMContentLoaded` eventos y en la herramienta `load` **Red**  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a>Mostrar el número total de solicitudes  

El número total de solicitudes se muestra en el **panel Resumen,** en la parte inferior de la **herramienta Red.**  

> [!CAUTION]
> Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.  Si se produjeron otras solicitudes antes de abrir DevTools, estas solicitudes no se cuentan.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="El número total de solicitudes desde que Se abrieron DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   El número total de solicitudes desde que Se abrieron DevTools  
:::image-end:::  

### <a name="display-the-total-download-size"></a>Mostrar el tamaño total de descarga  

El tamaño total de descarga de las solicitudes se muestra en el **panel Resumen,** en la parte inferior de la **herramienta Red.**  

> [!CAUTION]
> Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.  Si se produjeron otras solicitudes antes de abrir DevTools, las solicitudes anteriores no se cuentan.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="El tamaño total de descarga de las solicitudes" lightbox="../media/network-network-total-download-size.msft.png":::
   El tamaño total de descarga de las solicitudes  
:::image-end:::  

Para comprobar el tamaño de los recursos grandes después de que el explorador descomprime cada elemento, navegue para mostrar el tamaño sin [comprimir de un recurso](#display-the-uncompressed-size-of-a-resource).  

### <a name="display-the-stack-trace-that-caused-a-request"></a>Mostrar el seguimiento de pila que causó una solicitud  

Después de que una instrucción JavaScript solicite un recurso, mantenga el mouse en la columna **Iniciador** para mostrar el seguimiento de la pila que conduce a la solicitud.  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Seguimiento de pila que conduce a una solicitud de recurso" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Seguimiento de pila que conduce a una solicitud de recurso  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a>Mostrar el tamaño sin comprimir de un recurso  

Active la casilla **Usar filas de solicitud grandes** y, a continuación, revise el valor inferior de la **columna** Tamaño.  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Un ejemplo de recursos sin comprimir" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Un ejemplo de recursos sin comprimir \(El tamaño comprimido del archivo que se envió a través de la red era , mientras que el tamaño sin comprimir `jquery-3.3.1.min.js` `29.9 KB` era `84.9 KB` \)  
:::image-end:::  

## <a name="export-requests-data"></a>Exportar datos de solicitudes  

### <a name="save-all-network-requests-to-a-har-file"></a>Guardar todas las solicitudes de red en un archivo HAR  

Para guardar todas las solicitudes de red en un archivo HAR, siga estos pasos.  

1.  Mantenga el mouse sobre cualquier solicitud de la tabla Solicitudes y abra el menú contextual \(hacer clic con el botón secundario\).  
1.  Elija **Guardar como HAR con contenido**.  DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.  No puede filtrar solicitudes.  Tampoco puede guardar una sola solicitud.  

Una vez guardado un archivo HAR, puede volver a importarlo en DevTools para su análisis.  Basta con arrastrar y colocar el archivo HAR en la tabla Solicitudes.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Elija Guardar como HAR con contenido" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Elija **Guardar como HAR con contenido**  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a>Copiar una o más solicitudes en el Portapapeles  

En la **columna Nombre** de la tabla Solicitudes, mantenga el mouse en una solicitud, abra el menú contextual \(clic con el botón derecho\), mantenga el mouse en **Copiar**y elija una de las siguientes opciones.  

| Nombre | Detalles |  
|:--- |:--- |  
| **Copiar dirección de vínculo** | Copie la dirección URL de la solicitud en el Portapapeles. |  
| **Copiar respuesta** | Copie el cuerpo de la respuesta en el Portapapeles. |  
| **Copiar como captura** | &nbsp; |  
| **Copiar como cURL** | Copie la solicitud como un comando cURL. |  
| **Copiar todo como captura** | &nbsp; |  
| **Copiar todo como cURL** | Copie todas las solicitudes como una cadena de comandos cURL. |  
| **Copiar todo como HAR** | Copie todas las solicitudes como datos de HAR. |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Elegir copiar respuesta" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Elegir **copiar respuesta**  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a>Copiar JSON de respuesta con formato en el Portapapeles  

Elija una solicitud de red y vaya al **panel Encabezados.**  Para copiar el valor JSON de una respuesta, vaya a Carga de solicitud **,** mantenga el mouse en el contenido de la respuesta JSON, abra el menú contextual \(haga clic con el botón secundario en\) y elija **Copiar valor**.  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copiar valor en el menú contextual" lightbox="../media/network-header-copy-property-value.msft.png":::
          **Copiar valor** en el menú contextual  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Microsoft Visual Studio Código con JSON de respuesta con formato" lightbox="../media/network-header-paste-property-value.msft.png":::
          Pegar JSON de respuesta con formato en Microsoft Visual Studio código  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a>Copiar valores de propiedad de solicitudes de red en el Portapapeles  

Para copiar valores de propiedad de solicitudes de red en el Portapapeles, realice las siguientes acciones.  

1.  Abra el **panel Encabezados.**  
1.  Abra una de las siguientes secciones de encabezado.  
    *   Carga de solicitud \(JSON\)  
    *   Datos del formulario  
    *   Parámetros de cadena de consulta  
    *   Encabezados de solicitud  
    *   Encabezados de respuesta  
1.  Abra el menú contextual \(clic con el botón secundario\) > **Valor de copia**.  Ahora puede pegar el valor en cualquier editor para revisarlo.  
    
## <a name="change-the-layout-of-the-network-panel"></a>Cambiar el diseño del panel Red  

Puedes expandir o contraer secciones de la interfaz de usuario de la herramienta **de** red para centrar información importante.  

### <a name="hide-the-filters-pane"></a>Ocultar el panel Filtros  

De forma predeterminada, DevTools muestra el **panel Filtros.**  
Elija **Filtro** \( ![ Filtro ](../media/filter-icon.msft.png) \) para ocultarlo.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="El botón Ocultar filtros" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   El botón Ocultar filtros  
:::image-end:::  

### <a name="use-large-request-rows"></a>Usar filas de solicitud grandes  

Use filas grandes cuando desee más espacios en blanco en la tabla de solicitudes de red.  Algunas columnas también proporcionan un poco más de información al usar filas grandes.  Por ejemplo, el valor inferior de la **columna Size** es el tamaño sin comprimir de una solicitud.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Un ejemplo de filas de solicitudes grandes en el panel Solicitudes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Un ejemplo de filas de solicitudes grandes en el **panel Solicitudes**  
:::image-end:::  

Para habilitar filas grandes, active la casilla **Usar filas de solicitud grandes.**  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Casilla Usar filas de solicitud grandes" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Casilla **Usar filas de solicitud grandes**  
:::image-end:::  

### <a name="hide-the-overview-pane"></a>Ocultar el panel Información general  

De forma predeterminada, DevTools muestra el **panel Información** general.  Para ocultarlo, desactiva la casilla **Mostrar información general.**  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Casilla Mostrar información general" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Casilla **Mostrar información general**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Depurar aplicaciones web progresivas | Microsoft Docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Direcciones URL de datos | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy- Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
