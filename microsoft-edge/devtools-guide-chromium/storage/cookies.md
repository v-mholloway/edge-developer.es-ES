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





# Ver, editar y eliminar cookies con Microsoft Edge DevTools   

  

Las [cookies http][MDNHTTPCookies] se usan principalmente para administrar sesiones de usuario, almacenar las preferencias de personalización del usuario y hacer un seguimiento del comportamiento del usuario.  También son la causa de todos los formularios de consentimiento "esta página usa cookies" que ve en la Web.  Esta guía le enseña a ver, editar y eliminar las cookies HTTP de una página con [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Abrir el panel cookies   

1.  [Abra DevTools][DevToolsOpen].  
1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** debe abrirse.  
    
    > ##### Figura 1  
    > El panel manifiesto  
    > ![El panel manifiesto][ImageManifest]  

1.  En **almacenamiento** , expanda **cookies**y, a continuación, seleccione un origen.  
    
    > ##### Figura 2  
    > El panel cookies  
    > ![El panel cookies][ImageCookies]  

## Campos   

La tabla **cookies** contiene los siguientes campos:  

*   **Nombre**.  El nombre de la cookie.  
*   **Value**.  El valor de la cookie.  
*   **Dominio**.  Los hosts que pueden recibir la cookie.  Ver el [ámbito de las cookies][MDNHTTPCookiesScope].  
*   **Ruta de acceso**.  La dirección URL que debe existir en la dirección URL solicitada para poder enviar el `Cookie` encabezado.  Ver el [ámbito de las cookies][MDNHTTPCookiesScope].  
*   **Vence o Max-Age**.  La fecha de expiración o la antigüedad máxima de la cookie.  Consulte [cookies permanentes][MDNHTTPCookiesPermanent].  En el caso de las [cookies de sesión][MDNHTTPCookiesSession] , este valor es siempre `Session` .  
*   **Tamaño**.  Tamaño, en bytes, de la cookie.  
*   **Http**.  Si es true, este campo indica que la cookie solo debe usarse a través de HTTP y no se permite la modificación de JavaScript.  Vea [cookies HttpOnly][MDNHTTPCookiesSecure].  
*   **Seguro**.  Si es true, este campo indica que la cookie debe enviarse al servidor solo a través de una conexión HTTPS segura.  Consulte [cookies seguras][MDNHTTPCookiesSecure].  
*   **SameSite**.  Contiene `strict` o `lax` si la cookie está usando el atributo [SameSite][MDNHTTPCookiesSamesite] experimental.  

## Filtrar cookies   

Use el cuadro de texto **filtrar** para filtrar las cookies por **nombre** o **valor**.  No se admite el filtrado por otros campos.  

> ##### Imagen 3  
> Filtrar las cookies que no contienen el texto `ID`  
> ![Filtrar las cookies que no contienen el identificador de texto][ImageCookiesFilter]  

## Editar una cookie   

Los campos **nombre**, **valor**, **dominio**, **ruta**y **vencimiento/edad máxima** son editables.  
Haga doble clic en un campo para modificarlo.  

> ##### Imagen 4  
> Establecer el nombre de una cookie en `DEVTOOLS!`  
> ![Establecer el nombre de una cookie en DEVTOOLSme!][ImageEditCookie]  

## Eliminar cookies   

Seleccione una cookie y, a continuación, haga clic en **eliminar** selección ![ eliminar seleccionada ][ImageDeleteIcon] para eliminarla.  

> ##### Imagen 5  
> Eliminar una cookie específica  
> ![Eliminar una cookie específica][ImageDeleteCookie]  

Seleccione **Borrar** todo ![ Borrar todo ][ImageClearIcon] para eliminar todas las cookies.  

> ##### Imagen 6  
> Borrar todas las cookies  
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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
