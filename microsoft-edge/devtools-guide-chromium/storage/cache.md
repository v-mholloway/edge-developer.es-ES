---
title: Ver datos de la caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7e7b4326204ce10732972c89b70c966e4bb665fb
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983880"
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

Si intenta inspeccionar los datos de [caché http][MDNHTTPCaching] , esta no es la guía que desea.  Busque la información en la columna **tamaño** del registro de **red**.  Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].  

## Ver datos de caché   

1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** generalmente se abre de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       El panel **manifiesto**  
    :::image-end:::  
    
1.  Expanda la sección **almacenamiento en caché** para ver las memorias caché disponibles.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Cachés disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       Cachés disponibles  
    :::image-end:::  
    
1.  Seleccione una caché para ver el contenido.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Ver el contenido de una caché" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Ver el contenido de una caché  
    :::image-end:::  
    
1.  Seleccione un recurso para ver los encabezados HTTP en la sección debajo de la tabla.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Ver los encabezados HTTP de un recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Ver los encabezados HTTP de un recurso  
    :::image-end:::  
    
1.  Seleccione **vista previa** para ver el contenido de un recurso.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Ver el contenido de un recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Ver el contenido de un recurso  
    :::image-end:::  
    
## Actualizar un recurso   

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Seleccione el recurso que desea actualizar.  DevTools lo resalta para indicar que está seleccionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Seleccionar un recurso" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Seleccionar un recurso  
    :::image-end:::  
    
1.  Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).  
    
## Filtrar recursos   

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Use el cuadro de texto **filtrar por ruta** para filtrar los recursos que no coincidan con la ruta de acceso que proporciona.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que no coincidan con la ruta de acceso especificada" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtrar recursos que no coincidan con la ruta de acceso especificada  
    :::image-end:::  
    
## Eliminar un recurso   

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Seleccione el recurso que desea eliminar.  DevTools lo resalta para indicar que está seleccionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Seleccionar un recurso" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Seleccionar un recurso  
    :::image-end:::  
    
1.  Seleccione **eliminar seleccionado** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).  
    
## Eliminar todos los datos de caché   

1.  **Application**  >  **Almacenamiento borrado**de aplicaciones abiertas.  
1.  Asegúrese de que la casilla **almacenamiento en caché** está habilitada.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Casilla de almacenamiento en caché" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Casilla de **almacenamiento en caché**  
    :::image-end:::  
    
1.  Seleccione **Borrar datos del sitio**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Botón **Borrar datos del sitio**  
    :::image-end:::  
    
<!--  
  


-->  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Registrar actividad de red | Microsoft docs"  

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
