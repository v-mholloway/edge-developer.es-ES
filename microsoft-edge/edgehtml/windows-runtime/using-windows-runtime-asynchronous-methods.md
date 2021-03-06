---
description: Usar métodos asíncronos en tiempo de ejecución de Windows Runtime
title: Usar métodos asíncronos en tiempo de ejecución de Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c7e8ac4690525ee89a06eccf843531c2c7a20324
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398157"
---
# <a name="using-windows-runtime-asynchronous-methods"></a><span data-ttu-id="e1a06-103">Usar métodos asíncronos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="e1a06-103">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="e1a06-104">Muchos métodos de Windows Runtime, especialmente los que pueden tardar mucho tiempo en completarse, son asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="e1a06-104">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="e1a06-105">Por lo general, estos métodos devuelven una acción o operación asincrónica \(por ejemplo, `Windows.Foundation.IAsyncAction` , `Windows.Foundation.IAsyncOperation` , o `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).</span><span class="sxs-lookup"><span data-stu-id="e1a06-105">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="e1a06-106">Estos métodos se representan en JavaScript mediante el patrón [CommonJS/Promises/A][CommonjsWikiPromises].</span><span class="sxs-lookup"><span data-stu-id="e1a06-106">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="e1a06-107">Es decir, devuelven un objeto Promise que tiene una función [then][PreviousVersionsWindowsAppsBr229728], para la que debe proporcionar una función que controle el resultado si `completed` la operación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1a06-107">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="e1a06-108">Si no desea proporcionar un controlador de errores, debe usar la [función done][PreviousVersionsWindowsAppsHr701079] en lugar de la `then` función.</span><span class="sxs-lookup"><span data-stu-id="e1a06-108">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="e1a06-109">Las características de Windows Runtime no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e1a06-109">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="examples-of-asynchronous-methods"></a><span data-ttu-id="e1a06-110">Ejemplos de métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="e1a06-110">Examples of asynchronous methods</span></span>  

<span data-ttu-id="e1a06-111">En el ejemplo siguiente, la `then` función toma un parámetro que representa el valor completado del `createResourceAsync` método.</span><span class="sxs-lookup"><span data-stu-id="e1a06-111">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="e1a06-112">En este caso, si se produce un error en el método, devuelve una promesa en estado de error, pero no `createResourceAsync` produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="e1a06-112">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="e1a06-113">Puede controlar un error mediante la `then` función de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="e1a06-113">You can handle an error by using the `then` function as follows.</span></span>  

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

<span data-ttu-id="e1a06-114">Si no desea controlar el error explícitamente, pero desea que se lance una excepción, puede usar la `done` función en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e1a06-114">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="e1a06-115">También puede mostrar el progreso realizado hacia la finalización mediante una tercera función.</span><span class="sxs-lookup"><span data-stu-id="e1a06-115">You can also display the progress made towards completion by using a third function.</span></span>  

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

<span data-ttu-id="e1a06-116">Para obtener más información acerca de la programación asincrónica, vea [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="e1a06-116">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1a06-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e1a06-117">See also</span></span>  

[<span data-ttu-id="e1a06-118">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="e1a06-118">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Uso de Windows Runtime en JavaScript | Microsoft Docs"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Método Promise.then | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programación asincrónica en JavaScript (HTML) | Microsoft Docs"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise.done | Microsoft Docs"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promesas | Wiki de especificaciones commonJS"  
