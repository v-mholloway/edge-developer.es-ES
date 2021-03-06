---
description: Use el panel Almacenamiento para inspeccionar el almacenamiento web, IndexedDB, las cookies y las memorias caché de solicitud y respuesta
title: Almacenamiento | DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, almacenamiento web, almacenamiento local, almacenamiento de sesiones, indexeddb, cookies, trabajador de servicio, caché
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e970ae0d8ca3a43a309eff7b77400aa3ced5b21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398899"
---
# <a name="storage"></a><span data-ttu-id="03b5d-104">Almacenamiento</span><span class="sxs-lookup"><span data-stu-id="03b5d-104">Storage</span></span>

<span data-ttu-id="03b5d-105">Use el panel **Almacenamiento** para inspeccionar y administrar varios datos almacenados en caché localmente, incluidos:</span><span class="sxs-lookup"><span data-stu-id="03b5d-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>  

*   <span data-ttu-id="03b5d-106">[Pares de clave y](#local-and-session-storage-managers) valores de almacenamiento web \(Almacenamiento local y de sesión\)</span><span class="sxs-lookup"><span data-stu-id="03b5d-106">[Web storage](#local-and-session-storage-managers) \(Local and Session storage\) key/values pairs</span></span>  
*   <span data-ttu-id="03b5d-107">[Datos estructurados de base de datos](#indexeddb-manager) indizados</span><span class="sxs-lookup"><span data-stu-id="03b5d-107">[Indexed DB](#indexeddb-manager) structured data</span></span>  
*   <span data-ttu-id="03b5d-108">[Cookies](#cookies-list) para el dominio</span><span class="sxs-lookup"><span data-stu-id="03b5d-108">[Cookies](#cookies-list) for the domain</span></span>  
*   <span data-ttu-id="03b5d-109">[Caché](#cache-manager) \(pares de solicitud/respuesta\) para la depuración del trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="03b5d-109">[Cache](#cache-manager) \(request/response pairs\) for service worker debugging</span></span>  

<span data-ttu-id="03b5d-110">Expanda cualquiera de estas categorías y haga clic en una entrada secundaria para abrir su pestaña administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="03b5d-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>  

## <a name="local-and-session-storage-managers"></a><span data-ttu-id="03b5d-111">Administradores de almacenamiento local y de sesión</span><span class="sxs-lookup"><span data-stu-id="03b5d-111">Local and Session storage managers</span></span>  

<span data-ttu-id="03b5d-112">Use el administrador de almacenamiento local y el administrador de almacenamiento de sesiones para inspeccionar y administrar el almacenamiento web de la página.</span><span class="sxs-lookup"><span data-stu-id="03b5d-112">Use the Local Storage manager and Session Storage manager to inspect and manage the web storage for your page.</span></span>  

<span data-ttu-id="03b5d-113">Las **carpetas** Almacenamiento local y **Almacenamiento de** sesiones dentro del selector De recursos del panel almacenamiento muestran una lista de orígenes de la página. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="03b5d-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [Resource picker](./debugger.md#resource-picker) display a list of origins for the page.</span></span>  <span data-ttu-id="03b5d-114">Al seleccionar uno de estos marcos, se abre una tabla editable de los pares clave/valor actuales establecidos a través de [](#storage-list) [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) o [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivamente \(y/o establecido directamente desde la lista Almacenamiento de DevTools \).</span><span class="sxs-lookup"><span data-stu-id="03b5d-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively \(and/or set directly from the  DevTools [Storage list](#storage-list)\).</span></span>  

![Administrador de almacenamiento de DevTools](./media/storage_web_storage.png)  

<span data-ttu-id="03b5d-116">En las pestañas Almacenamiento local y Almacenamiento de sesiones puede:</span><span class="sxs-lookup"><span data-stu-id="03b5d-116">From the Local Storage and Session Storage tabs you can:</span></span>  

*   <span data-ttu-id="03b5d-117">**Actualice** \( \) la lista de almacenamiento para ver el conjunto actual de pares `Ctrl+F5` clave/valores para el dominio determinado. [](#cookies-list)</span><span class="sxs-lookup"><span data-stu-id="03b5d-117">**Refresh** \(`Ctrl+F5`\) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span>  <span data-ttu-id="03b5d-118">\(La lista no se actualiza automáticamente tras las actualizaciones de scripts.\)</span><span class="sxs-lookup"><span data-stu-id="03b5d-118">\(The list does not auto-refresh upon script updates.\)</span></span>  
*   <span data-ttu-id="03b5d-119">**Simular alcanzar el límite de almacenamiento**  para el almacenamiento web de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="03b5d-119">**Simulate reaching the storage limit**  for Microsoft Edge web storage.</span></span>  <span data-ttu-id="03b5d-120">Cada dominio y subdominio tiene su propio área de almacenamiento, pero hay un límite combinado:</span><span class="sxs-lookup"><span data-stu-id="03b5d-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>  
    *   <span data-ttu-id="03b5d-121">**Subdominios:** hasta 5 MB de espacio</span><span class="sxs-lookup"><span data-stu-id="03b5d-121">**Subdomains**:  up to 5 MBs of space</span></span>  
    *   <span data-ttu-id="03b5d-122">**Dominios:** hasta 10 MB de espacio</span><span class="sxs-lookup"><span data-stu-id="03b5d-122">**Domains**:  up to 10 MBs of space</span></span>  
    *   <span data-ttu-id="03b5d-123">**Total para todos los dominios:** hasta 50 MB de espacio</span><span class="sxs-lookup"><span data-stu-id="03b5d-123">**Total for all domains**:  up to 50 MBs of space</span></span>  

   <span data-ttu-id="03b5d-124">El almacenamiento de sesión se borra tan pronto como se cierra la última pestaña del explorador que hace referencia a su origen.</span><span class="sxs-lookup"><span data-stu-id="03b5d-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span>  <span data-ttu-id="03b5d-125">Las entradas de almacenamiento local persisten indefinidamente hasta que el usuario lo borra mediante programación o manualmente:</span><span class="sxs-lookup"><span data-stu-id="03b5d-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>  

   <span data-ttu-id="03b5d-126">**Configuración**  >  **Borrar datos de exploración**  >  **Cookies y datos guardados del sitio web**</span><span class="sxs-lookup"><span data-stu-id="03b5d-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

![Borrar datos de exploración desde el panel Configuración de Microsoft Edge](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a><span data-ttu-id="03b5d-128">Lista de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="03b5d-128">Storage list</span></span>  

<span data-ttu-id="03b5d-129">En la tabla de lista Almacenamiento puede:</span><span class="sxs-lookup"><span data-stu-id="03b5d-129">From the Storage list table you can:</span></span>  

*   <span data-ttu-id="03b5d-130">**Inspeccione y ordene** `key/value` los pares haciendo clic en el nombre de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="03b5d-130">**Inspect and sort** your `key/value` pairs by clicking on either column name in the table.</span></span>  
*   <span data-ttu-id="03b5d-131">**Edite** `Key` el y de una entrada existente haciendo clic en la `Value` celda.</span><span class="sxs-lookup"><span data-stu-id="03b5d-131">**Edit** the `Key` and `Value` of an existing entry by clicking in the cell.</span></span>  
*   <span data-ttu-id="03b5d-132">**Eliminar** \( \) una entrada de la opción del menú contextual con el botón `Del` secundario, **Eliminar elemento**.</span><span class="sxs-lookup"><span data-stu-id="03b5d-132">**Delete** \(`Del`\) an entry from the right-click context menu option, **Delete item**.</span></span>  
*   <span data-ttu-id="03b5d-133">**Agregue** un par `key/value` nuevo haciendo clic en la fila vacía de la parte inferior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="03b5d-133">**Add** a new `key/value` pair by clicking on the empty row at the bottom of the table.</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="03b5d-134">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="03b5d-134">Shortcuts</span></span>

| <span data-ttu-id="03b5d-135">Acción</span><span class="sxs-lookup"><span data-stu-id="03b5d-135">Action</span></span> | <span data-ttu-id="03b5d-136">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="03b5d-136">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="03b5d-137">Actualizar</span><span class="sxs-lookup"><span data-stu-id="03b5d-137">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="03b5d-138">Eliminar elemento</span><span class="sxs-lookup"><span data-stu-id="03b5d-138">Delete item</span></span> | `Del` |  
| <span data-ttu-id="03b5d-139">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="03b5d-139">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="03b5d-140">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="03b5d-140">Select all</span></span> | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a><span data-ttu-id="03b5d-141">Administrador de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="03b5d-141">IndexedDB manager</span></span>  

<span data-ttu-id="03b5d-142">Use la **pestaña IndexedDB** para inspeccionar y administrar los datos estructurados almacenados localmente en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="03b5d-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span>  <span data-ttu-id="03b5d-143">En concreto, puede inspeccionar/ordenar y actualizar los almacenes e índices de objetos, y también eliminar entradas de clave-valor individuales.</span><span class="sxs-lookup"><span data-stu-id="03b5d-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>  

> [!TIP]
> <span data-ttu-id="03b5d-144">Puede usar nuestra demostración [del mezclador de audio](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) para probar la unidad del administrador de *IndexedDB* en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="03b5d-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="03b5d-145">Para eliminar todos los datos IndexedDB almacenados para el usuario actual en Microsoft Edge, use el menú Configuración **de** Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="03b5d-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge **Settings** menu:</span></span>  

<span data-ttu-id="03b5d-146">**...** >  **Configuración**  >  **Borrar datos de exploración**  >  **Cookies y datos guardados del sitio web**</span><span class="sxs-lookup"><span data-stu-id="03b5d-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

<span data-ttu-id="03b5d-147">La carpeta dentro del selector de recursos del depurador muestra una lista de orígenes de `IndexedDB` los recursos cargados por la página. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="03b5d-147">The `IndexedDB` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="03b5d-148">Las bases de datos IndexedDB \(IDB\) aparecerán en el origen, junto con sus almacenes de objetos.</span><span class="sxs-lookup"><span data-stu-id="03b5d-148">Any IndexedDB \(IDB\) databases will be listed under the origin, along with their object stores.</span></span>  

![Administrador de IndexedDB de DevTools](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a><span data-ttu-id="03b5d-150">Barra de herramientas IndexedDB</span><span class="sxs-lookup"><span data-stu-id="03b5d-150">IndexedDB Toolbar</span></span>  

<span data-ttu-id="03b5d-151">Desde la barra de herramientas IndexedDB puede:</span><span class="sxs-lookup"><span data-stu-id="03b5d-151">From the IndexedDB toolbar you can:</span></span>  

*   <span data-ttu-id="03b5d-152">**Actualice** \( `Ctrl` + `F5` \) para ver las entradas actuales en el almacén de objetos o el índice de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="03b5d-152">**Refresh** \(`Ctrl`+`F5`\) to see the current entries in the object store or index of your database.</span></span>  <span data-ttu-id="03b5d-153">El administrador de IndexedDB no se actualiza automáticamente cuando se realizan cambios en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="03b5d-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>  

### <a name="object-store-entries-list"></a><span data-ttu-id="03b5d-154">Lista de entradas del almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="03b5d-154">Object store entries list</span></span>  

<span data-ttu-id="03b5d-155">Desde el almacén de objetos o la tabla Índice puede:</span><span class="sxs-lookup"><span data-stu-id="03b5d-155">From the Object store or Index table you can:</span></span>  

*   <span data-ttu-id="03b5d-156">**Inspeccione y ordene** los pares clave-valor haciendo clic en cualquier nombre de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="03b5d-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="03b5d-157">**Actualizar** \( `Ctrl` + `F5` \)</span><span class="sxs-lookup"><span data-stu-id="03b5d-157">**Refresh** \(`Ctrl`+`F5`\)</span></span>  
*   <span data-ttu-id="03b5d-158">**Eliminar elemento** \( `Del` \) para quitar la entrada seleccionada en el índice o el almacén de objetos.</span><span class="sxs-lookup"><span data-stu-id="03b5d-158">**Delete item** \(`Del`\) to remove the selected entry in your object store or index.</span></span>  <span data-ttu-id="03b5d-159">También puede hacerlo desde la opción de menú [contextual](#context-menu) Clic con el botón secundario, **Eliminar elemento**.</span><span class="sxs-lookup"><span data-stu-id="03b5d-159">You can also do this from the right-click [context menu](#context-menu) option, **Delete item**.</span></span>  
*   <span data-ttu-id="03b5d-160">**Copie los elementos seleccionados** `Ctrl` + `C` \( \) para copiar el elemento seleccionado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="03b5d-160">**Copy selected items** \(`Ctrl`+`C`\) to copy the selected item to your clipboard.</span></span>  <span data-ttu-id="03b5d-161">También puede hacerlo desde la opción de menú [contextual](#context-menu) clic con el botón derecho, **Copiar elemento seleccionado**.</span><span class="sxs-lookup"><span data-stu-id="03b5d-161">You can also do this from the right-click [context menu](#context-menu) option, **Copy selected item**.</span></span>  
*   <span data-ttu-id="03b5d-162">**Seleccione todo** \( \) para seleccionar todas las entradas del índice o `Ctrl` + `A` almacén de objetos.</span><span class="sxs-lookup"><span data-stu-id="03b5d-162">**Select all** \(`Ctrl`+`A`\) to select all the entries in your object store or index.</span></span>  <span data-ttu-id="03b5d-163">También puede hacerlo desde la opción de menú [contextual](#context-menu) clic con el botón derecho, **Seleccionar todo**.</span><span class="sxs-lookup"><span data-stu-id="03b5d-163">You can also do this from the right-click [context menu](#context-menu) option, **Select all**.</span></span>  

<span data-ttu-id="03b5d-164">Las columnas del almacén de objetos o la tabla Index se pueden ordenar:</span><span class="sxs-lookup"><span data-stu-id="03b5d-164">The columns of the Object store or Index table are sortable:</span></span>  

| <span data-ttu-id="03b5d-165">Columna</span><span class="sxs-lookup"><span data-stu-id="03b5d-165">Column</span></span> | <span data-ttu-id="03b5d-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="03b5d-166">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="03b5d-167">Key</span><span class="sxs-lookup"><span data-stu-id="03b5d-167">Key</span></span> | <span data-ttu-id="03b5d-168">Nombre del par clave-valor \(igual que **la clave principal**\) al iterar por un almacén de objetos; Nombre de la clave de índice \(tecla actual del cursor\) al iterar sobre un índice</span><span class="sxs-lookup"><span data-stu-id="03b5d-168">Name of the key-value pair \(same as **Primary Key**\) when iterating over an object store; Name of the index key \(cursor's current key\) when iterating over an index</span></span> |  
| <span data-ttu-id="03b5d-169">Clave principal</span><span class="sxs-lookup"><span data-stu-id="03b5d-169">Primary Key</span></span> | <span data-ttu-id="03b5d-170">Nombre del par clave-valor \(see **MDN web docs** for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span><span class="sxs-lookup"><span data-stu-id="03b5d-170">Name of the key-value pair \(see **MDN web docs** for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span></span> |  
| <span data-ttu-id="03b5d-171">Valor</span><span class="sxs-lookup"><span data-stu-id="03b5d-171">Value</span></span> | <span data-ttu-id="03b5d-172">Valor del par clave-valor</span><span class="sxs-lookup"><span data-stu-id="03b5d-172">Value of the key-value pair</span></span> |  

<span data-ttu-id="03b5d-173">Consulte *documentos web de MDN* para obtener más información sobre los conceptos y el uso [de IndexedDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span><span class="sxs-lookup"><span data-stu-id="03b5d-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>  

### <a name="context-menu"></a><span data-ttu-id="03b5d-174">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="03b5d-174">Context menu</span></span>  

<span data-ttu-id="03b5d-175">Además de la barra de herramientas [ *IndexedDB,* ](#indexeddb-toolbar)también puede administrar los datos \*\*\*\* en almacenes de objetos o índices desde el menú Contextual y/o los [métodos abreviados de teclado](#shortcuts).</span><span class="sxs-lookup"><span data-stu-id="03b5d-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="03b5d-176">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="03b5d-176">Shortcuts</span></span>

| <span data-ttu-id="03b5d-177">Acción</span><span class="sxs-lookup"><span data-stu-id="03b5d-177">Action</span></span> | <span data-ttu-id="03b5d-178">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="03b5d-178">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="03b5d-179">Actualizar</span><span class="sxs-lookup"><span data-stu-id="03b5d-179">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="03b5d-180">Eliminar par clave-valor</span><span class="sxs-lookup"><span data-stu-id="03b5d-180">Delete key-value pair</span></span> | `Del` |  
| <span data-ttu-id="03b5d-181">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="03b5d-181">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="03b5d-182">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="03b5d-182">Select all</span></span> | `Ctrl +`<span data-ttu-id="03b5d-183">A'</span><span class="sxs-lookup"><span data-stu-id="03b5d-183">A\`</span></span> |  

## <a name="cookies-manager"></a><span data-ttu-id="03b5d-184">Administrador de cookies</span><span class="sxs-lookup"><span data-stu-id="03b5d-184">Cookies manager</span></span>  

<span data-ttu-id="03b5d-185">Use el administrador de cookies para inspeccionar y administrar las cookies del dominio determinado.</span><span class="sxs-lookup"><span data-stu-id="03b5d-185">Use the Cookies manager to inspect and manage the cookies for the given domain.</span></span>  

<span data-ttu-id="03b5d-186">La carpeta dentro del selector de recursos del depurador muestra una lista de orígenes de `Cookies` los recursos cargados por la página. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="03b5d-186">The `Cookies` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="03b5d-187">Al seleccionar uno de estos fotogramas se abre una tabla que representa las cookies actuales establecidas por el encabezado [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) o mediante un script [con Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span><span class="sxs-lookup"><span data-stu-id="03b5d-187">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>  

![Administrador de cookies de DevTools](./media/storage_cookies.png)  

<span data-ttu-id="03b5d-189">En la barra de herramientas de la pestaña Cookies puede:</span><span class="sxs-lookup"><span data-stu-id="03b5d-189">From the Cookies tab toolbar you can:</span></span>  

*   <span data-ttu-id="03b5d-190">**Actualice** \( `Ctrl` + `F5` \) la lista [cookies](#cookies-list) para ver el conjunto actual de cookies para el dominio determinado.</span><span class="sxs-lookup"><span data-stu-id="03b5d-190">**Refresh** \(`Ctrl`+`F5`\) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span>  <span data-ttu-id="03b5d-191">\(La lista no se actualiza automáticamente.\)</span><span class="sxs-lookup"><span data-stu-id="03b5d-191">\(The list does not auto-refresh.\)</span></span>  
*   <span data-ttu-id="03b5d-192">**Elimine todas las cookies** `Ctrl` + `Shift` + `Del` \( \) \(session y permanent\) de la ruta de acceso de la página actual.</span><span class="sxs-lookup"><span data-stu-id="03b5d-192">**Delete all cookies** \(`Ctrl`+`Shift`+`Del`\) \(session and permanent\) for the path of the current page.</span></span>  
*   <span data-ttu-id="03b5d-193">**Elimine todas las cookies de sesión** `Ctrl` + `Del` \( \) de la ruta de acceso de la página actual.</span><span class="sxs-lookup"><span data-stu-id="03b5d-193">**Delete all session cookies** \(`Ctrl`+`Del`\) for the path of the current page.</span></span>  

<span data-ttu-id="03b5d-194">Para borrar completamente la lista de cookies, es posible que deba borrar todas **las cookies** del dominio desde la barra de [herramientas del](./network.md#toolbar) panel Red.</span><span class="sxs-lookup"><span data-stu-id="03b5d-194">To completely clear your Cookies list, you might need to **Clear all cookies for the domain** from the [Network](./network.md#toolbar) panel toolbar.</span></span>  

### <a name="cookies-list"></a><span data-ttu-id="03b5d-195">Lista de cookies</span><span class="sxs-lookup"><span data-stu-id="03b5d-195">Cookies list</span></span>  

<span data-ttu-id="03b5d-196">En la tabla de lista Cookies puede:</span><span class="sxs-lookup"><span data-stu-id="03b5d-196">From the Cookies list table you can:</span></span>  

*   <span data-ttu-id="03b5d-197">**Inspeccione y ordene** las cookies haciendo clic en cualquier nombre de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="03b5d-197">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="03b5d-198">**Edite** `Name` el y de una cookie existente haciendo clic en la `Value` celda.</span><span class="sxs-lookup"><span data-stu-id="03b5d-198">**Edit** the `Name` and `Value` of an existing cookie by clicking in the cell.</span></span>  
*   <span data-ttu-id="03b5d-199">**Eliminar** \( \) una cookie de la opción del menú contextual con el botón `Del` secundario, [](#context-menu) `Delete cookie` .</span><span class="sxs-lookup"><span data-stu-id="03b5d-199">**Delete** \(`Del`\) a cookie from the right-click [context menu](#context-menu) option, `Delete cookie`.</span></span>  
*   <span data-ttu-id="03b5d-200">**Agregue** una nueva cookie de sesión para el dado `Domain/Path` haciendo clic en la fila vacía en la parte inferior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="03b5d-200">**Add** a new session cookie for the given `Domain/Path` by clicking on the empty row at the bottom of the table.</span></span>  <span data-ttu-id="03b5d-201">Esto solo funciona para las cookies de sesión; las cookies permanentes \(con fechas de expiración específicas\) deben establecerse con métodos tradicionales.</span><span class="sxs-lookup"><span data-stu-id="03b5d-201">This only works for session cookies; permanent cookies \(with specific expiry dates\) must be set with traditional methods.</span></span>  <span data-ttu-id="03b5d-202">Los `Domain` valores y se `Path` rellenan automáticamente según la ubicación de la página.</span><span class="sxs-lookup"><span data-stu-id="03b5d-202">The `Domain` and `Path` values are auto-filled according to the location of the page.</span></span>  

<span data-ttu-id="03b5d-203">Las columnas de la lista cookies se pueden ordenar:</span><span class="sxs-lookup"><span data-stu-id="03b5d-203">The columns of the Cookies list are sortable:</span></span>

| <span data-ttu-id="03b5d-204">Columna</span><span class="sxs-lookup"><span data-stu-id="03b5d-204">Column</span></span> | <span data-ttu-id="03b5d-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="03b5d-205">Description</span></span> |  
| :--- | :--- |  
| <span data-ttu-id="03b5d-206">Name</span><span class="sxs-lookup"><span data-stu-id="03b5d-206">Name</span></span> | <span data-ttu-id="03b5d-207">Nombre de la cookie</span><span class="sxs-lookup"><span data-stu-id="03b5d-207">Name of the cookie</span></span> |  
| <span data-ttu-id="03b5d-208">Valor</span><span class="sxs-lookup"><span data-stu-id="03b5d-208">Value</span></span> | <span data-ttu-id="03b5d-209">Valor de la cookie</span><span class="sxs-lookup"><span data-stu-id="03b5d-209">Value of the cookie</span></span> |  
| <span data-ttu-id="03b5d-210">Dominio</span><span class="sxs-lookup"><span data-stu-id="03b5d-210">Domain</span></span> | <span data-ttu-id="03b5d-211">Nombre de host de la cookie \(puede estar vacío\)</span><span class="sxs-lookup"><span data-stu-id="03b5d-211">Host name of the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="03b5d-212">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="03b5d-212">Path</span></span> | <span data-ttu-id="03b5d-213">Ruta de acceso url para la cookie \(puede estar vacía\)</span><span class="sxs-lookup"><span data-stu-id="03b5d-213">URL path for the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="03b5d-214">Expira</span><span class="sxs-lookup"><span data-stu-id="03b5d-214">Expires</span></span> | <span data-ttu-id="03b5d-215">Duración máxima de la cookie como marca de tiempo de fecha HTTP.</span><span class="sxs-lookup"><span data-stu-id="03b5d-215">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span>  <span data-ttu-id="03b5d-216">Si no `Expires` se `Max-Age` estableció o no, la entrada se considera una cookie de sesión.</span><span class="sxs-lookup"><span data-stu-id="03b5d-216">If no `Expires` or `Max-Age` was set, the entry is considered a Session cookie.</span></span>  |  
| <span data-ttu-id="03b5d-217">Solo HTTP</span><span class="sxs-lookup"><span data-stu-id="03b5d-217">HTTP only</span></span> | <span data-ttu-id="03b5d-218">Indica si la cookie se estableció con directiva, lo que indica que no es `HttpOnly` accesible desde JavaScript</span><span class="sxs-lookup"><span data-stu-id="03b5d-218">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span> |  
| <span data-ttu-id="03b5d-219">Seguro</span><span class="sxs-lookup"><span data-stu-id="03b5d-219">Secure</span></span> | <span data-ttu-id="03b5d-220">Indica si la cookie se estableció con la directiva, lo que indica que solo se enviará al servidor desde una solicitud mediante SSL y `Secure` el protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="03b5d-220">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>  |  

<span data-ttu-id="03b5d-221">Consulta la referencia [set-cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) de documentos web de **MDN** para obtener más información sobre las propiedades de las cookies.</span><span class="sxs-lookup"><span data-stu-id="03b5d-221">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>  

### <a name="context-menu"></a><span data-ttu-id="03b5d-222">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="03b5d-222">Context menu</span></span>  

<span data-ttu-id="03b5d-223">Además de la barra de herramientas [de](#cookies-manager)la pestaña Cookies, también puede administrar las cookies desde el menú contextual y/o los [métodos abreviados de teclado.](#shortcuts) \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03b5d-223">In addition to the Cookies tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="03b5d-224">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="03b5d-224">Shortcuts</span></span>  

| <span data-ttu-id="03b5d-225">Acción</span><span class="sxs-lookup"><span data-stu-id="03b5d-225">Action</span></span> | <span data-ttu-id="03b5d-226">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="03b5d-226">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="03b5d-227">Actualizar</span><span class="sxs-lookup"><span data-stu-id="03b5d-227">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="03b5d-228">Eliminar cookie</span><span class="sxs-lookup"><span data-stu-id="03b5d-228">Delete cookie</span></span> | `Del` |  
| <span data-ttu-id="03b5d-229">Eliminar todas las cookies</span><span class="sxs-lookup"><span data-stu-id="03b5d-229">Delete all cookies</span></span> | `Ctrl`+`Shift`+`Del` |  
| <span data-ttu-id="03b5d-230">Eliminar todas las cookies de sesión</span><span class="sxs-lookup"><span data-stu-id="03b5d-230">Delete all session cookies</span></span> | `Ctrl`+`Del` |  
| <span data-ttu-id="03b5d-231">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="03b5d-231">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="03b5d-232">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="03b5d-232">Select all</span></span> | `Ctrl`+`A` |  

### <a name="cache-manager"></a><span data-ttu-id="03b5d-233">Administrador de caché</span><span class="sxs-lookup"><span data-stu-id="03b5d-233">Cache manager</span></span>  

<span data-ttu-id="03b5d-234">Al hacer clic en una entrada \*\*\*\* de caché específica, se abrirá el administrador de caché de trabajo de servicio, donde puede inspeccionar y eliminar opcionalmente entradas de caché \( y pares `Request` `Response` clave/valor\):</span><span class="sxs-lookup"><span data-stu-id="03b5d-234">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries \(`Request` and `Response` key/value pairs\):</span></span>  

![Administrador de caché](./media/storage_cache.png)  

### <a name="shortcuts"></a><span data-ttu-id="03b5d-236">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="03b5d-236">Shortcuts</span></span>  

#### <a name="cache-manager"></a><span data-ttu-id="03b5d-237">Administrador de caché</span><span class="sxs-lookup"><span data-stu-id="03b5d-237">Cache manager</span></span>  

| <span data-ttu-id="03b5d-238">Acción</span><span class="sxs-lookup"><span data-stu-id="03b5d-238">Action</span></span> | <span data-ttu-id="03b5d-239">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="03b5d-239">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="03b5d-240">Actualizar</span><span class="sxs-lookup"><span data-stu-id="03b5d-240">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="03b5d-241">Eliminar elemento</span><span class="sxs-lookup"><span data-stu-id="03b5d-241">Delete item</span></span> | `Del` |  
| <span data-ttu-id="03b5d-242">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="03b5d-242">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="03b5d-243">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="03b5d-243">Select all</span></span> | `Ctrl`+`A` |  
