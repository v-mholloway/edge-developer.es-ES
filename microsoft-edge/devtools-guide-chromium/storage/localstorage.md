---
title: Ver y editar el almacenamiento local con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612014"
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



En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver, editar y eliminar [`localStorage`][MDNWindowsLocalStorage] pares clave-valor.  

## Ver las claves y los valores de localStorage   

1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** se muestra de forma predeterminada.  
    
    > ##### Figura 1  
    > El panel manifiesto  
    > ![El panel manifiesto][ImageManifest]  

1.  Expanda el menú **almacenamiento local** .  
    
    > ##### Figura 2  
    > El menú **almacenamiento local** muestra dos dominios: `https://business.bing.com` y `https://www.bing.com`  
    > ![El menú almacenamiento local][ImageLocalStorageMenu]  

1.  Seleccione un dominio para ver los pares de clave y valor.  
    
    > ##### Imagen 3  
    > `localStorage`Pares clave-valor para el `https://www.bing.com` dominio  
    > ![Pares de clave y valor de localStorage para el https://www.bing.com dominio][ImageLocalStorage]  

1.  Seleccione una fila de la tabla para ver el valor en el visor debajo de la tabla.  
    
    > ##### Imagen 4  
    > Ver el valor de la `eventLogQueue_Online` clave  
    > ![Visualización del valor de la tecla eventLogQueue_Online][ImageLocalStorageViewer]  

## Crear un nuevo `localStorage` par clave-valor   

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Haga doble clic en la parte vacía de la tabla.  DevTools crea una fila nueva y centra el cursor en la columna de **clave** .  
    
    > ##### Imagen 5  
    > La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor  
    > ![La parte vacía de la tabla para hacer doble clic para crear un nuevo par clave-valor][ImageLocalStorageCreate]  

## Modificar `localStorage` claves o valores   

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Haga doble clic en una celda de la columna **clave** o **valor** para editar esa clave o valor.  
    
    > ##### Imagen 6  
    > Editar una `localStorage` clave  
    > ![Editar una clave de localStorage][ImageLocalStorageEdit]  

## Eliminar `localStorage` pares clave-valor   

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  
1.  Seleccione el par de clave y valor que desea eliminar.  DevTools lo resalta azul para indicar que está seleccionado.  

1.  Presione la `Delete` tecla o haga clic en **eliminar** selección ![ eliminar seleccionados ][ImageDeleteIcon] .  

## Eliminar todos los `localStorage` pares clave-valor para un dominio   

1.  [Ver los `localStorage` pares clave-valor de un dominio](#view-localstorage-keys-and-values).  

1.  Seleccione **Borrar** todo ![ Borrar todo ][ImageClearIcon] .  

## Interactuar con `localStorage` desde la consola   

Dado que puede ejecutar JavaScript en la **consola**y que la **consola** tiene acceso a los contextos de JavaScript de la página, es posible interactuar con ella `localStorage` en la **consola**.  

1.  Use el menú **contextos de JavaScript** para cambiar el contexto de JavaScript de la **consola** si desea obtener acceso a los `localStorage` pares clave-valor de un dominio que no sea la página que se muestra.  
    
    > ##### Imagen 7  
    > Cambiar el contexto de JavaScript de la **consola**  
    > ![Cambiar el contexto de JavaScript de la consola][ImageJSContext]  

1.  Ejecuta tus `localStorage` expresiones en la consola, de la misma forma en que lo haces en tu JavaScript.  
    
    > ##### Imagen 8  
    > Interacción con `localStorage` desde la **consola**  
    > ![Interacción con localStorage desde la consola][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Ilustración 1: el panel manifiesto"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Ilustración 2: el menú almacenamiento local"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Ilustración 3: los pares de clave y valor de localStorage para el https://www.bing.com dominio"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Ilustración 4: ver el valor de la clave eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Ilustración 5: la parte vacía de la tabla para crear un nuevo par clave-valor"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Ilustración 6: edición de una clave de localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Ilustración 7: cambiar el contexto de JavaScript de la consola"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Ilustración 8: interacción con localStorage desde la consola"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

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
