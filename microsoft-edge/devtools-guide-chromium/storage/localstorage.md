---
title: Ver y editar el almacenamiento local con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 72aee823d3a3143ae7399c7057f3b606bd1078c3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983537"
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





# <span data-ttu-id="030c0-103">Ver y editar el almacenamiento local con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="030c0-103">View and edit local storage with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="030c0-104">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar [localStorage][MDNWindowsLocalStorage] pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="030c0-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="030c0-105">Ver las claves y los valores de localStorage</span><span class="sxs-lookup"><span data-stu-id="030c0-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="030c0-106">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="030c0-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="030c0-107">El panel **manifiesto** se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="030c0-107">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="030c0-109">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="030c0-109">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="030c0-110">Expanda el menú **almacenamiento local** .</span><span class="sxs-lookup"><span data-stu-id="030c0-110">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="El menú almacenamiento local" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="030c0-112">El menú **almacenamiento local**</span><span class="sxs-lookup"><span data-stu-id="030c0-112">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="030c0-113">Seleccione un dominio para ver los pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="030c0-113">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Pares de clave y valor de localStorage para el https://www.bing.com dominio" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="030c0-115">`localStorage`Pares clave-valor para el `https://www.bing.com` dominio</span><span class="sxs-lookup"><span data-stu-id="030c0-115">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="030c0-116">Seleccione una fila de la tabla para ver el valor en el visor debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="030c0-116">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Ver el valor de la clave eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="030c0-118">Ver el valor de la `eventLogQueue_Online` clave</span><span class="sxs-lookup"><span data-stu-id="030c0-118">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="030c0-119">Crear un nuevo par clave-valor de localStorage</span><span class="sxs-lookup"><span data-stu-id="030c0-119">Create a new localStorage key-value pair</span></span>   

1.  <span data-ttu-id="030c0-120">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="030c0-120">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="030c0-121">Haga doble clic en la parte vacía de la tabla.</span><span class="sxs-lookup"><span data-stu-id="030c0-121">Double-click the empty part of the table.</span></span>  <span data-ttu-id="030c0-122">DevTools crea una fila nueva y centra el cursor en la columna de **clave** .</span><span class="sxs-lookup"><span data-stu-id="030c0-122">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="030c0-124">La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor</span><span class="sxs-lookup"><span data-stu-id="030c0-124">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="030c0-125">Editar claves o valores de localStorage</span><span class="sxs-lookup"><span data-stu-id="030c0-125">Edit localStorage keys or values</span></span>   

1.  <span data-ttu-id="030c0-126">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="030c0-126">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="030c0-127">Haga doble clic en una celda de la columna **clave** o **valor** para editar esa clave o valor.</span><span class="sxs-lookup"><span data-stu-id="030c0-127">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Editar una clave de localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="030c0-129">Modificar una `localStorage` tecla</span><span class="sxs-lookup"><span data-stu-id="030c0-129">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="030c0-130">Eliminar pares de clave y valor de localStorage</span><span class="sxs-lookup"><span data-stu-id="030c0-130">Delete localStorage key-value pairs</span></span>   

1.  <span data-ttu-id="030c0-131">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="030c0-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="030c0-132">Seleccione el par de clave y valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="030c0-132">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="030c0-133">DevTools lo resalta azul para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="030c0-133">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="030c0-134">Presione la `Delete` tecla o haga clic en **eliminar seleccionada** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="030c0-134">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="030c0-135">Eliminar todos los `localStorage` pares clave-valor para un dominio</span><span class="sxs-lookup"><span data-stu-id="030c0-135">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="030c0-136">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="030c0-136">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="030c0-137">Seleccione **Borrar todo** \ ( ![ Borrar todo ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="030c0-137">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="030c0-138">Interactuar con localStorage desde la consola</span><span class="sxs-lookup"><span data-stu-id="030c0-138">Interact with localStorage from the Console</span></span>   

<span data-ttu-id="030c0-139">Dado que puede ejecutar JavaScript en la **consola**y que la **consola** tiene acceso a los contextos de JavaScript de la página, es posible interactuar con ella `localStorage` en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="030c0-139">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="030c0-140">Use el menú **contextos de JavaScript** para cambiar el contexto de JavaScript de la **consola** si desea obtener acceso a los `localStorage` pares clave-valor de un dominio que no sea la página que se muestra.</span><span class="sxs-lookup"><span data-stu-id="030c0-140">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Cambiar el contexto de JavaScript de la consola" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="030c0-142">Cambiar el contexto de JavaScript de la consola</span><span class="sxs-lookup"><span data-stu-id="030c0-142">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="030c0-143">Ejecuta tus `localStorage` expresiones en la consola, de la misma forma en que lo haces en tu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="030c0-143">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interactuar con localStorage desde la consola" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="030c0-145">Interactuar con `localStorage` desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="030c0-145">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="030c0-148">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="030c0-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="030c0-149">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="030c0-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="030c0-151">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="030c0-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
