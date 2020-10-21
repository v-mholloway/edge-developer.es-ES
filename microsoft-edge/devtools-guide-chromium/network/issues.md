---
description: Obtenga información sobre cómo detectar problemas de red en el panel de red de Microsoft Edge DevTools.
title: Guía de problemas de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4713dc252d428abbf5b60ee5f74a7316a102dab6
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125380"
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

# Guía de problemas de red  

En esta guía se muestra cómo detectar problemas de red o oportunidades de optimización en el panel red de Microsoft Edge DevTools.  

Consulte [Introducción][NetworkPerformance] a los conceptos básicos del panel **red** .  

## Solicitudes en cola o detenidas  

**Síntomas**  

Se están descargando seis solicitudes al mismo tiempo.  Después de eso, una serie de solicitudes se ponen en cola o se detienen.  Una vez finalizada una de las primeras seis solicitudes, se inicia una de las solicitudes de la cola.  

En la **cascada** de la siguiente ilustración, las seis primeras solicitudes del `edge-iconx1024.msft.png` activo se inician simultáneamente.  Las siguientes solicitudes se detienen hasta que se haya completado una de seis originales.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Ejemplo de una serie en cola o detenida en el panel red" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Ejemplo de una serie en cola o detenida en el panel **red**  
:::image-end:::  

**Causas**  

Se están realizando demasiadas solicitudes en un solo dominio.  En las conexiones HTTP/1.0 o HTTP/1.1, Microsoft Edge permite un máximo de seis conexiones TCP simultáneas por host.  

**Arreglos**  

*   Implemente la particionamiento del dominio si necesita usar HTTP/1.0 o HTTP/1.1.  
*   Use HTTP/2.  No use el particionamiento del dominio con HTTP/2.  
*   Quite o aplaza las solicitudes innecesarias para que las solicitudes críticas se descarguen anteriormente.  
    
## Tiempo lento para el primer byte (TTFB)  

**Síntomas**  

Una solicitud dedica mucho tiempo a esperar a recibir el primer byte del servidor.  

En la siguiente ilustración, la larga barra verde en la **cascada** indica que la solicitud estaba esperando mucho tiempo.  Esto se ha simulado usando un perfil para restringir la velocidad de la red y agregar un retraso.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Ejemplo de una serie en cola o detenida en el panel red" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Ejemplo de una solicitud con un tiempo lento para el primer byte  
:::image-end:::  

**Causas**  

*   La conexión entre el cliente y el servidor es lenta.  
*   El servidor tarda en responder.  Aloje el servidor de forma local para determinar si es la conexión o el servidor que es lento.  Si sigue demorando el primer byte \ (TTFB \) durante el acceso a un servidor local, entonces el servidor es lento.  
    
**Arreglos**  

*   Si la conexión es lenta, considere la posibilidad de hospedar el contenido en una red CDN o de cambiar los proveedores de hospedaje.  
*   Si el servidor es lento, considere la posibilidad de optimizar las consultas de la base de datos, implementar una caché o modificar la configuración del servidor.  
    
## Descarga de contenido lento  

**Síntomas**  

Una solicitud tarda mucho tiempo en descargarse.  

En la siguiente ilustración, la larga barra azul en la **cascada** que se encuentra junto al formato PNG significa que se ha tardado mucho tiempo en descargarlo.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Ejemplo de una serie en cola o detenida en el panel red" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Ejemplo de una solicitud que tarda mucho tiempo en descargarse  
:::image-end:::  

**Causas**  

*   La conexión entre el cliente y el servidor es lenta.  
*   Se está descargando una gran cantidad de contenido.  
    
**Arreglos**  

*   Considere la posibilidad de hospedar el contenido en una red CDN o de cambiar proveedores de hospedaje.  
*   Reenvíes menos bytes optimizando las solicitudes.  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspeccionar la actividad de la red en Microsoft Edge DevTools | Microsoft docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nuevo problema: MicrosoftDocs/Edge-Developer"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/issues) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Jonathan confuso][JonathanGarbee] \ (Google Developer Expert para tecnología web \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
