---
title: Ver datos de la caché de aplicaciones con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fc1800fc54e5fb0d7998c62ce163ece7a461dd82
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931220"
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

# <span data-ttu-id="dc277-103">Ver datos de la caché de aplicaciones con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="dc277-103">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="dc277-104">La API de la caché de aplicaciones se está [quitando de la plataforma web][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="dc277-104">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="dc277-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los recursos de caché de la [aplicación][MDNWebAPIsWindowApplicationCache] .</span><span class="sxs-lookup"><span data-stu-id="dc277-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="dc277-106">Ver datos de la caché de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="dc277-106">View Application Cache data</span></span>  

1.  <span data-ttu-id="dc277-107">Seleccione la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="dc277-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="dc277-108">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dc277-108">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="dc277-110">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="dc277-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="dc277-111">Expanda la sección caché de la **aplicación** y elija una caché para ver los recursos.</span><span class="sxs-lookup"><span data-stu-id="dc277-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Panel de caché de aplicaciones" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="dc277-113">Panel de **caché de aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="dc277-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="dc277-114">Cada fila de la tabla representa un recurso almacenado en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="dc277-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="dc277-115">La columna **tipo** representa la [categoría del recurso][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="dc277-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="dc277-116">Categoría</span><span class="sxs-lookup"><span data-stu-id="dc277-116">Category</span></span> | <span data-ttu-id="dc277-117">Detalles</span><span class="sxs-lookup"><span data-stu-id="dc277-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="dc277-118">Este recurso se mostraba explícitamente en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="dc277-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="dc277-119">La dirección URL es una reserva de otro recurso.</span><span class="sxs-lookup"><span data-stu-id="dc277-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="dc277-120">La dirección URL del otro recurso no se enumera en DevTools.</span><span class="sxs-lookup"><span data-stu-id="dc277-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="dc277-121">El `manifest` atributo en el recurso indica que la memoria caché es el elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="dc277-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="dc277-122">El manifiesto especificó que el recurso debe proceder de la red.</span><span class="sxs-lookup"><span data-stu-id="dc277-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="dc277-123">En la parte inferior de la tabla hay iconos de estado que indican su conexión de red y el estado de la **memoria caché**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc277-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="dc277-124">La **caché** de la aplicación puede tener los siguientes Estados.</span><span class="sxs-lookup"><span data-stu-id="dc277-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="dc277-125">Estado</span><span class="sxs-lookup"><span data-stu-id="dc277-125">State</span></span> | <span data-ttu-id="dc277-126">Detalles</span><span class="sxs-lookup"><span data-stu-id="dc277-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="dc277-127">El manifiesto se está buscando y comprobando para obtener actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="dc277-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="dc277-128">Los recursos se están agregando a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="dc277-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="dc277-129">La caché no tiene cambios nuevos.</span><span class="sxs-lookup"><span data-stu-id="dc277-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="dc277-130">Se está eliminando la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="dc277-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="dc277-131">Hay una nueva versión de la caché disponible.</span><span class="sxs-lookup"><span data-stu-id="dc277-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicaciones web sin conexión: estándar HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos en una caché de aplicaciones | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-API Web | MDN"  

> [!NOTE]
> <span data-ttu-id="dc277-136">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dc277-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dc277-137">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="dc277-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dc277-139">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dc277-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
