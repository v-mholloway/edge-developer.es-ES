---
description: Uso de métodos asincrónicos de Windows Runtime.
title: Usar métodos asíncronos en tiempo de ejecución de Windows Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 26ed26e07049a9488aebe5fda92a65550474b51c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236193"
---
# <span data-ttu-id="344aa-103">Usar métodos asíncronos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="344aa-103">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="344aa-104">Muchos métodos de Windows Runtime, sobre todo aquellos que pueden tardar mucho tiempo en completarse, son asíncronos.</span><span class="sxs-lookup"><span data-stu-id="344aa-104">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="344aa-105">Estos métodos devuelven generalmente una acción o operación asincrónica \ (por ejemplo,,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` o `Windows.Foundation.IAsyncOperationWithProgress` \).</span><span class="sxs-lookup"><span data-stu-id="344aa-105">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="344aa-106">Estos métodos están representados en JavaScript por el [patrón CommonJS/promesas/A][CommonjsWikiPromises].</span><span class="sxs-lookup"><span data-stu-id="344aa-106">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="344aa-107">Es decir, devuelven un objeto Promise que tiene una [función then][PreviousVersionsWindowsAppsBr229728], para la que debe proporcionar una `completed` función que controle el resultado si la operación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="344aa-107">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="344aa-108">Si no desea proporcionar un controlador de errores, debe usar la [función Done][PreviousVersionsWindowsAppsHr701079] en lugar de la `then` función.</span><span class="sxs-lookup"><span data-stu-id="344aa-108">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="344aa-109">Las características de Windows en tiempo de ejecución no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="344aa-109">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="344aa-110">Ejemplos de métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="344aa-110">Examples of asynchronous methods</span></span>  

<span data-ttu-id="344aa-111">En el ejemplo siguiente, la `then` función toma un parámetro que representa el valor completado del `createResourceAsync` método.</span><span class="sxs-lookup"><span data-stu-id="344aa-111">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="344aa-112">En este caso, si `createResourceAsync` se produce un error en el método, devuelve una promesa en el estado del error, pero no inicia una excepción.</span><span class="sxs-lookup"><span data-stu-id="344aa-112">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="344aa-113">Puede controlar un error con la función de la `then` siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="344aa-113">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="344aa-114">Si no desea controlar el error de forma explícita, pero desea que inicie una excepción, puede usar la `done` función en su lugar.</span><span class="sxs-lookup"><span data-stu-id="344aa-114">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="344aa-115">También puede mostrar el progreso realizado hacia la finalización mediante una tercera función.</span><span class="sxs-lookup"><span data-stu-id="344aa-115">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
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

<span data-ttu-id="344aa-116">Para obtener más información sobre la programación asincrónica, vea [programación asincrónica en JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="344aa-116">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <span data-ttu-id="344aa-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="344aa-117">See also</span></span>  

[<span data-ttu-id="344aa-118">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="344aa-118">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar Windows Runtime en JavaScript | Microsoft docs"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise. then (método) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programación asincrónica en JavaScript (HTML) | Microsoft docs"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise. Done | Microsoft docs"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promesas | Wiki de especificaciones de CommonJS"  
