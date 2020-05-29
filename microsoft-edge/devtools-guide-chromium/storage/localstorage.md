---
title: Ver y editar el almacenamiento local con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612014"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="6b424-103">Ver y editar el almacenamiento local con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6b424-103">View And Edit Local Storage With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="6b424-104">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar [`localStorage`][MDNWindowsLocalStorage] pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="6b424-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`localStorage`][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="6b424-105">Ver las claves y los valores de localStorage</span><span class="sxs-lookup"><span data-stu-id="6b424-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="6b424-106">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="6b424-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="6b424-107">El panel **manifiesto** se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6b424-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="6b424-108">Figura 1</span><span class="sxs-lookup"><span data-stu-id="6b424-108">Figure 1</span></span>  
    > <span data-ttu-id="6b424-109">El panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="6b424-109">The Manifest pane</span></span>  
    > ![El panel manifiesto][ImageManifest]  

1.  <span data-ttu-id="6b424-111">Expanda el menú **almacenamiento local** .</span><span class="sxs-lookup"><span data-stu-id="6b424-111">Expand the **Local Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="6b424-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="6b424-112">Figure 2</span></span>  
    > <span data-ttu-id="6b424-113">El menú **almacenamiento local** muestra dos dominios: `https://business.bing.com` y</span><span class="sxs-lookup"><span data-stu-id="6b424-113">The **Local Storage** menu shows two domains: `https://business.bing.com` and</span></span> `https://www.bing.com`  
    > ![El menú almacenamiento local][ImageLocalStorageMenu]  

1.  <span data-ttu-id="6b424-115">Seleccione un dominio para ver los pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="6b424-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="6b424-116">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="6b424-116">Figure 3</span></span>  
    > <span data-ttu-id="6b424-117">`localStorage`Pares clave-valor para el `https://www.bing.com` dominio</span><span class="sxs-lookup"><span data-stu-id="6b424-117">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    > ![Pares de clave y valor de localStorage para el https://www.bing.com dominio][ImageLocalStorage]  

1.  <span data-ttu-id="6b424-119">Seleccione una fila de la tabla para ver el valor en el visor debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6b424-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="6b424-120">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="6b424-120">Figure 4</span></span>  
    > <span data-ttu-id="6b424-121">Ver el valor de la `eventLogQueue_Online` clave</span><span class="sxs-lookup"><span data-stu-id="6b424-121">Viewing the value of the `eventLogQueue_Online` key</span></span>  
    > ![Visualización del valor de la tecla eventLogQueue_Online][ImageLocalStorageViewer]  

## <span data-ttu-id="6b424-123">Crear un nuevo `localStorage` par clave-valor</span><span class="sxs-lookup"><span data-stu-id="6b424-123">Create a new `localStorage` key-value pair</span></span>   

1.  <span data-ttu-id="6b424-124">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="6b424-124">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="6b424-125">Haga doble clic en la parte vacía de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6b424-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="6b424-126">DevTools crea una fila nueva y centra el cursor en la columna de **clave** .</span><span class="sxs-lookup"><span data-stu-id="6b424-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="6b424-127">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="6b424-127">Figure 5</span></span>  
    > <span data-ttu-id="6b424-128">La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor</span><span class="sxs-lookup"><span data-stu-id="6b424-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor][ImageLocalStorageCreate]  

## <span data-ttu-id="6b424-130">Modificar `localStorage` claves o valores</span><span class="sxs-lookup"><span data-stu-id="6b424-130">Edit `localStorage` keys or values</span></span>   

1.  <span data-ttu-id="6b424-131">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="6b424-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="6b424-132">Haga doble clic en una celda de la columna **clave** o **valor** para editar esa clave o valor.</span><span class="sxs-lookup"><span data-stu-id="6b424-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="6b424-133">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="6b424-133">Figure 6</span></span>  
    > <span data-ttu-id="6b424-134">Editar una `localStorage` clave</span><span class="sxs-lookup"><span data-stu-id="6b424-134">Editing a `localStorage` key</span></span>  
    > ![Editar una clave de localStorage][ImageLocalStorageEdit]  

## <span data-ttu-id="6b424-136">Eliminar `localStorage` pares clave-valor</span><span class="sxs-lookup"><span data-stu-id="6b424-136">Delete `localStorage` key-value pairs</span></span>   

1.  <span data-ttu-id="6b424-137">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="6b424-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="6b424-138">Seleccione el par de clave y valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="6b424-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="6b424-139">DevTools lo resalta azul para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="6b424-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="6b424-140">Presione la `Delete` tecla o haga clic en **eliminar** selección ![ eliminar seleccionados ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="6b424-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="6b424-141">Eliminar todos los `localStorage` pares clave-valor para un dominio</span><span class="sxs-lookup"><span data-stu-id="6b424-141">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="6b424-142">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="6b424-142">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="6b424-143">Seleccione **Borrar** todo ![ Borrar todo ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="6b424-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="6b424-144">Interactuar con `localStorage` desde la consola</span><span class="sxs-lookup"><span data-stu-id="6b424-144">Interact with `localStorage` from the Console</span></span>   

<span data-ttu-id="6b424-145">Dado que puede ejecutar JavaScript en la **consola**y que la **consola** tiene acceso a los contextos de JavaScript de la página, es posible interactuar con ella `localStorage` en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="6b424-145">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="6b424-146">Use el menú **contextos de JavaScript** para cambiar el contexto de JavaScript de la **consola** si desea obtener acceso a los `localStorage` pares clave-valor de un dominio que no sea la página que se muestra.</span><span class="sxs-lookup"><span data-stu-id="6b424-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    > ##### <span data-ttu-id="6b424-147">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="6b424-147">Figure 7</span></span>  
    > <span data-ttu-id="6b424-148">Cambiar el contexto de JavaScript de la **consola**</span><span class="sxs-lookup"><span data-stu-id="6b424-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Cambiar el contexto de JavaScript de la consola][ImageJSContext]  

1.  <span data-ttu-id="6b424-150">Ejecuta tus `localStorage` expresiones en la consola, de la misma forma en que lo haces en tu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6b424-150">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="6b424-151">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="6b424-151">Figure 8</span></span>  
    > <span data-ttu-id="6b424-152">Interacción con `localStorage` desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="6b424-152">Interacting with `localStorage` from the **Console**</span></span>  
    > ![Interacción con localStorage desde la consola][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Ilustración 1: el panel manifiesto"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Ilustración 2: el menú almacenamiento local"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Ilustración 3: los pares de clave y valor de localStorage para el https://www.bing.com dominio"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Ilustración 4: ver el valor de la clave eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Ilustración 5: la parte vacía de la tabla para crear un nuevo par clave-valor"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Ilustración 6: edición de una clave de localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Ilustración 7: cambiar el contexto de JavaScript de la consola"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Ilustración 8: interacción con localStorage desde la consola"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="6b424-164">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6b424-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6b424-165">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6b424-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6b424-167">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6b424-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
