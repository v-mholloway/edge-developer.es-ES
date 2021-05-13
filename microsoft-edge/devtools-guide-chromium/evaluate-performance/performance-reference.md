---
description: El modo de eventos de escala de tiempo muestra todos los eventos desencadenados al realizar una grabación.  Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.
title: Referencia de evento de escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b8a15dd3503a891698d1f96bdc99946163d738ff
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564213"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="timeline-event-reference"></a>Referencia de evento de escala de tiempo  

El modo de eventos de escala de tiempo muestra todos los eventos desencadenados al realizar una grabación.  Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.  

## <a name="common-timeline-event-properties"></a>Propiedades de eventos de escala de tiempo comunes  

Algunos detalles están presentes en eventos de todos los tipos, mientras que algunos solo se aplican a determinados tipos de eventos.  En esta sección se enumeran las propiedades comunes a diferentes tipos de eventos.  Las propiedades específicas de determinados tipos de eventos se enumeran en las referencias para los tipos de eventos siguientes.  

| Propiedad | Cuándo se muestra |  
|:--- |:--- |  
| Tiempo agregado | Para eventos con **eventos anidados**, el tiempo que toma cada categoría de eventos. |  
| Pila de llamadas | Para eventos con **eventos secundarios**, el tiempo que toma cada categoría de eventos. |  
| Tiempo de CPU | Cuánto tiempo de CPU tardó el evento grabado. |  
| Detalles | Otros detalles sobre el evento. |  
| Duración \(at time-stamp\) | Cuánto tiempo tardó el evento con todos sus secundarios en completarse; timestamp es la hora en la que se produjo el evento, en relación con el momento en que se inició la grabación. |  
| Tiempo de autoservicio | Cuánto tiempo tardó el evento sin ninguno de sus secundarios. |  
| Tamaño de montón usado | Cantidad de memoria que usa la aplicación cuando se registró el evento y el delta \(+/-\) cambia en el tamaño del montón usado desde el último muestreo. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a>Cargar eventos  

En esta sección se enumeran los eventos que pertenecen a la categoría Loading y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| ANALIZAR HTML |  Microsoft Edge el algoritmo de análisis HTML. |  
| Finalizar la carga |  Una solicitud de red completada. |  
| Recibir datos |  Se recibieron los datos de una solicitud.  Hay uno o varios eventos De recepción de datos. |  
| Respuesta de recepción |  La respuesta HTTP inicial de una solicitud. |  
| Enviar solicitud |  Se ha enviado una solicitud de red. |  

### <a name="loading-event-properties"></a>Cargar propiedades de evento  

| Propiedad | Descripción |  
|:--- |:--- |  
| Recurso | Dirección URL del recurso solicitado. |  
| Vista previa | Vista previa del recurso solicitado \(solo imágenes\). |  
| Request (método) | Método HTTP usado para la solicitud \( `GET` o `POST` , por ejemplo\). |  
| Código de estado | Código de respuesta HTTP. |  
| Tipo MIME | Tipo MIME del recurso solicitado. |  
| Longitud de datos codificada | Longitud del recurso solicitado en bytes. |  

## <a name="scripting-events"></a>Eventos de scripting  

