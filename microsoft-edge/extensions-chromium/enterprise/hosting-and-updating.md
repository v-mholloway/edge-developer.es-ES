---
description: Extensions documentación de Enterprise para extensiones de Edge (cromo).
title: Alojamiento y actualización
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: eb1f9921d503d25557fc9efb1517537e7a90f4aa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573716"
---
# <span data-ttu-id="f8503-104">Hospedaje y actualización de tiendas web</span><span class="sxs-lookup"><span data-stu-id="f8503-104">Web Store Hosting and Updating</span></span>  

<span data-ttu-id="f8503-105">La mayoría de las extensiones se hospedan en el [Catálogo de complementos de Microsoft Edge Insider \ (Microsoft Edge Insider addons \)][MicrosoftStoreExtensions] para proteger mejor a los usuarios de las extensiones malintencionadas.</span><span class="sxs-lookup"><span data-stu-id="f8503-105">Most Extensions are hosted in the [Microsoft Edge Insider Addons catalog \(Microsoft Edge Insider Addons\)][MicrosoftStoreExtensions] to best protect users from malicious Extensions.</span></span>  

## <span data-ttu-id="f8503-106">Alojamiento</span><span class="sxs-lookup"><span data-stu-id="f8503-106">Hosting</span></span>  

<span data-ttu-id="f8503-107">Todas las extensiones se distribuyen a los usuarios como un archivo ZIP especial con un sufijo. CRX.</span><span class="sxs-lookup"><span data-stu-id="f8503-107">All Extensions are distributed to users as a special ZIP file with a .crx suffix.</span></span>  <span data-ttu-id="f8503-108">Las extensiones hospedadas en los complementos de Microsoft Edge se cargan como archivos. zip.</span><span class="sxs-lookup"><span data-stu-id="f8503-108">Extensions hosted in the Microsoft Edge Addons are uploaded as .zip files.</span></span> <span data-ttu-id="f8503-109">El proceso de publicación convierte automáticamente el archivo. zip en un archivo. CRX.</span><span class="sxs-lookup"><span data-stu-id="f8503-109">The publishing process automatically converts the .zip into a .crx file.</span></span>  

<span data-ttu-id="f8503-110">Hay dos excepciones a la regla de hospedaje de complementos de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="f8503-110">There are two exceptions to the Microsoft Edge Addons hosting rule:</span></span>  

1.  <span data-ttu-id="f8503-111">Extensiones que se distribuyen a través de la Directiva de empresa.</span><span class="sxs-lookup"><span data-stu-id="f8503-111">Extensions that are distributed through the Enterprise policy.</span></span>  
1.  <span data-ttu-id="f8503-112">Directorios de extensión sin empaquetar desde un equipo local mientras está en el modo de programador.</span><span class="sxs-lookup"><span data-stu-id="f8503-112">Unpacked Extension directories from a local machine while in developer mode.</span></span>  

## <span data-ttu-id="f8503-113">Actualizándose</span><span class="sxs-lookup"><span data-stu-id="f8503-113">Updating</span></span>  

<span data-ttu-id="f8503-114">El explorador de Microsoft Edge comprueba periódicamente si hay nuevas versiones de las extensiones instaladas y las actualizaciones sin la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="f8503-114">The Microsoft Edge browser periodically checks for new versions of installed Extensions and updates each without user intervention.</span></span>  

> [!NOTE]
> <span data-ttu-id="f8503-115">Se agregarán los pasos para actualizar una extensión en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f8503-115">Steps to update an Extension on Microsoft Edge Addons are planned be added.</span></span>  

<!-- image links -->

<!-- links -->  

[MicrosoftStoreExtensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensiones-complementos de Insider de Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="f8503-117">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8503-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f8503-118">La página original se encuentra [aquí](https://developer.chrome.com/extensions/hosting).</span><span class="sxs-lookup"><span data-stu-id="f8503-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f8503-120">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8503-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
