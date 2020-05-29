---
title: Ver, editar y eliminar cookies con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 084c4116cd4c9c5e70b2fe341257fa68ba2c8ae7
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612072"
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





# <span data-ttu-id="d3760-103">Ver, editar y eliminar cookies con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d3760-103">View, Edit, And Delete Cookies With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="d3760-104">Las [cookies http][MDNHTTPCookies] se usan principalmente para administrar sesiones de usuario, almacenar las preferencias de personalización del usuario y hacer un seguimiento del comportamiento del usuario.</span><span class="sxs-lookup"><span data-stu-id="d3760-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="d3760-105">También son la causa de todos los formularios de consentimiento "esta página usa cookies" que ve en la Web.</span><span class="sxs-lookup"><span data-stu-id="d3760-105">They are also the cause of all of those annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="d3760-106">Esta guía le enseña a ver, editar y eliminar las cookies HTTP de una página con [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="d3760-106">This guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="d3760-107">Abrir el panel cookies</span><span class="sxs-lookup"><span data-stu-id="d3760-107">Open the Cookies pane</span></span>   

1.  <span data-ttu-id="d3760-108">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="d3760-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="d3760-109">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="d3760-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="d3760-110">El panel **manifiesto** debe abrirse.</span><span class="sxs-lookup"><span data-stu-id="d3760-110">The **Manifest** pane should open.</span></span>  
    
    > ##### <span data-ttu-id="d3760-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="d3760-111">Figure 1</span></span>  
    > <span data-ttu-id="d3760-112">El panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="d3760-112">The Manifest pane</span></span>  
    > ![El panel manifiesto][ImageManifest]  

1.  <span data-ttu-id="d3760-114">En **almacenamiento** , expanda **cookies**y, a continuación, seleccione un origen.</span><span class="sxs-lookup"><span data-stu-id="d3760-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    > ##### <span data-ttu-id="d3760-115">Figura 2</span><span class="sxs-lookup"><span data-stu-id="d3760-115">Figure 2</span></span>  
    > <span data-ttu-id="d3760-116">El panel cookies</span><span class="sxs-lookup"><span data-stu-id="d3760-116">The Cookies pane</span></span>  
    > ![El panel cookies][ImageCookies]  

## <span data-ttu-id="d3760-118">Campos</span><span class="sxs-lookup"><span data-stu-id="d3760-118">Fields</span></span>   

<span data-ttu-id="d3760-119">La tabla **cookies** contiene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="d3760-119">The **Cookies** table contains the following fields:</span></span>  

