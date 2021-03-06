---
description: Propiedades de error especial de métodos asíncronos de Windows Runtime
title: Propiedades de error especial de métodos asíncronos de Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9f2fdb007f00c2ab1d1a2050378af80f0075db6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398843"
---
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a><span data-ttu-id="f07b5-103">Propiedades de error especiales de métodos asíncronos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="f07b5-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="f07b5-104">Puede ser difícil depurar métodos asincrónicos de Windows Runtime en JavaScript, ya que el error puede producirse desde algún lugar profundo de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f07b5-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="f07b5-105">El objeto JavaScript tiene propiedades adicionales que solo aparecen cuando se produce el error desde un método asincrónico de Windows Runtime cuando la aplicación se ejecuta `Error` en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="f07b5-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <a name="special-error-properties"></a><span data-ttu-id="f07b5-106">Propiedades de error especiales</span><span class="sxs-lookup"><span data-stu-id="f07b5-106">Special error properties</span></span>  

<span data-ttu-id="f07b5-107">Un objeto de error que resulta de una operación asincrónica de Windows Runtime con error en modo de depuración tiene las siguientes propiedades especiales:</span><span class="sxs-lookup"><span data-stu-id="f07b5-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="f07b5-108">\(Object\) Obtiene información sobre la ubicación original donde se realizó la llamada que produjo un error.</span><span class="sxs-lookup"><span data-stu-id="f07b5-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="f07b5-109">La propiedad \(String\) muestra la ubicación en el código del usuario que `asyncOpSource.originatingCall` originó la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f07b5-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="f07b5-110">asyncOpType \(String\) Obtiene el nombre del tipo de operación asincrónica que ha producido el error.</span><span class="sxs-lookup"><span data-stu-id="f07b5-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="f07b5-111">Para obtener más información acerca de los errores con operaciones asincrónicas, vea:</span><span class="sxs-lookup"><span data-stu-id="f07b5-111">For more information about errors with asynchronous operations, see:</span></span>  

*   [<span data-ttu-id="f07b5-112">Cómo controlar errores con promesas</span><span class="sxs-lookup"><span data-stu-id="f07b5-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="f07b5-113">Solución de errores de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="f07b5-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Cómo controlar errores con promesas (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solución de problemas de errores de Windows Runtime (HTML) | Microsoft Docs"  
