---
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611843"
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
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## Registrar solicitudes de red   

De forma predeterminada, DevTools registra todas las solicitudes de red en el panel red, siempre y cuando DevTools esté abierto.  

> ##### Figura 1  
> Panel red  
> ![Panel red][ImageNetworkPanel]  

### Detener la grabación de solicitudes de red   

Para detener la grabación de solicitudes:  

*   Seleccione **Detener grabación registro de red** ![ detener la grabación del registro ][ImageRecordOnIcon] de red en el panel **red** .  Se vuelve gris para indicar que DevTools ya no graba solicitudes.  
*   Pulse `Control` + `E` \ (Windows \) o `Command` + `E` \ (MacOS \) mientras el panel **red** está en el foco.  

### Borrar solicitudes   

Seleccione **Borrar** ![ Borrar ][ImageClearIcon] en el panel red para borrar todas las solicitudes de la tabla solicitudes.  

> ##### Figura 2  
> Botón borrar  
> ![Botón borrar][ImageClearButton]  

### Guardar solicitudes en la carga de páginas   

Para guardar las solicitudes en la carga de la página, active la casilla **conservar registro** en el panel red.  DevTools guarda todas las solicitudes hasta que Deshabilites **conservar registro**.  

> ##### Imagen 3  
> Casilla de verificación conservar registro  
> ![Casilla de verificación conservar registro][ImagePreserveLogCheckBox]  

### Capturar capturas de pantallas durante la carga de la página   

Capture las capturas de pantallas para analizar lo que los usuarios ven al esperar a que se cargue la página.  

Para habilitar capturas de pantalla, seleccione **configuración de red** y marque la casilla **capturar capturas** de pantalla en el panel **red** .  

Vuelva a cargar la página mientras el panel **red** está en el foco para capturar capturas de pantalla.  

Después de capturar una captura de pantalla, puede interactuar con ella de las siguientes maneras.  

*   Desplace el puntero sobre una captura de pantalla para ver el punto en el que se capturó la captura de pantalla.  Aparece una línea amarilla en el panel de **información general** .  
*   Seleccione la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de que se capturó la captura de pantalla.  
*   Haga doble clic en una miniatura para acercarla.  

