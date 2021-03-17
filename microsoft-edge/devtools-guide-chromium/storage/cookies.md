---
description: Obtenga información sobre cómo ver, editar y eliminar las cookies HTTP de una página con Microsoft Edge DevTools.
title: Ver, editar y eliminar cookies con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c208ca628fe91ed5922bc36566be2b9bdd20ec0b
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439685"
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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a>Ver, editar y eliminar cookies con Microsoft Edge DevTools  

[Las cookies HTTP][MDNHTTPCookies] se usan principalmente para administrar sesiones de usuario, almacenar preferencias de personalización de usuario y realizar un seguimiento del comportamiento del usuario.  Las cookies también son la causa de todos los molestos que esta página **usa formularios** de consentimiento de cookies que se encuentran en toda la web.  La siguiente guía le enseña a ver, editar y eliminar las cookies HTTP de una página web con [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## <a name="open-the-cookies-pane"></a>Abrir el panel Cookies  

1.  [Abra DevTools][DevToolsOpen].  
1.  Elija la **pestaña** Aplicación para abrir **el** panel Aplicación.  El **panel Manifiesto** debe abrirse.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Figura 1: Panel manifiesto  
    :::image-end:::  

1.  En **Almacenamiento,** expanda **Cookies**y, a continuación, seleccione un origen.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="El panel Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Figura 2: Panel cookies  
    :::image-end:::  

## <a name="fields"></a>Campos  

La **tabla Cookies** contiene los siguientes campos.  

*   **Nombre**.  El nombre de la cookie.  
*   **Valor**.  Valor de la cookie.  
*   **Dominio**.  Los hosts que pueden recibir la cookie.  Vaya a [Ámbito de las cookies][MDNHTTPCookiesScope].  
*   **Ruta**de acceso .  Dirección URL que debe existir en la dirección URL solicitada para enviar el `Cookie` encabezado.  Vaya a [Ámbito de las cookies][MDNHTTPCookiesScope].  
*   **Expira / Max-Age**.  Fecha de expiración o antigüedad máxima de la cookie.  Vaya a [Cookies permanentes][MDNHTTPCookiesPermanent].  Para [las cookies de][MDNHTTPCookiesSession] sesión, este valor siempre es `Session` .  
*   **Tamaño**.  Tamaño, en bytes, de la cookie.  
*   **HTTP**.  Si es true, este campo indica que la cookie solo debe usarse a través de HTTP y no se permite la modificación de JavaScript.  Vaya a [Cookies HttpOnly][MDNHTTPCookiesSecure].  
*   **Proteger**.  Si es true, este campo indica que la cookie debe enviarse al servidor solo a través de una conexión HTTPS segura.  Vaya a [Cookies seguras][MDNHTTPCookiesSecure].  
*   **SameSite**.  Contiene `strict` o si la cookie usa el atributo experimental `lax` [Samesite.][MDNHTTPCookiesSamesite]  
*   **Prioridad**.  Contiene `low` , `medium` \(default\), o si la cookie usa el atributo priority de cookie en desuso. `high` [][ChromiumIssue232693]

## <a name="filter-cookies"></a>Filtrar cookies  

Use el **cuadro de** texto Filtrar para filtrar las cookies **por Nombre** o **Valor**.  No se admite el filtrado por otros campos.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrar las cookies que no contienen el identificador de texto" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Figura 3: Filtrado de las cookies que no contienen el texto `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a>Editar una cookie  

Los **campos Name**, **Value**, **Domain**, **Path**y **Expires / Max-Age** son editables.  
Haga doble clic en un campo para editarlo.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Establecer el nombre de una cookie en DEVTOOLS." lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Figura 4: Establecer el nombre de una cookie en `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a>Eliminar cookies  

Elija una cookie y **elija Eliminar seleccionada** \( Eliminar seleccionada ![ ](../media/delete-icon.msft.png) \) para eliminar la cookie específica.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Eliminación de una cookie específica" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Figura 5: Eliminación de una cookie específica  
:::image-end:::  

Elija **Borrar todo** \( Borrar todo ![ ](../media/clear-icon.msft.png) \) para eliminar todas las cookies.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Borrar todas las cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Figura 6: Borrar todas las cookies  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Chromium Issue 232693: Implementing Priority Field for Cookies | Errores de Chromium"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP: cookies permanentes | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP: cookies de SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP: ámbito de las cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP: cookies seguras y HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP: cookies de sesión | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
