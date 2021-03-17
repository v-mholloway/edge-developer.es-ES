---
description: Cómo ver y editar localStorage con el panel Almacenamiento local y la consola.
title: Ver y editar el almacenamiento local con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4eebf3108e7b1c6ecaecbfed445e8f3fe26215c4
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439678"
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

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="d0486-104">Ver y editar el almacenamiento local con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d0486-104">View and edit local storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d0486-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar pares [clave-valor localStorage.][MDNWindowsLocalStorage]</span><span class="sxs-lookup"><span data-stu-id="d0486-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <a name="view-localstorage-keys-and-values"></a><span data-ttu-id="d0486-106">Ver claves y valores de localStorage</span><span class="sxs-lookup"><span data-stu-id="d0486-106">View localStorage keys and values</span></span>  

1.  <span data-ttu-id="d0486-107">Elija la **pestaña** Aplicación para abrir la **herramienta** Aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0486-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="d0486-108">El **panel** Manifiesto se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d0486-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="d0486-110">Panel **Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="d0486-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d0486-111">Expanda el **menú Almacenamiento** local.</span><span class="sxs-lookup"><span data-stu-id="d0486-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Menú Almacenamiento local" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="d0486-113">Menú **Almacenamiento** local</span><span class="sxs-lookup"><span data-stu-id="d0486-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d0486-114">Elija un dominio para ver los pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="d0486-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Los pares clave-valor localStorage para el https://www.bing.com dominio" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="d0486-116">Pares `localStorage` clave-valor para el `https://www.bing.com` dominio</span><span class="sxs-lookup"><span data-stu-id="d0486-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d0486-117">Elija una fila de la tabla para ver el valor en el visor debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d0486-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Ver el valor de la eventLogQueue_Online clave" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="d0486-119">Ver el valor de la `eventLogQueue_Online` clave</span><span class="sxs-lookup"><span data-stu-id="d0486-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a><span data-ttu-id="d0486-120">Crear un nuevo par clave-valor localStorage</span><span class="sxs-lookup"><span data-stu-id="d0486-120">Create a new localStorage key-value pair</span></span>  

1.  <span data-ttu-id="d0486-121">[Ver los pares clave-valor localStorage de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d0486-121">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d0486-122">Haga doble clic en la parte vacía de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d0486-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="d0486-123">DevTools crea una nueva fila y centra el cursor en la **columna** Clave.</span><span class="sxs-lookup"><span data-stu-id="d0486-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="d0486-125">La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor</span><span class="sxs-lookup"><span data-stu-id="d0486-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a><span data-ttu-id="d0486-126">Editar claves o valores de localStorage</span><span class="sxs-lookup"><span data-stu-id="d0486-126">Edit localStorage keys or values</span></span>  

1.  <span data-ttu-id="d0486-127">[Ver los pares clave-valor localStorage de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d0486-127">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d0486-128">Haga doble clic en una celda de la **columna Clave** **o** Valor para editar esa clave o valor.</span><span class="sxs-lookup"><span data-stu-id="d0486-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Editar una clave localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="d0486-130">Editar una `localStorage` clave</span><span class="sxs-lookup"><span data-stu-id="d0486-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a><span data-ttu-id="d0486-131">Eliminar pares clave-valor localStorage</span><span class="sxs-lookup"><span data-stu-id="d0486-131">Delete localStorage key-value pairs</span></span>  

1.  <span data-ttu-id="d0486-132">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d0486-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d0486-133">Elija el par clave-valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="d0486-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="d0486-134">DevTools lo resalta en azul para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d0486-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="d0486-135">Seleccione la `Delete` clave o elija Eliminar **seleccionado** \( Eliminar ![ seleccionado ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="d0486-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="d0486-136">Eliminar todos `localStorage` los pares clave-valor de un dominio</span><span class="sxs-lookup"><span data-stu-id="d0486-136">Delete all `localStorage` key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="d0486-137">[Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d0486-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d0486-138">Elija **Borrar todo** \( Borrar todo ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="d0486-138">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\).</span></span>  
    
## <a name="interact-with-localstorage-from-the-console"></a><span data-ttu-id="d0486-139">Interactuar con localStorage desde la consola</span><span class="sxs-lookup"><span data-stu-id="d0486-139">Interact with localStorage from the Console</span></span>  

<span data-ttu-id="d0486-140">Dado que puede ejecutar JavaScript en la \*\*\*\* consola **y**dado que la consola tiene acceso a los contextos de JavaScript de la página, es posible interactuar con desde `localStorage` la **consola**.</span><span class="sxs-lookup"><span data-stu-id="d0486-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="d0486-141">Use el **menú contextos de JavaScript** para \*\*\*\* cambiar el contexto de JavaScript de la consola si desea tener acceso a los pares clave-valor de un dominio distinto de la página `localStorage` que se muestra.</span><span class="sxs-lookup"><span data-stu-id="d0486-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Cambiar el contexto de JavaScript de la consola" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="d0486-143">Cambiar el contexto de JavaScript de la consola</span><span class="sxs-lookup"><span data-stu-id="d0486-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d0486-144">Ejecute las `localStorage` expresiones en la consola, lo mismo que en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d0486-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interactuar con localStorage desde la consola" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="d0486-146">Interactuar con `localStorage` desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="d0486-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d0486-147">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d0486-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (Chromium) | Microsoft Docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="d0486-150">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0486-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d0486-151">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="d0486-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d0486-153">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0486-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
