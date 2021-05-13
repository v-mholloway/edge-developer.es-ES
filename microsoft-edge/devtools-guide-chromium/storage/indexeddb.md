---
description: Cómo ver y cambiar los datos de IndexedDB con el panel Aplicación y los fragmentos de código.
title: Ver y cambiar datos IndexedDB con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b0927ab436d1278f50b0dee099ba3526e5506762
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564808"
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
# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a><span data-ttu-id="50368-104">Ver y cambiar datos IndexedDB con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="50368-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="50368-105">En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] ver y cambiar [los datos de IndexedDB.][MDNIndexedDBAPI]</span><span class="sxs-lookup"><span data-stu-id="50368-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="50368-106">Se supone que está familiarizado con DevTools.</span><span class="sxs-lookup"><span data-stu-id="50368-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="50368-107">También supone que está familiarizado con IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="50368-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="50368-108">Si no es así, vaya [a Using IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="50368-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <a name="view-indexeddb-data"></a><span data-ttu-id="50368-109">Ver datos indexadosDB</span><span class="sxs-lookup"><span data-stu-id="50368-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="50368-110">Elija la **pestaña** Aplicación para abrir la **herramienta** Aplicación.</span><span class="sxs-lookup"><span data-stu-id="50368-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="50368-111">El **panel Manifiesto** normalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="50368-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="50368-113">Panel **Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="50368-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50368-114">Expanda el **menú IndexedDB** para revisar qué bases de datos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="50368-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Menú IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="50368-116">Menú **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="50368-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="50368-117">\( Icono de base de datos \) representa una base de datos, donde es el nombre de la base de datos y es el origen que ![ tiene acceso a la base de ](../media/database-icon.msft.png) `notes - https://mdn.github.io` `notes` `https://mdn.github.io` datos.</span><span class="sxs-lookup"><span data-stu-id="50368-117">\(![Database icon](../media/database-icon.msft.png)\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="50368-118">\( ![ Icono del almacén de objetos ](../media/object-store-icon.msft.png) \) es un almacén de `notes` objetos.</span><span class="sxs-lookup"><span data-stu-id="50368-118">\(![Object Store icon](../media/object-store-icon.msft.png)\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="50368-119">**title** y **body** son [índices][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="50368-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="50368-120">**Limitación conocida**  Las bases de datos de terceros no están visibles.</span><span class="sxs-lookup"><span data-stu-id="50368-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="50368-121">Por ejemplo, si usas un anuncio para insertar un anuncio en tu página y la red de anuncios usa IndexedDB, los datos indexados de la red de anuncios no `<iframe>` estarán visibles.</span><span class="sxs-lookup"><span data-stu-id="50368-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="50368-122">Vaya a [emitir #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="50368-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="50368-123">Elija una base de datos para revisar el origen y el número de versión.</span><span class="sxs-lookup"><span data-stu-id="50368-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="La base de datos de notas" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="50368-125">La **base de datos de notas**</span><span class="sxs-lookup"><span data-stu-id="50368-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50368-126">Elija un almacén de objetos para revisar los pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="50368-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="50368-127">Los datos indexadosDB no se actualizan en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="50368-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="50368-128">Vaya a [Actualizar datos indexadosDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="50368-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="El almacén de objetos de notas" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="50368-130">El **almacén de objetos de** notas</span><span class="sxs-lookup"><span data-stu-id="50368-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="50368-131">**El número total de entradas** es el número total de pares clave-valor en el almacén de objetos.</span><span class="sxs-lookup"><span data-stu-id="50368-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="50368-132">**El valor del generador de** claves es la siguiente clave disponible.</span><span class="sxs-lookup"><span data-stu-id="50368-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="50368-133">El campo solo se muestra cuando se usan [generadores de claves][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="50368-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="50368-134">Elija una celda en la **columna Valor** para expandir el valor.</span><span class="sxs-lookup"><span data-stu-id="50368-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Ver un valor IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="50368-136">Ver un **valor IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="50368-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50368-137">Elija un índice, como **el título** **o** el cuerpo de la siguiente figura, para ordenar el almacén de objetos según los valores de ese índice.</span><span class="sxs-lookup"><span data-stu-id="50368-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Ordenar un almacén de objetos por un índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="50368-139">Ordenar un almacén de objetos por un índice</span><span class="sxs-lookup"><span data-stu-id="50368-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a><span data-ttu-id="50368-140">Actualizar datos indexadosDB</span><span class="sxs-lookup"><span data-stu-id="50368-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="50368-141">Los valores indexadosDB en **la herramienta Aplicación** no se actualizan en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="50368-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="50368-142">Elija **Actualizar** \( Actualizar \) al ver un almacén de objetos para actualizar los datos o ver una base de datos y elegir Actualizar base de datos para ![ actualizar todos los ](../media/reload-icon.msft.png) datos. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="50368-142">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Ver una base de datos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="50368-144">Ver una base de datos</span><span class="sxs-lookup"><span data-stu-id="50368-144">View a database</span></span>  
:::image-end:::  

