---
description: Cómo ver los datos SQL web desde el panel Aplicación de Microsoft Edge DevTools.
title: Ver datos SQL web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 326fe492a3436a40d81c8e31db99a26da4ea054f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397555"
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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a><span data-ttu-id="5f28e-104">Ver datos SQL web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5f28e-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="5f28e-105">La especificación SQL web no [se está conservando.][W3CWebSQLStatus]</span><span class="sxs-lookup"><span data-stu-id="5f28e-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="5f28e-106">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspeccionar los datos SQL web.</span><span class="sxs-lookup"><span data-stu-id="5f28e-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <a name="view-web-sql-data"></a><span data-ttu-id="5f28e-107">Ver datos SQL web</span><span class="sxs-lookup"><span data-stu-id="5f28e-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="5f28e-108">Elija la **herramienta Orígenes** para abrir la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="5f28e-108">Choose the **Sources** tool to open the **Sources** tool.</span></span>  <span data-ttu-id="5f28e-109">El **panel Manifiesto** normalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5f28e-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="5f28e-111">Panel **Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="5f28e-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5f28e-112">Expanda la **sección Web SQL** para ver bases de datos y tablas.</span><span class="sxs-lookup"><span data-stu-id="5f28e-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="5f28e-113">En la siguiente figura, debajo **de html5meetup** hay una base de datos y **salas** es una tabla.</span><span class="sxs-lookup"><span data-stu-id="5f28e-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Panel web SQL web" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="5f28e-115">Panel **de SQL** web</span><span class="sxs-lookup"><span data-stu-id="5f28e-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5f28e-116">Elija una tabla para ver los datos de esa tabla.</span><span class="sxs-lookup"><span data-stu-id="5f28e-116">Choose a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Ver los datos de una tabla SQL web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="5f28e-118">Ver los datos de una tabla SQL web</span><span class="sxs-lookup"><span data-stu-id="5f28e-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a><span data-ttu-id="5f28e-119">Editar datos SQL web</span><span class="sxs-lookup"><span data-stu-id="5f28e-119">Edit Web SQL data</span></span>  

<span data-ttu-id="5f28e-120">No puede editar datos web SQL al ver una tabla de SQL web, como en la anterior.</span><span class="sxs-lookup"><span data-stu-id="5f28e-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in previous above.</span></span>  <span data-ttu-id="5f28e-121">Pero puede ejecutar instrucciones desde la consola web SQL que editan o eliminan tablas.</span><span class="sxs-lookup"><span data-stu-id="5f28e-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="5f28e-122">Vaya a [Ejecutar consultas SQL web](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="5f28e-122">Navigate to [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <a name="run-web-sql-queries"></a><span data-ttu-id="5f28e-123">Ejecutar consultas SQL web</span><span class="sxs-lookup"><span data-stu-id="5f28e-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="5f28e-124">Elija una base de datos para abrir una consola para esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="5f28e-124">Choose a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="5f28e-125">Escriba una instrucción Web SQL y, a continuación, `Enter` seleccione para ejecutarla.</span><span class="sxs-lookup"><span data-stu-id="5f28e-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Usar la Consola de SQL web para eliminar una fila de una tabla" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="5f28e-127">Usar la Consola de SQL web para eliminar una fila de una tabla</span><span class="sxs-lookup"><span data-stu-id="5f28e-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a><span data-ttu-id="5f28e-128">Actualizar una tabla de SQL web</span><span class="sxs-lookup"><span data-stu-id="5f28e-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="5f28e-129">DevTools no actualiza tablas en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="5f28e-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="5f28e-130">Para actualizar los datos de una tabla, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="5f28e-130">To update the data in a table, complete the following actions.</span></span>  

1.  <span data-ttu-id="5f28e-131">[Ver los datos en una tabla web SQL web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="5f28e-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5f28e-132">Elija **Actualizar** \( ![ Actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="5f28e-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a><span data-ttu-id="5f28e-133">Filtrar las columnas de una tabla de SQL web</span><span class="sxs-lookup"><span data-stu-id="5f28e-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="5f28e-134">[Ver los datos en una tabla web SQL web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="5f28e-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5f28e-135">Use el cuadro de texto Columnas **visibles** para especificar qué columnas desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="5f28e-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="5f28e-136">Proporcione los nombres de columna como una lista CSV.</span><span class="sxs-lookup"><span data-stu-id="5f28e-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Usar el cuadro de texto Columnas visibles para reducir el número de columnas mostradas" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="5f28e-138">Usar el **cuadro de texto Columnas** visibles para reducir el número de columnas mostradas</span><span class="sxs-lookup"><span data-stu-id="5f28e-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a><span data-ttu-id="5f28e-139">Eliminar todos los datos SQL web</span><span class="sxs-lookup"><span data-stu-id="5f28e-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="5f28e-140">Abra el **panel Borrar** almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5f28e-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="5f28e-141">Asegúrese de que la **casilla web SQL** está activada.</span><span class="sxs-lookup"><span data-stu-id="5f28e-141">Make sure that the **Web SQL** checkbox is turned on.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="La casilla de SQL web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="5f28e-143">La **casilla de SQL** web</span><span class="sxs-lookup"><span data-stu-id="5f28e-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5f28e-144">Elija **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="5f28e-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Botón Borrar datos del sitio" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="5f28e-146">Botón **Borrar datos del** sitio</span><span class="sxs-lookup"><span data-stu-id="5f28e-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5f28e-147">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5f28e-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de SQL web | W3C"  

> [!NOTE]
> <span data-ttu-id="5f28e-150">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5f28e-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5f28e-151">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/websql) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5f28e-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5f28e-153">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5f28e-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
