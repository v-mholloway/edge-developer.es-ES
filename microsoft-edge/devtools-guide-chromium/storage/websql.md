---
title: Ver datos de web SQL con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 8b2e6d1a117e401f9e579cb28f81da9676eea979
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983481"
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
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       El panel **manifiesto**  
    :::image-end:::  
    
1.  Expanda la sección **SQL web** para ver bases de datos y tablas.  En la siguiente ilustración, debajo de **html5meetup** es una base de datos y **salas** es una tabla.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="El panel web SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       El panel **Web SQL**  
    :::image-end:::  
    
1.  Seleccione una tabla para ver los datos de esa tabla.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Ver los datos de una tabla de SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Ver los datos de una tabla de SQL Web  
    :::image-end:::  
    
## Editar datos de SQL Web   

No puede editar datos de web SQL al ver una tabla de SQL Web, como en la **figura 3** anterior.  Pero puede ejecutar instrucciones de la consola de web SQL que modifican o eliminan tablas.  Consulte [ejecutar consultas Web de SQL](#run-web-sql-queries).  

## Ejecutar consultas de web SQL   

1.  Seleccione una base de datos para abrir una consola para esa base de datos.  
1.  Escriba una instrucción SQL web y, después, presione `Enter` para ejecutarla.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Usar la consola de web SQL para eliminar una fila de una tabla" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Usar la consola de web SQL para eliminar una fila de una tabla  
    :::image-end:::  
    
## Actualizar una tabla de SQL Web   

DevTools no actualiza las tablas en tiempo real.  Para actualizar los datos de una tabla:  

1.  [Ver los datos de una tabla Web SQL](#view-web-sql-data).  
1.  Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).  
    
## Filtrar columnas en una tabla de SQL Web   

1.  [Ver los datos de una tabla Web SQL](#view-web-sql-data).  
1.  Use el cuadro de texto **columnas visibles** para especificar qué columnas desea mostrar.  Proporcione los nombres de columna como una lista CSV.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Usar el cuadro de texto columnas visibles para reducir el número de columnas que se muestran" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Usar el cuadro de texto **columnas visibles** para reducir el número de columnas que se muestran  
    :::image-end:::  
    
## Eliminar todos los datos de SQL Web   

1.  Abra el panel **Borrar almacenamiento** .  
1.  Asegúrese de que la casilla de verificación **Web SQL** está habilitada.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="La casilla de verificación Web SQL" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       La casilla de verificación **Web SQL**  
    :::image-end:::  
    
1.  Seleccione **Borrar datos del sitio**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Botón **Borrar datos del sitio**  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

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
