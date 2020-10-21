---
description: Aprenda a ver, editar y eliminar las cookies HTTP de una página con Microsoft Edge DevTools.
title: Ver, editar y eliminar cookies con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 328771aa254dac1f851535a44126ea220dc95a9c
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125485"
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

# <span data-ttu-id="5be30-104">Ver, editar y eliminar cookies con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5be30-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="5be30-105">Las [cookies http][MDNHTTPCookies] se usan principalmente para administrar sesiones de usuario, almacenar las preferencias de personalización del usuario y hacer un seguimiento del comportamiento del usuario.</span><span class="sxs-lookup"><span data-stu-id="5be30-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="5be30-106">Las cookies también son la causa de todos los formularios de consentimiento "esta página usa cookies" que ve en la Web.</span><span class="sxs-lookup"><span data-stu-id="5be30-106">Cookies are also the cause of all of the annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="5be30-107">La siguiente guía le enseña a ver, editar y eliminar las cookies HTTP de una página con [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="5be30-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="5be30-108">Abrir el panel cookies</span><span class="sxs-lookup"><span data-stu-id="5be30-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="5be30-109">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="5be30-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="5be30-110">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="5be30-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="5be30-111">El panel **manifiesto** debe abrirse.</span><span class="sxs-lookup"><span data-stu-id="5be30-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="5be30-113">Ilustración 1: el panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="5be30-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="5be30-114">En **almacenamiento** , expanda **cookies**y, a continuación, seleccione un origen.</span><span class="sxs-lookup"><span data-stu-id="5be30-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="5be30-116">Ilustración 2: el panel cookies</span><span class="sxs-lookup"><span data-stu-id="5be30-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <span data-ttu-id="5be30-117">Campos</span><span class="sxs-lookup"><span data-stu-id="5be30-117">Fields</span></span>  

