---
title: Ver datos de la caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7e7b4326204ce10732972c89b70c966e4bb665fb
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983880"
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





# <span data-ttu-id="0b532-103">Ver datos de la caché con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0b532-103">View cache data with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="0b532-104">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de [caché][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="0b532-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="0b532-105">Si intenta inspeccionar los datos de [caché http][MDNHTTPCaching] , esta no es la guía que desea.</span><span class="sxs-lookup"><span data-stu-id="0b532-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="0b532-106">Busque la información en la columna **tamaño** del registro de **red**.</span><span class="sxs-lookup"><span data-stu-id="0b532-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="0b532-107">Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="0b532-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="0b532-108">Ver datos de caché</span><span class="sxs-lookup"><span data-stu-id="0b532-108">View cache data</span></span>   

1.  <span data-ttu-id="0b532-109">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="0b532-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="0b532-110">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0b532-110">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="0b532-112">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="0b532-112">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0b532-113">Expanda la sección **almacenamiento en caché** para ver las memorias caché disponibles.</span><span class="sxs-lookup"><span data-stu-id="0b532-113">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Cachés disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="0b532-115">Cachés disponibles</span><span class="sxs-lookup"><span data-stu-id="0b532-115">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0b532-116">Seleccione una caché para ver el contenido.</span><span class="sxs-lookup"><span data-stu-id="0b532-116">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Ver el contenido de una caché" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="0b532-118">Ver el contenido de una caché</span><span class="sxs-lookup"><span data-stu-id="0b532-118">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0b532-119">Seleccione un recurso para ver los encabezados HTTP en la sección debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0b532-119">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Ver los encabezados HTTP de un recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="0b532-121">Ver los encabezados HTTP de un recurso</span><span class="sxs-lookup"><span data-stu-id="0b532-121">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0b532-122">Seleccione **vista previa** para ver el contenido de un recurso.</span><span class="sxs-lookup"><span data-stu-id="0b532-122">Select **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Ver el contenido de un recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="0b532-124">Ver el contenido de un recurso</span><span class="sxs-lookup"><span data-stu-id="0b532-124">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="0b532-125">Actualizar un recurso</span><span class="sxs-lookup"><span data-stu-id="0b532-125">Refresh a resource</span></span>   

1.  <span data-ttu-id="0b532-126">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="0b532-126">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="0b532-127">Seleccione el recurso que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="0b532-127">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="0b532-128">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="0b532-128">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Seleccionar un recurso" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="0b532-130">Seleccionar un recurso</span><span class="sxs-lookup"><span data-stu-id="0b532-130">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0b532-131">Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0b532-131">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="0b532-132">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="0b532-132">Filter resources</span></span>   

1.  <span data-ttu-id="0b532-133">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="0b532-133">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="0b532-134">Use el cuadro de texto **filtrar por ruta** para filtrar los recursos que no coincidan con la ruta de acceso que proporciona.</span><span class="sxs-lookup"><span data-stu-id="0b532-134">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que no coincidan con la ruta de acceso especificada" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="0b532-136">Filtrar recursos que no coincidan con la ruta de acceso especificada</span><span class="sxs-lookup"><span data-stu-id="0b532-136">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="0b532-137">Eliminar un recurso</span><span class="sxs-lookup"><span data-stu-id="0b532-137">Delete a resource</span></span>   

1.  <span data-ttu-id="0b532-138">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="0b532-138">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="0b532-139">Seleccione el recurso que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="0b532-139">Select the resource that you want to delete.</span></span>  <span data-ttu-id="0b532-140">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="0b532-140">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Seleccionar un recurso" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="0b532-142">Seleccionar un recurso</span><span class="sxs-lookup"><span data-stu-id="0b532-142">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0b532-143">Seleccione **eliminar seleccionado** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0b532-143">Select **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="0b532-144">Eliminar todos los datos de caché</span><span class="sxs-lookup"><span data-stu-id="0b532-144">Delete all cache data</span></span>   

1.  <span data-ttu-id="0b532-145">**Application**  >  **Almacenamiento borrado**de aplicaciones abiertas.</span><span class="sxs-lookup"><span data-stu-id="0b532-145">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="0b532-146">Asegúrese de que la casilla **almacenamiento en caché** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0b532-146">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Casilla de almacenamiento en caché" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="0b532-148">Casilla de **almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="0b532-148">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0b532-149">Seleccione **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="0b532-149">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="0b532-151">Botón **Borrar datos del sitio**</span><span class="sxs-lookup"><span data-stu-id="0b532-151">The **Clear Site Data** button</span></span>  
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
> <span data-ttu-id="0b532-156">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0b532-156">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0b532-157">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cache) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="0b532-157">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0b532-159">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0b532-159">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