En esta sección se enumeran los eventos que pertenecen a la categoría Scripting y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| Fotograma de animación desencadenado | Se desencadena un marco de animación programado y se invoca su controlador de devolución de llamada. |  
| Cancelar fotograma de animación |  Se canceló un marco de animación programado. |  
| Evento GC |  Se produjo la recolección de elementos no utilizados. |  
| DOMContentLoaded |  El explorador despidió el evento [DOMContentLoaded.][MDNWindowDOMContentLoadedEvent]  Este evento se desencadena cuando se carga y analiza todo el contenido DOM de la página. |  
| Evaluar script | Se evaluó un script. |  
| Evento | Un evento De JavaScript \(por ejemplo, `mousedown` o `key` \). |  
| Llamada de función | Se realizó una llamada de función de JavaScript de nivel superior \(solo aparece cuando el explorador entra en el motor de JavaScript\). |  
| Instalar temporizador | Se creó un temporizador [con setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] o [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout]. |  
| Fotograma de animación de solicitud | Una `requestAnimationFrame()` llamada programó un nuevo marco. |  
| Quitar temporizador | Se ha borrado un temporizador creado anteriormente. |  
| Tiempo |  Un script denominado [console.time()][ConsoleApiTime]. |  
| Fin de la hora | Un script denominado [console.timeEnd()][ConsoleApiTimeEnd]. |  
| Temporizador desencadenado | Temporizador desencadenado que estaba programado con `setInterval()` o `setTimeout()` . |  
| XHR Ready State Change | Se ha cambiado el estado listo de un OBJETO XMLHTTPRequest. |  
| Carga XHR | Una `XMLHTTPRequest` carga finalizada. |  

### <a name="scripting-event-properties"></a>Propiedades del evento Scripting  

| Propiedad | Descripción |  
|:--- |:--- |  
| Id. del temporizador | El identificador del temporizador. |  
| Tiempo de espera agotado | Tiempo de espera especificado por el temporizador. |  
| Repeticiones | Boolean que especifica si el temporizador se repite. |  
| Llamada de función | Función que se invocó. |  

## <a name="rendering-events"></a>Eventos de representación  

En esta sección se enumeran los eventos que pertenecen a la categoría Representación y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| Invalidar diseño | El diseño de página se invalidó mediante un cambio de DOM. |  
| Diseño | Se completó un diseño de página. |  
| Recalcular estilo | Microsoft Edge de elementos recalculados. |  
| Scroll | El contenido de la vista anidada se desplazó. |  

### <a name="rendering-event-properties"></a>Propiedades de evento de representación  

| Propiedad | Descripción |  
|:--- |:--- |  
| Diseño invalidado | Para los registros de diseño, el seguimiento de pila del código que provocó la invalidación del diseño. |  
| Nodos que necesitan diseño | Para los registros de diseño, el número de nodos que se marcaron como diseño necesario antes de que se iniciara el relayout.  Estos son normalmente los nodos que se invalidaron mediante código de desarrollador, además de una ruta hacia arriba para volver a la raíz de layout. |  
| Tamaño del árbol de diseño | Para los registros layout, el número total de nodos bajo la raíz de relayout \(el nodo que Microsoft Edge inicia el relayout\). |  
| Ámbito de diseño | Los valores posibles `Partial` son \(el límite de nuevo diseño es una parte del DOM\) o `Whole document` . |  
| Elementos afectados | Para volver a calcular los registros de estilo, el número de elementos afectados por una actualización de estilo. |  
| Estilos invalidados | Para volver a calcular los registros de estilo, proporciona el seguimiento de pila del código que provocó la invalidación del estilo. |  

## <a name="painting-events"></a>Eventos de pintura  

En esta sección se enumeran los eventos que pertenecen a la categoría Painting y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| Capas compuestas | Las capas de imagen compuestas para el Microsoft Edge de representación. |  
| Descodificación de imágenes | Se descodificó un recurso de imagen. |  
| Cambio de tamaño de imagen | Se ha cambiado el tamaño de una imagen desde sus dimensiones nativas. |  
| Paint | Las capas compuestas se pintaron en una región de la pantalla.  Al pasar el mouse sobre Paint de datos se resalta la región de la pantalla que se actualizó. |  

### <a name="painting-event-properties"></a>Propiedades del evento Painting  

| Propiedad | Descripción |  
|:--- |:--- |  
| Ubicación | Para Paint eventos, las coordenadas x e y del rectángulo de pintura. |  
| Dimensiones | Para Paint eventos, el alto y el ancho de la región pintada. |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time: Referencia de api de consola"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd: referencia de api de consola"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Ventana: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) y es creado por [Meggin Kearney][MegginKearney] \(Tech Writer\) y [Flavio Copes][FlavioCopes] \(Full Stack Developer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors#flavio-copes  
