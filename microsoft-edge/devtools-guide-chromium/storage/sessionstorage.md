---
title: Ver y editar el almacenamiento de sesión con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612084"
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





# <span data-ttu-id="7be2f-103">Ver y editar el almacenamiento de sesión con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7be2f-103">View And Edit Session Storage With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="7be2f-104">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar [`sessionStorage`][MDNSessionStorage] pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="7be2f-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="7be2f-105">Ver las claves y los valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="7be2f-105">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="7be2f-106">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="7be2f-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="7be2f-107">El panel **manifiesto** se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7be2f-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-108">Figura 1</span><span class="sxs-lookup"><span data-stu-id="7be2f-108">Figure 1</span></span>  
    > <span data-ttu-id="7be2f-109">El panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="7be2f-109">The Manifest pane</span></span>  
    > ![El panel manifiesto][ImageManifest]  

1.  <span data-ttu-id="7be2f-111">Expanda el menú almacenamiento de la **sesión** .</span><span class="sxs-lookup"><span data-stu-id="7be2f-111">Expand the **Session Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="7be2f-112">Figure 2</span></span>  
    > <span data-ttu-id="7be2f-113">El menú de **almacenamiento de sesión**</span><span class="sxs-lookup"><span data-stu-id="7be2f-113">The **Session Storage** Menu</span></span>  
    > ![El menú de almacenamiento de sesión][ImageSessionStorageMenu]  

1.  <span data-ttu-id="7be2f-115">Seleccione un dominio para ver los pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="7be2f-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-116">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="7be2f-116">Figure 3</span></span>  
    > <span data-ttu-id="7be2f-117">Pares de clave y valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="7be2f-117">The sessionStorage key-value pairs</span></span>  
    > ![Pares clave-valor ' sessionStorage '][ImageSessionStorage]  

1.  <span data-ttu-id="7be2f-119">Seleccione una fila de la tabla para ver el valor en el visor debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7be2f-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-120">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="7be2f-120">Figure 4</span></span>  
    > <span data-ttu-id="7be2f-121">Ver el valor de la `x-sid` clave</span><span class="sxs-lookup"><span data-stu-id="7be2f-121">Viewing the value of the `x-sid` key</span></span>  
    > ![Ver el valor de la clave x-SID][ImageSessionStorageViewer]  

## <span data-ttu-id="7be2f-123">Crear un nuevo par clave-valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="7be2f-123">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="7be2f-124">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="7be2f-124">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="7be2f-125">Haga doble clic en la parte vacía de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7be2f-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="7be2f-126">DevTools crea una fila nueva y centra el cursor en la columna de **clave** .</span><span class="sxs-lookup"><span data-stu-id="7be2f-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-127">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="7be2f-127">Figure 5</span></span>  
    > <span data-ttu-id="7be2f-128">La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor</span><span class="sxs-lookup"><span data-stu-id="7be2f-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor][ImageSessionStorageCreate]  

## <span data-ttu-id="7be2f-130">Editar claves o valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="7be2f-130">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="7be2f-131">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="7be2f-131">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="7be2f-132">Haga doble clic en una celda de la columna **clave** o **valor** para editar esa clave o valor.</span><span class="sxs-lookup"><span data-stu-id="7be2f-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-133">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="7be2f-133">Figure 6</span></span>  
    > <span data-ttu-id="7be2f-134">Editar una `sessionStorage` clave</span><span class="sxs-lookup"><span data-stu-id="7be2f-134">Editing a `sessionStorage` key</span></span>  
    > ![Editar una clave de sessionStorage][ImageSessionStorageEdit]  

## <span data-ttu-id="7be2f-136">Eliminar pares de clave y valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="7be2f-136">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="7be2f-137">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="7be2f-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="7be2f-138">Seleccione el par de clave y valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="7be2f-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="7be2f-139">DevTools lo resalta azul para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7be2f-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="7be2f-140">Presione la `Delete` tecla o haga clic en **eliminar** selección ![ eliminar seleccionados ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="7be2f-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="7be2f-141">Eliminar todas las parejas de clave y valor de sessionStorage para un dominio</span><span class="sxs-lookup"><span data-stu-id="7be2f-141">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="7be2f-142">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="7be2f-142">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="7be2f-143">Seleccione **Borrar** todo ![ Borrar todo ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="7be2f-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="7be2f-144">Interactuar con sessionStorage desde la consola</span><span class="sxs-lookup"><span data-stu-id="7be2f-144">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="7be2f-145">Dado que puede ejecutar JavaScript en la **consola**y que la **consola** tiene acceso a los contextos de JavaScript de la página, es posible interactuar con él `sessionStorage` en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="7be2f-145">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="7be2f-146">Use el menú **contextos de JavaScript** para cambiar el contexto de JavaScript de la **consola** si desea acceder a los `sessionStorage` pares clave-valor de un dominio que no sea la página en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="7be2f-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-147">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="7be2f-147">Figure 7</span></span>  
    > <span data-ttu-id="7be2f-148">Cambiar el contexto de JavaScript de la **consola**</span><span class="sxs-lookup"><span data-stu-id="7be2f-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Cambiar el contexto de JavaScript de la consola][ImageJSContext]  

1.  <span data-ttu-id="7be2f-150">Ejecuta tus `sessionStorage` expresiones en la consola, de la misma manera en que lo harías en tu código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7be2f-150">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="7be2f-151">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="7be2f-151">Figure 8</span></span>  
    > <span data-ttu-id="7be2f-152">Interacción con `sessionStorage` desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="7be2f-152">Interacting with `sessionStorage` from the **Console**</span></span>  
    > ![Interacción con sessionStorage desde la consola][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Ilustración 1: el panel manifiesto"  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Ilustración 2: menú de almacenamiento de sesión"  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Ilustración 3: los pares de clave y valor de sessionStorage"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Ilustración 4: ver el valor de la clave x-SID"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Ilustración 5: la parte vacía de la tabla para crear un nuevo par clave-valor"  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Ilustración 6: edición de una clave de sessionStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Ilustración 7: cambiar el contexto de JavaScript de la consola"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Ilustración 8: interacción con sessionStorage desde la consola"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="7be2f-164">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7be2f-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7be2f-165">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7be2f-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7be2f-167">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7be2f-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
