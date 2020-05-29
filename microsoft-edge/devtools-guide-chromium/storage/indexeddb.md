---
title: Ver y cambiar datos de IndexedDB con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612091"
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





# <span data-ttu-id="fd04f-103">Ver y cambiar datos de IndexedDB con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fd04f-103">View And Change IndexedDB Data With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="fd04f-104">En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver y cambiar los datos de [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="fd04f-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="fd04f-105">Se da por sentado que estás familiarizado con DevTools.</span><span class="sxs-lookup"><span data-stu-id="fd04f-105">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="fd04f-106">También se supone que estás familiarizado con IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="fd04f-106">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="fd04f-107">Si no es así, vea [usar IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="fd04f-107">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="fd04f-108">Ver datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-108">View IndexedDB data</span></span>   

1.  <span data-ttu-id="fd04f-109">Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="fd04f-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="fd04f-110">El panel **manifiesto** generalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fd04f-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="fd04f-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="fd04f-111">Figure 1</span></span>  
    > <span data-ttu-id="fd04f-112">El panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="fd04f-112">The Manifest pane</span></span>  
    > ![El panel manifiesto][ImageManifest]  

1.  <span data-ttu-id="fd04f-114">Expanda el menú **IndexedDB** para ver qué bases de datos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="fd04f-114">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    > ##### <span data-ttu-id="fd04f-115">Figura 2</span><span class="sxs-lookup"><span data-stu-id="fd04f-115">Figure 2</span></span>  
    > <span data-ttu-id="fd04f-116">El menú **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="fd04f-116">The **IndexedDB** menu</span></span>  
    > ![El menú IndexedDB][ImageIndexedDBMenu]  
    
    *   ![<span data-ttu-id="fd04f-118">El icono ][ImageDatabaseIcon] `notes - https://mdn.github.io` de base de datos representa una base de datos, donde `notes` es el nombre de la base de datos y `https://mdn.github.io` es el origen que tiene acceso a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd04f-118">Database icon][ImageDatabaseIcon] `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   ![<span data-ttu-id="fd04f-119">El icono de almacén de objetos ][ImageObjectStoreIcon] `notes` es un almacén de objetos.</span><span class="sxs-lookup"><span data-stu-id="fd04f-119">Object Store icon][ImageObjectStoreIcon] `notes` is an object store.</span></span>  
    *   <span data-ttu-id="fd04f-120">el **título** y el **cuerpo** son [índices][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="fd04f-120">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="fd04f-121">**Limitación conocida**  Las bases de datos de terceros no están visibles.</span><span class="sxs-lookup"><span data-stu-id="fd04f-121">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="fd04f-122">Por ejemplo, si usa una `<iframe>` para insertar un anuncio en la página y su red de anuncios usa IndexedDB, los datos de IndexedDB de la red de anuncios no estarán visibles.</span><span class="sxs-lookup"><span data-stu-id="fd04f-122">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="fd04f-123">Consulte el [problema #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="fd04f-123">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="fd04f-124">Seleccione una base de datos para ver el origen y el número de versión.</span><span class="sxs-lookup"><span data-stu-id="fd04f-124">Select a database to see the origin and version number.</span></span>  
    
    > ##### <span data-ttu-id="fd04f-125">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="fd04f-125">Figure 3</span></span>  
    > <span data-ttu-id="fd04f-126">La base de datos de **Notes**</span><span class="sxs-lookup"><span data-stu-id="fd04f-126">The **notes** database</span></span>  
    > ![La base de datos de Notes][ImageIndexedDBDatabase]  
    
1.  <span data-ttu-id="fd04f-128">Seleccione un almacén de objetos para ver los pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="fd04f-128">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="fd04f-129">Los datos de IndexedDB no se actualizan en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="fd04f-129">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="fd04f-130">Consulte [actualizar datos de IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="fd04f-130">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="fd04f-131">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="fd04f-131">Figure 4</span></span>  
    > <span data-ttu-id="fd04f-132">El almacén de objetos de **Notes**</span><span class="sxs-lookup"><span data-stu-id="fd04f-132">The **notes** object store</span></span>  
    > ![El almacén de objetos de Notes][ImageIndexedDBObjectStore]  

    *   <span data-ttu-id="fd04f-134">**Entradas totales** es el número total de pares de clave y valor en el almacén de objetos.</span><span class="sxs-lookup"><span data-stu-id="fd04f-134">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="fd04f-135">El **valor del generador de claves** es la siguiente clave disponible.</span><span class="sxs-lookup"><span data-stu-id="fd04f-135">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="fd04f-136">Este campo solo se muestra al usar [generadores de claves][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="fd04f-136">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  

1.  <span data-ttu-id="fd04f-137">Seleccione una celda en la columna **valor** para expandir ese valor.</span><span class="sxs-lookup"><span data-stu-id="fd04f-137">Select a cell in the **Value** column to expand that value.</span></span>  
    
    > ##### <span data-ttu-id="fd04f-138">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="fd04f-138">Figure 5</span></span>  
    > <span data-ttu-id="fd04f-139">Visualización de un valor de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-139">Viewing an IndexedDB value</span></span>  
    > ![Visualización de un valor de IndexedDB][ImageIndexedBDValue]  
    
1.  <span data-ttu-id="fd04f-141">Seleccione un índice, como **título** o **cuerpo** en la [figura 6](#figure-6), para ordenar el objeto almacén según los valores de ese índice.</span><span class="sxs-lookup"><span data-stu-id="fd04f-141">Select an index, such as **title** or **body** in [Figure 6](#figure-6), to sort the object store according to the values of that index.</span></span>  
   
    > ##### <span data-ttu-id="fd04f-142">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="fd04f-142">Figure 6</span></span>  
    > <span data-ttu-id="fd04f-143">Un almacén de objetos ordenado alfabéticamente según la clave de **título**</span><span class="sxs-lookup"><span data-stu-id="fd04f-143">An object store that is sorted alphabetically according to the **title** key</span></span>  
    > ![Ordenar un objeto por un índice][ImageIndexedDBIndex]  

## <span data-ttu-id="fd04f-145">Actualizar datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-145">Refresh IndexedDB data</span></span>   

<span data-ttu-id="fd04f-146">Los valores de IndexedDB en el panel de **aplicaciones** no se actualizan en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="fd04f-146">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="fd04f-147">Seleccione **Actualizar** ![ actualización ][ImageReloadIcon] al ver un almacén de objetos para actualizar los datos, o ver una base de datos y haga clic en **actualizar la base** de datos para actualizar todos los datos.</span><span class="sxs-lookup"><span data-stu-id="fd04f-147">Select **Refresh** ![Refresh][ImageReloadIcon] when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

> ##### <span data-ttu-id="fd04f-148">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="fd04f-148">Figure 7</span></span>  
> <span data-ttu-id="fd04f-149">Ver una base de datos</span><span class="sxs-lookup"><span data-stu-id="fd04f-149">Viewing a database</span></span>  
> ![Ver una base de datos][ImageIndexedDBDatabase2]  

## <span data-ttu-id="fd04f-151">Editar datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-151">Edit IndexedDB data</span></span>   

<span data-ttu-id="fd04f-152">Las claves y los valores de IndexedDB no se pueden modificar en el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="fd04f-152">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="fd04f-153">Como DevTools tiene acceso al contexto de la página, puede ejecutar el código de JavaScript dentro de DevTools para editar los datos de IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="fd04f-153">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="fd04f-154">Editar datos de IndexedDB con fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="fd04f-154">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="fd04f-155">Los recortes [son una][DevtoolsJavascriptSnippets] forma de almacenar y ejecutar bloques de código JavaScript dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="fd04f-155">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="fd04f-156">Al ejecutar un fragmento de código, el resultado se registra en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="fd04f-156">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="fd04f-157">Puede usar un fragmento de código de JavaScript para editar una base de datos IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="fd04f-157">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

> ##### <span data-ttu-id="fd04f-158">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="fd04f-158">Figure 8</span></span>  
> <span data-ttu-id="fd04f-159">Uso de un fragmento de código para interactuar con IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-159">Using a Snippet to interact with IndexedDB</span></span>  
> ![Uso de un fragmento de código para interactuar con IndexedDB][ImageIndexedDBSnippet]  

## <span data-ttu-id="fd04f-161">Eliminar datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-161">Delete IndexedDB data</span></span>   

### <span data-ttu-id="fd04f-162">Eliminar un par de clave y valor de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-162">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="fd04f-163">[Ver un almacén de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="fd04f-163">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="fd04f-164">Seleccione el par de clave y valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="fd04f-164">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="fd04f-165">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fd04f-165">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="fd04f-166">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="fd04f-166">Figure 9</span></span>  
    > <span data-ttu-id="fd04f-167">Selección de un par clave-valor para eliminarlo</span><span class="sxs-lookup"><span data-stu-id="fd04f-167">Selecting a key-value pair in order to delete it</span></span>  
    > ![Selección de un par clave-valor para eliminarlo][ImageIndexedDBKeyValuePair]  

1.  <span data-ttu-id="fd04f-169">Presione la `Delete` tecla o haga clic en **eliminar** selección ![ eliminar seleccionados ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="fd04f-169">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  
    
    > ##### <span data-ttu-id="fd04f-170">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="fd04f-170">Figure 10</span></span>  
    > <span data-ttu-id="fd04f-171">Aspecto del almacén de objetos después de eliminar el par de clave y valor</span><span class="sxs-lookup"><span data-stu-id="fd04f-171">How the object store looks after the key-value pair has been deleted</span></span>  
    > ![Aspecto del almacén de objetos después de eliminar el par de clave y valor][ImageIndexedDBKeyValuePairDeleted]  

### <span data-ttu-id="fd04f-173">Eliminar todos los pares clave-valor en un almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="fd04f-173">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="fd04f-174">[Ver un almacén de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="fd04f-174">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="fd04f-175">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="fd04f-175">Figure 11</span></span>  
    > <span data-ttu-id="fd04f-176">Visualización de un almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="fd04f-176">Viewing an object store</span></span>  
    > ![Visualización de un almacén de objetos][ImageIndexedDBObjectStore]  

1.  <span data-ttu-id="fd04f-178">Seleccione Borrar almacén de objetos borrar **almacén de objetos** ![ ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="fd04f-178">Select **Clear object store** ![Clear object store][ImageClearIcon].</span></span>  

### <span data-ttu-id="fd04f-179">Eliminar una base de datos de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-179">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="fd04f-180">[Vea la base de datos IndexedDB](#view-indexeddb-data) que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="fd04f-180">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="fd04f-181">Seleccione **eliminar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="fd04f-181">Select **Delete database**.</span></span>  
    
    > ##### <span data-ttu-id="fd04f-182">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="fd04f-182">Figure 12</span></span>  
    > <span data-ttu-id="fd04f-183">El botón **eliminar base de datos**</span><span class="sxs-lookup"><span data-stu-id="fd04f-183">The **Delete database** button</span></span>  
    > ![El botón Eliminar base de datos][ImageIndexedDBDatabase]  

### <span data-ttu-id="fd04f-185">Eliminar todo el almacenamiento de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="fd04f-185">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="fd04f-186">Abra el panel **Borrar almacenamiento** .</span><span class="sxs-lookup"><span data-stu-id="fd04f-186">Open the **Clear storage** pane.</span></span>  

1.  <span data-ttu-id="fd04f-187">Asegúrese de que la casilla de verificación **IndexedDB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fd04f-187">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  

1.  <span data-ttu-id="fd04f-188">Seleccione **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="fd04f-188">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="fd04f-189">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="fd04f-189">Figure 13</span></span>  
    > <span data-ttu-id="fd04f-190">El panel **Borrar almacenamiento** ![ el panel borrar almacenamiento][ImageIndexedDBClearStorage]</span><span class="sxs-lookup"><span data-stu-id="fd04f-190">The **Clear storage** pane ![The Clear storage pane][ImageIndexedDBClearStorage]</span></span>  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Ilustración 1: el panel manifiesto"  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Ilustración 2: el menú IndexedDB"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Ilustración 3: la notes_db base de datos"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Ilustración 4: el almacén de objetos de notes_os"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Ilustración 5: ver un valor de IndexedDB"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Ilustración 6: ordenar un objeto almacenado por un índice"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Ilustración 7: ver una base de datos"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Ilustración 8: uso de un fragmento de código para interactuar con IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Ilustración 9: selección de un par clave-valor para eliminarlo"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Ilustración 10: el aspecto del almacén de objetos después de que se haya eliminado el par de clave y valor"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Ilustración 11: visualización de un almacén de objetos"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Ilustración 12: el botón Eliminar base de datos"  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Ilustración 13: el panel borrar almacenamiento"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: Mostrar bases de datos de IndexedDB de iframe, cromo-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Generador de claves: conceptos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API de IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Uso de IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usar un índice-Using IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="fd04f-211">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd04f-211">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fd04f-212">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="fd04f-212">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fd04f-214">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd04f-214">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
