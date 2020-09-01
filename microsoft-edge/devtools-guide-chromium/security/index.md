---
title: Comprender los problemas de seguridad con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 850dde157a673a84a3e603f22a5e54abd90bde5d
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984328"
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





# <span data-ttu-id="5fd82-103">Comprender los problemas de seguridad con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5fd82-103">Understand security issues with Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="5fd82-104">Abrir el panel seguridad</span><span class="sxs-lookup"><span data-stu-id="5fd82-104">Open the Security panel</span></span>   

<span data-ttu-id="5fd82-105">El panel **seguridad** es el lugar principal en DevTools para inspeccionar la seguridad de una página.</span><span class="sxs-lookup"><span data-stu-id="5fd82-105">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="5fd82-106">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="5fd82-106">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="5fd82-107">Haga clic en la pestaña **seguridad** para abrir el panel **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="5fd82-107">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="5fd82-109">El panel **seguridad**</span><span class="sxs-lookup"><span data-stu-id="5fd82-109">The **Security** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5fd82-110">Problemas comunes</span><span class="sxs-lookup"><span data-stu-id="5fd82-110">Common problems</span></span>   

### <span data-ttu-id="5fd82-111">Orígenes principales no seguros</span><span class="sxs-lookup"><span data-stu-id="5fd82-111">Non-secure main origins</span></span>   

<span data-ttu-id="5fd82-112">Cuando el origen principal de una página no es seguro, la **información general de seguridad** indica que **esta página no es segura**.</span><span class="sxs-lookup"><span data-stu-id="5fd82-112">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Una página no segura" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="5fd82-114">Una página no segura</span><span class="sxs-lookup"><span data-stu-id="5fd82-114">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="5fd82-115">Este problema se produce cuando se solicitó la dirección URL que visitó a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="5fd82-115">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="5fd82-116">Para asegurarte de que es necesario solicitarlo a través de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5fd82-116">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="5fd82-117">Por ejemplo, si miras la dirección URL en la barra de direcciones, probablemente tenga un aspecto parecido a `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="5fd82-117">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="5fd82-118">Para que sea segura, la dirección URL debe ser `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="5fd82-118">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="5fd82-119">Si ya ha configurado HTTPS en el servidor, todo lo que debe hacer para solucionar este problema es configurar su servidor para redirigir todas las solicitudes HTTP a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5fd82-119">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="5fd82-120">Si no ha configurado HTTPS en el servidor, vamos a [cifrar][LetsEncrypt] proporciona una forma gratuita y relativamente fácil de iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="5fd82-120">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="5fd82-121">O bien, puede que considere hospedar su sitio en una red CDN.</span><span class="sxs-lookup"><span data-stu-id="5fd82-121">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="5fd82-122">La mayoría de los principales sitios CDN hospedan en HTTPS de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5fd82-122">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="5fd82-123">La sugerencia [use HTTPS][WebhintUseHttps] en [webhint][Webhint] puede ayudar a automatizar el proceso de asegurarse de que todas las solicitudes HTTP se dirijan a https.</span><span class="sxs-lookup"><span data-stu-id="5fd82-123">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="5fd82-124">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="5fd82-124">Mixed content</span></span>   

<span data-ttu-id="5fd82-125">El **contenido mixto** significa que el origen principal de una página es seguro, pero la página solicitó recursos de orígenes no seguros.</span><span class="sxs-lookup"><span data-stu-id="5fd82-125">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="5fd82-126">Las páginas de contenido mixto solo están parcialmente protegidas porque el contenido HTTP es accesible para los rastreadores y es vulnerable a ataques de intermediario.</span><span class="sxs-lookup"><span data-stu-id="5fd82-126">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Contenido mixto" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="5fd82-128">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="5fd82-128">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="5fd82-129">En la ilustración anterior, haga clic en **Ver 1 solicitud en el panel de red** para abrir el panel **red** y aplicar el `mixed-content:displayed` filtro para que el **registro de red** solo muestre recursos no seguros.</span><span class="sxs-lookup"><span data-stu-id="5fd82-129">In the previous figure, click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Recursos mixtos en el registro de red" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="5fd82-131">Recursos mixtos en el **registro de red**</span><span class="sxs-lookup"><span data-stu-id="5fd82-131">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <span data-ttu-id="5fd82-132">Ver detalles</span><span class="sxs-lookup"><span data-stu-id="5fd82-132">View details</span></span>   

### <span data-ttu-id="5fd82-133">Ver certificado de origen principal</span><span class="sxs-lookup"><span data-stu-id="5fd82-133">View main origin certificate</span></span>   

<span data-ttu-id="5fd82-134">En la **Introducción**a la seguridad, haga clic en **Ver certificado** para inspeccionar rápidamente el certificado del origen principal.</span><span class="sxs-lookup"><span data-stu-id="5fd82-134">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Un certificado de origen principal" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="5fd82-136">Un certificado de origen principal</span><span class="sxs-lookup"><span data-stu-id="5fd82-136">A main origin certificate</span></span>  
:::image-end:::  

### <span data-ttu-id="5fd82-137">Ver detalles de origen</span><span class="sxs-lookup"><span data-stu-id="5fd82-137">View origin details</span></span>   

<span data-ttu-id="5fd82-138">Haga clic en una de las entradas en el barra de navegación de la izquierda para ver los detalles del origen.</span><span class="sxs-lookup"><span data-stu-id="5fd82-138">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="5fd82-139">En la página de detalles puede ver la información de la conexión y el certificado.</span><span class="sxs-lookup"><span data-stu-id="5fd82-139">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="5fd82-140">La información de transparencia del certificado también se muestra cuando está disponible.</span><span class="sxs-lookup"><span data-stu-id="5fd82-140">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Detalles de origen principal" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="5fd82-142">Detalles de origen principal</span><span class="sxs-lookup"><span data-stu-id="5fd82-142">Main origin details</span></span>  
:::image-end:::  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  


[LetsEncrypt]: https://letsencrypt.org "Vamos a cifrar los certificados SSL/TLS sin cifrar"  

[Webhint]: https://webhint.io "sugerencia"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar HTTPS | documentación de webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="5fd82-148">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5fd82-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5fd82-149">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/security/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5fd82-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5fd82-151">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5fd82-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
