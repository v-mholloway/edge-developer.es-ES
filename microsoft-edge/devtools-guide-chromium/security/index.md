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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a>Comprender los problemas de seguridad con Microsoft Edge DevTools  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a>Abrir el panel Seguridad  

El **** panel Seguridad es el lugar principal de DevTools para inspeccionar la seguridad de una página.  

1.  [Abra DevTools][DevToolsOpen].  
1.  Elija la **pestaña** Seguridad para abrir la **herramienta** Seguridad.  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="El panel Seguridad" lightbox="../media/security-security-overview-secure.msft.png":::
       El panel **Seguridad**  
    :::image-end:::  
    
## <a name="common-problems"></a>Problemas comunes  

### <a name="non-secure-main-origins"></a>Orígenes principales no seguros  

Cuando el origen principal de una página no es seguro, la **información** general sobre seguridad indica **que esta página no es segura.**  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Una página no segura" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Una página no segura  
:::image-end:::  

Este problema se produce cuando la dirección URL que visitó se solicitó a través de HTTP.  Para que sea seguro, debe solicitarlo a través de HTTPS.  Por ejemplo, si observa la dirección URL de la barra de direcciones, probablemente tenga un aspecto similar a `http://example.com` .  Para que sea segura, la dirección URL debe ser `https://example.com` .  

Si ya ha configurado HTTPS en el servidor, lo único que debe hacer para solucionar este problema es configurar el servidor para redirigir todas las solicitudes HTTP a HTTPS.  

Si no ha configurado HTTPS en el servidor, [Let's Encrypt][LetsEncrypt] proporciona una forma gratuita y relativamente fácil de iniciar el proceso.  O bien, puede considerar hospedar su sitio en una red CDN.  La mayoría de los principales sitios de host de CDN en HTTPS ahora son de forma predeterminada.  

> [!TIP]
> La [sugerencia Usar HTTPS][WebhintUseHttps] en [webhint][Webhint] puede ayudar a automatizar el proceso de asegurarse de que todas las solicitudes HTTP se dirigen a HTTPS.  

### <a name="mixed-content"></a>Contenido mixto  

**El contenido mixto** significa que el origen principal de una página es seguro, pero la página solicitó recursos de orígenes no seguros.  Las páginas de contenido mixto solo están parcialmente protegidas porque el contenido HTTP es accesible para los sniffers y vulnerable a los ataques de man-in-the-middle.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Contenido mixto" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Contenido mixto  
:::image-end:::  

En la figura anterior, elija Ver **1** **** solicitud en el panel Red para abrir la herramienta Red y aplicar el filtro para que el registro de red solo muestre `mixed-content:displayed` recursos no seguros. ****  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Recursos mixtos en el registro de red" lightbox="../media/security-network-filter.msft.png":::
   Recursos mixtos en el **registro de red**  
:::image-end:::  

## <a name="view-details"></a>Ver detalles  

### <a name="view-main-origin-certificate"></a>Ver certificado de origen principal  

En Información **general sobre seguridad,** elija **Ver certificado** para inspeccionar rápidamente el certificado para el origen principal.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Un certificado de origen principal" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Un certificado de origen principal  
:::image-end:::  

### <a name="view-origin-details"></a>Ver detalles de origen  

Elija una de las entradas de la navegación a la izquierda para ver los detalles del origen.  En la página de detalles puede ver la información de conexión y certificado.  La información de transparencia de certificados también se muestra cuando está disponible.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Detalles del origen principal" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Detalles del origen principal  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevToolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[LetsEncrypt]: https://letsencrypt.org "Vamos a cifrar: certificados SSL/TLS gratuitos"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar https | documentación de webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/security/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
