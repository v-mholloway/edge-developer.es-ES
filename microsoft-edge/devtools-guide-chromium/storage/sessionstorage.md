---
title: Ver y editar el almacenamiento de sesión con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d0631f69a082a2a73c51e4359c21cf94636d665e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983593"
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





# Ver y editar el almacenamiento de sesión con Microsoft Edge DevTools   

  

En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar [`sessionStorage`][MDNSessionStorage] pares clave-valor.  

## Ver las claves y los valores de sessionStorage   

1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** se muestra de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       El panel **manifiesto**  
    :::image-end:::  
    
1.  Expanda el menú almacenamiento de la **sesión** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="El menú de almacenamiento de sesión" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       El menú de **almacenamiento de sesión**  
    :::image-end:::  
    
1.  Seleccione un dominio para ver los pares de clave y valor.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Pares clave-valor ' sessionStorage '" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       `sessionStorage`Pares de clave y valor  
    :::image-end:::  
    
1.  Seleccione una fila de la tabla para ver el valor en el visor debajo de la tabla.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Ver el valor de la clave x-SID" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Ver el valor de la `x-sid` clave  
    :::image-end:::  
    
## Crear un nuevo par clave-valor de sessionStorage   

1.  [Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).  
1.  Haga doble clic en la parte vacía de la tabla.  DevTools crea una fila nueva y centra el cursor en la columna de **clave** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor  
    :::image-end:::  
    
## Editar claves o valores de sessionStorage   

1.  [Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).  
1.  Haga doble clic en una celda de la columna **clave** o **valor** para editar esa clave o valor.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Editar una clave de sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Modificar una `sessionStorage` tecla  
    :::image-end:::  
    
## Eliminar pares de clave y valor de sessionStorage   

1.  [Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).  
1.  Seleccione el par de clave y valor que desea eliminar.  DevTools lo resalta azul para indicar que está seleccionado.  
1.  Presione la `Delete` tecla o haga clic en **eliminar seleccionada** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).  
    
## Eliminar todas las parejas de clave y valor de sessionStorage para un dominio   

1.  [Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).  
1.  Seleccione **Borrar todo** \ ( ![ Borrar todo ][ImageClearIcon] \).  
    
## Interactuar con sessionStorage desde la consola   

Dado que puede ejecutar JavaScript en la **consola**y que la **consola** tiene acceso a los contextos de JavaScript de la página, es posible interactuar con él `sessionStorage` en la **consola**.  

1.  Use el menú **contextos de JavaScript** para cambiar el contexto de JavaScript de la **consola** si desea acceder a los `sessionStorage` pares clave-valor de un dominio que no sea la página en la que se encuentre.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Cambiar el contexto de JavaScript de la consola" lightbox="../media/storage-console-domain-selection.msft.png":::
       Cambiar el contexto de JavaScript de la consola  
    :::image-end:::  
    
1.  Ejecuta tus `sessionStorage` expresiones en la consola, de la misma manera en que lo harías en tu código JavaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interactuar con sessionStorage desde la consola" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interactuar con `sessionStorage` desde la **consola**  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
