---
description: Use el Panel de seguridad para asegurarse de que una página está totalmente protegida por HTTPS.
title: Comprender los problemas de seguridad con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397779"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a><span data-ttu-id="67ec3-104">Comprender los problemas de seguridad con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="67ec3-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a><span data-ttu-id="67ec3-105">Abrir el panel Seguridad</span><span class="sxs-lookup"><span data-stu-id="67ec3-105">Open the Security panel</span></span>  

<span data-ttu-id="67ec3-106">El \*\*\*\* panel Seguridad es el lugar principal de DevTools para inspeccionar la seguridad de una página.</span><span class="sxs-lookup"><span data-stu-id="67ec3-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="67ec3-107">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="67ec3-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="67ec3-108">Elija la **pestaña** Seguridad para abrir la **herramienta** Seguridad.</span><span class="sxs-lookup"><span data-stu-id="67ec3-108">Choose the **Security** tab to open the **Security** tool.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="El panel Seguridad" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="67ec3-110">El panel **Seguridad**</span><span class="sxs-lookup"><span data-stu-id="67ec3-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <a name="common-problems"></a><span data-ttu-id="67ec3-111">Problemas comunes</span><span class="sxs-lookup"><span data-stu-id="67ec3-111">Common problems</span></span>  

### <a name="non-secure-main-origins"></a><span data-ttu-id="67ec3-112">Orígenes principales no seguros</span><span class="sxs-lookup"><span data-stu-id="67ec3-112">Non-secure main origins</span></span>  

<span data-ttu-id="67ec3-113">Cuando el origen principal de una página no es seguro, la **información** general sobre seguridad indica **que esta página no es segura.**</span><span class="sxs-lookup"><span data-stu-id="67ec3-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Una página no segura" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="67ec3-115">Una página no segura</span><span class="sxs-lookup"><span data-stu-id="67ec3-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="67ec3-116">Este problema se produce cuando la dirección URL que visitó se solicitó a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="67ec3-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="67ec3-117">Para que sea seguro, debe solicitarlo a través de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="67ec3-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="67ec3-118">Por ejemplo, si observa la dirección URL de la barra de direcciones, probablemente tenga un aspecto similar a `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="67ec3-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="67ec3-119">Para que sea segura, la dirección URL debe ser `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="67ec3-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="67ec3-120">Si ya ha configurado HTTPS en el servidor, lo único que debe hacer para solucionar este problema es configurar el servidor para redirigir todas las solicitudes HTTP a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="67ec3-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="67ec3-121">Si no ha configurado HTTPS en el servidor, [Let's Encrypt][LetsEncrypt] proporciona una forma gratuita y relativamente fácil de iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="67ec3-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="67ec3-122">O bien, puede considerar hospedar su sitio en una red CDN.</span><span class="sxs-lookup"><span data-stu-id="67ec3-122">Or, you may consider hosting your site on a CDN.</span></span>  <span data-ttu-id="67ec3-123">La mayoría de los principales sitios de host de CDN en HTTPS ahora son de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="67ec3-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="67ec3-124">La [sugerencia Usar HTTPS][WebhintUseHttps] en [webhint][Webhint] puede ayudar a automatizar el proceso de asegurarse de que todas las solicitudes HTTP se dirigen a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="67ec3-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <a name="mixed-content"></a><span data-ttu-id="67ec3-125">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="67ec3-125">Mixed content</span></span>  

<span data-ttu-id="67ec3-126">**El contenido mixto** significa que el origen principal de una página es seguro, pero la página solicitó recursos de orígenes no seguros.</span><span class="sxs-lookup"><span data-stu-id="67ec3-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="67ec3-127">Las páginas de contenido mixto solo están parcialmente protegidas porque el contenido HTTP es accesible para los sniffers y vulnerable a los ataques de man-in-the-middle.</span><span class="sxs-lookup"><span data-stu-id="67ec3-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Contenido mixto" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="67ec3-129">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="67ec3-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="67ec3-130">En la figura anterior, elija Ver **1** \*\*\*\* solicitud en el panel Red para abrir la herramienta Red y aplicar el filtro para que el registro de red solo muestre `mixed-content:displayed` recursos no seguros. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="67ec3-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** tool and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Recursos mixtos en el registro de red" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="67ec3-132">Recursos mixtos en el **registro de red**</span><span class="sxs-lookup"><span data-stu-id="67ec3-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <a name="view-details"></a><span data-ttu-id="67ec3-133">Ver detalles</span><span class="sxs-lookup"><span data-stu-id="67ec3-133">View details</span></span>  

### <a name="view-main-origin-certificate"></a><span data-ttu-id="67ec3-134">Ver certificado de origen principal</span><span class="sxs-lookup"><span data-stu-id="67ec3-134">View main origin certificate</span></span>  

<span data-ttu-id="67ec3-135">En Información **general sobre seguridad,** elija **Ver certificado** para inspeccionar rápidamente el certificado para el origen principal.</span><span class="sxs-lookup"><span data-stu-id="67ec3-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Un certificado de origen principal" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="67ec3-137">Un certificado de origen principal</span><span class="sxs-lookup"><span data-stu-id="67ec3-137">A main origin certificate</span></span>  
:::image-end:::  

### <a name="view-origin-details"></a><span data-ttu-id="67ec3-138">Ver detalles de origen</span><span class="sxs-lookup"><span data-stu-id="67ec3-138">View origin details</span></span>  

<span data-ttu-id="67ec3-139">Elija una de las entradas de la navegación a la izquierda para ver los detalles del origen.</span><span class="sxs-lookup"><span data-stu-id="67ec3-139">Choose one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="67ec3-140">En la página de detalles puede ver la información de conexión y certificado.</span><span class="sxs-lookup"><span data-stu-id="67ec3-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="67ec3-141">La información de transparencia de certificados también se muestra cuando está disponible.</span><span class="sxs-lookup"><span data-stu-id="67ec3-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Detalles del origen principal" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="67ec3-143">Detalles del origen principal</span><span class="sxs-lookup"><span data-stu-id="67ec3-143">Main origin details</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="67ec3-144">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="67ec3-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevToolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[LetsEncrypt]: https://letsencrypt.org "Vamos a cifrar: certificados SSL/TLS gratuitos"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar https | documentación de webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="67ec3-150">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="67ec3-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="67ec3-151">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/security/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="67ec3-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="67ec3-153">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="67ec3-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
