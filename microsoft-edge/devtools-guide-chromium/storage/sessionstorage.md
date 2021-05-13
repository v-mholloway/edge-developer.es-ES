---
description: Cómo ver y editar sessionStorage con el panel De Storage sesión y la consola.
title: Ver y editar session Storage con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6d686a6eb7bc6fca46d65c46fa9c5aee044ec052
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565067"
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
# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="fd0a0-104">Ver y editar session Storage con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fd0a0-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="fd0a0-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] ver, editar y eliminar pares [clave-valor sessionStorage.][MDNSessionStorage]</span><span class="sxs-lookup"><span data-stu-id="fd0a0-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [sessionStorage][MDNSessionStorage] key-value pairs.</span></span>  

## <a name="view-sessionstorage-keys-and-values"></a><span data-ttu-id="fd0a0-106">Ver claves y valores sessionStorage</span><span class="sxs-lookup"><span data-stu-id="fd0a0-106">View sessionStorage keys and values</span></span>  

1.  <span data-ttu-id="fd0a0-107">Elija la **pestaña** Aplicación para abrir la **herramienta** Aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="fd0a0-108">El \*\*\*\* panel Manifiesto se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-108">The **Manifest** panel is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="fd0a0-110">Panel **Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="fd0a0-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fd0a0-111">Expanda el **menú Storage** sesión.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Menú de Storage sesión" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="fd0a0-113">Menú **de Storage** sesión</span><span class="sxs-lookup"><span data-stu-id="fd0a0-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fd0a0-114">Elija un dominio para ver los pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Pares clave-valor sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="fd0a0-116">Pares `sessionStorage` clave-valor</span><span class="sxs-lookup"><span data-stu-id="fd0a0-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fd0a0-117">Elija una fila de la tabla para ver el valor en el visor debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Ver el valor de la clave x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="fd0a0-119">Ver el valor de la `x-sid` clave</span><span class="sxs-lookup"><span data-stu-id="fd0a0-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a><span data-ttu-id="fd0a0-120">Crear un nuevo par clave-valor sessionStorage</span><span class="sxs-lookup"><span data-stu-id="fd0a0-120">Create a new sessionStorage key-value pair</span></span>  

1.  <span data-ttu-id="fd0a0-121">[Ver los pares clave-valor sessionStorage de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="fd0a0-121">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="fd0a0-122">Haga doble clic en la parte vacía de la tabla.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="fd0a0-123">DevTools crea una nueva fila y centra el cursor en la **columna** Clave.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="fd0a0-125">La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor</span><span class="sxs-lookup"><span data-stu-id="fd0a0-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a><span data-ttu-id="fd0a0-126">Editar claves o valores sessionStorage</span><span class="sxs-lookup"><span data-stu-id="fd0a0-126">Edit sessionStorage keys or values</span></span>  

1.  <span data-ttu-id="fd0a0-127">[Ver los pares clave-valor sessionStorage de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="fd0a0-127">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="fd0a0-128">Haga doble clic en una celda de la **columna Clave** **o** Valor para editar esa clave o valor.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Editar una clave sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="fd0a0-130">Editar una `sessionStorage` clave</span><span class="sxs-lookup"><span data-stu-id="fd0a0-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a><span data-ttu-id="fd0a0-131">Eliminar pares clave-valor sessionStorage</span><span class="sxs-lookup"><span data-stu-id="fd0a0-131">Delete sessionStorage key-value pairs</span></span>  

1.  <span data-ttu-id="fd0a0-132">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="fd0a0-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="fd0a0-133">Elija el par clave-valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="fd0a0-134">DevTools lo resalta en azul para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="fd0a0-135">Seleccione la `Delete` clave o elija Eliminar **seleccionado** \( Eliminar ![ seleccionado ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="fd0a0-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="fd0a0-136">Eliminar todos los pares clave-valor sessionStorage de un dominio</span><span class="sxs-lookup"><span data-stu-id="fd0a0-136">Delete all sessionStorage key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="fd0a0-137">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="fd0a0-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="fd0a0-138">Elija **Borrar todo** \( Borrar todo ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="fd0a0-138">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\).</span></span>  
    
## <a name="interact-with-sessionstorage-from-the-console"></a><span data-ttu-id="fd0a0-139">Interactuar con sessionStorage desde la consola</span><span class="sxs-lookup"><span data-stu-id="fd0a0-139">Interact with sessionStorage from the Console</span></span>  

<span data-ttu-id="fd0a0-140">Dado que puede ejecutar JavaScript en \*\*\*\* la consola **y**dado que la consola tiene acceso a los contextos de JavaScript de la página, es posible interactuar con desde `sessionStorage` la **consola**.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-140">Since you may run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="fd0a0-141">Use el **menú contextos de JavaScript** para \*\*\*\* cambiar el contexto de JavaScript de la consola si desea tener acceso a los pares clave-valor de un dominio distinto de la página en la que `sessionStorage` se encuentra.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Cambiar el contexto de JavaScript de la consola" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="fd0a0-143">Cambiar el contexto de JavaScript de la **consola**</span><span class="sxs-lookup"><span data-stu-id="fd0a0-143">Change the JavaScript context of the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fd0a0-144">Ejecute las `sessionStorage` expresiones en la **consola,** lo mismo que su JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fd0a0-144">Run your `sessionStorage` expressions in the **Console**, the same as your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interactuar con sessionStorage desde la consola" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="fd0a0-146">Interactuar con `sessionStorage` desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="fd0a0-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="fd0a0-147">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fd0a0-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Herramientas para desarrolladores | Microsoft Docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="fd0a0-150">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd0a0-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fd0a0-151">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="fd0a0-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fd0a0-153">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd0a0-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
