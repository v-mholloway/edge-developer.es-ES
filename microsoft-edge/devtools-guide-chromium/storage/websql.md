---
description: Cómo ver datos de SQL web desde el panel Aplicación de Microsoft Edge DevTools.
title: Ver datos SQL web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 0d75dbf5c7ae684e07b28f625636e89b6385f293bbff1ff0fb297beb34ef86e8
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11809624"
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
# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a>Ver datos SQL web con Microsoft Edge DevTools  

> [!WARNING]
> La especificación SQL web no [se está conservando.][W3CWebSQLStatus]  

En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] inspeccionar los datos SQL web.  

## <a name="view-web-sql-data"></a>Ver datos SQL web  

1.  Elija la **herramienta Orígenes** para abrir la **herramienta Orígenes.**  El **panel Manifiesto** normalmente se abre de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       Panel **Manifiesto**  
    :::image-end:::  
    
1.  Expanda la **sección Web SQL** para ver bases de datos y tablas.  En la siguiente figura, debajo **de html5meetup** hay una base de datos y **salas** es una tabla.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Panel web SQL web" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       Panel **web SQL** web  
    :::image-end:::  
    
1.  Elija una tabla para ver los datos de esa tabla.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Ver los datos de una tabla SQL web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Ver los datos de una tabla SQL web  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a>Editar datos SQL web  

No puede editar los datos de SQL web al ver una tabla de SQL web, como en la anterior.  Pero puede ejecutar instrucciones desde la consola web SQL que editan o eliminan tablas.  Vaya a [Ejecutar consultas SQL web](#run-web-sql-queries).  

## <a name="run-web-sql-queries"></a>Ejecutar consultas SQL web  

1.  Elija una base de datos para abrir una consola para esa base de datos.  
1.  Escriba una instrucción Web SQL y, a continuación, `Enter` seleccione para ejecutarla.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Usar la Consola SQL web para eliminar una fila de una tabla" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Usar la Consola SQL web para eliminar una fila de una tabla  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a>Actualizar una tabla de SQL web  

DevTools no actualiza tablas en tiempo real.  Para actualizar los datos de una tabla, complete las siguientes acciones.  

1.  [Ver los datos en una tabla web SQL .](#view-web-sql-data)  
1.  Elija **Actualizar** \( ![ Actualizar ](../media/refresh-icon.msft.png) \).  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a>Filtrar las columnas de una tabla de SQL web  

1.  [Ver los datos en una tabla web SQL .](#view-web-sql-data)  
1.  Use el cuadro de texto Columnas **visibles** para especificar qué columnas desea mostrar.  Proporcione los nombres de columna como una lista CSV.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Usar el cuadro de texto Columnas visibles para reducir el número de columnas mostradas" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Usar el **cuadro de texto Columnas** visibles para reducir el número de columnas mostradas  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a>Eliminar todos los datos SQL web  

1.  Abra el **panel Borrar Storage.**  
1.  Asegúrese de que la **casilla web SQL** esté activada.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="La casilla SQL web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       La **casilla SQL** web  
    :::image-end:::  
    
1.  Elija **Borrar datos del sitio**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Botón **Borrar datos del** sitio  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de SQL web | W3C"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/websql) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
