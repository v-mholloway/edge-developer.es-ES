---
description: Una referencia completa de las características del panel de red de Microsoft Edge DevTools.
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 758623482ab2179987c6467f8e30c72d8893d710
ms.sourcegitcommit: addfd27bb765c92880a59f259dc702f6e4e1bf28
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "11092317"
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

# Referencia de análisis de red  

Descubra nuevas formas de analizar cómo se carga su página en esta referencia completa de las características de análisis de red de Microsoft Edge DevTools.  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## Registrar solicitudes de red  

De forma predeterminada, DevTools graba todas las solicitudes de red en el panel red, siempre y cuando DevTools esté abierto.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panel red" lightbox="../media/network-network-panel.msft.png":::
   Panel **red**  
:::image-end:::  

### Detener la grabación de solicitudes de red  

Siga los pasos que se indican a continuación para detener la grabación de solicitudes.  

1.  Seleccione **Detener grabación de registro de red** \ ( ![ Detener grabación ][ImageRecordOnIcon] de registro de red \) en el panel **red** .  Se vuelve gris para indicar que DevTools ya no graba solicitudes.  
1.  Pulse `Control` + `E` \ (Windows \) o `Command` + `E` \ (MacOS \) mientras el panel **red** está en el foco.  

### Borrar solicitudes  

Seleccione **Borrar** \ ( ![ Borrar ][ImageClearIcon] \) en el panel red para borrar todas las solicitudes de la tabla solicitudes.  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Panel red" lightbox="../media/network-network-clear-button.msft.png":::
   Botón **Borrar**  
:::image-end:::  

### Guardar solicitudes en la carga de páginas  

Para guardar las solicitudes en la carga de la página, active la casilla **conservar registro** en el panel red.  DevTools guarda todas las solicitudes hasta que Deshabilites **conservar registro**.  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Panel red" lightbox="../media/network-network-preserve-log.msft.png":::
   Casilla de verificación **conservar registro**  
:::image-end:::  

### Capturar capturas de pantallas durante la carga de la página  

Capture las capturas de pantallas para analizar qué se muestra para los usuarios mientras esperan la página que desea cargar.  

Para habilitar capturas de pantalla, seleccione **configuración de red** y marque la casilla **capturar capturas** de pantalla en el panel **red** .  

Actualice la página mientras el panel **red** está enfocado para capturar capturas de pantalla.  

Después de capturar una captura de pantalla, puede interactuar con ella de las siguientes maneras.  

*   Desplace el puntero sobre una captura de pantalla para ver el punto en el que se capturó la captura de pantalla.  Se muestra una línea amarilla en el panel de **información general** .  
*   Seleccione la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de que se capturó la captura de pantalla.  
*   Haga doble clic en una miniatura para acercarla.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Panel red" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Colocar el puntero sobre una captura de pantalla  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Panel red" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## Cambiar el comportamiento de carga  

### Emular a un primer visitante mediante la deshabilitación de la memoria caché del explorador  

Para emular el funcionamiento de su sitio por primera vez, active la casilla **deshabilitar la caché** .  DevTools deshabilita la caché del explorador.  Esta característica emula con más precisión la experiencia de un usuario por primera vez, ya que las solicitudes se proporcionan desde la memoria caché del explorador al repetir visitas.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Panel red" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Casilla **deshabilitar caché**  
:::image-end:::  

#### Deshabilitar la memoria caché del explorador en el cajón de condiciones de red  

Si desea deshabilitar la caché mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.  

1.  Abra el cajón de **condiciones de redes** .  
1.  Active o desactive la casilla **deshabilitar caché** .  

<!--todo: add network condition section when available -->  

### Borrar manualmente la memoria caché del explorador  

Para borrar manualmente la memoria caché del explorador en cualquier momento, abra el menú contextual \ (haga clic con el botón secundario del mouse \) en cualquier lugar de la tabla solicitudes y seleccione **Borrar caché del explorador**.  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Panel red" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Selección de **Borrar caché del explorador**  
:::image-end:::  

