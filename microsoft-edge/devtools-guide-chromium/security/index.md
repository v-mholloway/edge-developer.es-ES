---
title: Comprender los problemas de seguridad con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611913"
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





# Comprender los problemas de seguridad con Microsoft Edge DevTools   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## Abrir el panel seguridad   

El panel **seguridad** es el lugar principal en DevTools para inspeccionar la seguridad de una página.  

1.  [Abra DevTools][DevToolsOpen].  

1.  Haga clic en la pestaña **seguridad** para abrir el panel **seguridad** .  
    
    > ##### Figura 1  
    > El panel seguridad  
    > ![El panel seguridad][ImageSecurityPanel]  
    
## Problemas comunes   

### Orígenes principales no seguros   

Cuando el origen principal de una página no es seguro, la **información general de seguridad** indica que **esta página no es segura**.  

> ##### Figura 2  
> Una página no segura  
> ![Una página no segura][ImageNonSecurePage]  

Este problema se produce cuando se solicitó la dirección URL que visitó a través de HTTP.  Para asegurarte de que es necesario solicitarlo a través de HTTPS.  Por ejemplo, si miras la dirección URL en la barra de direcciones, probablemente tenga un aspecto parecido a `http://example.com` .  Para que sea segura, la dirección URL debe ser `https://example.com` .  

Si ya ha configurado HTTPS en el servidor, todo lo que debe hacer para solucionar este problema es configurar su servidor para redirigir todas las solicitudes HTTP a HTTPS.  

Si no ha configurado HTTPS en el servidor, vamos a [cifrar][LetsEncrypt] proporciona una forma gratuita y relativamente fácil de iniciar el proceso.  O bien, puede que considere hospedar su sitio en una red CDN.  La mayoría de los principales sitios CDN hospedan en HTTPS de forma predeterminada.  

> [!TIP]
> La sugerencia [use HTTPS][WebhintUseHttps] en [webhint][Webhint] puede ayudar a automatizar el proceso de asegurarse de que todas las solicitudes HTTP se dirijan a https.  

### Contenido mixto   

El **contenido mixto** significa que el origen principal de una página es seguro, pero la página solicitó recursos de orígenes no seguros.  Las páginas de contenido mixto solo están parcialmente protegidas porque el contenido HTTP es accesible para los rastreadores y es vulnerable a ataques de intermediario.  

> ##### Imagen 3  
> Contenido mixto  
> ![Contenido mixto][ImageMixedContent]  

En la [figura 3](#figure-3), haga clic en **Ver 1 solicitud en el panel red** para abrir el panel **red** y aplicar el `mixed-content:displayed` filtro para que el **registro de red** solo muestre recursos no seguros.  

> ##### Imagen 4  
> Recursos mixtos en el registro de red  
> ![Recursos mixtos en el registro de red][ImageMixedResourcesNetworkLog]  

## Ver detalles   

### Ver certificado de origen principal   

En la **Introducción**a la seguridad, haga clic en **Ver certificado** para inspeccionar rápidamente el certificado del origen principal.  

> ##### Imagen 5  
> Un certificado de origen principal  
> ![Un certificado de origen principal][ImageCertificate]  

### Ver detalles de origen   

Haga clic en una de las entradas en el barra de navegación de la izquierda para ver los detalles del origen.  En la página de detalles puede ver la información de la conexión y el certificado.  La información de transparencia del certificado también se muestra cuando está disponible.  

> ##### Imagen 6  
> Detalles de origen principal  
> ![Detalles de origen principal][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Ilustración 1: panel de seguridad"  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Ilustración 2: una página no segura"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Ilustración 3: contenido mixto"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Ilustración 4: recursos mixtos en el registro de red"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Ilustración 5: un certificado de origen principal"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Ilustración 6: detalles de origen principal"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  


[LetsEncrypt]: https://letsencrypt.org "Vamos a cifrar los certificados SSL/TLS sin cifrar"  

[Webhint]: https://webhint.io "sugerencia"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar HTTPS | documentación de webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/security/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
