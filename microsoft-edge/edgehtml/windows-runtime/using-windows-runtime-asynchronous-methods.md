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
# <a name="using-windows-runtime-asynchronous-methods"></a>Usar métodos asíncronos de Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Muchos métodos de Windows Runtime, especialmente los que pueden tardar mucho tiempo en completarse, son asincrónicos.  Por lo general, estos métodos devuelven una acción o operación asincrónica \(por ejemplo, `Windows.Foundation.IAsyncAction` , `Windows.Foundation.IAsyncOperation` , o `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).  Estos métodos se representan en JavaScript mediante el patrón [CommonJS/Promises/A][CommonjsWikiPromises].  Es decir, devuelven un objeto Promise que tiene una función [then][PreviousVersionsWindowsAppsBr229728], para la que debe proporcionar una función que controle el resultado si `completed` la operación se realiza correctamente.  Si no desea proporcionar un controlador de errores, debe usar la [función done][PreviousVersionsWindowsAppsHr701079] en lugar de la `then` función.  

> [!IMPORTANT]
> Las características de Windows Runtime no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.  

## <a name="examples-of-asynchronous-methods"></a>Ejemplos de métodos asincrónicos  

En el ejemplo siguiente, la `then` función toma un parámetro que representa el valor completado del `createResourceAsync` método.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

En este caso, si se produce un error en el método, devuelve una promesa en estado de error, pero no `createResourceAsync` produce una excepción.  Puede controlar un error mediante la `then` función de la siguiente manera.  

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

Si no desea controlar el error explícitamente, pero desea que se lance una excepción, puede usar la `done` función en su lugar.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

También puede mostrar el progreso realizado hacia la finalización mediante una tercera función.  

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

Para obtener más información acerca de la programación asincrónica, vea [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].  

## <a name="see-also"></a>Consulte también  

[Use Windows en tiempo de ejecución en JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Uso de Windows Runtime en JavaScript | Microsoft Docs"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Método Promise.then | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programación asincrónica en JavaScript (HTML) | Microsoft Docs"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise.done | Microsoft Docs"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promesas | Wiki de especificaciones commonJS"  
