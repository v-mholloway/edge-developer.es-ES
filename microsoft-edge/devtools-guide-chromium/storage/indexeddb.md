---
description: Cómo ver y cambiar los datos de IndexedDB con el panel de aplicación y los fragmentos de código.
title: Ver y cambiar datos de IndexedDB con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 03e6d04050677a0ba153c6adc06dd795cc42115d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231205"
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

# <span data-ttu-id="3b6cc-104">Ver y cambiar datos de IndexedDB con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3b6cc-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3b6cc-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver y cambiar los datos de [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="3b6cc-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="3b6cc-106">Se da por sentado que estás familiarizado con DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="3b6cc-107">También se supone que estás familiarizado con IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="3b6cc-108">En caso contrario, vaya a [usar IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="3b6cc-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="3b6cc-109">Ver datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="3b6cc-110">Elija la pestaña **aplicación** para abrir la herramienta **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="3b6cc-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="3b6cc-111">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="3b6cc-113">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="3b6cc-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b6cc-114">Expanda el menú **IndexedDB** para revisar qué bases de datos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="El menú IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="3b6cc-116">El menú **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="3b6cc-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="3b6cc-117">\ ( ![ Icono de base de datos ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` representa una base de datos, donde `notes` es el nombre de la base de datos y `https://mdn.github.io` es el origen que tiene acceso a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="3b6cc-118">\ ( ![ Icono del almacén de objetos ][ImageObjectStoreIcon] \) `notes` es un almacén de objetos.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="3b6cc-119">el **título** y el **cuerpo** son [índices][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="3b6cc-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3b6cc-120">**Limitación conocida**  Las bases de datos de terceros no están visibles.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="3b6cc-121">Por ejemplo, si usa una `<iframe>` para insertar un anuncio en la página y su red de anuncios usa IndexedDB, los datos de IndexedDB de la red de anuncios no estarán visibles.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="3b6cc-122">Desplácese hasta el [#943770 de problemas][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="3b6cc-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="3b6cc-123">Elija una base de datos para revisar el origen y el número de versión.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="La base de datos de Notes" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="3b6cc-125">La base de datos de **Notes**</span><span class="sxs-lookup"><span data-stu-id="3b6cc-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b6cc-126">Elija un almacén de objetos para revisar los pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3b6cc-127">Los datos de IndexedDB no se actualizan en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="3b6cc-128">Vaya a [actualizar datos de IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="3b6cc-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="El almacén de objetos de Notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="3b6cc-130">El almacén de objetos de **Notes**</span><span class="sxs-lookup"><span data-stu-id="3b6cc-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="3b6cc-131">**Entradas totales** es el número total de pares de clave y valor en el almacén de objetos.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="3b6cc-132">El **valor del generador de claves** es la siguiente clave disponible.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="3b6cc-133">El campo solo se muestra cuando se usan [generadores de claves][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="3b6cc-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="3b6cc-134">Elija una celda en la columna **valor** para expandir el valor.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Ver un valor de IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="3b6cc-136">Ver un valor de **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="3b6cc-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b6cc-137">Elija un índice, como **título** o **cuerpo** en la siguiente ilustración, para ordenar el objeto almacén según los valores de ese índice.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Ordenar un objeto por un índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="3b6cc-139">Ordenar un objeto por un índice</span><span class="sxs-lookup"><span data-stu-id="3b6cc-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3b6cc-140">Actualizar datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="3b6cc-141">Los valores de IndexedDB en la herramienta de **aplicaciones** no se actualizan en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="3b6cc-142">Elija **Actualizar** \ ( ![ actualizar ][ImageReloadIcon] \) al ver un almacén de objetos para actualizar los datos, o ver una base de datos y elegir **actualizar la base** de datos para actualizar todos los datos.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-142">Choose **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Ver una base de datos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="3b6cc-144">Ver una base de datos</span><span class="sxs-lookup"><span data-stu-id="3b6cc-144">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="3b6cc-145">Editar datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="3b6cc-146">Las claves y los valores de IndexedDB no se pueden modificar en la herramienta de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="3b6cc-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="3b6cc-147">Como DevTools tiene acceso al contexto de la página, puede ejecutar el código de JavaScript dentro de DevTools para editar los datos de IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="3b6cc-148">Editar datos de IndexedDB con fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="3b6cc-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="3b6cc-149">Los recortes [son una][DevtoolsJavascriptSnippets] forma de almacenar y ejecutar bloques de código JavaScript dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="3b6cc-150">Al ejecutar un fragmento de código, el resultado se registra en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="3b6cc-151">Puede usar un fragmento de código de JavaScript para editar una base de datos IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar un fragmento de código para interactuar con IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="3b6cc-153">Usar un fragmento de código para interactuar con IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="3b6cc-154">Eliminar datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-154">Delete IndexedDB data</span></span>  

### <span data-ttu-id="3b6cc-155">Eliminar un par de clave y valor de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="3b6cc-156">[Ver un almacén de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="3b6cc-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="3b6cc-157">Seleccione el par de clave y valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-157">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="3b6cc-158">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Seleccione un par clave-valor para eliminarlo." lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="3b6cc-160">Seleccione un par clave-valor para eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-160">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b6cc-161">Presione la `Delete` tecla o elija **eliminar seleccionado** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3b6cc-161">Press the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Aspecto del almacén de objetos después de eliminar el par de clave y valor" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="3b6cc-163">Aspecto del almacén de objetos después de eliminar el par de clave y valor</span><span class="sxs-lookup"><span data-stu-id="3b6cc-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3b6cc-164">Eliminar todos los pares clave-valor en un almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="3b6cc-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="3b6cc-165">[Ver un almacén de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="3b6cc-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Ver un almacén de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="3b6cc-167">Ver un almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="3b6cc-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b6cc-168">Elija **Borrar almacén de objetos** \ ( ![ Borrar almacén de objetos ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3b6cc-168">Choose **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="3b6cc-169">Eliminar una base de datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="3b6cc-170">[Vea la base de datos IndexedDB](#view-indexeddb-data) que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="3b6cc-171">Elija **eliminar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="El botón Eliminar base de datos" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="3b6cc-173">El botón **eliminar base de datos**</span><span class="sxs-lookup"><span data-stu-id="3b6cc-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3b6cc-174">Eliminar todo el almacenamiento de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="3b6cc-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="3b6cc-175">Abra el panel **Borrar almacenamiento** .</span><span class="sxs-lookup"><span data-stu-id="3b6cc-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="3b6cc-176">Asegúrese de que la casilla de verificación **IndexedDB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="3b6cc-177">Elija **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="3b6cc-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="El panel borrar almacenamiento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="3b6cc-179">El panel **Borrar almacenamiento**</span><span class="sxs-lookup"><span data-stu-id="3b6cc-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3b6cc-180">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3b6cc-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: Mostrar bases de datos de IndexedDB de iframe, cromo-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Generador de claves: conceptos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API de IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Uso de IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usar un índice-Using IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="3b6cc-188">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3b6cc-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3b6cc-189">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3b6cc-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3b6cc-191">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3b6cc-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