> ##### Imagen 4  
> Colocar el puntero sobre una captura de pantalla  
> ![Colocar el puntero sobre una captura de pantalla][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## Cambiar el comportamiento de carga  

### Emular a un primer visitante mediante la deshabilitación de la memoria caché del explorador   

Para emular el funcionamiento de su sitio por primera vez, active la casilla **deshabilitar la caché** .  DevTools deshabilita la caché del explorador.  Esto emula con más precisión la experiencia de un usuario por primera vez, ya que las solicitudes se proporcionan desde la memoria caché del explorador en las visitas repetidas.  

> ##### Imagen 5  
> Casilla deshabilitar caché  
> ! [Deshabilitar la casilla de la caché] [ImageDisableCacheCheckBox]  

#### Deshabilitar la memoria caché del explorador en el cajón de condiciones de red   

Si desea deshabilitar la caché mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.  

1.  Abra el cajón de **condiciones de redes** .  
1.  Active o desactive la casilla **deshabilitar caché** .  

<!--todo: add network condition section when available -->  

### Borrar manualmente la memoria caché del explorador   

Para borrar manualmente la memoria caché del explorador en cualquier momento, haga clic con el botón secundario en cualquier lugar de la tabla solicitudes y seleccione **Borrar caché del explorador**.  

> ##### Imagen 6  
> Selección de borrar caché del explorador  
> ! [Seleccionando Borrar caché del explorador] [ImageClearBrowserCache]  

### Emular sin conexión   

Una nueva clase de aplicaciones Web, llamadas [aplicaciones web progresivas][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores de servicio**.  Es posible que le resulte útil simular rápidamente un dispositivo que no tiene conexión de datos cuando está creando este tipo de aplicación.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Seleccione el menú desplegable **en línea** , búsqueda en **preestablecidos**y seleccione **sin conexión** para simular una experiencia de red completamente desconectada.  

> ##### Imagen 7  
> Menú desplegable desconectado  
> ! [Menú desplegable desconectado] [ImageOfflineDropdown]  

### Emular conexiones de red lentas   

Emular 3G lento, 3G rápido y otras velocidades de conexión en el menú desplegable **en línea** .  

> ##### Imagen 8  
> El menú desplegable limitación de peticiones  
> ! [El menú desplegable de limitación de peticiones] [ImageNetworkThrottlingMenu]  

Puedes elegir entre una variedad de ajustes preestablecidos, como 3G lento o 3G rápido.  También puede agregar sus propios ajustes preestablecidos personalizados abriendo el menú de limitación y seleccionando **Custom**  >  **añadir**personalizados.  

DevTools muestra un icono de advertencia junto a la pestaña **red** para recordarle que la limitación está habilitada.  

#### Emular conexiones de red lentas del cajón de condiciones de red   

Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.  

1.  Abra el cajón de **condiciones de redes** .  
1.  Seleccione la velocidad de conexión que desee en el menú **limitación** .  

<!--todo: add network condition section when available -->  

### Borrar manualmente las cookies del explorador   

Para borrar manualmente las cookies del explorador en cualquier momento, haga clic con el botón secundario en cualquier lugar de la tabla solicitudes y seleccione **Borrar cookies del explorador**.  

> ##### Imagen 9  
> Selección de las cookies de borrar explorador  
> ! [Seleccionando borrar cookies del explorador] [ImageClearBrowserCookies]  

### Invalidar el agente de usuario   

Para anular manualmente el agente de usuario:  

1.  Abra el cajón de **condiciones de redes** .  
1.  Desactive **seleccionar automáticamente**.  
1.  Elija una opción de agente de usuario en el menú o escriba una personalizada en el cuadro de texto.  

<!--todo: add network condition section when available -->  

## Filtrar solicitudes   

### Filtrar las solicitudes por propiedades   

Use el cuadro de texto **filtrar** para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.  

Si no ve el cuadro de texto, es probable que el panel filtros esté oculto.  
Consulte [ocultar el panel de filtros](#hide-the-filters-pane).  

> ##### Imagen 10  
> El cuadro de texto filtros  
> ! [El cuadro de texto filtros] [ImageFilterTextBox]  

Puede usar varias propiedades simultáneamente al separar cada propiedad con un espacio.  Por ejemplo, `mime-type:image/png larger-than:1K` se muestran todos los PNGs que tengan más de un kilobyte.  Estos filtros de varias propiedades son equivalentes a `AND` las operaciones.  `OR` Actualmente no se admiten las operaciones.  

La lista completa de propiedades compatibles.  

| Propiedad | Detalles |  
|:--- | :--- |  
| `domain` | Mostrar solo los recursos del dominio especificado.  Puede usar un carácter comodín \ ( `*` \) para incluir varios dominios.  Por ejemplo, `*.com` muestra los recursos de todos los nombres de dominio que terminan en `.com` .  DevTools rellena el menú desplegable de autocompletar con todos los dominios que ha encontrado. |  
| `has-response-header` | Mostrar los recursos que contienen el encabezado de respuesta HTTP especificado.  DevTools rellena la lista desplegable de autocompletar con todos los encabezados de respuesta que ha encontrado. |  
| `is` | Usar `is:running` para buscar `WebSocket` recursos. |  
| `larger-than` | Mostrar recursos mayores que el tamaño especificado, en bytes.  Establecer un valor de `1000` es equivalente a establecer un valor de `1k` . |  
| `method` | Mostrar recursos que se recuperaron en un tipo de método HTTP especificado.  DevTools rellena la lista desplegable con todos los métodos HTTP que ha encontrado. |  
| `mime-type` | Mostrar los recursos de un tipo MIME especificado.  DevTools rellena la lista desplegable con todos los tipos MIME que ha encontrado. |  
| `mixed-content` | Mostrar todos los recursos de contenido mixto \ ( `mixed-content:all` \) o solo los que se muestran actualmente \ ( `mixed-content:displayed` \). |  
| `scheme` | Mostrar los recursos recuperados en HTTP \ ( `scheme:http` \) no protegidos o en https \ ( `scheme:https` \). |  
| `set-cookie-domain` | Mostrar los recursos que tienen un `Set-Cookie` encabezado con un `Domain` atributo que coincide con el valor especificado.  DevTools rellena el autocompletar con todos los dominios de cookies que ha encontrado. |  
| `set-cookie-name` | Mostrar los recursos que tengan un `Set-Cookie` encabezado con un nombre que coincida con el valor especificado.  DevTools rellena la autocompletar con todos los nombres de cookies que ha encontrado. |  
| `set-cookie-value` | Mostrar los recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.  DevTools rellena el autocompletar con todos los valores de cookie que ha encontrado. |  
| `status-code` | Mostrar solo los recursos para los que el código de Estado HTTP coincide con el código especificado.  DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que ha encontrado. |  

### Filtrar solicitudes por tipo   

Para filtrar las solicitudes según el tipo de solicitud, seleccione los botones **XHR**, **JS**, **CSS**, **IMG**, **multimedia**, **fuente**, **documento**, **WS** \ (WebSocket \), **manifiesto**u **otros** \ (cualquier otro tipo no incluido aquí \) en el panel red.  

Si no ve estos botones, es probable que el panel filtros esté oculto.  
Consulte [ocultar el panel de filtros](#hide-the-filters-pane).  

Para habilitar varios filtros de tipo al mismo tiempo, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione.  

> ##### Imagen 11  
> Usar los filtros de tipo para mostrar los recursos JS, CSS y Document  
> ! [Usar los filtros de tipo para mostrar JS, CSS y recursos de documento] [ImageMultiTypeFilter]  

### Filtrar solicitudes por tiempo   

Seleccione y arrastre a la izquierda o a la derecha en el panel de descripción para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.  El filtro es inclusivo.  Se muestra cualquier solicitud que estuviera activa durante la hora resaltada.  

> ##### Imagen 12  
> Filtrar las solicitudes inactivas en 300ms  
> ! [Filtrando las solicitudes inactivas en 300ms] [ImageOverviewFilter]  

### Ocultar direcciones URL de datos  

Las [direcciones URL de datos][MDNHTTPDataURIs] son pequeños archivos incrustados en otros documentos.  Cualquier solicitud que vea en la tabla solicitudes que comienza por `data:` es una dirección URL de datos.  

Active la casilla **ocultar URLs de datos** para ocultar estas solicitudes.  

> ##### Imagen 13  
> La casilla ocultar direcciones URL de datos  
> ! [Casilla ocultar direcciones URL de datos] [ImageHideDataURLsCheckBox]  

## Ordenar solicitudes  

De forma predeterminada, las solicitudes de la tabla solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla mediante otros criterios.  

### Ordenar por columna   

Seleccione el encabezado de cualquier columna en las solicitudes para ordenar las solicitudes por esa columna.  

### Ordenar por fase de actividad   

Para cambiar la forma en que la cascada ordena las solicitudes, haga clic con el botón secundario en el encabezado de la tabla solicitudes, desplace el puntero sobre **cascada**y seleccione una de las opciones siguientes.  

*   **Hora de inicio**.  La primera solicitud iniciada se encuentra en la parte superior.  
*   **Tiempo de respuesta**.  La primera solicitud que comenzó a descargarse está en la parte superior.  
*   **Hora de finalización**.  La primera solicitud que ha finalizado se encuentra en la parte superior.  
*   **Duración total**.  La solicitud con la configuración de conexión más corta y la solicitud o respuesta se encuentra en la parte superior.  
*   **Latencia**.  La solicitud que esperó el tiempo más breve para una respuesta está en la parte superior.  

En estas descripciones se supone que cada opción respectiva está clasificada de menor a mayor.  Al seleccionar el encabezado de la columna **cascada** se invierte el orden.  

> ##### Imagen 14  
> Ordenar la cascada por duración total \ (la parte más clara de cada barra está en espera y la parte más oscura es el tiempo dedicado a descargar bytes \)  
> ! [Ordenando la cascada por duración total] [ImageWaterfallTotalDuration]  

## Analizar solicitudes   

Siempre que DevTools esté abierto, registra todas las solicitudes en el panel de red.  
Use el panel red para analizar las solicitudes.  

### Ver un registro de solicitudes   

Use la tabla solicitudes para ver un registro de todas las solicitudes realizadas mientras se ha abierto DevTools.  Al seleccionar o mantener el puntero sobre solicitudes, se muestra más información sobre cada elemento.  

> ##### Imagen 15  
> La tabla solicitudes  
> ! [La tabla solicitudes] [ImageRequestsTable]  

De forma predeterminada, en la tabla solicitudes se muestran las siguientes columnas:  

*   **Nombre**.  El nombre de archivo de un recurso o un identificador de él.  
*   **Estado**.  El código de Estado HTTP.  
*   **Tipo**.  Tipo MIME del recurso solicitado.  
*   **Iniciador**.  Los siguientes objetos o procesos inician solicitudes:  
    *   **Parser**.  El analizador HTML para Microsoft Edge.  
    *   **Redirigir**.  Una redirección de HTTP.  
    *   **Script**.  Una función de JavaScript.  
    *   **Otros**.  Otro proceso o acción, como navegar hasta una página a través de un vínculo o escribir una dirección URL en la barra de direcciones.  
*   **Tamaño**.  El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, tal y como lo proporciona el servidor.  
*   **Momento**.  La duración total, desde el inicio de la solicitud hasta la recepción del byte final en la respuesta.  
*   [**Cascada**](#view-the-timing-of-requests-in-relation-to-one-another).  Un desglose visual de la actividad de cada solicitud.  

#### Agregar o quitar columnas   

Haga clic con el botón secundario en el encabezado de la tabla solicitudes y seleccione una opción para ocultarla o mostrarla.  Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.  

> ##### Imagen 16  
> Agregar una columna a la tabla solicitudes  
> ! [Agregando una columna a la tabla solicitudes] [ImageRequestsTableAddColumn]  

#### Agregar columnas personalizadas   

Para agregar una columna personalizada a la tabla solicitudes, haga clic con el botón secundario en el encabezado de la tabla solicitudes y seleccione **encabezados de respuesta**  >  **administrar columnas de encabezado**.  

> ##### Imagen 17  
> Agregar una columna personalizada a la tabla solicitudes  
> ! [Agregando una columna personalizada a la tabla solicitudes] [ImageRequestsTableCustomColumn]  

### Ver los intervalos de solicitudes relacionados entre sí   

Use la cascada para ver los intervalos de solicitudes relacionados entre sí.  
De forma predeterminada, la cascada está organizada por la hora de inicio de las solicitudes.  
Por lo tanto, las solicitudes que se encuentren más lejanas a la izquierda iniciadas antes de las que están más lejos a la derecha.  

Consulte [ordenar por fase de actividad](#sort-by-activity-phase) para ver las diferentes formas de ordenar la cascada.  

> ##### Ilustración 18  
> La columna cascada del panel solicitudes  
> ! [La columna cascada del panel solicitudes] [ImageRequestsTableWaterfallColumn]  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### Ver una vista previa del cuerpo de una respuesta   

Para ver una vista previa del cuerpo de una respuesta:  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **vista previa** .  

Esta pestaña es principalmente útil para visualizar imágenes.  

> ##### Ilustración 19  
> La ficha vista previa  
> ! [Ficha vista previa] [ImagePreview]  

### Ver el cuerpo de una respuesta   

Para ver el cuerpo de la respuesta de una solicitud:  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **respuesta** .  

> ##### Ilustración 20  
> La ficha respuesta  
> ! [La pestaña respuesta] [ImageResponse]  

### Ver encabezados HTTP   

Para ver los datos de encabezado HTTP sobre una solicitud:  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **encabezados** .  

> ##### Ilustración 21  
> La pestaña encabezados  
> ! [Ficha encabezados] [ImageHeaders]  

#### Ver origen de encabezado HTTP   

De forma predeterminada, la pestaña encabezados muestra los nombres de encabezado alfabéticamente.  Para ver los nombres de encabezado HTTP en el orden en que se recibieron:  

1.  Abre la pestaña **encabezados** para la solicitud que te interese.  Consulte [Ver encabezados HTTP](#view-http-headers).  
1.  Seleccione **Ver origen**, junto a la sección **solicitar** encabezado o **respuesta de encabezado** .  

### Ver parámetros de cadena de consulta   

Para ver los parámetros de cadena de consulta de una dirección URL en un formato legible:  

1.  Abre la pestaña **encabezados** para la solicitud que te interese.  Consulte [Ver encabezados HTTP](#view-http-headers).  
1.  Vaya a la sección **parámetros de cadena de consulta** .  

> ##### Ilustración 22  
> Sección parámetros de cadena de consulta  
> ! [Sección de parámetros de cadena de consulta] [ImageQueryStringParameters]  

#### Ver origen de parámetros de cadena de consulta   

Para ver el origen de parámetro de cadena de consulta de una solicitud:  

1.  Vaya a la sección parámetros de cadena de consulta.  Consulte [ver parámetros de cadena de consulta](#view-query-string-parameters).  
1.  Seleccione **Ver origen**.  

#### Ver parámetros de cadena de consulta con codificación URL   

Para ver los parámetros de cadena de consulta en un formato legible, pero conservando las codificaciones:  

1.  Vaya a la sección parámetros de cadena de consulta.  Consulte [ver parámetros de cadena de consulta](#view-query-string-parameters).  
1.  Seleccione **Ver dirección URL codificada**.  

### Ver cookies   

Para ver las cookies enviadas en el encabezado HTTP de una solicitud:  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la ficha **cookies** .  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

> ##### Ilustración 23  
> La ficha cookies  
> ! [Ficha cookies] [ImageCookies]  

### Ver el desglose de intervalos de una solicitud   

Para ver el desglose de intervalos de una solicitud:  

1.  Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.  
1.  Seleccione la pestaña **intervalos** .  

Vea obtener una [vista previa de un desglose de intervalos](#preview-a-timing-breakdown) para obtener acceso a estos datos más rápidamente.  

Consulte [fases de desglose de intervalos explicadas](#timing-breakdown-phases-explained) para obtener más información sobre cada una de las fases que puede ver en la pestaña intervalos.  

> ##### Ilustración 24  
> La ficha intervalos  
> ! [Ficha intervalos] [ImageTiming]  

Más información sobre cada una de las fases.  

Consulte [Ver desglose de intervalos](#view-the-timing-breakdown-of-a-request) para obtener acceso a esta vista.  

#### Obtener una vista previa de intervalos   

Para obtener una vista previa del desglose de intervalos de una solicitud, desplace el puntero sobre la entrada de la solicitud en la columna **cascada** de la tabla solicitudes.  

Vea [ver el desglose de intervalos de una solicitud](#view-the-timing-breakdown-of-a-request) para obtener acceso a estos datos que no requieren el desplazamiento.  

> ##### Ilustración 25  
> Obtener una vista previa del desglose de intervalos de una solicitud  
> ! [Vista previa del desglose de intervalos de una solicitud] [ImageWaterfallHover]  

#### Explicación de fases de desglose de intervalos   

Más información sobre cada una de las fases que puede ver en la pestaña intervalos:  

*   **Poner en cola**.  El explorador pone en cola las solicitudes cuando:  
    *   Hay solicitudes de prioridad más alta.  
    *   Ya hay seis conexiones TCP abiertas para este origen, que es el límite.  Solo se aplica a HTTP/1.0 y HTTP/1.1.  
    *   El explorador está asignando un poco de espacio en la caché de disco.  
*   **Detenido**.  La solicitud podría estar detenida por cualquiera de las razones descritas en **puesta en cola**.  
*   **Búsqueda DNS**.  El explorador está resolviendo la dirección IP de la solicitud.  
*   **Negociación de proxy**.  El explorador está negociando la solicitud con un [servidor proxy][WikiProxyServer].  
*   **Solicitud enviada**.  Se está enviando la solicitud.  
*   **Preparación de ServiceWorker**.  El explorador está iniciando el trabajo del servicio.  
*   **Solicitud para ServiceWorker**.  La solicitud se está enviando al trabajador del servicio.  
*   **Esperando \ (TTFB \)**.  El explorador está esperando el primer byte de una respuesta.  
  TTFB es el primer byte.  Este intervalo incluye 1 recorrido de ida y vuelta de la latencia y el tiempo que el servidor necesitó para preparar la respuesta.  
*   **Descarga de contenido**.  El explorador está recibiendo la respuesta.  
*   **Recibiendo Push**.  El explorador está recibiendo datos de esta respuesta a través de la inserción de servidor HTTP/2.  
*   **Leyendo inserción**.  El explorador está leyendo los datos locales recibidos anteriormente.  

### Ver iniciadores y dependencias   

Para ver los iniciadores y las dependencias de una solicitud, mantenga presionado `Shift` el mouse sobre la solicitud en la tabla solicitudes.  Colores de DevTools: los iniciadores se muestran en verde y las dependencias en rojo.  

> ##### Ilustración 26  
> Visualización de los iniciadores y las dependencias de una solicitud  
> ! [Visualización de los iniciadores y las dependencias de una solicitud] [ImageRequestInitiatorsDependencies]  

Cuando la tabla solicitudes está ordenada cronológicamente, la primera solicitud verde por encima de la que está pasando es el iniciador de la dependencia.  Si aparece otra solicitud de color verde encima de esa, esa solicitud superior es el iniciador del iniciador.  Etcétera.  

### Ver eventos de carga   

DevTools muestra la temporización de los `DOMContentLoaded` `load` eventos y en varios lugares del panel red.  El `DOMContentLoaded` evento está coloreado en azul y el `load` evento es rojo.  

> ##### Ilustración 27  
> Las ubicaciones de los `DOMContentLoaded` `load` eventos y en el panel red  
> ! [Ubicaciones de la DOMContentLoaded y cargar eventos en el panel de red] [ImageNetworkPanelDOMContentLoadedLoadEvents]  

### Ver el número total de solicitudes   

El número total de solicitudes se muestra en el panel Resumen, en la parte inferior del panel red.  

> [!CAUTION]
> Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.  Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.  

> ##### Ilustración 28  
> El número total de solicitudes desde que se abrió DevTools  
> ! [El número total de solicitudes desde que se abrió DevTools] [ImageTotalRequests]  

### Ver el tamaño total de la descarga   

El tamaño total de las solicitudes de descarga se muestra en el panel Resumen, en la parte inferior del panel red.  

> [!CAUTION]
> Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.  Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.  

> ##### Ilustración 29  
> El tamaño total de las solicitudes de descarga  
> ! [El tamaño total de las solicitudes de descarga] [ImageTotalSize]  

Consulte [ver el tamaño descomprimido de un recurso](#view-the-uncompressed-size-of-a-resource) para ver cómo se encuentran los recursos grandes después de que el explorador descomprime cada elemento.  

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

> ##### Ilustración 30  
> El seguimiento de la pila que lleva a una solicitud de recursos  
> ! [El seguimiento de la pila llevado a una solicitud de recursos] [ImageInitiatorStack]  

### Ver el tamaño descomprimido de un recurso   

Seleccione la casilla **usar filas de solicitudes grandes** y, a continuación, mire el valor inferior de la columna **tamaño** .  

> ##### Ilustración 31  
> Un ejemplo de recursos sin comprimir \ (el tamaño comprimido del `jquery-3.3.1.min.js` archivo que se envió a través de la red fue `29.9 KB` , mientras que el tamaño descomprimido fue `84.9 KB` \)  
> ! [Un ejemplo de recursos no comprimidos] [ImageUncompressedResources]  

## Exportar datos de solicitudes   

### Guardar todas las solicitudes de red en un archivo HAR   

Para guardar todas las solicitudes de red en un archivo HAR:  

1.  Haga clic con el botón secundario en cualquier solicitud de la tabla solicitudes.  
1.  Seleccione **Guardar como Har with Content**.  DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.  No hay ninguna manera de filtrar las solicitudes o de guardar una sola.  

Una vez que haya guardado un archivo HAR, podrá volver a importarlo en DevTools para analizarlo.  Simplemente arrastre y coloque el archivo HAR en la tabla solicitudes.  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### Ilustración 32  
> Seleccionar Guardar como HAR with Content  
> ! [Seleccionando Guardar como HAR with Content] [ImageSaveAsHAR]  

### Copiar una o más solicitudes en el portapapeles   

En la columna **nombre** de la tabla solicitudes, haga clic con el botón secundario en una solicitud, mueva el puntero sobre **copia**y seleccione una de las siguientes opciones:  

*   **Copiar la dirección del vínculo**.  Copie la dirección URL de la solicitud en el portapapeles.  
*   **Copiar respuesta**.  Copie el cuerpo de la respuesta en el portapapeles.  
*   **Copiar como fetch**.  
*   **Copiar como rizo**.  Copie la solicitud como un comando de rizo.  
*   **Copiar todo como fetch**.  
*   **Copiar todos como rizo**.  Copiar todas las solicitudes como una cadena de comandos de rizo.  
*   **Copiar todo como Har**.  Copie todas las solicitudes como datos de HAR.  

> ##### Ilustración 33  
> Selección de copiar respuesta  
> ! [Seleccionando respuesta de copia] [ImageCopyResponse]  

## Cambiar el diseño del panel red  

Puede expandir o contraer secciones de la interfaz de usuario del panel red para destacar información importante.  

### Ocultar el panel de filtros   

De forma predeterminada, DevTools muestra el **Panel filtros**.  
Seleccione filtro de **filtro** ![ ][ImageFilterIcon] para ocultarlo.  

> ##### Ilustración 34  
> El botón ocultar filtros  
> ! [El botón ocultar filtros] [ImageHideFiltersButton]  

### Usar filas de solicitudes grandes   

Use filas grandes cuando desee más espacios en blanco en la tabla solicitudes de red.  Algunas columnas también proporcionan un poco más de información cuando se usan filas grandes.  Por ejemplo, el valor inferior de la columna **tamaño** es el tamaño descomprimido de una solicitud.  

> ##### Ilustración 35  
> Ejemplo de filas de solicitudes grandes en el panel solicitudes  
> ! [Un ejemplo de filas de solicitudes grandes en el panel solicitudes] [ImageLargeRequestRows]  

Seleccione la casilla **usar filas de solicitudes grandes** para habilitar las filas grandes.  

> ##### Ilustración 36  
> Casilla de verificación filas de solicitudes grandes  
> ! [Casilla de verificación filas de solicitudes grandes] [ImageLargeRequestRowsCheckbox]  

### Ocultar el panel de información general   

De forma predeterminada, DevTools muestra el **Panel de información general**.  
Anule la selección de la casilla **Mostrar información general** para ocultarla.  

> ##### Ilustración 37  
> La casilla Mostrar información general  
> ! [La casilla Mostrar información general] [ImageHideOverviewCheckbox]  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Ilustración 1: panel de red"  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Ilustración 2: el botón borrar"  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Figura 3: casilla de verificación conservar registro"  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Ilustración 4: mantener el puntero sobre una captura de pantalla"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Disable-cache-CheckBox.msft.png "Figura 5: casilla deshabilitar la caché"  
[ImageClearBrowserCache]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Clear-Browser-cache.msft.png "Ilustración 6: selección de la caché de borrar explorador"  
[ImageOfflineDropdown]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-offline-DropDown.msft.png "Figura 7: menú desplegable sin conexión"  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-throttling-menu.msft.png "Ilustración 8: el menú de limitación de redes"  
[ImageClearBrowserCookies]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Clear-Browser-cookies.msft.png "Ilustración 9: selección de las cookies de borrar explorador"  
[ImageFilterTextBox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-filters-TextBox.msft.png "Figura 10: el cuadro de texto filtros"  
[ImageMultiTypeFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Type-filters.msft.png "ilustración 11: usar los filtros de tipo para mostrar JS, CSS y recursos de documento"  
[ImageOverviewFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Overview-Filter.msft.png "Ilustración 12: filtrar las solicitudes que estaban inactivas en 300ms"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Hide-Data-URLs.msft.png "ilustración 13: la casilla ocultar direcciones URL de datos"  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Waterfall-total-Duration.msft.png "Ilustración 14: ordenar la cascada por duración total"  
[ImageRequestsTable]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Table.msft.png "Ilustración 15: la tabla solicitudes"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Add-Column.msft.png "Ilustración 16: agregar una columna a la tabla solicitudes"  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Add-Custom.msft.png "Ilustración 17: agregar una columna personalizada a la tabla solicitudes"  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Waterfall.msft.png "ilustración 18: la columna cascada del panel solicitudes"  
[ImagePreview]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Preview.msft.png "Ilustración 19: la pestaña vista previa"  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[ImageResponse]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Response.msft.png "Ilustración 20: la pestaña respuesta"  
[ImageHeaders]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Resources-headers.msft.png "ilustración 21: la pestaña encabezados"  
[ImageQueryStringParameters]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-headers-Query-String-Parameters.msft.png "figura 22: sección de parámetros de cadena de consulta"  
[ImageCookies]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-cookies.msft.png "Ilustración 23: la ficha cookies"  
[ImageTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Timing.msft.png "Ilustración 24: ficha intervalos"  
[ImageWaterfallHover]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-Hover.msft.png "Ilustración 25: obtener una vista previa del desglose de intervalos de una solicitud"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Initiators-dependencies.msft.png "ilustración 26: visualización de los iniciadores y las dependencias de una solicitud"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Load-Events.msft.png "Ilustración 27: las ubicaciones de los DOMContentLoaded y cargar eventos en el panel de red"  
[ImageTotalRequests]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-total-requests.msft.png "Ilustración 28: el número total de solicitudes desde que se abrió DevTools"  
[ImageTotalSize]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-total-download-size.msft.png "Ilustración 29: el tamaño total de las solicitudes de descarga"  
[ImageInitiatorStack]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Initiator-Stack.msft.png "Ilustración 30: el seguimiento de pila que lleva a una solicitud de recurso"  
[ImageUncompressedResources]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Uncompressed-Compare.msft.png "Ilustración 31: un ejemplo de recursos sin comprimir"  
[ImageSaveAsHAR]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Save-har-Content.msft.png "ilustración 32: seleccionar Guardar como HAR with Content"  
[ImageCopyResponse]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Copy-Response.msft.png "Ilustración 33: selección de la respuesta de copia"  
[ImageHideFiltersButton]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Hide-filters-Button.msft.png "figura 34: el botón ocultar filtros"  
[ImageLargeRequestRows]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Large-request-Rows.msft.png "Ilustración 35: un ejemplo de filas de solicitudes grandes en el panel solicitudes"  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-use-Large-request-Rows-on.msft.png "Ilustración 36: casilla de verificación filas de gran tamaño"  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-show-Overview-OFF.msft.png "Ilustración 37: la casilla ocultar Descripción general"  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Depurar aplicaciones web progresivas"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

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
