---
description: Hospedar y publicar extensiones en la empresa para Microsoft Edge (Chromium).
title: Publicar y actualizar extensiones en el almacén de complementos de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327690"
---
# Publicar y actualizar extensiones en el almacén de complementos de Microsoft Edge  

La mayoría de las extensiones se publican en el almacén de complementos de [Microsoft Edge][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] para proteger a los usuarios de extensiones malintencionadas.  

## Opciones de publicación para extensiones  

Todas las extensiones se distribuyen a los usuarios como un archivo especial \( `.zip` \) con un `.crx` sufijo.  Las extensiones publicadas en el almacén de complementos de Microsoft Edge se cargan como `.zip` archivos.  El proceso de publicación convierte automáticamente el `.zip` archivo en un `.crx` archivo.  

Los dos escenarios siguientes no requieren que publiques la extensión en el almacén de complementos de Microsoft Edge.  

*   Extensiones distribuidas mediante la directiva enterprise.  
*   Usar directorios de extensión desempaquetar en un equipo local cuando Microsoft Edge está en modo de desarrollador.  

## Actualizaciones de extensiones

El explorador Microsoft Edge comprueba periódicamente si hay nuevas versiones de extensiones instaladas y actualiza cada una de ellas sin la intervención del usuario.  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensiones: complementos de Microsoft Edge Insider | Microsoft"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/extensions/hosting)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
