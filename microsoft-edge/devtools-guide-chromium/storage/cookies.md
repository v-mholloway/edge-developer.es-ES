---
description: Obtenga información sobre cómo ver, editar y eliminar las cookies HTTP de una página mediante Microsoft Edge DevTools.
title: Ver, editar y eliminar cookies con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4f5a352445bd13b82ada82df3a528a1e80aa144e
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565060"
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
# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a><span data-ttu-id="06791-104">Ver, editar y eliminar cookies con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="06791-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="06791-105">[Las cookies HTTP][MDNHTTPCookies] se usan principalmente para administrar sesiones de usuario, almacenar preferencias de personalización de usuario y realizar un seguimiento del comportamiento del usuario.</span><span class="sxs-lookup"><span data-stu-id="06791-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="06791-106">Las cookies también son la causa de todos los molestos que esta página **usa formularios** de consentimiento de cookies que se encuentran en toda la web.</span><span class="sxs-lookup"><span data-stu-id="06791-106">Cookies are also the cause of all of the annoying **this page uses cookies** consent forms that are found across the web.</span></span>  <span data-ttu-id="06791-107">La siguiente guía le enseña a ver, editar y eliminar las cookies HTTP de una página web [con Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="06791-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a webpage with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-the-cookies-pane"></a><span data-ttu-id="06791-108">Abrir el panel Cookies</span><span class="sxs-lookup"><span data-stu-id="06791-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="06791-109">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="06791-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="06791-110">Elija la **pestaña** Aplicación para abrir **el** panel Aplicación.</span><span class="sxs-lookup"><span data-stu-id="06791-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="06791-111">El **panel Manifiesto** debe abrirse.</span><span class="sxs-lookup"><span data-stu-id="06791-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="06791-113">Figura 1: Panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="06791-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="06791-114">En **Storage** **expanda Cookies**y, a continuación, seleccione un origen.</span><span class="sxs-lookup"><span data-stu-id="06791-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="El panel Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="06791-116">Figura 2: Panel cookies</span><span class="sxs-lookup"><span data-stu-id="06791-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <a name="fields"></a><span data-ttu-id="06791-117">Campos</span><span class="sxs-lookup"><span data-stu-id="06791-117">Fields</span></span>  

