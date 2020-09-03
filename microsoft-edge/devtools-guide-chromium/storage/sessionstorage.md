---
description: Cómo ver y editar sessionStorage con el panel almacenamiento de la sesión y la consola.
title: Ver y editar el almacenamiento de sesión con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 24fca3fd3a068f3b2ffbe4ec1c23e6b80b968953
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993551"
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





# <span data-ttu-id="59ebe-104">Ver y editar el almacenamiento de sesión con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="59ebe-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="59ebe-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar [`sessionStorage`][MDNSessionStorage] pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="59ebe-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="59ebe-106">Ver las claves y los valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="59ebe-106">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="59ebe-107">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="59ebe-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="59ebe-108">El panel **manifiesto** se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="59ebe-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="59ebe-110">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="59ebe-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="59ebe-111">Expanda el menú almacenamiento de la **sesión** .</span><span class="sxs-lookup"><span data-stu-id="59ebe-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="El menú de almacenamiento de sesión" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="59ebe-113">El menú de **almacenamiento de sesión**</span><span class="sxs-lookup"><span data-stu-id="59ebe-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="59ebe-114">Seleccione un dominio para ver los pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="59ebe-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Pares clave-valor ' sessionStorage '" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="59ebe-116">`sessionStorage`Pares de clave y valor</span><span class="sxs-lookup"><span data-stu-id="59ebe-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="59ebe-117">Seleccione una fila de la tabla para ver el valor en el visor debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="59ebe-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Ver el valor de la clave x-SID" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="59ebe-119">Ver el valor de la `x-sid` clave</span><span class="sxs-lookup"><span data-stu-id="59ebe-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="59ebe-120">Crear un nuevo par clave-valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="59ebe-120">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="59ebe-121">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="59ebe-121">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="59ebe-122">Haga doble clic en la parte vacía de la tabla.</span><span class="sxs-lookup"><span data-stu-id="59ebe-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="59ebe-123">DevTools crea una fila nueva y centra el cursor en la columna de **clave** .</span><span class="sxs-lookup"><span data-stu-id="59ebe-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="59ebe-125">La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor</span><span class="sxs-lookup"><span data-stu-id="59ebe-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="59ebe-126">Editar claves o valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="59ebe-126">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="59ebe-127">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="59ebe-127">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="59ebe-128">Haga doble clic en una celda de la columna **clave** o **valor** para editar esa clave o valor.</span><span class="sxs-lookup"><span data-stu-id="59ebe-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Editar una clave de sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="59ebe-130">Modificar una `sessionStorage` tecla</span><span class="sxs-lookup"><span data-stu-id="59ebe-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="59ebe-131">Eliminar pares de clave y valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="59ebe-131">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="59ebe-132">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="59ebe-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="59ebe-133">Seleccione el par de clave y valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="59ebe-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="59ebe-134">DevTools lo resalta azul para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="59ebe-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="59ebe-135">Presione la `Delete` tecla o haga clic en **eliminar seleccionada** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="59ebe-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="59ebe-136">Eliminar todas las parejas de clave y valor de sessionStorage para un dominio</span><span class="sxs-lookup"><span data-stu-id="59ebe-136">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="59ebe-137">[Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="59ebe-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="59ebe-138">Seleccione **Borrar todo** \ ( ![ Borrar todo ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="59ebe-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="59ebe-139">Interactuar con sessionStorage desde la consola</span><span class="sxs-lookup"><span data-stu-id="59ebe-139">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="59ebe-140">Dado que puede ejecutar JavaScript en la **consola**y que la **consola** tiene acceso a los contextos de JavaScript de la página, es posible interactuar con él `sessionStorage` en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="59ebe-140">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="59ebe-141">Use el menú **contextos de JavaScript** para cambiar el contexto de JavaScript de la **consola** si desea acceder a los `sessionStorage` pares clave-valor de un dominio que no sea la página en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="59ebe-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Cambiar el contexto de JavaScript de la consola" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="59ebe-143">Cambiar el contexto de JavaScript de la consola</span><span class="sxs-lookup"><span data-stu-id="59ebe-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="59ebe-144">Ejecuta tus `sessionStorage` expresiones en la consola, de la misma manera en que lo harías en tu código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="59ebe-144">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interactuar con sessionStorage desde la consola" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="59ebe-146">Interactuar con `sessionStorage` desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="59ebe-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="59ebe-149">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="59ebe-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="59ebe-150">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="59ebe-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="59ebe-152">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="59ebe-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
