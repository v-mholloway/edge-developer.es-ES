---
title: Ver datos de la caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612077"
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





# <span data-ttu-id="a983a-103">Ver datos de la caché con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a983a-103">View Cache Data With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="a983a-104">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de [caché][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="a983a-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="a983a-105">Si intenta inspeccionar los datos de [caché http][MDNHTTPCaching] , esta no es la guía que desea.</span><span class="sxs-lookup"><span data-stu-id="a983a-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  
<span data-ttu-id="a983a-106">Busque la información en la columna **tamaño** del registro de **red**.</span><span class="sxs-lookup"><span data-stu-id="a983a-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="a983a-107">Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="a983a-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="a983a-108">Ver datos de caché</span><span class="sxs-lookup"><span data-stu-id="a983a-108">View cache data</span></span>   

1.  <span data-ttu-id="a983a-109">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="a983a-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="a983a-110">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a983a-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="a983a-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="a983a-111">Figure 1</span></span>  
    > <span data-ttu-id="a983a-112">El panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="a983a-112">The Manifest pane</span></span>  
    > ![El panel manifiesto][ImageManifestPane]  

1.  <span data-ttu-id="a983a-114">Expanda la sección **almacenamiento en caché** para ver las memorias caché disponibles.</span><span class="sxs-lookup"><span data-stu-id="a983a-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    > ##### <span data-ttu-id="a983a-115">Figura 2</span><span class="sxs-lookup"><span data-stu-id="a983a-115">Figure 2</span></span>  
    > <span data-ttu-id="a983a-116">Cachés disponibles</span><span class="sxs-lookup"><span data-stu-id="a983a-116">Available caches</span></span>  
    > ![Cachés disponibles][ImageCache]  

1.  <span data-ttu-id="a983a-118">Seleccione una caché para ver el contenido.</span><span class="sxs-lookup"><span data-stu-id="a983a-118">Select a cache to view the contents.</span></span>  
    
    > ##### <span data-ttu-id="a983a-119">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="a983a-119">Figure 3</span></span>  
    > <span data-ttu-id="a983a-120">Ver el contenido de una caché</span><span class="sxs-lookup"><span data-stu-id="a983a-120">Viewing the contents of a cache</span></span>  
    > ![Ver el contenido de una caché][ImageCacheView]  

1.  <span data-ttu-id="a983a-122">Seleccione un recurso para ver los encabezados HTTP en la sección debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a983a-122">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    > ##### <span data-ttu-id="a983a-123">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="a983a-123">Figure 4</span></span>  
    > <span data-ttu-id="a983a-124">Visualización de los encabezados HTTP de un recurso</span><span class="sxs-lookup"><span data-stu-id="a983a-124">Viewing the HTTP headers of a resource</span></span>  
    > ![Visualización de los encabezados HTTP de un recurso][ImageViewCacheResource]  

1.  <span data-ttu-id="a983a-126">Seleccione **vista previa** para ver el contenido de un recurso.</span><span class="sxs-lookup"><span data-stu-id="a983a-126">Select **Preview** to view the content of a resource.</span></span>  
    
    > ##### <span data-ttu-id="a983a-127">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="a983a-127">Figure 5</span></span>  
    > <span data-ttu-id="a983a-128">Ver el contenido de un recurso</span><span class="sxs-lookup"><span data-stu-id="a983a-128">Viewing the content of a resource</span></span>  
    > ![Ver el contenido de un recurso][ImageCacheContent]  

## <span data-ttu-id="a983a-130">Actualizar un recurso</span><span class="sxs-lookup"><span data-stu-id="a983a-130">Refresh a resource</span></span>   

1.  <span data-ttu-id="a983a-131">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="a983a-131">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="a983a-132">Seleccione el recurso que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="a983a-132">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="a983a-133">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a983a-133">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="a983a-134">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="a983a-134">Figure 6</span></span>  
    > <span data-ttu-id="a983a-135">Selección de un recurso</span><span class="sxs-lookup"><span data-stu-id="a983a-135">Selecting a resource</span></span>  
    > ![Selección de un recurso][ImageCacheSelected]  

1.  <span data-ttu-id="a983a-137">Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="a983a-137">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="a983a-138">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="a983a-138">Filter resources</span></span>   

1.  <span data-ttu-id="a983a-139">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="a983a-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="a983a-140">Use el cuadro de texto **filtrar por ruta** para filtrar los recursos que no coincidan con la ruta de acceso que proporciona.</span><span class="sxs-lookup"><span data-stu-id="a983a-140">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    > ##### <span data-ttu-id="a983a-141">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="a983a-141">Figure 7</span></span>  
    > <span data-ttu-id="a983a-142">Filtrar recursos que no coincidan con la ruta especificada</span><span class="sxs-lookup"><span data-stu-id="a983a-142">Filtering out resources that do not match the specified path</span></span>  
    > ![Filtrar recursos que no coincidan con la ruta especificada][ImageCacheFilter]  

## <span data-ttu-id="a983a-144">Eliminar un recurso</span><span class="sxs-lookup"><span data-stu-id="a983a-144">Delete a resource</span></span>   

1.  <span data-ttu-id="a983a-145">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="a983a-145">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="a983a-146">Seleccione el recurso que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="a983a-146">Select the resource that you want to delete.</span></span>  <span data-ttu-id="a983a-147">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a983a-147">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="a983a-148">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="a983a-148">Figure 8</span></span>  
    > <span data-ttu-id="a983a-149">Selección de un recurso</span><span class="sxs-lookup"><span data-stu-id="a983a-149">Selecting a resource</span></span>  
    > ![Selección de un recurso][ImageCacheSelected2]  

1.  <span data-ttu-id="a983a-151">Seleccione **eliminar** selección ![ eliminar seleccionados ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="a983a-151">Select **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="a983a-152">Eliminar todos los datos de caché</span><span class="sxs-lookup"><span data-stu-id="a983a-152">Delete all cache data</span></span>   

1.  <span data-ttu-id="a983a-153">**Application**  >  **Almacenamiento borrado**de aplicaciones abiertas.</span><span class="sxs-lookup"><span data-stu-id="a983a-153">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="a983a-154">Asegúrese de que la casilla **almacenamiento en caché** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a983a-154">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="a983a-155">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="a983a-155">Figure 9</span></span>  
    > <span data-ttu-id="a983a-156">Casilla de **almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="a983a-156">The **Cache Storage** checkbox</span></span>  
    > ![Casilla de almacenamiento en caché][ImageCacheCheckbox]  

1.  <span data-ttu-id="a983a-158">Seleccione **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="a983a-158">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="a983a-159">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="a983a-159">Figure 10</span></span>  
    > <span data-ttu-id="a983a-160">Botón **Borrar datos del sitio**</span><span class="sxs-lookup"><span data-stu-id="a983a-160">The **Clear Site Data** button</span></span>  
    > ![Botón Borrar datos del sitio][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Ilustración 1: el panel manifiesto"  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Ilustración 2: memorias caché disponibles"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Ilustración 3: visualización del contenido de una caché"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Ilustración 4: visualización de los encabezados HTTP de un recurso"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Ilustración 5: visualización del contenido de un recurso"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Ilustración 6: selección de un recurso"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Ilustración 7: filtrar recursos que no coinciden con la ruta de acceso especificada"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Ilustración 8: selección de un recurso"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Ilustración 9: la casilla de almacenamiento en caché"  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Ilustración 10: botón Borrar datos del sitio"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Registrar actividad de la red"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché de HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="a983a-176">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a983a-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a983a-177">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cache) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a983a-177">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a983a-179">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a983a-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
