---
title: Referencia de evento de escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611723"
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





# Referencia de evento de escala de tiempo   




El modo eventos de escala de tiempo muestra todos los eventos desencadenados mientras se realiza una grabación.  Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.  

## Propiedades de evento de escala de tiempo comunes  

Algunos detalles están presentes en eventos de todos los tipos, mientras que algunos solo se aplican a determinados tipos de eventos.  En esta sección se enumeran las propiedades comunes a los distintos tipos de eventos.  Las propiedades específicas de determinados tipos de eventos se muestran en las referencias de los siguientes tipos de eventos.  

| Propiedad | ¿Cuándo se muestra? |  
|:--- |:--- |  
| Tiempo agregado | Para eventos con **eventos anidados**, el tiempo que toma cada categoría de eventos. |  
| Pila de llamadas | Para eventos con **eventos secundarios**, el tiempo que toma cada categoría de eventos. |  
| Tiempo de CPU | La cantidad de tiempo de CPU que tomó el evento registrado. |  
| Detalles | Otros detalles sobre el evento. |  
| Duration \ (en la marca de hora \) | Cuánto tiempo duró el evento con todos sus elementos secundarios para completar. TIMESTAMP es la hora en que se produjo el evento, en relación con la grabación iniciada. |  
| Tiempo propio | Cuánto tiempo lleva el evento sin ninguno de sus elementos secundarios. |  
| Tamaño de montón usado | Cantidad de memoria usada por la aplicación cuando se registró el evento y el cambio Delta \ (+/-\) en el tamaño de montón usado desde el último muestreo. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## Cargando eventos  

En esta sección se enumeran los eventos que pertenecen a la categoría de carga y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| Analizar HTML |  Microsoft Edge ejecutó el algoritmo de análisis HTML. |  
| Finalizar la carga |  Una solicitud de red completada. |  
| Recibir datos |  Se recibieron datos para una solicitud.  Hay uno o más eventos de datos de recepción. |  
| Recibir respuesta |  La respuesta HTTP inicial de una solicitud. |  
| Enviar solicitud |  Se ha enviado una solicitud de red. |  

### Cargando propiedades de evento  

| Propiedad | Descripción |  
|:--- |:--- |  
| Recurso | Dirección URL del recurso solicitado. |  
| Vista previa | Vista previa del recurso solicitado \ (solo imágenes \). |  
| Método de solicitud | Método HTTP usado para la solicitud \ ( `GET` o `POST` , por ejemplo, \). |  
| Código de estado | Código de respuesta HTTP. |  
| Tipo MIME | Tipo MIME del recurso solicitado. |  
| Longitud de datos codificados | Longitud del recurso solicitado en bytes. |  

## Eventos de scripting  

En esta sección se enumeran los eventos que pertenecen a la categoría de scripting y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| Marco de animación desencadenado | Se activó un marco de animación programada y se llamará a su controlador de devolución de llamada. |  
| Cancelar marco de animación |  Se ha cancelado un marco de animación programado. |  
| Evento GC |  Se realizó la recolección de elementos no utilizados. |  
| DOMContentLoaded |  El [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] fue desencadenado por el explorador.  Este evento se desencadena cuando todo el contenido de DOM de la página se ha cargado y analizado. |  
| Evaluar script | Se evaluó un script. |  
| Evento | Un evento de JavaScript \ (por ejemplo, `mousedown` , o `key` \). |  
| Llamada de función | Se realizó una llamada de función de JavaScript de nivel superior \ (solo aparece cuando el explorador escribe el motor de JavaScript \). |  
| Instalar cronómetro | Se creó un temporizador con [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] o [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout]. |  
| Marco de animación de la solicitud | Una `requestAnimationFrame()` llamada programó un nuevo marco. |  
| Quitar cronómetro | Se borró un temporizador creado previamente. |  
| Tiempo |  Un script denominado [Console. Time ()][ConsoleApiTime]. |  
| Hora de finalización | Un script denominado [Console. timeEnd ()][ConsoleApiTimeEnd]. |  
| Cronómetro desencadenado | Un temporizador desencadenado que se programó con `setInterval()` o `setTimeout()` . |  
| Cambio de estado de XHR listo | El estado de lista de un XMLHTTPRequest ha cambiado. |  
| Carga de XHR | `XMLHTTPRequest`Finalizó la carga. |  

### Propiedades de eventos de scripting  

| Propiedad | Descripción |  
|:--- |:--- |  
| IDENTIFICADOR del temporizador | IDENTIFICADOR del temporizador. |  
| Tiempo de espera agotado | El tiempo de espera especificado por el temporizador. |  
| Repite | Valor booleano que especifica si el temporizador se repite. |  
| Llamada de función | Una función que se invocó. |  

## Representar eventos  

En esta sección se enumeran los eventos que pertenecen a la categoría de representación y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| Invalidar diseño | Un cambio de DOM invalidó el diseño de página. |  
| Diseño | Se completó un diseño de página. |  
| Recalcular estilo | Estilos de elemento recalculado de Microsoft Edge. |  
| Scroll | Se ha desplazado el contenido de la vista anidada. |  

### Representación de propiedades de eventos  

| Propiedad | Descripción |  
|:--- |:--- |  
| Diseño invalidado | En los registros de diseño, el seguimiento de la pila del código que causó que se invalidara el diseño. |  
| Nodos que necesitan diseño | En los registros de diseño, el número de nodos que se han marcado como que necesitan diseño antes de que se inicie el redistribución.  Suelen ser aquellos nodos que el código del desarrollador invalidó, además de una ruta de acceso ascendente para rediseñar la raíz. |  
| Tamaño del árbol de diseño | En los registros de diseño, el número total de nodos en la raíz de redistribución \ (el nodo en el que Microsoft Edge inicia el rediseño \). |  
| Ámbito de diseño | Los valores posibles son `Partial` \ (el límite de redistribución es una parte del DOM \) o `Whole document` . |  
| Elementos afectados | Para volver a calcular los registros de estilo, el número de elementos afectados por un nuevo cálculo de estilo. |  
| Estilos invalidados | Para recalcular los registros de estilo, proporciona el seguimiento de pila del código que causó la invalidación de estilo. |  

## Eventos de pintura  

En esta sección se enumeran los eventos que pertenecen a la categoría de pintura y sus propiedades.  

| Evento | Descripción |  
|:--- |:--- |  
| Capas compuestas | Las capas de imagen compuestas para el motor de representación de Microsoft Edge. |  
| Descodificación de imagen | Se ha descodificado un recurso de imagen. |  
| Cambiar el tamaño de la imagen | Se ha cambiado el tamaño de una imagen desde sus dimensiones nativas. |  
| Paint | Las capas compuestas se han pintado en una región de la pantalla.  Al mantener el puntero sobre un registro de pintura, se resalta la región de la pantalla que se ha actualizado. |  

### Propiedades de evento de dibujo  

| Propiedad | Descripción |  
|:--- |:--- |  
| Ubicación | Para eventos de pintura, las coordenadas x e y del rectángulo de pintura. |  
| Dimensiones | Para eventos de pintura, el alto y el ancho de la región pintada. |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Referencia de la API de consola de hora"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd: referencia de la API de consola"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Ventana: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Flavio Copes][FlavioCopes] \ (desarrollador de pila completa \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
