---
description: Cómo ver los datos de la caché desde el panel de aplicaciones de Microsoft Edge DevTools.
title: Ver datos de la caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 770001beb9b7eebd4dae76355a1f3e41a8021ecb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230806"
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

# <span data-ttu-id="4f4e0-104">Ver datos de la caché con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4f4e0-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="4f4e0-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de [caché][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="4f4e0-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="4f4e0-106">Si intenta inspeccionar los datos de [caché http][MDNHTTPCaching] , esta no es la guía que desea.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="4f4e0-107">Busque la información en la columna **tamaño** del registro de **red**.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="4f4e0-108">Desplácese hasta [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="4f4e0-108">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="4f4e0-109">Ver datos de caché</span><span class="sxs-lookup"><span data-stu-id="4f4e0-109">View cache data</span></span>  

1.  <span data-ttu-id="4f4e0-110">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="4f4e0-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="4f4e0-111">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="4f4e0-113">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="4f4e0-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4e0-114">Expanda la sección **almacenamiento en caché** para ver las memorias caché disponibles.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Cachés disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="4f4e0-116">Cachés disponibles</span><span class="sxs-lookup"><span data-stu-id="4f4e0-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4e0-117">Seleccione una caché para ver el contenido.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-117">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Ver el contenido de una caché" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="4f4e0-119">Ver el contenido de una caché</span><span class="sxs-lookup"><span data-stu-id="4f4e0-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4e0-120">Seleccione un recurso para ver los encabezados HTTP en la sección debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-120">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Ver los encabezados HTTP de un recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="4f4e0-122">Ver los encabezados HTTP de un recurso</span><span class="sxs-lookup"><span data-stu-id="4f4e0-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4e0-123">Elija **vista previa** para ver el contenido de un recurso.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Ver el contenido de un recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="4f4e0-125">Ver el contenido de un recurso</span><span class="sxs-lookup"><span data-stu-id="4f4e0-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4f4e0-126">Actualizar un recurso</span><span class="sxs-lookup"><span data-stu-id="4f4e0-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="4f4e0-127">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="4f4e0-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="4f4e0-128">Seleccione el recurso que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-128">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="4f4e0-129">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Seleccionar un recurso para actualizarlo" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="4f4e0-131">Seleccionar un recurso para actualizarlo</span><span class="sxs-lookup"><span data-stu-id="4f4e0-131">Select a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4e0-132">Elija **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4f4e0-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="4f4e0-133">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="4f4e0-133">Filter resources</span></span>  

1.  <span data-ttu-id="4f4e0-134">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="4f4e0-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="4f4e0-135">Use el cuadro de texto **filtrar por ruta** para filtrar los recursos que no coincidan con la ruta de acceso que proporciona.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que no coincidan con la ruta de acceso especificada" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="4f4e0-137">Filtrar recursos que no coincidan con la ruta de acceso especificada</span><span class="sxs-lookup"><span data-stu-id="4f4e0-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4f4e0-138">Eliminar un recurso</span><span class="sxs-lookup"><span data-stu-id="4f4e0-138">Delete a resource</span></span>  

1.  <span data-ttu-id="4f4e0-139">[Ver los datos de una memoria caché](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="4f4e0-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="4f4e0-140">Seleccione el recurso que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-140">Select the resource that you want to delete.</span></span>  <span data-ttu-id="4f4e0-141">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Seleccionar un recurso para eliminarlo" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="4f4e0-143">Seleccionar un recurso para eliminarlo</span><span class="sxs-lookup"><span data-stu-id="4f4e0-143">Select a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4e0-144">Elija **eliminar seleccionado** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4f4e0-144">Choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="4f4e0-145">Eliminar todos los datos de caché</span><span class="sxs-lookup"><span data-stu-id="4f4e0-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="4f4e0-146">\*\*\*\*  >  **Almacenamiento borrado**de aplicaciones abiertas.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="4f4e0-147">Asegúrese de que la casilla **almacenamiento en caché** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Casilla de almacenamiento en caché" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="4f4e0-149">Casilla de **almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="4f4e0-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4e0-150">Elija **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="4f4e0-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="4f4e0-152">Botón **Borrar datos del sitio**</span><span class="sxs-lookup"><span data-stu-id="4f4e0-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4f4e0-153">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4f4e0-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Registrar actividad de red | Microsoft docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché de HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="4f4e0-158">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4f4e0-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4f4e0-159">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cache) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4f4e0-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4f4e0-161">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4f4e0-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
