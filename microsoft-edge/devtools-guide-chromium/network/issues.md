---
description: Obtenga información sobre cómo detectar problemas de red en el panel Red de Microsoft Edge DevTools.
title: Guía de problemas de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c99f43872abe04800880c63ee4126bfcdd633edb
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564983"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="network-issues-guide"></a>Guía de problemas de red  

En esta guía se muestra cómo detectar problemas de red o oportunidades de optimización en el panel Red de Microsoft Edge DevTools.  

Para conocer los conceptos básicos de la **herramienta Red,** vaya [a Introducción][NetworkPerformance].  

## <a name="queued-or-stalled-requests"></a>Solicitudes en cola o en espera  

**Síntomas**  

Seis solicitudes se descargan simultáneamente.  Después de eso, una serie de solicitudes se ponen en cola o se detienen.  Una vez que finaliza una de las seis primeras solicitudes, se inicia una de las solicitudes de la cola.  

En la **cascada de** la siguiente figura, las seis primeras solicitudes del activo se `edge-iconx1024.msft.png` inician simultáneamente.  Las solicitudes posteriores se detienen hasta que uno de los seis finales originales.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Un ejemplo de una serie en cola o en espera en el panel Red" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Un ejemplo de una serie en cola o en espera en la **herramienta Red**  
:::image-end:::  

**Causas**  

Se están haciendo demasiadas solicitudes en un solo dominio.  En las conexiones HTTP/1.0 o HTTP/1.1, Microsoft Edge un máximo de seis conexiones TCP simultáneas por host.  

**Correcciones**  

*   Implemente el particionamiento de dominios si debe usar HTTP/1.0 o HTTP/1.1.  
*   Use HTTP/2.  No use el particionamiento de dominios con HTTP/2.  
*   Quite o aplaza las solicitudes innecesarias para que las solicitudes críticas se descarguen anteriormente.  
    
## <a name="slow-time-to-first-byte-ttfb"></a>Tiempo lento hasta el primer byte (TTFB)  

**Síntomas**  

Una solicitud pasa mucho tiempo esperando a recibir el primer byte del servidor.  

En la siguiente figura, la barra verde y larga de **la cascada** indica que la solicitud estaba esperando mucho tiempo.  Esto se simuló con un perfil para restringir la velocidad de red y agregar un retraso.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Un ejemplo de una solicitud con un tiempo lento al primer byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Un ejemplo de una solicitud con un tiempo lento al primer byte  
:::image-end:::  

**Causas**  

*   La conexión entre el cliente y el servidor es lenta.  
*   El servidor es lento para responder.  Hospedar el servidor localmente para determinar si la conexión o el servidor es lento.  Si sigue teniendo un tiempo lento al primer byte \(TTFB\) al obtener acceso a un servidor local, el servidor será lento.  
    
**Correcciones**  

*   Si la conexión es lenta, considere la posibilidad de hospedar el contenido en un CDN o cambiar los proveedores de hospedaje.  
*   Si el servidor es lento, considere la posibilidad de optimizar las consultas de base de datos, implementar una memoria caché o modificar la configuración del servidor.  
    
## <a name="slow-content-download"></a>Descarga lenta de contenido  

**Síntomas**  

Una solicitud tarda mucho tiempo en descargarse.  

En la siguiente figura, la barra larga y azul de **la cascada** junto al png significa que tardó mucho tiempo en descargarse.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Un ejemplo de una solicitud que tarda mucho tiempo en descargarse" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Un ejemplo de una solicitud que tarda mucho tiempo en descargarse  
:::image-end:::  

**Causas**  

*   La conexión entre el cliente y el servidor es lenta.  
*   Se está descargando gran cantidad de contenido.  
    
**Correcciones**  

*   Considere la posibilidad de hospedar el contenido en un CDN o cambiar los proveedores de hospedaje.  
*   Envíe menos bytes optimizando las solicitudes.  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback](../media/smile-icon.msft.png)\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nuevo problema: MicrosoftDocs/edge-developer"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original [](https://developers.google.com/web/tools/chrome-devtools/network/issues) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors#jonathan-garbee
