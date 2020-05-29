---
description: Lista de referencias para dominios admitidos en el protocolo Microsoft Edge DevTools, versión 0,1.
title: 'Dominios: Protocolo de DevTools versión 0,1'
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: b3cf3411a8402b7407012eb789f8bf267b4997a8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573755"
---
# Dominios de protocolo de DevTools
## [Depurador](debugger.md)
El dominio del depurador expone capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.
## [Página](page.md)
Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
## [Motores](runtime.md)
El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos. Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto. Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.
## [Esquema](schema.md)
Proporciona información sobre el esquema de protocolo.