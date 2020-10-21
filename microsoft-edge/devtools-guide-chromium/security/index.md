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

# Comprender los problemas de seguridad con Microsoft Edge DevTools  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## Abrir el panel seguridad  

El panel **seguridad** es el lugar principal en DevTools para inspeccionar la seguridad de una página.  

1.  [Abra DevTools][DevToolsOpen].  
1.  Seleccione la pestaña **seguridad** para abrir el panel **seguridad** .  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-secure.msft.png":::
       El panel **seguridad**  
    :::image-end:::  
    
## Problemas comunes  

### Orígenes principales no seguros  

Cuando el origen principal de una página no es seguro, la **información general de seguridad** indica que **esta página no es segura**.  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Una página no segura  
:::image-end:::  

Este problema se produce cuando se solicitó la dirección URL que visitó a través de HTTP.  Para asegurarte de que es necesario solicitarlo a través de HTTPS.  Por ejemplo, si miras la dirección URL en la barra de direcciones, probablemente tenga un aspecto parecido a `http://example.com` .  Para que sea segura, la dirección URL debe ser `https://example.com` .  

Si ya ha configurado HTTPS en el servidor, todo lo que debe hacer para solucionar este problema es configurar su servidor para redirigir todas las solicitudes HTTP a HTTPS.  

Si no ha configurado HTTPS en el servidor, vamos a [cifrar][LetsEncrypt] proporciona una forma gratuita y relativamente fácil de iniciar el proceso.  O bien, puede que considere hospedar su sitio en una red CDN.  La mayoría de los principales sitios CDN hospedan en HTTPS de forma predeterminada.  

> [!TIP]
> La sugerencia [use HTTPS][WebhintUseHttps] en [webhint][Webhint] puede ayudar a automatizar el proceso de asegurarse de que todas las solicitudes HTTP se dirijan a https.  

### Contenido mixto  

El **contenido mixto** significa que el origen principal de una página es seguro, pero la página solicitó recursos de orígenes no seguros.  Las páginas de contenido mixto solo están parcialmente protegidas porque el contenido HTTP es accesible para los rastreadores y es vulnerable a ataques de intermediario.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Contenido mixto  
:::image-end:::  

En la ilustración anterior, elija **Ver 1 solicitud en el panel red** para abrir el panel **red** y aplicar el `mixed-content:displayed` filtro para que el **registro de red** solo muestre recursos no seguros.  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="El panel seguridad" lightbox="../media/security-network-filter.msft.png":::
   Recursos mixtos en el **registro de red**  
:::image-end:::  

## Ver detalles  

### Ver certificado de origen principal  

En la **Descripción de seguridad**, elija **Ver certificado** para inspeccionar rápidamente el certificado para el origen principal.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Un certificado de origen principal  
:::image-end:::  

### Ver detalles de origen  

Haga clic en una de las entradas en el barra de navegación de la izquierda para ver los detalles del origen.  En la página de detalles puede ver la información de la conexión y el certificado.  La información de transparencia del certificado también se muestra cuando está disponible.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="El panel seguridad" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Detalles de origen principal  
:::image-end:::  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  
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
