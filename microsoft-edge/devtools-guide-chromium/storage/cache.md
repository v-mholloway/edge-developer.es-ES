---
title: Ver datos de la caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612077"
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





# Ver datos de la caché con Microsoft Edge DevTools   



En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de [caché][MDNCache] .  

Si intenta inspeccionar los datos de [caché http][MDNHTTPCaching] , esta no es la guía que desea.  
Busque la información en la columna **tamaño** del registro de **red**.  Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].  

## Ver datos de caché   

1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** generalmente se abre de forma predeterminada.  
    
    > ##### Figura 1  
    > El panel manifiesto  
    > ![El panel manifiesto][ImageManifestPane]  

1.  Expanda la sección **almacenamiento en caché** para ver las memorias caché disponibles.  
    
    > ##### Figura 2  
    > Cachés disponibles  
    > ![Cachés disponibles][ImageCache]  

1.  Seleccione una caché para ver el contenido.  
    
    > ##### Imagen 3  
    > Ver el contenido de una caché  
    > ![Ver el contenido de una caché][ImageCacheView]  

1.  Seleccione un recurso para ver los encabezados HTTP en la sección debajo de la tabla.  
    
    > ##### Imagen 4  
    > Visualización de los encabezados HTTP de un recurso  
    > ![Visualización de los encabezados HTTP de un recurso][ImageViewCacheResource]  

1.  Seleccione **vista previa** para ver el contenido de un recurso.  
    
    > ##### Imagen 5  
    > Ver el contenido de un recurso  
    > ![Ver el contenido de un recurso][ImageCacheContent]  

## Actualizar un recurso   

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Seleccione el recurso que desea actualizar.  DevTools lo resalta para indicar que está seleccionado.  
    
    > ##### Imagen 6  
    > Selección de un recurso  
    > ![Selección de un recurso][ImageCacheSelected]  

1.  Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .  

## Filtrar recursos   

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Use el cuadro de texto **filtrar por ruta** para filtrar los recursos que no coincidan con la ruta de acceso que proporciona.  
    
    > ##### Imagen 7  
    > Filtrar recursos que no coincidan con la ruta especificada  
    > ![Filtrar recursos que no coincidan con la ruta especificada][ImageCacheFilter]  

## Eliminar un recurso   

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Seleccione el recurso que desea eliminar.  DevTools lo resalta para indicar que está seleccionado.  
    
    > ##### Imagen 8  
    > Selección de un recurso  
    > ![Selección de un recurso][ImageCacheSelected2]  

1.  Seleccione **eliminar** selección ![ eliminar seleccionados ][ImageDeleteIcon] .  

## Eliminar todos los datos de caché   

1.  **Application**  >  **Almacenamiento borrado**de aplicaciones abiertas.  
1.  Asegúrese de que la casilla **almacenamiento en caché** está habilitada.  
    
    > ##### Imagen 9  
    > Casilla de **almacenamiento en caché**  
    > ![Casilla de almacenamiento en caché][ImageCacheCheckbox]  

1.  Seleccione **Borrar datos del sitio**.  
    
    > ##### Imagen 10  
    > Botón **Borrar datos del sitio**  
    > ![Botón Borrar datos del sitio][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Ilustración 1: el panel manifiesto"  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Ilustración 2: memorias caché disponibles"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Ilustración 3: visualización del contenido de una caché"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Ilustración 4: visualización de los encabezados HTTP de un recurso"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Ilustración 5: visualización del contenido de un recurso"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Ilustración 6: selección de un recurso"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Ilustración 7: filtrar recursos que no coinciden con la ruta de acceso especificada"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Ilustración 8: selección de un recurso"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Ilustración 9: la casilla de almacenamiento en caché"  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Ilustración 10: botón Borrar datos del sitio"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Registrar actividad de la red"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché de HTTP | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cache) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
