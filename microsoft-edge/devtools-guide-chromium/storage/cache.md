---
description: Cómo ver datos de caché desde el panel Aplicación de Microsoft Edge DevTools.
title: Ver datos de caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0ce4dbbf2456579abe84fca48bca8106384995dd
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439320"
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

# <a name="view-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="565b0-104">Ver datos de caché con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="565b0-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="565b0-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los [datos de caché.][MDNCache]</span><span class="sxs-lookup"><span data-stu-id="565b0-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="565b0-106">Si está intentando inspeccionar los datos de [caché HTTP,][MDNHTTPCaching] esta no es la guía que desea.</span><span class="sxs-lookup"><span data-stu-id="565b0-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="565b0-107">Busque la información en la columna **Tamaño** del registro **de red**.</span><span class="sxs-lookup"><span data-stu-id="565b0-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="565b0-108">Vaya a [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="565b0-108">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <a name="view-cache-data"></a><span data-ttu-id="565b0-109">Ver datos de caché</span><span class="sxs-lookup"><span data-stu-id="565b0-109">View cache data</span></span>  

1.  <span data-ttu-id="565b0-110">Elija la **pestaña** Aplicación para abrir **el** panel Aplicación.</span><span class="sxs-lookup"><span data-stu-id="565b0-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="565b0-111">El **panel Manifiesto** normalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="565b0-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="565b0-113">Panel **Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="565b0-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="565b0-114">Expanda la **sección Almacenamiento de caché** para ver las memorias caché disponibles.</span><span class="sxs-lookup"><span data-stu-id="565b0-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Cachés disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="565b0-116">Cachés disponibles</span><span class="sxs-lookup"><span data-stu-id="565b0-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="565b0-117">Elija una memoria caché para ver el contenido.</span><span class="sxs-lookup"><span data-stu-id="565b0-117">Choose a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Ver el contenido de una memoria caché" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="565b0-119">Ver el contenido de una memoria caché</span><span class="sxs-lookup"><span data-stu-id="565b0-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="565b0-120">Elija un recurso para ver los encabezados HTTP en la sección debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="565b0-120">Choose a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Ver los encabezados HTTP de un recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="565b0-122">Ver los encabezados HTTP de un recurso</span><span class="sxs-lookup"><span data-stu-id="565b0-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="565b0-123">Elija **Vista** previa para ver el contenido de un recurso.</span><span class="sxs-lookup"><span data-stu-id="565b0-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Ver el contenido de un recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="565b0-125">Ver el contenido de un recurso</span><span class="sxs-lookup"><span data-stu-id="565b0-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a><span data-ttu-id="565b0-126">Actualizar un recurso</span><span class="sxs-lookup"><span data-stu-id="565b0-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="565b0-127">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="565b0-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="565b0-128">Elija el recurso que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="565b0-128">Choose the resource that you want to refresh.</span></span>  <span data-ttu-id="565b0-129">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="565b0-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Elegir un recurso para actualizar" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="565b0-131">Elegir un recurso para actualizar</span><span class="sxs-lookup"><span data-stu-id="565b0-131">Choose a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="565b0-132">Elija **Actualizar** \( ![ Actualizar ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="565b0-132">Choose **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\).</span></span>  
    
## <a name="filter-resources"></a><span data-ttu-id="565b0-133">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="565b0-133">Filter resources</span></span>  

1.  <span data-ttu-id="565b0-134">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="565b0-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="565b0-135">Use el **cuadro de texto** Filtrar por ruta de acceso para filtrar los recursos que no coincidan con la ruta de acceso que proporcione.</span><span class="sxs-lookup"><span data-stu-id="565b0-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que no coinciden con la ruta de acceso especificada" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="565b0-137">Filtrar recursos que no coinciden con la ruta de acceso especificada</span><span class="sxs-lookup"><span data-stu-id="565b0-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <a name="delete-a-resource"></a><span data-ttu-id="565b0-138">Eliminar un recurso</span><span class="sxs-lookup"><span data-stu-id="565b0-138">Delete a resource</span></span>  

1.  <span data-ttu-id="565b0-139">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="565b0-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="565b0-140">Elija el recurso que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="565b0-140">Choose the resource that you want to delete.</span></span>  <span data-ttu-id="565b0-141">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="565b0-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Elegir un recurso para eliminar" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="565b0-143">Elegir un recurso para eliminar</span><span class="sxs-lookup"><span data-stu-id="565b0-143">Choose a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="565b0-144">Elija **Eliminar seleccionado** \( Eliminar seleccionado ![ ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="565b0-144">Choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-cache-data"></a><span data-ttu-id="565b0-145">Eliminar todos los datos de caché</span><span class="sxs-lookup"><span data-stu-id="565b0-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="565b0-146">Abra **Almacenamiento sin**formato de  >  **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="565b0-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="565b0-147">Asegúrese de que la casilla **Almacenamiento en caché** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="565b0-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="La casilla Almacenamiento en caché" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="565b0-149">La **casilla Almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="565b0-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="565b0-150">Elija **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="565b0-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="565b0-152">Botón **Borrar datos del** sitio</span><span class="sxs-lookup"><span data-stu-id="565b0-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="565b0-153">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="565b0-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Registrar actividad de red | Microsoft Docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="565b0-158">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="565b0-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="565b0-159">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cache) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="565b0-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="565b0-161">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="565b0-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