<span data-ttu-id="5be30-118">La tabla **cookies** contiene los siguientes campos.</span><span class="sxs-lookup"><span data-stu-id="5be30-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="5be30-119">**Nombre**.</span><span class="sxs-lookup"><span data-stu-id="5be30-119">**Name**.</span></span>  <span data-ttu-id="5be30-120">El nombre de la cookie.</span><span class="sxs-lookup"><span data-stu-id="5be30-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="5be30-121">**Value**.</span><span class="sxs-lookup"><span data-stu-id="5be30-121">**Value**.</span></span>  <span data-ttu-id="5be30-122">El valor de la cookie.</span><span class="sxs-lookup"><span data-stu-id="5be30-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="5be30-123">**Dominio**.</span><span class="sxs-lookup"><span data-stu-id="5be30-123">**Domain**.</span></span>  <span data-ttu-id="5be30-124">Los hosts que pueden recibir la cookie.</span><span class="sxs-lookup"><span data-stu-id="5be30-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="5be30-125">Ver el [ámbito de las cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="5be30-125">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="5be30-126">**Ruta de acceso**.</span><span class="sxs-lookup"><span data-stu-id="5be30-126">**Path**.</span></span>  <span data-ttu-id="5be30-127">La dirección URL que debe existir en la dirección URL solicitada para poder enviar el `Cookie` encabezado.</span><span class="sxs-lookup"><span data-stu-id="5be30-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="5be30-128">Ver el [ámbito de las cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="5be30-128">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="5be30-129">**Vence o Max-Age**.</span><span class="sxs-lookup"><span data-stu-id="5be30-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="5be30-130">La fecha de expiración o la antigüedad máxima de la cookie.</span><span class="sxs-lookup"><span data-stu-id="5be30-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="5be30-131">Consulte [cookies permanentes][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="5be30-131">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="5be30-132">En el caso de las [cookies de sesión][MDNHTTPCookiesSession] , este valor es siempre `Session` .</span><span class="sxs-lookup"><span data-stu-id="5be30-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="5be30-133">**Tamaño**.</span><span class="sxs-lookup"><span data-stu-id="5be30-133">**Size**.</span></span>  <span data-ttu-id="5be30-134">Tamaño, en bytes, de la cookie.</span><span class="sxs-lookup"><span data-stu-id="5be30-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="5be30-135">**Http**.</span><span class="sxs-lookup"><span data-stu-id="5be30-135">**HTTP**.</span></span>  <span data-ttu-id="5be30-136">Si es true, este campo indica que la cookie solo debe usarse a través de HTTP y no se permite la modificación de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5be30-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="5be30-137">Vea [cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="5be30-137">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="5be30-138">**Seguro**.</span><span class="sxs-lookup"><span data-stu-id="5be30-138">**Secure**.</span></span>  <span data-ttu-id="5be30-139">Si es true, este campo indica que la cookie debe enviarse al servidor solo a través de una conexión HTTPS segura.</span><span class="sxs-lookup"><span data-stu-id="5be30-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="5be30-140">Consulte [cookies seguras][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="5be30-140">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="5be30-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="5be30-141">**SameSite**.</span></span>  <span data-ttu-id="5be30-142">Contiene `strict` o `lax` si la cookie está usando el atributo [SameSite][MDNHTTPCookiesSamesite] experimental.</span><span class="sxs-lookup"><span data-stu-id="5be30-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="5be30-143">**Priority**.</span><span class="sxs-lookup"><span data-stu-id="5be30-143">**Priority**.</span></span>  <span data-ttu-id="5be30-144">Contains `low` , `medium` \ (default \) o `high` si la cookie usa el atributo de [prioridad de cookies][ChromiumIssue232693] obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5be30-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <span data-ttu-id="5be30-145">Filtrar cookies</span><span class="sxs-lookup"><span data-stu-id="5be30-145">Filter cookies</span></span>  

<span data-ttu-id="5be30-146">Use el cuadro de texto **filtrar** para filtrar las cookies por **nombre** o **valor**.</span><span class="sxs-lookup"><span data-stu-id="5be30-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="5be30-147">No se admite el filtrado por otros campos.</span><span class="sxs-lookup"><span data-stu-id="5be30-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="5be30-149">Ilustración 3: filtrar las cookies que no contienen el texto</span><span class="sxs-lookup"><span data-stu-id="5be30-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <span data-ttu-id="5be30-150">Editar una cookie</span><span class="sxs-lookup"><span data-stu-id="5be30-150">Edit a cookie</span></span>  

<span data-ttu-id="5be30-151">Los campos **nombre**, **valor**, **dominio**, **ruta**y **vencimiento/edad máxima** son editables.</span><span class="sxs-lookup"><span data-stu-id="5be30-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="5be30-152">Haga doble clic en un campo para modificarlo.</span><span class="sxs-lookup"><span data-stu-id="5be30-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="5be30-154">Ilustración 4: establecer el nombre de una cookie en</span><span class="sxs-lookup"><span data-stu-id="5be30-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <span data-ttu-id="5be30-155">Eliminar cookies</span><span class="sxs-lookup"><span data-stu-id="5be30-155">Delete cookies</span></span>  

<span data-ttu-id="5be30-156">Seleccione una cookie y elija **eliminar** selección de ![ eliminación seleccionada ][ImageDeleteIcon]  para eliminarla.</span><span class="sxs-lookup"><span data-stu-id="5be30-156">Select a cookie and choose **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="5be30-158">Ilustración 5: eliminar una cookie específica</span><span class="sxs-lookup"><span data-stu-id="5be30-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="5be30-159">Elija **Borrar** todo ![ Borrar todo ][ImageClearIcon]  para eliminar todas las cookies.</span><span class="sxs-lookup"><span data-stu-id="5be30-159">Choose **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="5be30-161">Ilustración 6: borrar todas las cookies</span><span class="sxs-lookup"><span data-stu-id="5be30-161">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

## <span data-ttu-id="5be30-162">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5be30-162">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Error de cromo 232693: campo de prioridad de implementación de cookies | Errores de cromo"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP: cookies permanentes | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP: cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP: ámbito de las cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP: cookies seguras y HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP: cookies de sesión | MDN"  

> [!NOTE]
> <span data-ttu-id="5be30-172">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5be30-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5be30-173">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5be30-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5be30-175">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5be30-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
