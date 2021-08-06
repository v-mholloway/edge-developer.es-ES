---
description: Cómo ver datos de caché desde el panel Aplicación de Microsoft Edge DevTools.
title: Ver datos de caché con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: ee4ae33b8cf287701e788b23b6a7fc52d52eac2ccefae29df71a871a41332480
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11805371"
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
# <a name="view-cache-data-with-microsoft-edge-devtools"></a>Ver datos de caché con Microsoft Edge DevTools  

En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] inspeccionar los datos [de][MDNCache] caché.  

Si está intentando inspeccionar los datos de [caché HTTP,][MDNHTTPCaching] esta no es la guía que desea.  Busque la información en la columna **Tamaño** del registro **de red**.  Vaya a [Registrar actividad de red][DevtoolsNetworkLogActivity].  

## <a name="view-cache-data"></a>Ver datos de caché  

1.  Elija la **pestaña** Aplicación para abrir **el** panel Aplicación.  El **panel Manifiesto** normalmente se abre de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       Panel **Manifiesto**  
    :::image-end:::  
    
1.  Expanda la **sección Storage** caché para ver las memorias caché disponibles.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Cachés disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       Cachés disponibles  
    :::image-end:::  
    
1.  Elija una memoria caché para ver el contenido.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Ver el contenido de una memoria caché" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Ver el contenido de una memoria caché  
    :::image-end:::  
    
1.  Elija un recurso para ver los encabezados HTTP en la sección debajo de la tabla.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Ver los encabezados HTTP de un recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Ver los encabezados HTTP de un recurso  
    :::image-end:::  
    
1.  Elija **Vista** previa para ver el contenido de un recurso.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Ver el contenido de un recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Ver el contenido de un recurso  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a>Actualizar un recurso  

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Elija el recurso que desea actualizar.  DevTools lo resalta para indicar que está seleccionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Elegir un recurso para actualizar" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Elegir un recurso para actualizar  
    :::image-end:::  
    
1.  Elija **Actualizar** \( ![ Actualizar ](../media/refresh-icon.msft.png) \).  
    
## <a name="filter-resources"></a>Filtrar recursos  

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Use el **cuadro de texto** Filtrar por ruta de acceso para filtrar los recursos que no coincidan con la ruta de acceso que proporcione.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que no coinciden con la ruta de acceso especificada" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtrar recursos que no coinciden con la ruta de acceso especificada  
    :::image-end:::  
    
## <a name="delete-a-resource"></a>Eliminar un recurso  

1.  [Ver los datos de una memoria caché](#view-cache-data).  
1.  Elija el recurso que desea eliminar.  DevTools lo resalta para indicar que está seleccionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Elegir un recurso para eliminar" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Elegir un recurso para eliminar  
    :::image-end:::  
    
1.  Elija **Eliminar seleccionado** \( Eliminar seleccionado ![ ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-cache-data"></a>Eliminar todos los datos de caché  

1.  Abra **Application**  >  **Clear Storage**.  
1.  Asegúrese de que la **casilla De Storage** caché está habilitada.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Casilla de verificación Storage caché" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Casilla **de verificación Storage** caché  
    :::image-end:::  
    
1.  Elija **Borrar datos del sitio**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Botón **Borrar datos del** sitio  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Herramientas para desarrolladores | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Registrar actividad de red | Microsoft Docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché HTTP | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/cache) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
