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





# <span data-ttu-id="8c62d-103">Ver datos de web SQL con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8c62d-103">View Web SQL Data With Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="8c62d-104">La especificación de SQL Web [no se mantiene][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="8c62d-104">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="8c62d-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos de web SQL.</span><span class="sxs-lookup"><span data-stu-id="8c62d-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="8c62d-106">Ver datos de web SQL</span><span class="sxs-lookup"><span data-stu-id="8c62d-106">View Web SQL Data</span></span>   

1.  <span data-ttu-id="8c62d-107">Seleccione la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="8c62d-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="8c62d-108">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8c62d-108">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="8c62d-109">Figura 1</span><span class="sxs-lookup"><span data-stu-id="8c62d-109">Figure 1</span></span>  
    > <span data-ttu-id="8c62d-110">El panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="8c62d-110">The Manifest pane</span></span>  
    > ![El panel manifiesto][ImageManifestPane]  
    
1.  <span data-ttu-id="8c62d-112">Expanda la sección **SQL web** para ver bases de datos y tablas.</span><span class="sxs-lookup"><span data-stu-id="8c62d-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="8c62d-113">En la [ilustración 2](#figure-2) , debajo de **html5meetup** hay una base de datos y **salas** es una tabla.</span><span class="sxs-lookup"><span data-stu-id="8c62d-113">In [Figure 2](#figure-2) below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    > ##### <span data-ttu-id="8c62d-114">Figura 2</span><span class="sxs-lookup"><span data-stu-id="8c62d-114">Figure 2</span></span>  
    > <span data-ttu-id="8c62d-115">El panel web SQL</span><span class="sxs-lookup"><span data-stu-id="8c62d-115">The Web SQL pane</span></span>  
    > ![El panel web SQL][ImageWebSQLPane]  

1.  <span data-ttu-id="8c62d-117">Seleccione una tabla para ver los datos de esa tabla.</span><span class="sxs-lookup"><span data-stu-id="8c62d-117">Select a table to view the data for that table.</span></span>  
    
    > ##### <span data-ttu-id="8c62d-118">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="8c62d-118">Figure 3</span></span>  
    > <span data-ttu-id="8c62d-119">Visualización de los datos de la tabla SQL Web **Rooms**</span><span class="sxs-lookup"><span data-stu-id="8c62d-119">Viewing the data of the **rooms** Web SQL table</span></span>  
    > ![Ver los datos de una tabla de SQL Web][ImageWebSQLTable]  

## <span data-ttu-id="8c62d-121">Editar datos de SQL Web</span><span class="sxs-lookup"><span data-stu-id="8c62d-121">Edit Web SQL data</span></span>   

<span data-ttu-id="8c62d-122">No puede editar datos de web SQL al ver una tabla de SQL Web, como en la **figura 3** anterior.</span><span class="sxs-lookup"><span data-stu-id="8c62d-122">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="8c62d-123">Pero puede ejecutar instrucciones de la consola de web SQL que modifican o eliminan tablas.</span><span class="sxs-lookup"><span data-stu-id="8c62d-123">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="8c62d-124">Consulte [ejecutar consultas Web de SQL](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="8c62d-124">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="8c62d-125">Ejecutar consultas de web SQL</span><span class="sxs-lookup"><span data-stu-id="8c62d-125">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="8c62d-126">Seleccione una base de datos para abrir una consola para esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="8c62d-126">Select a database to open a console for that database.</span></span>  

1.  <span data-ttu-id="8c62d-127">Escriba una instrucción SQL web y, después, presione `Enter` para ejecutarla.</span><span class="sxs-lookup"><span data-stu-id="8c62d-127">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    > ##### <span data-ttu-id="8c62d-128">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="8c62d-128">Figure 4</span></span>  
    > <span data-ttu-id="8c62d-129">Usar la consola SQL de web para eliminar una fila de la tabla **salas**</span><span class="sxs-lookup"><span data-stu-id="8c62d-129">Using the Web SQL Console to delete a row from the **rooms** table</span></span>  
    > ![Usar la consola SQL de web para eliminar una fila de una tabla][ImageWebSQLEdit]  

## <span data-ttu-id="8c62d-131">Actualizar una tabla de SQL Web</span><span class="sxs-lookup"><span data-stu-id="8c62d-131">Refresh a Web SQL table</span></span>   

<span data-ttu-id="8c62d-132">DevTools no actualiza las tablas en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="8c62d-132">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="8c62d-133">Para actualizar los datos de una tabla:</span><span class="sxs-lookup"><span data-stu-id="8c62d-133">To update the data in a table:</span></span>  

1.  <span data-ttu-id="8c62d-134">[Ver los datos de una tabla Web SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="8c62d-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="8c62d-135">Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="8c62d-135">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="8c62d-136">Filtrar columnas en una tabla de SQL Web</span><span class="sxs-lookup"><span data-stu-id="8c62d-136">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="8c62d-137">[Ver los datos de una tabla Web SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="8c62d-137">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="8c62d-138">Use el cuadro de texto **columnas visibles** para especificar qué columnas desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="8c62d-138">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="8c62d-139">Proporcione los nombres de columna como una lista CSV.</span><span class="sxs-lookup"><span data-stu-id="8c62d-139">Provide the column names as a CSV list.</span></span>  
    
    > ##### <span data-ttu-id="8c62d-140">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="8c62d-140">Figure 5</span></span>  
    > <span data-ttu-id="8c62d-141">Usar el cuadro de texto **columnas visibles** para mostrar solo `room_name` las `last_updated` columnas y</span><span class="sxs-lookup"><span data-stu-id="8c62d-141">Using the **Visible Columns** text box to only show the `room_name` and `last_updated` columns</span></span>  
    > ![Usar el cuadro de texto columnas visibles para reducir el número de columnas que se muestran][ImageWebSQLFilter]  

## <span data-ttu-id="8c62d-143">Eliminar todos los datos de SQL Web</span><span class="sxs-lookup"><span data-stu-id="8c62d-143">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="8c62d-144">Abra el panel **Borrar almacenamiento** .</span><span class="sxs-lookup"><span data-stu-id="8c62d-144">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="8c62d-145">Asegúrese de que la casilla de verificación **Web SQL** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8c62d-145">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="8c62d-146">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="8c62d-146">Figure 6</span></span>  
    > <span data-ttu-id="8c62d-147">La casilla de verificación **Web SQL**</span><span class="sxs-lookup"><span data-stu-id="8c62d-147">The **Web SQL** checkbox</span></span>  
    > ![La casilla de verificación Web SQL][ImageWebSQLCheckbox]  

1.  <span data-ttu-id="8c62d-149">Seleccione **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="8c62d-149">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="8c62d-150">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="8c62d-150">Figure 7</span></span>  
    > <span data-ttu-id="8c62d-151">Botón **Borrar datos del sitio**</span><span class="sxs-lookup"><span data-stu-id="8c62d-151">The **Clear Site Data** button</span></span>  
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
> <span data-ttu-id="8c62d-162">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8c62d-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8c62d-163">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/websql) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="8c62d-163">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8c62d-165">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8c62d-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