<span data-ttu-id="06791-118">La **tabla Cookies** contiene los siguientes campos.</span><span class="sxs-lookup"><span data-stu-id="06791-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="06791-119">**Nombre**.</span><span class="sxs-lookup"><span data-stu-id="06791-119">**Name**.</span></span>  <span data-ttu-id="06791-120">El nombre de la cookie.</span><span class="sxs-lookup"><span data-stu-id="06791-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="06791-121">**Valor**.</span><span class="sxs-lookup"><span data-stu-id="06791-121">**Value**.</span></span>  <span data-ttu-id="06791-122">Valor de la cookie.</span><span class="sxs-lookup"><span data-stu-id="06791-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="06791-123">**Dominio**.</span><span class="sxs-lookup"><span data-stu-id="06791-123">**Domain**.</span></span>  <span data-ttu-id="06791-124">Los hosts que pueden recibir la cookie.</span><span class="sxs-lookup"><span data-stu-id="06791-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="06791-125">Vaya a [Ámbito de las cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="06791-125">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="06791-126">**Ruta**de acceso .</span><span class="sxs-lookup"><span data-stu-id="06791-126">**Path**.</span></span>  <span data-ttu-id="06791-127">Dirección URL que debe existir en la dirección URL solicitada para enviar el `Cookie` encabezado.</span><span class="sxs-lookup"><span data-stu-id="06791-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="06791-128">Vaya a [Ámbito de las cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="06791-128">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="06791-129">**Expira / Max-Age**.</span><span class="sxs-lookup"><span data-stu-id="06791-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="06791-130">Fecha de expiración o antigüedad máxima de la cookie.</span><span class="sxs-lookup"><span data-stu-id="06791-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="06791-131">Vaya a [Cookies permanentes][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="06791-131">Navigate to [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="06791-132">Para [las cookies de][MDNHTTPCookiesSession] sesión, este valor siempre es `Session` .</span><span class="sxs-lookup"><span data-stu-id="06791-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="06791-133">**Tamaño**.</span><span class="sxs-lookup"><span data-stu-id="06791-133">**Size**.</span></span>  <span data-ttu-id="06791-134">Tamaño, en bytes, de la cookie.</span><span class="sxs-lookup"><span data-stu-id="06791-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="06791-135">**HTTP**.</span><span class="sxs-lookup"><span data-stu-id="06791-135">**HTTP**.</span></span>  <span data-ttu-id="06791-136">Si es true, este campo indica que la cookie solo debe usarse a través de HTTP y no se permite la modificación de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="06791-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="06791-137">Vaya a [Cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="06791-137">Navigate to [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="06791-138">**Proteger**.</span><span class="sxs-lookup"><span data-stu-id="06791-138">**Secure**.</span></span>  <span data-ttu-id="06791-139">Si es true, este campo indica que la cookie debe enviarse al servidor solo a través de una conexión HTTPS segura.</span><span class="sxs-lookup"><span data-stu-id="06791-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="06791-140">Vaya a [Cookies seguras][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="06791-140">Navigate to [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="06791-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="06791-141">**SameSite**.</span></span>  <span data-ttu-id="06791-142">Contiene `strict` o si la cookie usa el atributo experimental `lax` [Samesite.][MDNHTTPCookiesSamesite]</span><span class="sxs-lookup"><span data-stu-id="06791-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="06791-143">**Prioridad**.</span><span class="sxs-lookup"><span data-stu-id="06791-143">**Priority**.</span></span>  <span data-ttu-id="06791-144">Contiene `low` , `medium` \(default\), o si la cookie usa el atributo priority de cookie en desuso. `high` [][ChromiumIssue232693]</span><span class="sxs-lookup"><span data-stu-id="06791-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <a name="filter-cookies"></a><span data-ttu-id="06791-145">Filtrar cookies</span><span class="sxs-lookup"><span data-stu-id="06791-145">Filter cookies</span></span>  

<span data-ttu-id="06791-146">Use el **cuadro de** texto Filtrar para filtrar las cookies **por Nombre** o **Valor**.</span><span class="sxs-lookup"><span data-stu-id="06791-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="06791-147">No se admite el filtrado por otros campos.</span><span class="sxs-lookup"><span data-stu-id="06791-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrar las cookies que no contienen el identificador de texto" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="06791-149">Figura 3: Filtrado de las cookies que no contienen el texto</span><span class="sxs-lookup"><span data-stu-id="06791-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a><span data-ttu-id="06791-150">Editar una cookie</span><span class="sxs-lookup"><span data-stu-id="06791-150">Edit a cookie</span></span>  

<span data-ttu-id="06791-151">Los **campos Name**, **Value**, **Domain**, **Path**y **Expires / Max-Age** son editables.</span><span class="sxs-lookup"><span data-stu-id="06791-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="06791-152">Haga doble clic en un campo para editarlo.</span><span class="sxs-lookup"><span data-stu-id="06791-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Establecer el nombre de una cookie en DEVTOOLS." lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="06791-154">Figura 4: Establecer el nombre de una cookie en</span><span class="sxs-lookup"><span data-stu-id="06791-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a><span data-ttu-id="06791-155">Eliminar cookies</span><span class="sxs-lookup"><span data-stu-id="06791-155">Delete cookies</span></span>  

<span data-ttu-id="06791-156">Elija una cookie y **elija Eliminar seleccionada** \( Eliminar seleccionada ![ ](../media/delete-icon.msft.png) \) para eliminar la cookie específica.</span><span class="sxs-lookup"><span data-stu-id="06791-156">Choose a cookie and choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\) to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Eliminación de una cookie específica" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="06791-158">Figura 5: Eliminación de una cookie específica</span><span class="sxs-lookup"><span data-stu-id="06791-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="06791-159">Elija **Borrar todo** \( Borrar todo ![ ](../media/clear-icon.msft.png) \) para eliminar todas las cookies.</span><span class="sxs-lookup"><span data-stu-id="06791-159">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\) to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Borrar todas las cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="06791-161">Figura 6: Borrar todas las cookies</span><span class="sxs-lookup"><span data-stu-id="06791-161">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="06791-162">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="06791-162">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) Developer Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Chromium Problema 232693: Implementar el campo de prioridad para las cookies | Chromium Errores"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP: cookies permanentes | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP: cookies de SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP: ámbito de las cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP: cookies seguras y HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP: cookies de sesión | MDN"  

> [!NOTE]
> <span data-ttu-id="06791-172">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06791-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="06791-173">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="06791-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="06791-175">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06791-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
