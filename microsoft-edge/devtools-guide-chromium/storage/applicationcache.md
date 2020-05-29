---
title: Ver datos de la caché de aplicaciones con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6ce3087e9c719efbcf4d9ebceb860edd0ed0c3b6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612098"
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





# Ver datos de la caché de aplicaciones con Microsoft Edge DevTools   



> [!WARNING]
> La API de la caché de aplicaciones se está [quitando de la plataforma web][HTMLStandardOfflineWebApplications].  

En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los recursos de caché de la [aplicación][MDNWebAPIsWindowApplicationCache] .  

## Ver datos de la caché de aplicaciones   

1.  Seleccione la pestaña **orígenes** para abrir el panel **fuentes** .  El panel **manifiesto** generalmente se abre de forma predeterminada.  
    
    > ##### Figura 1  
    > El panel manifiesto  
    > ![El panel manifiesto][ImageManifestPane]  

1.  Expanda la sección caché de la **aplicación** y haga clic en una caché para ver los recursos.  
    
    > ##### Figura 2  
    > Panel de caché de aplicaciones  
    > ![Panel de caché de aplicaciones][ImageApplicationCachePane]  

Cada fila de la tabla representa un recurso almacenado en la memoria caché.  

La columna **tipo** representa la [categoría del recurso][MDNHTMLResourcesInAnApplicationCache].  

| Categoría | Detalles |  
|:--- |:--- |  
| `Explicit` | Este recurso se mostraba explícitamente en el manifiesto. |  
| `Fallback` | La dirección URL es una reserva de otro recurso.  La dirección URL del otro recurso no se enumera en DevTools. |  
| `Master` | El `manifest` atributo del recurso indicó que esta caché es el elemento primario del recurso. |  
| `Network` | El manifiesto especificó que este recurso debe proceder de la red. |  

En la parte inferior de la tabla hay iconos de estado que indican su conexión de red y el estado de la memoria caché de la aplicación.  La caché de la aplicación puede tener los siguientes Estados.  

| Estado | Detalles |  
|:--- |:--- |  
| `CHECKING` | El manifiesto se está buscando y comprobando para obtener actualizaciones. |  
| `DOWNLOADING` | Los recursos se están agregando a la memoria caché. |  
| `IDLE` | La caché no tiene cambios nuevos. |  
| `OBSOLETE` | Se está eliminando la memoria caché. |  
| `UPDATEREADY` |  Hay una nueva versión de la caché disponible. |  

<!--   -->  



<!-- image links -->  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Ilustración 1: el panel manifiesto"  
[ImageApplicationCachePane]: /microsoft-edge/devtools-guide-chromium/media/storage-cache-pane-cache-storage-resources.msft.png "Ilustración 2: el panel de caché de la aplicación"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicaciones web sin conexión: estándar HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos en una caché de aplicaciones | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-API Web | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
