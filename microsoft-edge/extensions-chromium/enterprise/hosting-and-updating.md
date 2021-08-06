---
description: Hospedar y publicar extensiones en la empresa para Microsoft Edge (Chromium).
title: Publicar y actualizar extensiones en el Microsoft Edge complementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 7deadd3ff21bc06574f1e6006e60af01f16ce55a0375f27a453cf998b3818c72
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803317"
---
# <a name="publish-and-update-extensions-in-the-microsoft-edge-add-ons-store"></a>Publicar y actualizar extensiones en el Microsoft Edge complementos  

La mayoría de las extensiones se publican en [el Microsoft Edge complementos][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] para proteger a los usuarios de extensiones malintencionadas.  

## <a name="publish-options-for-extensions"></a>Opciones de publicación para extensiones  

Todas las extensiones se distribuyen a los usuarios como un archivo especial \( `.zip` \) con un `.crx` sufijo.  Las extensiones publicadas en el Microsoft Edge complementos se cargan como `.zip` archivos.  El proceso de publicación convierte automáticamente el `.zip` archivo en un `.crx` archivo.  

Los dos escenarios siguientes no requieren que publiques la extensión en el Microsoft Edge complementos.  

*   Extensiones distribuidas mediante Enterprise directiva.  
*   Usar directorios de extensión desempaquetar en un equipo local Microsoft Edge está en modo de desarrollador.  

## <a name="updates-to-extensions"></a>Actualizaciones de extensiones

El Microsoft Edge busca automáticamente nuevas versiones de extensiones instaladas. Las actualizaciones se instalan sin intervención del usuario.  


<!-- image links -->

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensiones: Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/extensions/hosting)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
