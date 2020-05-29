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
# Uso de los métodos asincrónicos de Windows Runtime  

Muchos métodos de Windows Runtime, sobre todo aquellos que pueden tardar mucho tiempo en completarse, son asíncronos.  Normalmente, estos métodos devuelven una acción o operación asincrónica (por ejemplo,,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` o `Windows.Foundation.IAsyncOperationWithProgress` ).  Estos métodos están representados en JavaScript por el [patrón CommonJS/promesas/A][CommonjsWikiPromises].  Es decir, devuelven un objeto Promise que tiene una [función then][PreviousVersionsWindowsAppsBr229728], para la que debe proporcionar una `completed` función que controle el resultado si la operación se realiza correctamente.  Si no desea proporcionar un controlador de errores, debe usar la [función Done][PreviousVersionsWindowsAppsHr701079] en lugar de la `then` función.  

> [!IMPORTANT]
> Las características de Windows en tiempo de ejecución no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.  

## Ejemplos de métodos asincrónicos  

En el ejemplo siguiente, la `then` función toma un parámetro que representa el valor completado del `createResourceAsync` método.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

En este caso, si `createResourceAsync` se produce un error en el método, devuelve una promesa en el estado del error, pero no inicia una excepción.  Puede controlar un error con la función de la `then` siguiente manera.  

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

Si no desea controlar el error de forma explícita, pero desea que inicie una excepción, puede usar la `done` función en su lugar.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

También puede mostrar el progreso realizado hacia la finalización mediante una tercera función.  

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

Para obtener más información sobre la programación asincrónica, vea [programación asincrónica en JavaScript][PreviousVersionsWindowsAppsHh700330].  

## Consulta también  

[Usar Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar Windows Runtime en JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Método Promise. then"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programación asincrónica en JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise. Done"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promesas | Wiki de especificaciones de CommonJS"  
