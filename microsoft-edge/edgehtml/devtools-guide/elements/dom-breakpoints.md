---
description: Usar puntos de interrupción de DOM para depurar visualmente problemas de diseño en la página
title: Puntos de interrupción de DevTools-Elements-DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, elementos, puntos de interrupción Dom, mutación Dom
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb60fa0497c98c152ca2c5adf28e9dee5d7c9f98
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236178"
---
# Puntos de interrupción DOM

Administre los puntos de interrupción de mutación de DOM desde este panel, incluyendo la desactivación, la eliminación y el reenlace.

Puedes usar puntos de interrupción de mutación de DOM para irrumpir en el depurador cada vez que cambie un nodo de elemento seleccionado. Esto es útil para realizar un seguimiento del código responsable de causar problemas visuales con la interfaz de usuario sin tener que establecer puntos de interrupción individuales en cada una de las API de 450 + DOM de *EdgeHTML* que pueden desencadenar dichos cambios. 

Para establecer un punto de interrupción de DOM, haga clic con el botón derecho en cualquier elemento de la *vista de árbol html* del panel **elementos** para abrir el menú contextual.

![Menú contextual de puntos de interrupción DOM](../media/elements_dom_breakpoints_contextmenu.png)

Puede establecer cualquiera de los siguientes puntos de interrupción:

 - **Interrupción en el nodo quitado**: salto en el depurador cuando el elemento seleccionado se quita del documento (árbol DOM).

 - **Interrupción en subárbol modificada**: salto en el depurador cuando se cambia cualquiera de los descendientes del elemento seleccionado (se agregan, se quitan o se modifican sus subárboles). Esto no se interrumpe cuando se modifican los atributos (consulte la siguiente opción para ello).

 - **Break on Attribute Modified**: salto en el depurador cuando se agrega un atributo al elemento seleccionado, se quita o cambia en Value.

El panel **puntos de interrupción Dom** mostrará el elemento seleccionado (generando un selector que describe su ubicación en el Dom) y los tipos de puntos de interrupción que ha establecido (*nodo eliminado, subárbol modificado, atributo modificado*). Desde aquí, también puede volver a *enlazar*, *deshabilitar*o *eliminar* los puntos de interrupción, individualmente (desde el menú contextual RT-click) o todos a la vez (mediante los botones).

![Panel de puntos de interrupción DOM](../media/elements_dom_breakpoints.png)

## Persistencia de puntos de interrupción

Los puntos de interrupción se almacenan (en el ámbito de la dirección URL de la página en la que están establecidos) como parte de la configuración de DevTools. Cuando se vuelva a cargar la página o se cierren las herramientas y se vuelvan a abrir, DevTools intentará volver a enlazar los puntos de interrupción a sus elementos asociados.

Los puntos de interrupción que no se podían volver a enlazar automáticamente se indican con un icono de advertencia en el círculo del punto de interrupción. En estos, puede esperar a volver a enlazar el elemento manualmente (con el botón **reenlazar punto de interrupción** o la opción de menú contextual) una vez que aparezca el elemento correspondiente en el Dom (y el icono punto de interrupción ya no muestra el indicador de advertencia) o **eliminar** el punto de interrupción por completo.

![Indicador de punto de interrupción sin enlazar](../media/elements_dom_breakpoint_unbound.png)

Además de este panel de *puntos de interrupción Dom* , también puede administrar los [puntos de interrupción de Dom](../debugger.md#dom-breakpoints) desde dentro del **depurador**.

## Limitaciones actuales

Tenga en cuenta las siguientes limitaciones de la depuración de puntos de interrupción de DOM en Edge DevTools:

- Edge DevTools actualmente no admite el reenlace de puntos de interrupción dentro de [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe). Si establece un punto de interrupción en un iframe y cierra la DevTools de borde o actualiza la página, se perderá el punto de interrupción.

- Si el script encuentra un punto de interrupción ejecutado de forma sincrónica antes de que [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) se complete el Dom, no podrá establecer un punto de interrupción de Dom mientras el depurador está en pausa. Por lo general, puede resolver esta situación configurando los [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) atributos o los atributos de la [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) secuencia de comandos.

- En el caso de las secuencias de comandos sincrónicas, desencadenamos un reenlace automático de los puntos de interrupción cuando [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) se llama al evento. En este caso, es posible que se pierdan los puntos de interrupción que se activarían durante la creación inicial de DOM por scripting. Para las secuencias de comandos asincrónicas, desencadenamos un intento de volver a enlazar antes de que se ejecute el primer script, por lo que los puntos de interrupción se pueden volver a enlazar y desencadenar como se desee.
