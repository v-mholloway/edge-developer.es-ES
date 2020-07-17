---
description: Lista de referencias para dominios admitidos en el protocolo Microsoft Edge DevTools, versión 0,2.
title: DevTools Protocol Domains-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: ba56b31bb750eb9c575c6d13ef296aae6604e99f
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882754"
---
# DevTools Protocol Domains-DevTools Protocol version 0,2 (EdgeHTML)  

## [CSS](css.md)  

Este dominio expone las operaciones de lectura y escritura de CSS. Todos los objetos CSS (hojas de estilos, reglas y estilos) tienen un `id` uso asociado en las siguientes operaciones en el objeto relacionado. Cada tipo de objeto tiene una `id` estructura específica, y no se pueden cambiar entre objetos de diferentes tipos. Los objetos CSS se pueden cargar mediante las `get*ForNode()` llamadas (que aceptan un identificador de nodo DOM). Un cliente también puede realizar un seguimiento de las hojas de estilos a través de los `styleSheetAdded` / `styleSheetRemoved` eventos y cargar posteriormente el contenido de la hoja de estilos necesaria con los `getStyleSheet[Text]()` métodos.
## [DOM](dom.md)
Este dominio expone las operaciones de lectura y escritura de DOM. Cada nodo DOM se representa con su objeto reflejado que tiene una `id` . Esto `id` se puede usar para obtener información adicional sobre el nodo, resolverlo en el contenedor de objetos de JavaScript, etc. Es importante que el cliente reciba eventos DOM solo para los nodos que son conocidos para el cliente. El back-end realiza un seguimiento de los nodos que se enviaron al cliente y nunca envía dos veces el mismo nodo. Es responsabilidad del cliente recopilar información acerca de los nodos que se enviaron al cliente.<p>Tenga en cuenta que `iframe` los elementos propietarios devolverán los elementos del documento correspondientes como sus nodos secundarios.</p>
## [DOMDebugger](domdebugger.md)
La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos. La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.
## [Depurador](debugger.md)
El dominio del depurador expone capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.
## [Overlay](overlay.md)
El dominio de superposición expone elementos visuales y la interacción de selección de nodos
## [Página](page.md)
Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
## [Tiempo de ejecución](runtime.md)
El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos. Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto. Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.
## [Esquema](schema.md)
Proporciona información sobre el esquema de protocolo.