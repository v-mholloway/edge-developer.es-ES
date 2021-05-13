---
description: Cómo ver y editar localStorage con el panel Storage local y la consola.
title: Ver y editar archivos Storage con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5088a1b9d7ab2b92051d099e76b8b07bbd5db5f8
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565053"
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
# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a>Ver y editar el almacenamiento local con Microsoft Edge DevTools  

En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] ver, editar y eliminar pares [clave-valor localStorage.][MDNWindowsLocalStorage]  

## <a name="view-localstorage-keys-and-values"></a>Ver claves y valores de localStorage  

1.  Elija la **pestaña** Aplicación para abrir la **herramienta** Aplicación.  El **panel** Manifiesto se muestra de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       Panel **Manifiesto**  
    :::image-end:::  
    
1.  Expanda el **menú Storage** local.  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="El menú Storage local" lightbox="../media/storage-application-local-storage.msft.png":::
       El **menú Storage** local  
    :::image-end:::  
    
1.  Elija un dominio para ver los pares clave-valor.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Los pares clave-valor localStorage para el https://www.bing.com dominio" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       Pares `localStorage` clave-valor para el `https://www.bing.com` dominio  
    :::image-end:::  
    
1.  Elija una fila de la tabla para ver el valor en el visor debajo de la tabla.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Ver el valor de la eventLogQueue_Online clave" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Ver el valor de la `eventLogQueue_Online` clave  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a>Crear un nuevo par clave-valor localStorage  

1.  [Ver los pares clave-valor localStorage de un dominio](#view-localstorage-keys-and-values).  
1.  Haga doble clic en la parte vacía de la tabla.  DevTools crea una nueva fila y centra el cursor en la **columna** Clave.  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a>Editar claves o valores de localStorage  

1.  [Ver los pares clave-valor localStorage de un dominio](#view-localstorage-keys-and-values).  
1.  Haga doble clic en una celda de la **columna Clave** **o** Valor para editar esa clave o valor.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Editar una clave localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Editar una `localStorage` clave  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a>Eliminar pares clave-valor localStorage  

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Elija el par clave-valor que desea eliminar.  DevTools lo resalta en azul para indicar que está seleccionado.  
1.  Seleccione la `Delete` clave o elija Eliminar **seleccionado** \( Eliminar ![ seleccionado ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a>Eliminar todos `localStorage` los pares clave-valor de un dominio  

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Elija **Borrar todo** \( Borrar todo ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-localstorage-from-the-console"></a>Interactuar con localStorage desde la consola  

Dado que puede ejecutar JavaScript en la **** consola **y**dado que la consola tiene acceso a los contextos de JavaScript de la página, es posible interactuar con desde `localStorage` la **consola**.  

1.  Use el **menú contextos de JavaScript** para **** cambiar el contexto de JavaScript de la consola si desea tener acceso a los pares clave-valor de un dominio distinto de la página `localStorage` que se muestra.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Cambiar el contexto de JavaScript de la consola" lightbox="../media/storage-console-local-storage.msft.png":::
       Cambiar el contexto de JavaScript de la consola  
    :::image-end:::  
    
1.  Ejecute las `localStorage` expresiones en la consola, lo mismo que en JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interactuar con localStorage desde la consola" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interactuar con `localStorage` desde la **consola**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Herramientas para desarrolladores | Microsoft Docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
