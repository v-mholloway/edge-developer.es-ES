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
# <span data-ttu-id="65d91-103">Dominios de protocolo de DevTools</span><span class="sxs-lookup"><span data-stu-id="65d91-103">DevTools Protocol Domains</span></span>
## [<span data-ttu-id="65d91-104">Depurador</span><span class="sxs-lookup"><span data-stu-id="65d91-104">Debugger</span></span>](debugger.md)
<span data-ttu-id="65d91-105">El dominio del depurador expone capacidades de depuración de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="65d91-105">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="65d91-106">Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.</span><span class="sxs-lookup"><span data-stu-id="65d91-106">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>
## [<span data-ttu-id="65d91-107">Página</span><span class="sxs-lookup"><span data-stu-id="65d91-107">Page</span></span>](page.md)
<span data-ttu-id="65d91-108">Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.</span><span class="sxs-lookup"><span data-stu-id="65d91-108">Actions and events related to the inspected page belong to the page domain.</span></span>
## [<span data-ttu-id="65d91-109">Motores</span><span class="sxs-lookup"><span data-stu-id="65d91-109">Runtime</span></span>](runtime.md)
<span data-ttu-id="65d91-110">El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos.</span><span class="sxs-lookup"><span data-stu-id="65d91-110">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="65d91-111">Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto.</span><span class="sxs-lookup"><span data-stu-id="65d91-111">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="65d91-112">Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="65d91-112">Original objects are maintained in memory unless they are either explicitly released.</span></span>
## [<span data-ttu-id="65d91-113">Esquema</span><span class="sxs-lookup"><span data-stu-id="65d91-113">Schema</span></span>](schema.md)
<span data-ttu-id="65d91-114">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="65d91-114">Provides information about the protocol schema.</span></span>