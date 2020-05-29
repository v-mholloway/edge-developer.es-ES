---
title: Propiedades de error especiales de métodos asincrónicos de Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5cf2604e26c84e769cf44e0879ee137cbfbe8b90
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574915"
---
# <span data-ttu-id="47392-102">Propiedades de error especiales de métodos asincrónicos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="47392-102">Special Error Properties from Asynchronous Windows Runtime Methods</span></span>  

<span data-ttu-id="47392-103">Puede ser difícil depurar métodos asincrónicos de Windows Runtime en JavaScript, porque el error puede producirse desde cualquier parte de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="47392-103">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span> <span data-ttu-id="47392-104">El objeto de JavaScript `Error` tiene propiedades adicionales que solo aparecen cuando el error se produce en un método asincrónico de Windows en tiempo de ejecución cuando la aplicación se está ejecutando en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="47392-104">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="47392-105">Propiedades de error especial</span><span class="sxs-lookup"><span data-stu-id="47392-105">Special Error Properties</span></span>  

<span data-ttu-id="47392-106">Un objeto de error que es el resultado de una operación asincrónica errónea de Windows Runtime en el modo de depuración tiene las siguientes propiedades especiales:</span><span class="sxs-lookup"><span data-stu-id="47392-106">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="47392-107">\ (Objeto \) obtiene información sobre la ubicación original en la que se realizó la llamada que produjo un error.</span><span class="sxs-lookup"><span data-stu-id="47392-107">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span> <span data-ttu-id="47392-108">La propiedad `asyncOpSource.originatingCall` \ (cadena \) muestra la ubicación en el código del usuario que originó la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="47392-108">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="47392-109">asyncOpType \ (cadena \) obtiene el nombre del tipo de operación asincrónica que ha provocado el error.</span><span class="sxs-lookup"><span data-stu-id="47392-109">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="47392-110">Para obtener más información sobre los errores con operaciones asincrónicas, vea:</span><span class="sxs-lookup"><span data-stu-id="47392-110">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="47392-111">Cómo controlar errores con promesas</span><span class="sxs-lookup"><span data-stu-id="47392-111">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="47392-112">Solución de errores de Windows en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="47392-112">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- image links -->  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Cómo controlar errores con las promesas (HTML)"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solución de errores de Windows Runtime (HTML)"  
