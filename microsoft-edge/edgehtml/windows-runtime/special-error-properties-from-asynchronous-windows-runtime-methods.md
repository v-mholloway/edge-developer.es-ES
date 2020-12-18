---
description: Propiedades de error especiales de métodos asincrónicos de Windows Runtime.
title: Propiedades de error especial de métodos asíncronos de Windows Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3557d0097d632f4058e46acbff748f7177d24ab1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236197"
---
# <span data-ttu-id="9f23b-103">Propiedades de error especiales de métodos asíncronos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="9f23b-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="9f23b-104">Puede ser difícil depurar métodos asincrónicos de Windows Runtime en JavaScript, porque el error puede producirse desde cualquier parte de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="9f23b-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="9f23b-105">El objeto de JavaScript `Error` tiene propiedades adicionales que solo aparecen cuando el error se produce en un método asincrónico de Windows en tiempo de ejecución cuando la aplicación se está ejecutando en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="9f23b-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="9f23b-106">Propiedades de error especial</span><span class="sxs-lookup"><span data-stu-id="9f23b-106">Special error properties</span></span>  

<span data-ttu-id="9f23b-107">Un objeto de error que es el resultado de una operación asincrónica errónea de Windows Runtime en el modo de depuración tiene las siguientes propiedades especiales:</span><span class="sxs-lookup"><span data-stu-id="9f23b-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="9f23b-108">\ (Objeto \) obtiene información sobre la ubicación original en la que se realizó la llamada que produjo un error.</span><span class="sxs-lookup"><span data-stu-id="9f23b-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="9f23b-109">La propiedad `asyncOpSource.originatingCall` \ (cadena \) muestra la ubicación en el código del usuario que originó la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9f23b-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="9f23b-110">asyncOpType \ (cadena \) obtiene el nombre del tipo de operación asincrónica que ha provocado el error.</span><span class="sxs-lookup"><span data-stu-id="9f23b-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="9f23b-111">Para obtener más información sobre los errores con operaciones asincrónicas, vea:</span><span class="sxs-lookup"><span data-stu-id="9f23b-111">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="9f23b-112">Cómo controlar errores con promesas</span><span class="sxs-lookup"><span data-stu-id="9f23b-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="9f23b-113">Solución de errores de Windows en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="9f23b-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Cómo controlar errores con promesas (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solución de errores de Windows Runtime (HTML) | Microsoft docs"  
