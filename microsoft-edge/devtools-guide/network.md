---
description: Usar el panel red para supervisar y perfilar las solicitudes de recursos de página
title: DevTools-red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, red, tiempo de carga, http, https, caché del explorador, HAR
ms.custom: seodec18
ms.openlocfilehash: 0b190f5163f9b7a9f9920877a94577177053e4f6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573798"
---
# Red

Use el panel **red** para supervisar, inspeccionar y perfilar las solicitudes y respuestas enviadas a través de la conexión. Con ella, puedes hacer lo siguiente:

 - [Examinar un registro de todas las solicitudes de recursos](#network-summary) realizadas por la página
 - [Medir el tiempo de carga de su sitio](#summary-bar) para los usuarios nuevos y devueltos 
 - [Inspeccionar los encabezados, los cuerpos de los mensajes, los parámetros y las cookies](#request-details) intercambiados entre la página y la red
 - [Identificar los eventos de red que causan cuellos de botella](#timings) en el tiempo de carga de su sitio

![Panel de red de Microsoft Edge DevTools](./media/network.png)

## Resumen de red

Al abrir DevTools, la generación de perfiles de red está activada de forma predeterminada. Todo el tráfico de red de la ficha del explorador activo se registra en la lista de Resumen de la red, incluso mientras se trabaja en un panel de DevTools diferente del de la *red*.

![Indicador de Perfil de red en curso](./media/network_profile_indicator.png)

### Barra de herramientas

La barra de herramientas proporciona controles para generar perfiles y filtrar la actividad de la red de la página. 

![Barra de herramientas de Network Profiler](./media/network_toolbar.png)

1. **Iniciar o detener sesión de generación de perfiles**: de forma predeterminada, la generación de perfiles de red está activada y el tráfico de red se registrará en la lista del [**generador de perfiles de red**](#network-request-list) . Puede desactivar la captura de red con el botón **detener** ( `Ctrl+E` ).

2. **Exportar como Har**: puede guardar la sesión de perfilamiento de red actual ( `Ctrl+S` ) como un archivo [http Archive (har)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) con formato JSON. 

3. **Filtro de tipo de contenido**: Filtre la lista de solicitudes de red por solicitudes de contenido específicas (*documentos, hojas de estilos, imágenes, scripts, multimedia, fuentes, XHR, otros*). De forma predeterminada, se muestran todos los tipos de contenido.

4. **Buscar**: filtrar ( `Ctrl+F` ) la lista de solicitudes de red por nombres de entrada (rutas de recursos) que contienen una cadena de búsqueda especificada.

5. **Actualizar siempre desde el servidor**: al presionar este botón, los recursos de página se cargarán desde la red en lugar de la caché del explorador. Puede actualizar la página desde la red una sola vez pulsando `Ctrl+F5` .

6. **Omitir trabajo de servicio para todas las solicitudes de red**: deshabilite los trabajadores de servicio registrados como proxies de red. 

7. Borrar botones

   - **Borrar caché**: quita todos los recursos almacenados en la memoria caché del explorador (y emula una experiencia de primera vez que cargue la página).
   - **Borrar Cookies**: quita todas las cookies para el dominio dado (y emula una experiencia de primera hora del sitio).
   - **Borrar las entradas en**la navegación: el tráfico grabado se borra con la navegación de la página. Esta opción está activada de forma predeterminada.
   - **Borrar sesión**: borra todas las entradas de solicitud de red de la lista de **Resumen de red** .

### Lista de solicitudes de red

Todo el tráfico de red se graba en una lista (hasta que se borra la navegación, la desactivación manual o DevTools se cierran). Al hacer clic en cualquier entrada, se abrirá una [vista más detallada de la solicitud](#request-details).

![Lista de solicitudes de red](./media/network_request_list.png)

La lista de solicitudes de red incluye la siguiente información: 

Columna | Descripción 
:------------ | :------------- 
**Name** | Nombre y dirección URL de la solicitud
**Protocolo** |  Tipo de protocolo para la solicitud (como *https, http/2*)
**Método** |    [Método http](https://developer.mozilla.org/docs/Web/HTTP/Methods) usado para la solicitud
**Resultado** |    Código de [Estado de respuesta http](https://developer.mozilla.org/docs/Web/HTTP/Status)
**Tipo de contenido** |  Tipo de medios solicitado ([tipo MIME](https://en.wikipedia.org/wiki/Media_type))
**Recibido** | Tamaño de la respuesta tal y como lo proporciona el servidor (no se calcula para las respuestas almacenadas en caché)
**Tiempo** |  Tiempo para cargar la respuesta del servidor (no se calcula para las respuestas almacenadas en caché)
**Inició** | Subsistema responsable de iniciar la solicitud (como *analizador, redirección, script, otro*)
**Línea de tiempo** | Escala de tiempo visual para los eventos de red de la solicitud (como *bloqueados, resolver (DNS), conexiones (TCP), SSL, envío, espera (TTFB), descargar*). Situar el puntero sobre el gráfico proporciona un desglose más granular de los [intervalos de red](#timings)de red).

### Barra de Resumen

La barra de la parte inferior del panel **red** resume el número total de errores de red http, solicitudes, datos transferidos y tiempos de carga durante la sesión de perfilamiento de red (es decir, porque DevTools se abrieron y grabaron tráfico de red).

![Barra de Resumen de red](./media/network_summary_bar.png)

**Tiempo transcurrido** significa el tiempo entre el inicio de la sesión de generación de perfiles y el último recurso que se ha descargado de la red. Los recursos que se capturan desde la caché del explorador no acumulan tiempo para este número. 

**Dom Load Time** significa el tiempo entre el inicio de la sesión de generación de perfiles y cuando se desencadena el evento [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) para indicar que se ha cargado y analizado la estructura del documento de página (aunque no necesariamente ninguna hoja de estilos, imágenes o submarcos).

Tiempo de carga de la **Página** significa el tiempo entre el inicio de la sesión de generación de perfiles y el momento en que se activó el evento de [carga](https://developer.mozilla.org/docs/Web/Events/load) para indicar que el documento de página (y todos sus recursos) se ha cargado por completo.

## Detalles de la solicitud

Al hacer clic en cualquier entrada de la lista de [**Resumen de red**](#network-summary) , se abrirá el panel de detalles de la [**solicitud**](#request-details) con más información en cada una de las siguientes pestañas.

![Panel de detalles de solicitud de red](./media/network_request_details.png)

### Encabezados
Muestra los [encabezados HTTP](https://developer.mozilla.org/docs/Web/HTTP/Headers) enviados y recibidos desde el servidor. Haga clic con el botón derecho en cualquier entrada de encabezado para copiarla ( `Ctrl+C` ) en el portapapeles. También puede seleccionar varias entradas manteniendo presionada la `Shift` tecla o seleccionar todo ( `Ctrl+A` ).

### Body
Muestra los datos de cuerpo (si están disponibles) de las cargas de solicitud y respuesta.

El contenido de la imagen se muestra con datos de tamaño y dimensiones.

El contenido de texto aparece en un editor (de solo lectura) con opciones para dar formato al contenido de minified con la **impresión** o el **ajuste** de texto, para facilitar la lectura.

![Pestaña cuerpo del panel Detalles de la solicitud](./media/network_details_body.png)

### Parameters
Muestra parámetros de cadena de consulta para solicitudes GET. Aunque los parámetros de las solicitudes POST se envían en los encabezados, las solicitudes GET las incluyen en la URL. Se desglosan aquí para facilitar la lectura.

Haga clic con el botón derecho en cualquier fila para copiarla ( `Ctrl+C` ) al portapapeles. También puede seleccionar varias entradas manteniendo presionada la `Shift` tecla o seleccionar todo ( `Ctrl+A` ).

### Cookies
Muestra las cookies enviadas o recibidas como pares de clave y valor.

Haga clic con el botón derecho en cualquier fila para copiarla ( `Ctrl+C` ) al portapapeles. También puede seleccionar varias entradas manteniendo presionada la `Shift` tecla o seleccionar todo ( `Ctrl+A` ).

Puede borrar las cookies almacenadas para el dominio dado de la [barra de herramientas](#network-summary) (botón**Borrar Cookies** ). 

### Intervalos

La pestaña **intervalos** proporciona una escala de tiempo de eventos de red implicados en la carga del recurso seleccionado. Es similar a la información que se encuentra en la columna *escala de tiempo* de la lista de [solicitudes de red](#network-request-list), pero también incluye los eventos que llevan a la solicitud enviada a través de la conexión, como el tiempo invertido en espera (*detenido*) en la cola de solicitudes, la resolución DNS y el establecimiento de la conexión TCP. 

![Pestaña intervalos del panel Detalles de la solicitud](./media/network_details_timings.png)

Se indican redireccionamientos a/desde otros recursos y al hacer clic en el vínculo se establece el foco en ese recurso en el panel de [detalles de solicitud](#request details) de red.

Los recursos cargados desde la caché no se ven afectados por la latencia de red, por lo que no se mostrará ningún gráfico de *intervalos* de red.

![Recurso Redirigido cargado desde la caché](./media/network_details_timings_cache_redirect.png)

Estos son los distintos eventos de red que puede ver para un recurso determinado, en orden cronológico:

#### Paralizado

Tiempo invertido esperando una conexión de red disponible en la cola de solicitudes. Para HTTP 1.0/1.1, Microsoft Edge permite un máximo de seis (6) conexiones TCP simultáneas por nombre de host. 

#### Resolver (DNS)

Tiempo dedicado a buscar la dirección IP del nombre de host del recurso en el DNS ([sistema de nombres de dominio](https://en.wikipedia.org/wiki/Domain_Name_System)).

#### Conexión (TCP)

Tiempo empleado en establecer la conexión TCP ([Protocolo de control de transmisión](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)).

#### SSL

Tiempo invertido en la negociación de una conexión SSL ([capa de sockets seguros](https://en.wikipedia.org/wiki/Transport_Layer_Security)) con el [servidor proxy](https://en.wikipedia.org/wiki/Proxy_server) para el host.

#### Remitente

Tiempo empleado en enviar la solicitud de recursos.

#### Esperando (TTFB)

Tiempo dedicado a esperar el primer byte de la respuesta del servidor host ("tiempo en el primer byte" o *TTFB*).

#### Descargar

Tiempo dedicado a leer la respuesta del servidor.

## Abreviados

| Acción                         | Método abreviado     |
|:-------------------------------|:-------------|
| Iniciar o detener sesión de generación de perfiles | `Ctrl` + `E` |
| Exportar como HAR                  | `Ctrl` + `S` |
| Buscar                           | `Ctrl` + `F` |
| Copiar                           | `Ctrl` + `C` |

## Problemas conocidos

### Error al iniciar el agente de recopilación de redes.

Si ve este mensaje de error: **el agente de recopilación de redes no se pudo iniciar** en la herramienta red, siga estos pasos para obtener una solución alternativa.

1. Presione `Windows Key`  +  `R` .

2. En el cuadro de diálogo Ejecutar, escriba **Services. msc**.
![problemas conocidos-1](./media/known_issues_1.PNG)

3. Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.
![problemas conocidos-2](./media/known_issues_2.PNG)

4. Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.
![problemas conocidos-3](./media/known_issues_3.PNG)

5. Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .

6. Ahora debe ver un distintivo de la reproducción junto a **red** y las solicitudes de red para su página web.
![problemas conocidos-4](./media/known_issues_4-network.PNG)

¿Aún tiene problemas? Envíenos sus comentarios con el icono para **Enviar comentarios** . 

![problemas conocidos-5](./media/known_issues_5.PNG)

### No se pudo detener el agente de recopilación de redes.

Si ve este mensaje de error: **el agente de recopilación de redes no se pudo detener** en la herramienta red, siga estos pasos para obtener una solución alternativa.

1. Presione `Windows Key`  +  `R` .

2. En el cuadro de diálogo Ejecutar, escriba **Services. msc**.
![problemas conocidos-1](./media/known_issues_1.PNG)

3. Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.
![problemas conocidos-2](./media/known_issues_2.PNG)

4. Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.
![problemas conocidos-3](./media/known_issues_3.PNG)

5. Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .

6. Ahora debe ver un distintivo de la reproducción junto a **red** y las solicitudes de red para su página web.
![problemas conocidos-4](./media/known_issues_4-network.PNG)

¿Aún tiene problemas? Envíenos sus comentarios con el icono para **Enviar comentarios** . 

![problemas conocidos-5](./media/known_issues_5.PNG)
