---
description: Cómo ver los datos de web SQL desde el panel de aplicaciones de Microsoft Edge DevTools.
title: Ver datos de web SQL con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: cc2f726c80fbf0c943b43ff6c131e9479db75b78
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993537"
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





# <span data-ttu-id="717c6-104">Ver datos de web SQL con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="717c6-104">View Web SQL data with Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="717c6-105">La especificación de SQL Web [no se mantiene][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="717c6-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="717c6-106">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de web SQL.</span><span class="sxs-lookup"><span data-stu-id="717c6-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="717c6-107">Ver datos de web SQL</span><span class="sxs-lookup"><span data-stu-id="717c6-107">View Web SQL Data</span></span>   

1.  <span data-ttu-id="717c6-108">Seleccione la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="717c6-108">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="717c6-109">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="717c6-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="717c6-111">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="717c6-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="717c6-112">Expanda la sección **SQL web** para ver bases de datos y tablas.</span><span class="sxs-lookup"><span data-stu-id="717c6-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="717c6-113">En la siguiente ilustración, debajo de **html5meetup** es una base de datos y **salas** es una tabla.</span><span class="sxs-lookup"><span data-stu-id="717c6-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="El panel web SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="717c6-115">El panel **Web SQL**</span><span class="sxs-lookup"><span data-stu-id="717c6-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="717c6-116">Seleccione una tabla para ver los datos de esa tabla.</span><span class="sxs-lookup"><span data-stu-id="717c6-116">Select a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Ver los datos de una tabla de SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="717c6-118">Ver los datos de una tabla de SQL Web</span><span class="sxs-lookup"><span data-stu-id="717c6-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="717c6-119">Editar datos de SQL Web</span><span class="sxs-lookup"><span data-stu-id="717c6-119">Edit Web SQL data</span></span>   

<span data-ttu-id="717c6-120">No puede editar datos de web SQL al ver una tabla de SQL Web, como en la **figura 3** anterior.</span><span class="sxs-lookup"><span data-stu-id="717c6-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="717c6-121">Pero puede ejecutar instrucciones de la consola de web SQL que modifican o eliminan tablas.</span><span class="sxs-lookup"><span data-stu-id="717c6-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="717c6-122">Consulte [ejecutar consultas Web de SQL](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="717c6-122">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="717c6-123">Ejecutar consultas de web SQL</span><span class="sxs-lookup"><span data-stu-id="717c6-123">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="717c6-124">Seleccione una base de datos para abrir una consola para esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="717c6-124">Select a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="717c6-125">Escriba una instrucción SQL web y, después, presione `Enter` para ejecutarla.</span><span class="sxs-lookup"><span data-stu-id="717c6-125">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Usar la consola de web SQL para eliminar una fila de una tabla" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="717c6-127">Usar la consola de web SQL para eliminar una fila de una tabla</span><span class="sxs-lookup"><span data-stu-id="717c6-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="717c6-128">Actualizar una tabla de SQL Web</span><span class="sxs-lookup"><span data-stu-id="717c6-128">Refresh a Web SQL table</span></span>   

<span data-ttu-id="717c6-129">DevTools no actualiza las tablas en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="717c6-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="717c6-130">Para actualizar los datos de una tabla:</span><span class="sxs-lookup"><span data-stu-id="717c6-130">To update the data in a table:</span></span>  

1.  <span data-ttu-id="717c6-131">[Ver los datos de una tabla Web SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="717c6-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="717c6-132">Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="717c6-132">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="717c6-133">Filtrar columnas en una tabla de SQL Web</span><span class="sxs-lookup"><span data-stu-id="717c6-133">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="717c6-134">[Ver los datos de una tabla Web SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="717c6-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="717c6-135">Use el cuadro de texto **columnas visibles** para especificar qué columnas desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="717c6-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="717c6-136">Proporcione los nombres de columna como una lista CSV.</span><span class="sxs-lookup"><span data-stu-id="717c6-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Usar el cuadro de texto columnas visibles para reducir el número de columnas que se muestran" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="717c6-138">Usar el cuadro de texto **columnas visibles** para reducir el número de columnas que se muestran</span><span class="sxs-lookup"><span data-stu-id="717c6-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="717c6-139">Eliminar todos los datos de SQL Web</span><span class="sxs-lookup"><span data-stu-id="717c6-139">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="717c6-140">Abra el panel **Borrar almacenamiento** .</span><span class="sxs-lookup"><span data-stu-id="717c6-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="717c6-141">Asegúrese de que la casilla de verificación **Web SQL** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="717c6-141">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="La casilla de verificación Web SQL" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="717c6-143">La casilla de verificación **Web SQL**</span><span class="sxs-lookup"><span data-stu-id="717c6-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="717c6-144">Seleccione **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="717c6-144">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="717c6-146">Botón **Borrar datos del sitio**</span><span class="sxs-lookup"><span data-stu-id="717c6-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de datos Web SQL | RELATIVA"  

> [!NOTE]
> <span data-ttu-id="717c6-149">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="717c6-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="717c6-150">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/websql) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="717c6-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="717c6-152">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="717c6-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