*   <span data-ttu-id="d3760-120">**Nombre**.</span><span class="sxs-lookup"><span data-stu-id="d3760-120">**Name**.</span></span>  <span data-ttu-id="d3760-121">El nombre de la cookie.</span><span class="sxs-lookup"><span data-stu-id="d3760-121">The name of the cookie.</span></span>  
*   <span data-ttu-id="d3760-122">**Value**.</span><span class="sxs-lookup"><span data-stu-id="d3760-122">**Value**.</span></span>  <span data-ttu-id="d3760-123">El valor de la cookie.</span><span class="sxs-lookup"><span data-stu-id="d3760-123">The value of the cookie.</span></span>  
*   <span data-ttu-id="d3760-124">**Dominio**.</span><span class="sxs-lookup"><span data-stu-id="d3760-124">**Domain**.</span></span>  <span data-ttu-id="d3760-125">Los hosts que pueden recibir la cookie.</span><span class="sxs-lookup"><span data-stu-id="d3760-125">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="d3760-126">Ver el [ámbito de las cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="d3760-126">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="d3760-127">**Ruta de acceso**.</span><span class="sxs-lookup"><span data-stu-id="d3760-127">**Path**.</span></span>  <span data-ttu-id="d3760-128">La dirección URL que debe existir en la dirección URL solicitada para poder enviar el `Cookie` encabezado.</span><span class="sxs-lookup"><span data-stu-id="d3760-128">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="d3760-129">Ver el [ámbito de las cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="d3760-129">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="d3760-130">**Vence o Max-Age**.</span><span class="sxs-lookup"><span data-stu-id="d3760-130">**Expires / Max-Age**.</span></span>  <span data-ttu-id="d3760-131">La fecha de expiración o la antigüedad máxima de la cookie.</span><span class="sxs-lookup"><span data-stu-id="d3760-131">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="d3760-132">Consulte [cookies permanentes][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="d3760-132">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="d3760-133">En el caso de las [cookies de sesión][MDNHTTPCookiesSession] , este valor es siempre `Session` .</span><span class="sxs-lookup"><span data-stu-id="d3760-133">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="d3760-134">**Tamaño**.</span><span class="sxs-lookup"><span data-stu-id="d3760-134">**Size**.</span></span>  <span data-ttu-id="d3760-135">Tamaño, en bytes, de la cookie.</span><span class="sxs-lookup"><span data-stu-id="d3760-135">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="d3760-136">**Http**.</span><span class="sxs-lookup"><span data-stu-id="d3760-136">**HTTP**.</span></span>  <span data-ttu-id="d3760-137">Si es true, este campo indica que la cookie solo debe usarse a través de HTTP y no se permite la modificación de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d3760-137">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="d3760-138">Vea [cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="d3760-138">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="d3760-139">**Seguro**.</span><span class="sxs-lookup"><span data-stu-id="d3760-139">**Secure**.</span></span>  <span data-ttu-id="d3760-140">Si es true, este campo indica que la cookie debe enviarse al servidor solo a través de una conexión HTTPS segura.</span><span class="sxs-lookup"><span data-stu-id="d3760-140">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="d3760-141">Consulte [cookies seguras][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="d3760-141">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="d3760-142">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="d3760-142">**SameSite**.</span></span>  <span data-ttu-id="d3760-143">Contiene `strict` o `lax` si la cookie está usando el atributo [SameSite][MDNHTTPCookiesSamesite] experimental.</span><span class="sxs-lookup"><span data-stu-id="d3760-143">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  

## <span data-ttu-id="d3760-144">Filtrar cookies</span><span class="sxs-lookup"><span data-stu-id="d3760-144">Filter cookies</span></span>   

<span data-ttu-id="d3760-145">Use el cuadro de texto **filtrar** para filtrar las cookies por **nombre** o **valor**.</span><span class="sxs-lookup"><span data-stu-id="d3760-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="d3760-146">No se admite el filtrado por otros campos.</span><span class="sxs-lookup"><span data-stu-id="d3760-146">Filtering by other fields is not supported.</span></span>  

> ##### <span data-ttu-id="d3760-147">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="d3760-147">Figure 3</span></span>  
> <span data-ttu-id="d3760-148">Filtrar las cookies que no contienen el texto</span><span class="sxs-lookup"><span data-stu-id="d3760-148">Filtering out any cookies that do not contain the text</span></span> `ID`  
> ![Filtrar las cookies que no contienen el identificador de texto][ImageCookiesFilter]  

## <span data-ttu-id="d3760-150">Editar una cookie</span><span class="sxs-lookup"><span data-stu-id="d3760-150">Edit a cookie</span></span>   

<span data-ttu-id="d3760-151">Los campos **nombre**, **valor**, **dominio**, **ruta**y **vencimiento/edad máxima** son editables.</span><span class="sxs-lookup"><span data-stu-id="d3760-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="d3760-152">Haga doble clic en un campo para modificarlo.</span><span class="sxs-lookup"><span data-stu-id="d3760-152">Double-click a field to edit it.</span></span>  

> ##### <span data-ttu-id="d3760-153">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="d3760-153">Figure 4</span></span>  
> <span data-ttu-id="d3760-154">Establecer el nombre de una cookie en</span><span class="sxs-lookup"><span data-stu-id="d3760-154">Setting the name of a cookie to</span></span> `DEVTOOLS!`  
> ![Establecer el nombre de una cookie en DEVTOOLSme!][ImageEditCookie]  

## <span data-ttu-id="d3760-156">Eliminar cookies</span><span class="sxs-lookup"><span data-stu-id="d3760-156">Delete cookies</span></span>   

<span data-ttu-id="d3760-157">Seleccione una cookie y, a continuación, haga clic en **eliminar** selección ![ eliminar seleccionada ][ImageDeleteIcon] para eliminarla.</span><span class="sxs-lookup"><span data-stu-id="d3760-157">Select a cookie and then click **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete that one cookie.</span></span>  

> ##### <span data-ttu-id="d3760-158">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="d3760-158">Figure 5</span></span>  
> <span data-ttu-id="d3760-159">Eliminar una cookie específica</span><span class="sxs-lookup"><span data-stu-id="d3760-159">Deleting a specific cookie</span></span>  
> ![Eliminar una cookie específica][ImageDeleteCookie]  

<span data-ttu-id="d3760-161">Seleccione **Borrar** todo ![ Borrar todo ][ImageClearIcon] para eliminar todas las cookies.</span><span class="sxs-lookup"><span data-stu-id="d3760-161">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

> ##### <span data-ttu-id="d3760-162">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="d3760-162">Figure 6</span></span>  
> <span data-ttu-id="d3760-163">Borrar todas las cookies</span><span class="sxs-lookup"><span data-stu-id="d3760-163">Clearing all cookies</span></span>  
> ![Borrar todas las cookies][ImageClearAllCookies]  

<!--    -->  

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Ilustración 1: el panel manifiesto"  
[ImageCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-selected.msft.png "Ilustración 2: el panel cookies"  
[ImageCookiesFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-filter-id.msft.png "Ilustración 3: filtrar las cookies que no contienen el identificador de texto"  
[ImageEditCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-rename.msft.png "Ilustración 4: establecer el nombre de una cookie en DEVTOOLSme!"  
[ImageDeleteCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-delete-selected.msft.png "Ilustración 5: eliminar una cookie específica"  
[ImageClearAllCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-clear-all.msft.png "Ilustración 6: borrar todas las cookies"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP: cookies permanentes | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP: cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP: ámbito de las cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP: cookies seguras y HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP: cookies de sesión | MDN"  

> [!NOTE]
> <span data-ttu-id="d3760-179">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d3760-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d3760-180">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d3760-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d3760-182">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d3760-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
