---
description: Lista de referencias para dominios admitidos en el protocolo Microsoft Edge DevTools, versión 0,1.
title: DevTools Protocol Domains-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: de816e2b07838ba1b6151967ff7b8751789c60ea
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882950"
---
# DevTools Protocol Domains-DevTools Protocol version 0,1 (EdgeHTML)  

## [Depurador](debugger.md)  

El dominio del depurador expone capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.
## [Página](page.md)
Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
## [Tiempo de ejecución](runtime.md)
El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos. Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto. Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.
## [Esquema](schema.md)
Proporciona información sobre el esquema de protocolo.