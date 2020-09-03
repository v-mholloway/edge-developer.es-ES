---
description: Cómo ver los datos de la caché desde el panel de aplicaciones de Microsoft Edge DevTools.
title: Ver datos de la caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c920a171ec89925cc79ab741eed01e11d749bf1b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993299"
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





# <span data-ttu-id="e92df-104">Ver datos de la caché con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e92df-104">View cache data with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="e92df-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de [caché][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="e92df-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="e92df-106">Si intenta inspeccionar los datos de [caché http][MDNHTTPCaching] , esta no es la guía que desea.</span><span class="sxs-lookup"><span data-stu-id="e92df-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="e92df-107">Busque la información en la columna **tamaño** del registro de **red**.</span><span class="sxs-lookup"><span data-stu-id="e92df-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="e92df-108">Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="e92df-108">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="e92df-109">Ver datos de caché</span><span class="sxs-lookup"><span data-stu-id="e92df-109">View cache data</span></span>   

1.  <span data-ttu-id="e92df-110">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="e92df-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="e92df-111">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e92df-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="e92df-113">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="e92df-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e92df-114">Expanda la sección **almacenamiento en caché** para ver las memorias caché disponibles.</span><span class="sxs-lookup"><span data-stu-id="e92df-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Cachés disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="e92df-116">Cachés disponibles</span><span class="sxs-lookup"><span data-stu-id="e92df-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e92df-117">Seleccione una caché para ver el contenido.</span><span class="sxs-lookup"><span data-stu-id="e92df-117">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Ver el contenido de una caché" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="e92df-119">Ver el contenido de una caché</span><span class="sxs-lookup"><span data-stu-id="e92df-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e92df-120">Seleccione un recurso para ver los encabezados HTTP en la sección debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e92df-120">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Ver los encabezados HTTP de un recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="e92df-122">Ver los encabezados HTTP de un recurso</span><span class="sxs-lookup"><span data-stu-id="e92df-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e92df-123">Seleccione **vista previa** para ver el contenido de un recurso.</span><span class="sxs-lookup"><span data-stu-id="e92df-123">Select **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Ver el contenido de un recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="e92df-125">Ver el contenido de un recurso</span><span class="sxs-lookup"><span data-stu-id="e92df-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e92df-126">Actualizar un recurso</span><span class="sxs-lookup"><span data-stu-id="e92df-126">Refresh a resource</span></span>   

1.  <span data-ttu-id="e92df-127">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="e92df-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="e92df-128">Seleccione el recurso que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="e92df-128">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="e92df-129">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e92df-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Seleccionar un recurso" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="e92df-131">Seleccionar un recurso</span><span class="sxs-lookup"><span data-stu-id="e92df-131">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e92df-132">Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e92df-132">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="e92df-133">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="e92df-133">Filter resources</span></span>   

1.  <span data-ttu-id="e92df-134">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="e92df-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="e92df-135">Use el cuadro de texto **filtrar por ruta** para filtrar los recursos que no coincidan con la ruta de acceso que proporciona.</span><span class="sxs-lookup"><span data-stu-id="e92df-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que no coincidan con la ruta de acceso especificada" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="e92df-137">Filtrar recursos que no coincidan con la ruta de acceso especificada</span><span class="sxs-lookup"><span data-stu-id="e92df-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e92df-138">Eliminar un recurso</span><span class="sxs-lookup"><span data-stu-id="e92df-138">Delete a resource</span></span>   

1.  <span data-ttu-id="e92df-139">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="e92df-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="e92df-140">Seleccione el recurso que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="e92df-140">Select the resource that you want to delete.</span></span>  <span data-ttu-id="e92df-141">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e92df-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Seleccionar un recurso" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="e92df-143">Seleccionar un recurso</span><span class="sxs-lookup"><span data-stu-id="e92df-143">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e92df-144">Seleccione **eliminar seleccionado** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e92df-144">Select **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="e92df-145">Eliminar todos los datos de caché</span><span class="sxs-lookup"><span data-stu-id="e92df-145">Delete all cache data</span></span>   

1.  <span data-ttu-id="e92df-146">**Application**  >  **Almacenamiento borrado**de aplicaciones abiertas.</span><span class="sxs-lookup"><span data-stu-id="e92df-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="e92df-147">Asegúrese de que la casilla **almacenamiento en caché** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e92df-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Casilla de almacenamiento en caché" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="e92df-149">Casilla de **almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="e92df-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e92df-150">Seleccione **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="e92df-150">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="e92df-152">Botón **Borrar datos del sitio**</span><span class="sxs-lookup"><span data-stu-id="e92df-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
  


-->  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Registrar actividad de red | Microsoft docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché de HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="e92df-157">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e92df-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e92df-158">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cache) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e92df-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e92df-160">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e92df-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
