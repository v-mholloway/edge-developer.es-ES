---
description: Cómo ver los datos de caché de aplicaciones desde el panel Aplicación de Microsoft Edge DevTools.
title: Ver datos de caché de aplicaciones Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 71e71555940d74f2071178be2e6daf0ec2f49dfd
ms.sourcegitcommit: d0a6959c5338cf1927093b4a9ed29a0bc0390b43
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "11615424"
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
# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="59a93-104">Ver datos de caché de aplicaciones con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="59a93-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="59a93-105">La caché de aplicaciones está en desuso y debe evitar usarlo.</span><span class="sxs-lookup"><span data-stu-id="59a93-105">The Application Cache is deprecated, and you should avoid using it.</span></span>  <span data-ttu-id="59a93-106">La API de caché de aplicaciones se está quitando de la plataforma web.</span><span class="sxs-lookup"><span data-stu-id="59a93-106">The Application Cache API is being removed from the web platform.</span></span>  <span data-ttu-id="59a93-107">Para obtener más información, vaya [a Preparar la eliminación de AppCache][WebDevAppcacheRemoval].</span><span class="sxs-lookup"><span data-stu-id="59a93-107">For more information, navigate to [Preparing for AppCache removal][WebDevAppcacheRemoval].</span></span>

<span data-ttu-id="59a93-108">En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] inspeccionar los [recursos de caché de][MDNWebAPIsWindowApplicationCache] aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="59a93-108">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <a name="view-application-cache-data"></a><span data-ttu-id="59a93-109">Ver datos de caché de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="59a93-109">View Application Cache data</span></span>  

1.  <span data-ttu-id="59a93-110">En la parte superior de DevTools, elija la **herramienta** Aplicación.</span><span class="sxs-lookup"><span data-stu-id="59a93-110">At the top of DevTools, choose the **Application** tool.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="59a93-112">Panel **Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="59a93-112">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="59a93-113">Expanda la **sección Caché de** aplicaciones y elija una caché para ver los recursos.</span><span class="sxs-lookup"><span data-stu-id="59a93-113">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Panel Caché de aplicaciones" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="59a93-115">Panel **Caché de** aplicaciones</span><span class="sxs-lookup"><span data-stu-id="59a93-115">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="59a93-116">Cada fila de la tabla representa un recurso almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="59a93-116">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="59a93-117">La **columna** Tipo representa la [categoría del recurso][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="59a93-117">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="59a93-118">Categoría</span><span class="sxs-lookup"><span data-stu-id="59a93-118">Category</span></span> | <span data-ttu-id="59a93-119">Detalles</span><span class="sxs-lookup"><span data-stu-id="59a93-119">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="59a93-120">Este recurso se enumeró explícitamente en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="59a93-120">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="59a93-121">La dirección URL es una reserva para otro recurso.</span><span class="sxs-lookup"><span data-stu-id="59a93-121">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="59a93-122">La dirección URL del otro recurso no se muestra en DevTools.</span><span class="sxs-lookup"><span data-stu-id="59a93-122">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="59a93-123">El `manifest` atributo del recurso indica que la memoria caché es el elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="59a93-123">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="59a93-124">El manifiesto especifica que el recurso debe venir de la red.</span><span class="sxs-lookup"><span data-stu-id="59a93-124">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="59a93-125">En la parte inferior de la tabla hay iconos de estado que indican la conexión de red y el estado de la caché **de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="59a93-125">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="59a93-126">La **caché de aplicaciones** puede tener los siguientes estados.</span><span class="sxs-lookup"><span data-stu-id="59a93-126">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="59a93-127">Estado</span><span class="sxs-lookup"><span data-stu-id="59a93-127">State</span></span> | <span data-ttu-id="59a93-128">Detalles</span><span class="sxs-lookup"><span data-stu-id="59a93-128">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="59a93-129">El manifiesto se está recuperando y buscando actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="59a93-129">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="59a93-130">Los recursos se agregan a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="59a93-130">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="59a93-131">La memoria caché no tiene nuevos cambios.</span><span class="sxs-lookup"><span data-stu-id="59a93-131">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="59a93-132">Se está eliminando la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="59a93-132">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="59a93-133">Hay disponible una nueva versión de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="59a93-133">A new version of the cache is available.</span></span> |  

<!-- links -->  
[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
<!-- external links: -->
[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos en una memoria caché de aplicaciones | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache: API web | MDN"  

[WebDevAppcacheRemoval]: https://web.dev/appcache-removal "Preparación para la eliminación de AppCache | web.dev"  

> [!NOTE]
> <span data-ttu-id="59a93-138">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="59a93-138">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="59a93-139">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="59a93-139">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="59a93-141">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="59a93-141">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
