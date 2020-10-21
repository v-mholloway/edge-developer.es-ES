---
description: Use el panel seguridad para asegurarse de que una página está totalmente protegida por HTTPS.
title: Comprender los problemas de seguridad con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 09f7e641ddd8da74c361980b9ce61b212a8477fe
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125387"
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

# <span data-ttu-id="42345-104">Comprender los problemas de seguridad con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="42345-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="42345-105">Abrir el panel seguridad</span><span class="sxs-lookup"><span data-stu-id="42345-105">Open the Security panel</span></span>  

<span data-ttu-id="42345-106">El panel **seguridad** es el lugar principal en DevTools para inspeccionar la seguridad de una página.</span><span class="sxs-lookup"><span data-stu-id="42345-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="42345-107">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="42345-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="42345-108">Seleccione la pestaña **seguridad** para abrir el panel **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="42345-108">Choose the **Security** tab to open the **Security** panel.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="42345-110">El panel **seguridad**</span><span class="sxs-lookup"><span data-stu-id="42345-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="42345-111">Problemas comunes</span><span class="sxs-lookup"><span data-stu-id="42345-111">Common problems</span></span>  

### <span data-ttu-id="42345-112">Orígenes principales no seguros</span><span class="sxs-lookup"><span data-stu-id="42345-112">Non-secure main origins</span></span>  

<span data-ttu-id="42345-113">Cuando el origen principal de una página no es seguro, la **información general de seguridad** indica que **esta página no es segura**.</span><span class="sxs-lookup"><span data-stu-id="42345-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="42345-115">Una página no segura</span><span class="sxs-lookup"><span data-stu-id="42345-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="42345-116">Este problema se produce cuando se solicitó la dirección URL que visitó a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="42345-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="42345-117">Para asegurarte de que es necesario solicitarlo a través de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="42345-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="42345-118">Por ejemplo, si miras la dirección URL en la barra de direcciones, probablemente tenga un aspecto parecido a `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="42345-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="42345-119">Para que sea segura, la dirección URL debe ser `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="42345-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="42345-120">Si ya ha configurado HTTPS en el servidor, todo lo que debe hacer para solucionar este problema es configurar su servidor para redirigir todas las solicitudes HTTP a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="42345-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="42345-121">Si no ha configurado HTTPS en el servidor, vamos a [cifrar][LetsEncrypt] proporciona una forma gratuita y relativamente fácil de iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="42345-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="42345-122">O bien, puede que considere hospedar su sitio en una red CDN.</span><span class="sxs-lookup"><span data-stu-id="42345-122">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="42345-123">La mayoría de los principales sitios CDN hospedan en HTTPS de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="42345-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="42345-124">La sugerencia [use HTTPS][WebhintUseHttps] en [webhint][Webhint] puede ayudar a automatizar el proceso de asegurarse de que todas las solicitudes HTTP se dirijan a https.</span><span class="sxs-lookup"><span data-stu-id="42345-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="42345-125">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="42345-125">Mixed content</span></span>  

<span data-ttu-id="42345-126">El **contenido mixto** significa que el origen principal de una página es seguro, pero la página solicitó recursos de orígenes no seguros.</span><span class="sxs-lookup"><span data-stu-id="42345-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="42345-127">Las páginas de contenido mixto solo están parcialmente protegidas porque el contenido HTTP es accesible para los rastreadores y es vulnerable a ataques de intermediario.</span><span class="sxs-lookup"><span data-stu-id="42345-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="42345-129">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="42345-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="42345-130">En la ilustración anterior, elija **Ver 1 solicitud en el panel red** para abrir el panel **red** y aplicar el `mixed-content:displayed` filtro para que el **registro de red** solo muestre recursos no seguros.</span><span class="sxs-lookup"><span data-stu-id="42345-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="El panel seguridad" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="42345-132">Recursos mixtos en el **registro de red**</span><span class="sxs-lookup"><span data-stu-id="42345-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <span data-ttu-id="42345-133">Ver detalles</span><span class="sxs-lookup"><span data-stu-id="42345-133">View details</span></span>  

### <span data-ttu-id="42345-134">Ver certificado de origen principal</span><span class="sxs-lookup"><span data-stu-id="42345-134">View main origin certificate</span></span>  

<span data-ttu-id="42345-135">En la **Descripción de seguridad**, elija **Ver certificado** para inspeccionar rápidamente el certificado para el origen principal.</span><span class="sxs-lookup"><span data-stu-id="42345-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="42345-137">Un certificado de origen principal</span><span class="sxs-lookup"><span data-stu-id="42345-137">A main origin certificate</span></span>  
:::image-end:::  

### <span data-ttu-id="42345-138">Ver detalles de origen</span><span class="sxs-lookup"><span data-stu-id="42345-138">View origin details</span></span>  

<span data-ttu-id="42345-139">Haga clic en una de las entradas en el barra de navegación de la izquierda para ver los detalles del origen.</span><span class="sxs-lookup"><span data-stu-id="42345-139">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="42345-140">En la página de detalles puede ver la información de la conexión y el certificado.</span><span class="sxs-lookup"><span data-stu-id="42345-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="42345-141">La información de transparencia del certificado también se muestra cuando está disponible.</span><span class="sxs-lookup"><span data-stu-id="42345-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="42345-143">Detalles de origen principal</span><span class="sxs-lookup"><span data-stu-id="42345-143">Main origin details</span></span>  
:::image-end:::  

## <span data-ttu-id="42345-144">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="42345-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  
[LetsEncrypt]: https://letsencrypt.org "Vamos a cifrar los certificados SSL/TLS sin cifrar"  

[Webhint]: https://webhint.io "sugerencia"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar HTTPS | documentación de webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="42345-150">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42345-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="42345-151">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/security/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="42345-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="42345-153">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42345-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
