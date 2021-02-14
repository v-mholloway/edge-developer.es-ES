---
description: Hospedar y publicar extensiones en la empresa para Microsoft Edge (Chromium).
title: Publicar y actualizar extensiones en el almacén de complementos de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327690"
---
# <span data-ttu-id="65c69-104">Publicar y actualizar extensiones en el almacén de complementos de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="65c69-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="65c69-105">La mayoría de las extensiones se publican en el almacén de complementos de [Microsoft Edge][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] para proteger a los usuarios de extensiones malintencionadas.</span><span class="sxs-lookup"><span data-stu-id="65c69-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <span data-ttu-id="65c69-106">Opciones de publicación para extensiones</span><span class="sxs-lookup"><span data-stu-id="65c69-106">Publish options for extensions</span></span>  

<span data-ttu-id="65c69-107">Todas las extensiones se distribuyen a los usuarios como un archivo especial \( `.zip` \) con un `.crx` sufijo.</span><span class="sxs-lookup"><span data-stu-id="65c69-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="65c69-108">Las extensiones publicadas en el almacén de complementos de Microsoft Edge se cargan como `.zip` archivos.</span><span class="sxs-lookup"><span data-stu-id="65c69-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="65c69-109">El proceso de publicación convierte automáticamente el `.zip` archivo en un `.crx` archivo.</span><span class="sxs-lookup"><span data-stu-id="65c69-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="65c69-110">Los dos escenarios siguientes no requieren que publiques la extensión en el almacén de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="65c69-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="65c69-111">Extensiones distribuidas mediante la directiva enterprise.</span><span class="sxs-lookup"><span data-stu-id="65c69-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="65c69-112">Usar directorios de extensión desempaquetar en un equipo local cuando Microsoft Edge está en modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="65c69-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <span data-ttu-id="65c69-113">Actualizaciones de extensiones</span><span class="sxs-lookup"><span data-stu-id="65c69-113">Updates to extensions</span></span>

<span data-ttu-id="65c69-114">El explorador Microsoft Edge comprueba periódicamente si hay nuevas versiones de extensiones instaladas y actualiza cada una de ellas sin la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="65c69-114">The Microsoft Edge browser periodically checks for new versions of installed extensions and updates each without user intervention.</span></span>  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensiones: complementos de Microsoft Edge Insider | Microsoft"  

> [!NOTE]
> <span data-ttu-id="65c69-116">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="65c69-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="65c69-117">La página original se encuentra [aquí.](https://developer.chrome.com/extensions/hosting)</span><span class="sxs-lookup"><span data-stu-id="65c69-117">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="65c69-119">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="65c69-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
