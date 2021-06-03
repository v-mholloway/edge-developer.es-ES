---
description: Hospedar y publicar extensiones en la empresa para Microsoft Edge (Chromium).
title: Publicar y actualizar extensiones en el Microsoft Edge complementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 2249462b0a2dac86efa4b775171e2a3229a34431
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461223"
---
# <a name="publish-and-update-extensions-in-the-microsoft-edge-add-ons-store"></a><span data-ttu-id="d404b-104">Publicar y actualizar extensiones en el Microsoft Edge complementos</span><span class="sxs-lookup"><span data-stu-id="d404b-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="d404b-105">La mayoría de las extensiones se publican en [el Microsoft Edge complementos][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] para proteger a los usuarios de extensiones malintencionadas.</span><span class="sxs-lookup"><span data-stu-id="d404b-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <a name="publish-options-for-extensions"></a><span data-ttu-id="d404b-106">Opciones de publicación para extensiones</span><span class="sxs-lookup"><span data-stu-id="d404b-106">Publish options for extensions</span></span>  

<span data-ttu-id="d404b-107">Todas las extensiones se distribuyen a los usuarios como un archivo especial \( `.zip` \) con un `.crx` sufijo.</span><span class="sxs-lookup"><span data-stu-id="d404b-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="d404b-108">Las extensiones publicadas en el Microsoft Edge complementos se cargan como `.zip` archivos.</span><span class="sxs-lookup"><span data-stu-id="d404b-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="d404b-109">El proceso de publicación convierte automáticamente el `.zip` archivo en un `.crx` archivo.</span><span class="sxs-lookup"><span data-stu-id="d404b-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="d404b-110">Los dos escenarios siguientes no requieren que publiques la extensión en el Microsoft Edge complementos.</span><span class="sxs-lookup"><span data-stu-id="d404b-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="d404b-111">Extensiones distribuidas mediante Enterprise directiva.</span><span class="sxs-lookup"><span data-stu-id="d404b-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="d404b-112">Usar directorios de extensión desempaquetar en un equipo local Microsoft Edge está en modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="d404b-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <a name="updates-to-extensions"></a><span data-ttu-id="d404b-113">Actualizaciones de extensiones</span><span class="sxs-lookup"><span data-stu-id="d404b-113">Updates to extensions</span></span>

<span data-ttu-id="d404b-114">El Microsoft Edge busca automáticamente nuevas versiones de extensiones instaladas.</span><span class="sxs-lookup"><span data-stu-id="d404b-114">The Microsoft Edge browser automatically checks for new versions of installed Extensions.</span></span> <span data-ttu-id="d404b-115">Las actualizaciones se instalan sin intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="d404b-115">Updates are installed without user intervention.</span></span>  


<!-- image links -->

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensiones: Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> <span data-ttu-id="d404b-117">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d404b-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d404b-118">La página original se encuentra [aquí.](https://developer.chrome.com/extensions/hosting)</span><span class="sxs-lookup"><span data-stu-id="d404b-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d404b-120">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d404b-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