### Emular sin conexión  

Una nueva clase de aplicaciones Web, denominada [aplicaciones web progresivas][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores de servicio**.  Es posible que le resulte útil simular rápidamente un dispositivo que no tiene conexión de datos cuando está creando este tipo de aplicación.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Seleccione el menú desplegable **en línea** , búsqueda en **preestablecidos**y seleccione **sin conexión** para simular una experiencia de red sin conexión.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Panel red" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Menú desplegable **desconectado**  
:::image-end:::  

### Emular conexiones de red lentas  

Emular 3G lento, 3G rápido y otras velocidades de conexión en el menú desplegable **en línea** .  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Panel red" lightbox="../media/network-network-throttling-menu.msft.png":::
   El menú desplegable **limitación de peticiones**  
:::image-end:::  

Puedes elegir entre diferentes ajustes preestablecidos, como 3G lento o 3G rápido.  También puede agregar sus propios ajustes preestablecidos personalizados abriendo el menú de limitación y seleccionando **Custom**  >  **añadir**personalizados.  

DevTools muestra un icono de advertencia junto a la pestaña **red** para recordarle que la limitación está habilitada.  

#### Emular conexiones de red lentas del cajón de condiciones de red  

Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.  

1.  Abra el cajón de **condiciones de redes** .  
1.  Seleccione la velocidad de conexión en el menú **limitación** .  

<!--todo: add network condition section when available -->  

### Borrar manualmente las cookies del explorador  

Para borrar manualmente las cookies del explorador en cualquier momento, abra el menú contextual \ (haga clic con el botón secundario del mouse \) en cualquier lugar de la tabla solicitudes y seleccione **Borrar cookies del explorador**.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Panel red" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Selección de las **cookies de borrar explorador**  
:::image-end:::  

### Invalidar el agente de usuario  

Para anular manualmente el agente de usuario, siga estos pasos.  

1.  Abra el cajón de **condiciones de redes** .  
1.  Desactive **seleccionar automáticamente**.  
1.  Elija una opción de agente de usuario en el menú o escriba una personalizada en el cuadro de texto.  

<!--todo: add network condition section when available -->  

## Filtrar solicitudes  

### Filtrar las solicitudes por propiedades  

Use el cuadro de texto **filtrar** para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.  

Si no se muestra el cuadro de texto, es probable que el panel **filtros** esté oculto.  
Para obtener más información, vaya a [ocultar el panel de filtros](#hide-the-filters-pane).  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Panel red" lightbox="../media/network-network-filters-textbox.msft.png":::
   El cuadro de texto **filtro**  
:::image-end:::  

Puede usar varias propiedades simultáneamente al separar cada propiedad con un espacio.  Por ejemplo, `mime-type:image/png larger-than:1K` se muestran todos los PNGs que tengan más de 1 kilobyte.  Los filtros de varias propiedades son equivalentes a `AND` las operaciones.  `OR` Actualmente no se admiten las operaciones.  

La lista completa de propiedades compatibles.  

| Propiedad | Detalles |  
|:--- | :--- |  
| `domain` | Mostrar solo los recursos del dominio especificado.  Puede usar un carácter comodín \ ( `*` \) para incluir varios dominios.  Por ejemplo, `*.com` muestra los recursos de todos los nombres de dominio que terminan en `.com` .  DevTools rellenar el menú desplegable de autocompletar con todos los dominios que se encuentran. |  
| `has-response-header` | Muestra los recursos que contienen el encabezado de respuesta HTTP especificado.  DevTools rellenar la lista desplegable de autocompletar con todos los encabezados de respuesta que se encuentran. |  
| `is` | Usar `is:running` para buscar `WebSocket` recursos. |  
| `larger-than` | Muestra los recursos que son mayores que el tamaño especificado, en bytes.  Establecer un valor de `1000` es equivalente a establecer un valor de `1k` . |  
| `method` | Muestra los recursos que se recuperaron en un tipo de método HTTP especificado.  DevTools rellenar la lista desplegable con todos los métodos HTTP que se encuentran. |  
| `mime-type` | Muestra los recursos de un tipo MIME especificado.  DevTools rellenar la lista desplegable con todos los tipos MIME que se encuentran. |  
| `mixed-content` | Mostrar todos los recursos de contenido mixto \ ( `mixed-content:all` \) o solo los que se muestran actualmente \ ( `mixed-content:displayed` \). |  
| `scheme` | Muestra los recursos recuperados en HTTP \ ( `scheme:http` \) no protegidos o en https \ ( `scheme:https` \). |  
| `set-cookie-domain` | Muestra los recursos que tienen un `Set-Cookie` encabezado con un `Domain` atributo que coincide con el valor especificado.  DevTools rellenar autocompletar con todos los dominios de cookies que se encuentran. |  
| `set-cookie-name` | Muestra los recursos que tienen un `Set-Cookie` encabezado con un nombre que coincide con el valor especificado.  DevTools rellenar autocompletar con todos los nombres de cookies que se encuentren. |  
| `set-cookie-value` | Muestra los recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.  DevTools rellenar autocompletar con todos los valores de las cookies que se encuentran. |  
| `status-code` | Muestra los recursos que coinciden con el código de Estado HTTP específico.  DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que se encuentran. |  

### Filtrar solicitudes por tipo  

Para filtrar las solicitudes por tipo de solicitud, seleccione uno de los siguientes botones en el panel **red** .  

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
      **IMG**  
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
      **Dividir**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **EB**  
   :::column-end:::
   :::column span="2":::
      WebSocket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Manifiesta**  
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
      Cualquier otro tipo no incluido en la lista.  
   :::column-end:::
:::row-end:::  

Si los botones no se muestran, es posible que el panel **filtros** esté oculto.  
Para obtener más información, vaya a [ocultar el panel de filtros](#hide-the-filters-pane).  

Para habilitar varios filtros de tipo al mismo tiempo, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Panel red" lightbox="../media/network-network-type-filters.msft.png":::
   Usar los filtros de tipo para mostrar los recursos JS, CSS y Document  
:::image-end:::  

### Filtrar solicitudes por tiempo  

Seleccione y arrastre a la izquierda o a la derecha en el panel de descripción para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.  El filtro es inclusivo.  Se muestra cualquier solicitud que estuviera activa durante la hora resaltada.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Panel red" lightbox="../media/network-network-overview-filter.msft.png":::
   Filtrar las solicitudes que hayan estado inactivas aproximadamente 300 ms  
:::image-end:::  

### Ocultar direcciones URL de datos  

Las [direcciones URL de datos][MDNHTTPDataURIs] son pequeños archivos incrustados en otros documentos.  Cualquier solicitud que se muestre en la tabla solicitudes que comienza por `data:` es una dirección URL de datos.  

Active la casilla **ocultar direcciones URL de datos** para ocultar las solicitudes.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Panel red" lightbox="../media/network-network-hide-data-urls.msft.png":::
   La casilla **ocultar direcciones URL de datos**  
:::image-end:::  

## Ordenar solicitudes  

De forma predeterminada, las solicitudes de la tabla solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla mediante otros criterios.  

### Ordenar por columna  

Seleccione el encabezado de cualquier columna en las solicitudes para ordenar las solicitudes por esa columna.  

### Ordenar por fase de actividad  

Para cambiar la forma en que la cascada ordena las solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \), desplace el puntero sobre la **cascada**y seleccione una de las opciones siguientes.  

:::row:::
   :::column span="1":::
      **Hora de inicio**  
   :::column-end:::
   :::column span="2":::
      La primera solicitud iniciada se encuentra en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tiempo de respuesta**  
   :::column-end:::
   :::column span="2":::
      La primera solicitud que comenzó a descargarse está en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Hora de finalización**  
   :::column-end:::
   :::column span="2":::
      La primera solicitud que ha finalizado se encuentra en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Duración total**  
   :::column-end:::
   :::column span="2":::
      La solicitud con la configuración de conexión más corta, solicitud o respuesta, se encuentra en la parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Latencia**  
   :::column-end:::
   :::column span="2":::
      La solicitud que esperó el tiempo más breve para una respuesta está en la parte superior.  
   :::column-end:::
:::row-end:::  

En estas descripciones se supone que cada opción respectiva está clasificada de menor a mayor.  Al seleccionar el encabezado de la columna **cascada** se invierte el orden.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Panel red" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Ordenar la cascada por duración total \ (la parte más clara de cada barra está en espera y la parte más oscura es el tiempo dedicado a descargar bytes \)  
:::image-end:::  

## Analizar solicitudes  

Siempre que DevTools estén abiertos, registra todas las solicitudes en el panel red.  
Use el panel red para analizar las solicitudes.  

### Ver un registro de solicitudes  

Use la tabla solicitudes para ver un registro de todas las solicitudes realizadas mientras DevTools abierto.  Al seleccionar o mantener el puntero sobre solicitudes, se muestra más información sobre cada elemento.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-table.msft.png":::
   La tabla solicitudes  
:::image-end:::  

De forma predeterminada, en la tabla solicitudes se muestran las siguientes columnas.  

:::row:::
   :::column span="1":::
      **Nombre**  
   :::column-end:::
   :::column span="2":::
      El nombre de archivo de un recurso o un identificador de él.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Estado**  
   :::column-end:::
   :::column span="2":::
      El código de Estado HTTP.  
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
      **Inició**  
   :::column-end:::
   :::column span="2":::
      Los siguientes objetos o procesos inician solicitudes.  
      
      *   **Analizador**  El analizador HTML para Microsoft Edge.  
      *   **Redirigir**  Una redirección de HTTP.  
      *   **Script**  Una función de JavaScript.  
      *   **Otros**  Otro proceso o acción, como navegar a una página con un vínculo o escribir una dirección URL en la barra de direcciones.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tamaño**  
   :::column-end:::
   :::column span="2":::
      El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, tal y como lo proporciona el servidor.  
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
      [Cascada](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Un desglose visual de la actividad de cada solicitud.  
   :::column-end:::
:::row-end:::  

#### Agregar o quitar columnas  

Desplace el puntero en el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione una opción para ocultarlo o mostrarlo.  Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-add-column.msft.png":::
   Agregar una columna a la tabla solicitudes  
:::image-end:::  

#### Agregar columnas personalizadas  

Para agregar una columna personalizada a la tabla solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **encabezados de respuesta**para  >  **administrar columnas de encabezado**.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Agregar una columna personalizada a la tabla solicitudes  
:::image-end:::  

### Ver la relación de sincronización de las solicitudes  

Use la cascada para ver las relaciones de temporización de las solicitudes.  
La organización predeterminada de la cascada usa la hora de inicio de las solicitudes.  
Por lo tanto, las solicitudes que se encuentren más lejanas a la izquierda iniciadas antes que las solicitudes más lejanas a la derecha.  

Para revisar las diferentes maneras en las que puede ordenar la cascada, vaya a [ordenar por fase de actividad](#sort-by-activity-phase).  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-waterfall.msft.png":::
   La columna cascada del panel **solicitudes**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="Panel red" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
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

### Ver una vista previa del cuerpo de una respuesta  

Para ver una vista previa del cuerpo de una respuesta, siga estos pasos.  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **vista previa** .  

Esta pestaña es principalmente útil para visualizar imágenes.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-preview.msft.png":::
   La ficha **vista previa**  
:::image-end:::  

### Ver el cuerpo de una respuesta  

Para ver el cuerpo de la respuesta de una solicitud, siga estos pasos.  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **respuesta** .  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-response.msft.png":::
   La ficha **respuesta**  
:::image-end:::  

### Ver encabezados HTTP  

Para ver los datos del encabezado HTTP sobre una solicitud, siga estos pasos.  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **encabezados** .  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Panel red" lightbox="../media/network-resources-headers.msft.png":::
   La pestaña **encabezados**  
:::image-end:::  

#### Ver origen de encabezado HTTP  

De forma predeterminada, la pestaña encabezados muestra los nombres de encabezado alfabéticamente.  Para ver los nombres de encabezados HTTP en el orden recibido, siga estos pasos.  

1.  Abre la pestaña **encabezados** para la solicitud que te interese.  Para obtener más información, vaya a [Ver encabezados HTTP](#view-http-headers).  
1.  Seleccione **Ver origen**, junto a la sección **solicitar** encabezado o **respuesta de encabezado** .  

### Ver parámetros de cadena de consulta  

Para ver los parámetros de cadena de consulta de una dirección URL en un formato legible, siga estos pasos.  

1.  Abre la pestaña **encabezados** para la solicitud que te interese.  Para obtener más información, vaya a [Ver encabezados HTTP](#view-http-headers).  
1.  Vaya a la sección **parámetros de cadena de consulta** .  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Sección **parámetros de cadena de consulta**  
:::image-end:::  

#### Ver origen de parámetros de cadena de consulta  

Para ver el origen de parámetro de cadena de consulta de una solicitud, realice los siguientes pasos.  

1.  Vaya a la sección parámetros de cadena de consulta.  Para obtener más información, vaya a [ver parámetros de cadena de consulta](#view-query-string-parameters).  
1.  Seleccione **Ver origen**.  

#### Ver parámetros de cadena de consulta con codificación URL  

Para ver los parámetros de cadena de consulta en un formato legible, pero con las codificaciones conservadas, siga estos pasos.  

1.  Vaya a la sección parámetros de cadena de consulta.  Para obtener más información, vaya a [ver parámetros de cadena de consulta](#view-query-string-parameters).  
1.  Seleccione **Ver dirección URL codificada**.  

### Ver cookies  

Para ver las cookies enviadas en el encabezado HTTP de una solicitud, siga estos pasos.  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la ficha **cookies** .  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-cookies.msft.png":::
   La ficha cookies  
:::image-end:::  

### Ver el desglose de intervalos de una solicitud  

Para ver el desglose de intervalos de una solicitud, siga estos pasos.  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **intervalos** .  

Para obtener acceso a los datos de una manera más rápida, navegue para [obtener una vista previa de un desglose por intervalos](#preview-a-timing-breakdown).  

Para obtener más información acerca de cada una de las fases que se pueden mostrar en la pestaña **intervalos** , vaya a [fases de desglose por intervalos explicadas](#timing-breakdown-phases-explained).  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-timing.msft.png":::
   La ficha **intervalos**  
:::image-end:::  

Más información sobre cada una de las fases.  

Para obtener más información sobre cómo obtener acceso a la vista, vaya a [Ver desglose de intervalos](#view-the-timing-breakdown-of-a-request).  

#### Obtener una vista previa de intervalos  

Para obtener una vista previa del desglose de intervalos de una solicitud, en la columna **cascada** de la tabla solicitudes, desplace el puntero sobre la entrada de la solicitud.  

Para obtener más información sobre cómo obtener acceso a los datos sin mantener el mouse, navegue para [ver el desglose de intervalos de una solicitud](#view-the-timing-breakdown-of-a-request).  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Obtener una vista previa del desglose de intervalos de una solicitud  
:::image-end:::  

#### Explicación de fases de desglose de intervalos  

Más información sobre cada una de las fases que pueden mostrarse en la pestaña **intervalos** .  

:::row:::
   :::column span="1":::
      **Poner en cola**  
   :::column-end:::
   :::column span="2":::
      El explorador pone en cola las solicitudes cuando cualquiera de las siguientes condiciones es verdadera.  
      *   Hay solicitudes de prioridad más alta.  
      *   Hay seis conexiones TCP abiertas para el mismo origen, que es el límite.  Solo se aplica a HTTP/1.0 y HTTP/1.1.  
      *   El explorador está asignando un poco de espacio en la caché de disco.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Paralizado**  
   :::column-end:::
   :::column span="2":::
      La solicitud se detiene por cualquiera de las razones descritas en **puesta en cola**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Búsqueda de DNS**  
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
      El explorador establece una conexión que incluye los protocolos de enlace TCP, los reintentos de TCP y negocia una capa de sockets seguros.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Negociación de proxy**  
   :::column-end:::
   :::column span="2":::
      El explorador está negociando la solicitud con un [servidor proxy][WikiProxyServer].  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Solicitud enviada**  
   :::column-end:::
   :::column span="2":::
      Se está enviando la solicitud.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Preparación de ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      El explorador está iniciando el trabajo del servicio.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Solicitud para ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      La solicitud se está enviando al trabajador del servicio.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Esperando \ (TTFB \)**  
   :::column-end:::
   :::column span="2":::
      El explorador está esperando el primer byte de una respuesta.  TTFB es el primer byte.  Este intervalo incluye un recorrido de ida y vuelta de la latencia y el tiempo que el servidor tomó para preparar la respuesta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Descarga de contenido**  
   :::column-end:::
   :::column span="2":::
      El explorador está recibiendo la respuesta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Recepción de envío**  
   :::column-end:::
   :::column span="2":::
      El explorador está recibiendo datos de esta respuesta a través de la inserción de servidor HTTP/2.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Insertar inserción**  
   :::column-end:::
   :::column span="2":::
      El explorador está leyendo los datos locales recibidos anteriormente.  
   :::column-end:::
:::row-end:::  

### Ver iniciadores y dependencias  

Para ver los iniciadores y las dependencias de una solicitud, mantenga presionado `Shift` el mouse sobre la solicitud en la tabla solicitudes.  Colores de DevTools: los iniciadores se muestran en verde y las dependencias en rojo.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Visualización de los iniciadores y las dependencias de una solicitud  
:::image-end:::  

Cuando la tabla solicitudes está ordenada cronológicamente, si coloca el puntero sobre una línea, la línea anterior muestra una solicitud verde.  La solicitud verde es el iniciador de la dependencia.  Si se muestra otra solicitud verde en la línea antes de ella, esa solicitud superior es el iniciador del iniciador.  Etcétera.  

### Ver eventos de carga  

DevTools muestra la temporización de los `DOMContentLoaded` `load` eventos y en varios lugares del panel red.  El `DOMContentLoaded` evento está coloreado en azul y el `load` evento es rojo.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-load-events.msft.png":::
   Las ubicaciones de los `DOMContentLoaded` `load` eventos y en el panel red  
:::image-end:::  

### Ver el número total de solicitudes  

El número total de solicitudes se muestra en el panel Resumen, en la parte inferior del panel red.  

> [!CAUTION]
> Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.  Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Panel red" lightbox="../media/network-network-total-requests.msft.png":::
   El número total de solicitudes desde que DevTools se abrieron  
:::image-end:::  

### Ver el tamaño total de la descarga  

El tamaño total de las solicitudes de descarga se muestra en el panel Resumen, en la parte inferior del panel red.  

> [!CAUTION]
> Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.  Si se han producido otras solicitudes antes de que se abriera DevTools, no se cuentan las solicitudes anteriores.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Panel red" lightbox="../media/network-network-total-download-size.msft.png":::
   El tamaño total de las solicitudes de descarga  
:::image-end:::  

Para comprobar cómo los recursos grandes están después de que el explorador descomprime cada elemento, navegue para [ver el tamaño descomprimido de un recurso](#view-the-uncompressed-size-of-a-resource).  

### Ver el seguimiento de la pila que causó una solicitud  

Después de que una instrucción de JavaScript solicite un recurso, mueva el puntero sobre la columna de **iniciador** para ver el seguimiento de la pila que se dirige a la solicitud.  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   El seguimiento de la pila que lleva a una solicitud de recursos  
:::image-end:::  

### Ver el tamaño descomprimido de un recurso  

Seleccione la casilla **usar filas de solicitudes grandes** y, a continuación, mire el valor inferior de la columna **tamaño** .  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Un ejemplo de recursos sin comprimir \ (el tamaño comprimido del `jquery-3.3.1.min.js` archivo que se envió a través de la red fue `29.9 KB` , mientras que el tamaño descomprimido fue `84.9 KB` \)  
:::image-end:::  

## Exportar datos de solicitudes  

### Guardar todas las solicitudes de red en un archivo HAR  

Para guardar todas las solicitudes de red en un archivo HAR, siga los pasos que se indican a continuación.  

1.  Mantenga el mouse sobre cualquier solicitud de la tabla solicitudes y abra el menú contextual \ (haga clic con el botón derecho \).  
1.  Seleccione **Guardar como Har with Content**.  DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.  No puedes filtrar solicitudes.  Tampoco puedes guardar una sola solicitud.  

Una vez que haya guardado un archivo HAR, podrá volver a importarlo en DevTools para analizarlo.  Simplemente arrastre y coloque el archivo HAR en la tabla solicitudes.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Seleccionar **Guardar como Har with Content**  
:::image-end:::  

### Copiar una o más solicitudes en el portapapeles  

En la columna **nombre** de la tabla solicitudes, desplace el puntero sobre una solicitud y abra el menú contextual \ (haga clic con el botón derecho \), mueva el puntero sobre **copiar**y seleccione una de las opciones siguientes.  

:::row:::
   :::column span="1":::
      **Copiar dirección del vínculo**  
   :::column-end:::
   :::column span="2":::
      Copie la dirección URL de la solicitud en el portapapeles.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copiar respuesta**  
   :::column-end:::
   :::column span="2":::
      Copie el cuerpo de la respuesta en el portapapeles.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copiar como fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copiar como rizo**  
   :::column-end:::
   :::column span="2":::
      Copie la solicitud como un comando de rizo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copiar todo como fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copiar todo como rizo**  
   :::column-end:::
   :::column span="2":::
      Copiar todas las solicitudes como una cadena de comandos de rizo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copiar todo como HAR**  
   :::column-end:::
   :::column span="2":::
      Copie todas las solicitudes como datos de HAR.  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Selección de **copiar respuesta**  
:::image-end:::  

## Cambiar el diseño del panel red  

Puede expandir o contraer secciones de la interfaz de usuario del panel red para destacar información importante.  

### Ocultar el panel de filtros  

De forma predeterminada, DevTools muestra el **Panel filtros**.  
Seleccione **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para ocultarlo.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   El botón ocultar filtros  
:::image-end:::  

### Usar filas de solicitudes grandes  

Use filas grandes cuando desee más espacios en blanco en la tabla solicitudes de red.  Algunas columnas también proporcionan un poco más de información cuando se usan filas grandes.  Por ejemplo, el valor inferior de la columna **tamaño** es el tamaño descomprimido de una solicitud.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Ejemplo de filas de solicitudes grandes en el panel **solicitudes**  
:::image-end:::  

Seleccione la casilla **usar filas de solicitudes grandes** para habilitar las filas grandes.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Casilla de verificación **usar filas de solicitudes grandes**  
:::image-end:::  

### Ocultar el panel de información general  

De forma predeterminada, DevTools muestra el **Panel de información general**.  Anule la selección de la casilla **Mostrar información general** para ocultarla.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   La casilla **Mostrar información general**  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Depurar aplicaciones web progresivas | Microsoft docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Direcciones URL de datos | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
