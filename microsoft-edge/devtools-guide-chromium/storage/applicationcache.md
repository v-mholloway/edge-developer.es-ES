---
description: Cómo ver los datos de caché de aplicaciones desde el panel Aplicación de Microsoft Edge DevTools.
title: Ver datos de caché de aplicaciones con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: cbe6623aa3132db4d01cd6b440702eb157525eed
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519145"
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

# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="89ae5-104">Ver datos de caché de aplicaciones con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="89ae5-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="89ae5-105">La API de caché de [aplicaciones se está quitando de la plataforma web][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="89ae5-105">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="89ae5-106">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los [recursos de caché de][MDNWebAPIsWindowApplicationCache] aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="89ae5-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <a name="view-application-cache-data"></a><span data-ttu-id="89ae5-107">Ver datos de caché de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="89ae5-107">View Application Cache data</span></span>  

1.  <span data-ttu-id="89ae5-108">En la parte superior de DevTools, elija la **herramienta** Aplicación.</span><span class="sxs-lookup"><span data-stu-id="89ae5-108">At the top of DevTools, choose the **Application** tool.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="89ae5-110">Panel **Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="89ae5-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="89ae5-111">Expanda la **sección Caché de** aplicaciones y elija una caché para ver los recursos.</span><span class="sxs-lookup"><span data-stu-id="89ae5-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Panel Caché de aplicaciones" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="89ae5-113">Panel **Caché de** aplicaciones</span><span class="sxs-lookup"><span data-stu-id="89ae5-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="89ae5-114">Cada fila de la tabla representa un recurso almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="89ae5-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="89ae5-115">La **columna** Tipo representa la [categoría del recurso][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="89ae5-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="89ae5-116">Categoría</span><span class="sxs-lookup"><span data-stu-id="89ae5-116">Category</span></span> | <span data-ttu-id="89ae5-117">Detalles</span><span class="sxs-lookup"><span data-stu-id="89ae5-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="89ae5-118">Este recurso se enumeró explícitamente en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="89ae5-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="89ae5-119">La dirección URL es una reserva para otro recurso.</span><span class="sxs-lookup"><span data-stu-id="89ae5-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="89ae5-120">La dirección URL del otro recurso no se muestra en DevTools.</span><span class="sxs-lookup"><span data-stu-id="89ae5-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="89ae5-121">El `manifest` atributo del recurso indica que la memoria caché es el elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="89ae5-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="89ae5-122">El manifiesto especifica que el recurso debe venir de la red.</span><span class="sxs-lookup"><span data-stu-id="89ae5-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="89ae5-123">En la parte inferior de la tabla hay iconos de estado que indican la conexión de red y el estado de la caché **de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="89ae5-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="89ae5-124">La **caché de aplicaciones** puede tener los siguientes estados.</span><span class="sxs-lookup"><span data-stu-id="89ae5-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="89ae5-125">Estado</span><span class="sxs-lookup"><span data-stu-id="89ae5-125">State</span></span> | <span data-ttu-id="89ae5-126">Detalles</span><span class="sxs-lookup"><span data-stu-id="89ae5-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="89ae5-127">El manifiesto se está recuperando y buscando actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="89ae5-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="89ae5-128">Los recursos se agregan a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="89ae5-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="89ae5-129">La memoria caché no tiene nuevos cambios.</span><span class="sxs-lookup"><span data-stu-id="89ae5-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="89ae5-130">Se está eliminando la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="89ae5-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="89ae5-131">Hay disponible una nueva versión de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="89ae5-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicaciones web sin conexión: estándar HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos en una memoria caché de aplicaciones | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache: API web | MDN"  

> [!NOTE]
> <span data-ttu-id="89ae5-136">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="89ae5-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="89ae5-137">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="89ae5-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="89ae5-139">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="89ae5-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
