---
description: Cómo ver y editar localStorage con el panel almacenamiento local y la consola.
title: Ver y editar el almacenamiento local con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 25404e454187db941dc12d356dfe5ae7437d833b
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125422"
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

# Ver y editar el almacenamiento local con Microsoft Edge DevTools  

En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar [localStorage][MDNWindowsLocalStorage] pares clave-valor.  

## Ver las claves y los valores de localStorage  

1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** se muestra de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       El panel **manifiesto**  
    :::image-end:::  
    
1.  Expanda el menú **almacenamiento local** .  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-local-storage.msft.png":::
       El menú **almacenamiento local**  
    :::image-end:::  
    
1.  Seleccione un dominio para ver los pares de clave y valor.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       `localStorage`Pares clave-valor para el `https://www.bing.com` dominio  
    :::image-end:::  
    
1.  Seleccione una fila de la tabla para ver el valor en el visor debajo de la tabla.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Ver el valor de la `eventLogQueue_Online` clave  
    :::image-end:::  
    
## Crear un nuevo par clave-valor de localStorage  

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Haga doble clic en la parte vacía de la tabla.  DevTools crea una fila nueva y centra el cursor en la columna de **clave** .  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor  
    :::image-end:::  
    
## Editar claves o valores de localStorage  

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Haga doble clic en una celda de la columna **clave** o **valor** para editar esa clave o valor.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Modificar una `localStorage` tecla  
    :::image-end:::  
    
## Eliminar pares de clave y valor de localStorage  

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Seleccione el par de clave y valor que desea eliminar.  DevTools lo resalta azul para indicar que está seleccionado.  
1.  Presione la `Delete` tecla o elija **eliminar seleccionado** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).  
    
## Eliminar todos los `localStorage` pares clave-valor para un dominio  

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Elija **Borrar todo** \ ( ![ Borrar todo ][ImageClearIcon] \).  
    
## Interactuar con localStorage desde la consola  

Dado que puede ejecutar JavaScript en la **consola**y que la **consola** tiene acceso a los contextos de JavaScript de la página, es posible interactuar con ella `localStorage` en la **consola**.  

1.  Use el menú **contextos de JavaScript** para cambiar el contexto de JavaScript de la **consola** si desea obtener acceso a los `localStorage` pares clave-valor de un dominio que no sea la página que se muestra.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-console-local-storage.msft.png":::
       Cambiar el contexto de JavaScript de la consola  
    :::image-end:::  
    
1.  Ejecuta tus `localStorage` expresiones en la consola, de la misma forma en que lo haces en tu JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interactuar con `localStorage` desde la **consola**  
    :::image-end:::  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
