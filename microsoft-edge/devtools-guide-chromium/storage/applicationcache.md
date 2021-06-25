---
description: Cómo ver los datos de caché de aplicaciones desde el panel Aplicación de Microsoft Edge DevTools.
title: Ver datos de caché de aplicaciones Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 71e71555940d74f2071178be2e6daf0ec2f49dfd
ms.sourcegitcommit: d0a6959c5338cf1927093b4a9ed29a0bc0390b43
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "11615424"
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
# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a>Ver datos de caché de aplicaciones con Microsoft Edge DevTools  

> [!WARNING]
> La caché de aplicaciones está en desuso y debe evitar usarlo.  La API de caché de aplicaciones se está quitando de la plataforma web.  Para obtener más información, vaya [a Preparar la eliminación de AppCache][WebDevAppcacheRemoval].

En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] inspeccionar los [recursos de caché de][MDNWebAPIsWindowApplicationCache] aplicaciones.  

## <a name="view-application-cache-data"></a>Ver datos de caché de aplicaciones  

1.  En la parte superior de DevTools, elija la **herramienta** Aplicación.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       Panel **Manifiesto**  
    :::image-end:::  

1.  Expanda la **sección Caché de** aplicaciones y elija una caché para ver los recursos.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Panel Caché de aplicaciones" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       Panel **Caché de** aplicaciones  
    :::image-end:::  

Cada fila de la tabla representa un recurso almacenado en caché.  

La **columna** Tipo representa la [categoría del recurso][MDNHTMLResourcesInAnApplicationCache].  

| Categoría | Detalles |  
|:--- |:--- |  
| `Explicit` | Este recurso se enumeró explícitamente en el manifiesto. |  
| `Fallback` | La dirección URL es una reserva para otro recurso.  La dirección URL del otro recurso no se muestra en DevTools. |  
| `Master` | El `manifest` atributo del recurso indica que la memoria caché es el elemento primario del recurso. |  
| `Network` | El manifiesto especifica que el recurso debe venir de la red. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

En la parte inferior de la tabla hay iconos de estado que indican la conexión de red y el estado de la caché **de aplicaciones**.  La **caché de aplicaciones** puede tener los siguientes estados.  

| Estado | Detalles |  
|:--- |:--- |  
| `CHECKING` | El manifiesto se está recuperando y buscando actualizaciones. |  
| `DOWNLOADING` | Los recursos se agregan a la memoria caché. |  
| `IDLE` | La memoria caché no tiene nuevos cambios. |  
| `OBSOLETE` | Se está eliminando la memoria caché. |  
| `UPDATEREADY` |  Hay disponible una nueva versión de la memoria caché. |  

<!-- links -->  
[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
<!-- external links: -->
[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos en una memoria caché de aplicaciones | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache: API web | MDN"  

[WebDevAppcacheRemoval]: https://web.dev/appcache-removal "Preparación para la eliminación de AppCache | web.dev"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
