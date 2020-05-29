---
title: Ver datos de web SQL con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7a1e3e47f6761cfdb23488683107ed0df6a8f4e2
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612063"
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





# Ver datos de web SQL con Microsoft Edge DevTools   



> [!WARNING]
> La especificación de SQL Web [no se mantiene][W3CWebSQLStatus].  

En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de web SQL.  

## Ver datos de web SQL   

1.  Seleccione la pestaña **orígenes** para abrir el panel **fuentes** .  El panel **manifiesto** generalmente se abre de forma predeterminada.  
    
    > ##### Figura 1  
    > El panel manifiesto  
    > ![El panel manifiesto][ImageManifestPane]  
    
1.  Expanda la sección **SQL web** para ver bases de datos y tablas.  En la [ilustración 2](#figure-2) , debajo de **html5meetup** hay una base de datos y **salas** es una tabla.  
    
    > ##### Figura 2  
    > El panel web SQL  
    > ![El panel web SQL][ImageWebSQLPane]  

1.  Seleccione una tabla para ver los datos de esa tabla.  
    
    > ##### Imagen 3  
    > Visualización de los datos de la tabla SQL Web **Rooms**  
    > ![Ver los datos de una tabla de SQL Web][ImageWebSQLTable]  

## Editar datos de SQL Web   

No puede editar datos de web SQL al ver una tabla de SQL Web, como en la **figura 3** anterior.  Pero puede ejecutar instrucciones de la consola de web SQL que modifican o eliminan tablas.  Consulte [ejecutar consultas Web de SQL](#run-web-sql-queries).  

## Ejecutar consultas de web SQL   

1.  Seleccione una base de datos para abrir una consola para esa base de datos.  

1.  Escriba una instrucción SQL web y, después, presione `Enter` para ejecutarla.  
    
    > ##### Imagen 4  
    > Usar la consola SQL de web para eliminar una fila de la tabla **salas**  
    > ![Usar la consola SQL de web para eliminar una fila de una tabla][ImageWebSQLEdit]  

## Actualizar una tabla de SQL Web   

DevTools no actualiza las tablas en tiempo real.  Para actualizar los datos de una tabla:  

1.  [Ver los datos de una tabla Web SQL](#view-web-sql-data).  
1.  Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .  

## Filtrar columnas en una tabla de SQL Web   

1.  [Ver los datos de una tabla Web SQL](#view-web-sql-data).  
1.  Use el cuadro de texto **columnas visibles** para especificar qué columnas desea mostrar.  Proporcione los nombres de columna como una lista CSV.  
    
    > ##### Imagen 5  
    > Usar el cuadro de texto **columnas visibles** para mostrar solo `room_name` las `last_updated` columnas y  
    > ![Usar el cuadro de texto columnas visibles para reducir el número de columnas que se muestran][ImageWebSQLFilter]  

## Eliminar todos los datos de SQL Web   

1.  Abra el panel **Borrar almacenamiento** .  
1.  Asegúrese de que la casilla de verificación **Web SQL** está habilitada.  
    
    > ##### Imagen 6  
    > La casilla de verificación **Web SQL**  
    > ![La casilla de verificación Web SQL][ImageWebSQLCheckbox]  

1.  Seleccione **Borrar datos del sitio**.  
    
    > ##### Imagen 7  
    > Botón **Borrar datos del sitio**  
    > ![Botón Borrar datos del sitio][ImageClearWebSQL]  

 



<!-- image links -->  

[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Ilustración 1: el panel manifiesto"  
[ImageWebSQLPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql.msft.png "Ilustración 2: el panel web SQL"  
[ImageWebSQLTable]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png "Ilustración 3: visualización de los datos de una tabla SQL Web"  
[ImageWebSQLEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-commands.msft.png "Ilustración 4: usar la consola SQL de web para eliminar una fila de una tabla"  
[ImageWebSQLFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png "Ilustración 5: usar el cuadro de texto columnas visibles para reducir el número de columnas que se muestran"  
[ImageWebSQLCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-web-sql.msft.png "Ilustración 6: la casilla de verificación Web SQL"  
[ImageClearWebSQL]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-clear-site-data-button.msft.png "Ilustración 7: botón Borrar datos del sitio"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de datos Web SQL | RELATIVA"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/websql) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
