---
title: Uso de los métodos asincrónicos de Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6d0f174d22d0d13571d78bc215356ad90a0ae7fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574910"
---
# <span data-ttu-id="bc83b-102">Uso de los métodos asincrónicos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="bc83b-102">Using Windows Runtime Asynchronous Methods</span></span>  

<span data-ttu-id="bc83b-103">Muchos métodos de Windows Runtime, sobre todo aquellos que pueden tardar mucho tiempo en completarse, son asíncronos.</span><span class="sxs-lookup"><span data-stu-id="bc83b-103">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="bc83b-104">Normalmente, estos métodos devuelven una acción o operación asincrónica (por ejemplo,,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` o `Windows.Foundation.IAsyncOperationWithProgress` ).</span><span class="sxs-lookup"><span data-stu-id="bc83b-104">These methods generally return an asynchronous action or operation (for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`).</span></span>  <span data-ttu-id="bc83b-105">Estos métodos están representados en JavaScript por el [patrón CommonJS/promesas/A][CommonjsWikiPromises].</span><span class="sxs-lookup"><span data-stu-id="bc83b-105">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="bc83b-106">Es decir, devuelven un objeto Promise que tiene una [función then][PreviousVersionsWindowsAppsBr229728], para la que debe proporcionar una `completed` función que controle el resultado si la operación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="bc83b-106">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="bc83b-107">Si no desea proporcionar un controlador de errores, debe usar la [función Done][PreviousVersionsWindowsAppsHr701079] en lugar de la `then` función.</span><span class="sxs-lookup"><span data-stu-id="bc83b-107">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="bc83b-108">Las características de Windows en tiempo de ejecución no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bc83b-108">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="bc83b-109">Ejemplos de métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="bc83b-109">Examples of Asynchronous Methods</span></span>  

<span data-ttu-id="bc83b-110">En el ejemplo siguiente, la `then` función toma un parámetro que representa el valor completado del `createResourceAsync` método.</span><span class="sxs-lookup"><span data-stu-id="bc83b-110">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="bc83b-111">En este caso, si `createResourceAsync` se produce un error en el método, devuelve una promesa en el estado del error, pero no inicia una excepción.</span><span class="sxs-lookup"><span data-stu-id="bc83b-111">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="bc83b-112">Puede controlar un error con la función de la `then` siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="bc83b-112">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="bc83b-113">Si no desea controlar el error de forma explícita, pero desea que inicie una excepción, puede usar la `done` función en su lugar.</span><span class="sxs-lookup"><span data-stu-id="bc83b-113">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="bc83b-114">También puede mostrar el progreso realizado hacia la finalización mediante una tercera función.</span><span class="sxs-lookup"><span data-stu-id="bc83b-114">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
            },
    // Error.
            function(error) {
               alert("Failed to create a resource.");
            },
    // Progress.
            function(progress, resultSoFar) {
               setProgressBar(progress);
            });
```  

<span data-ttu-id="bc83b-115">Para obtener más información sobre la programación asincrónica, vea [programación asincrónica en JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="bc83b-115">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <span data-ttu-id="bc83b-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="bc83b-116">See Also</span></span>  

[<span data-ttu-id="bc83b-117">Usar Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="bc83b-117">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar Windows Runtime en JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Método Promise. then"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programación asincrónica en JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise. Done"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promesas | Wiki de especificaciones de CommonJS"  