## <a name="edit-indexeddb-data"></a><span data-ttu-id="50368-145">Editar datos indexadosDB</span><span class="sxs-lookup"><span data-stu-id="50368-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="50368-146">Las claves indexadasDB y los valores no se pueden editar desde la **herramienta Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="50368-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="50368-147">Sin embargo, dado que DevTools tiene acceso al contexto de página, puede ejecutar código JavaScript en DevTools para editar datos indexadosDB.</span><span class="sxs-lookup"><span data-stu-id="50368-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <a name="edit-indexeddb-data-with-snippets"></a><span data-ttu-id="50368-148">Editar datos IndexedDB con fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="50368-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="50368-149">[Los fragmentos][DevtoolsJavascriptSnippets] de código son una forma de almacenar y ejecutar bloques de código JavaScript en DevTools.</span><span class="sxs-lookup"><span data-stu-id="50368-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="50368-150">Al ejecutar un fragmento de código, el resultado se registra en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="50368-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="50368-151">Puede usar un fragmento de código para ejecutar código JavaScript para editar una base de datos IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="50368-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar un fragmento de código para interactuar con IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="50368-153">Usar un fragmento de código para interactuar con IndexedDB</span><span class="sxs-lookup"><span data-stu-id="50368-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <a name="delete-indexeddb-data"></a><span data-ttu-id="50368-154">Eliminar datos indexadosDB</span><span class="sxs-lookup"><span data-stu-id="50368-154">Delete IndexedDB data</span></span>  

### <a name="delete-an-indexeddb-key-value-pair"></a><span data-ttu-id="50368-155">Eliminar un par clave-valor IndexedDB</span><span class="sxs-lookup"><span data-stu-id="50368-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="50368-156">[Ver un almacén de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="50368-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="50368-157">Elija el par clave-valor que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="50368-157">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="50368-158">DevTools lo resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="50368-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Elegir un par clave-valor para eliminarlo" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="50368-160">Elegir un par clave-valor para eliminarlo</span><span class="sxs-lookup"><span data-stu-id="50368-160">Choose a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50368-161">Seleccione la `Delete` clave o elija Eliminar **seleccionado** \( Eliminar ![ seleccionado ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="50368-161">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Cómo se ve el almacén de objetos después de eliminar el par clave-valor" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="50368-163">Cómo se ve el almacén de objetos después de eliminar el par clave-valor</span><span class="sxs-lookup"><span data-stu-id="50368-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a><span data-ttu-id="50368-164">Eliminar todos los pares clave-valor de un almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="50368-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="50368-165">[Ver un almacén de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="50368-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Ver un almacén de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="50368-167">Ver un almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="50368-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50368-168">Elija **Borrar almacén de objetos** \( Borrar almacén de objetos ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="50368-168">Choose **Clear object store** \(![Clear object store](../media/clear-icon.msft.png)\).</span></span>  
    
### <a name="delete-an-indexeddb-database"></a><span data-ttu-id="50368-169">Eliminar una base de datos IndexedDB</span><span class="sxs-lookup"><span data-stu-id="50368-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="50368-170">[Vea la base de datos IndexedDB](#view-indexeddb-data) que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="50368-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="50368-171">Elija **Eliminar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="50368-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Botón Eliminar base de datos" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="50368-173">Botón **Eliminar base de datos**</span><span class="sxs-lookup"><span data-stu-id="50368-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a><span data-ttu-id="50368-174">Eliminar todo el almacenamiento de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="50368-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="50368-175">Abra el **panel Borrar** almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="50368-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="50368-176">Asegúrese de que la **casilla IndexedDB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="50368-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="50368-177">Elija **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="50368-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="El panel Despejar almacenamiento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="50368-179">El **panel Despejar almacenamiento**</span><span class="sxs-lookup"><span data-stu-id="50368-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="50368-180">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="50368-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Herramientas para desarrolladores | Microsoft Docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Ejecute fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools: Mostrar bases de datos de iframe IndexedDB - chromium - Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Generador de claves: conceptos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "Api IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Uso de indexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Uso de un índice: uso de IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="50368-188">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50368-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="50368-189">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="50368-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="50368-191">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50368-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
