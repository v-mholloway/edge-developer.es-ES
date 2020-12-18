---
description: Usar el panel de almacenamiento para inspeccionar el almacenamiento Web, IndexedDB, cookies y las memorias caché de solicitudes/respuestas
title: 'DevTools: almacenamiento'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, almacenamiento Web, almacenamiento local, almacenamiento de sesión, IndexedDB, cookies, trabajo de servicio, caché
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 90a2e2fdb0f329c3d83f52beb9eba169bdd48520
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235993"
---
# <span data-ttu-id="104de-104">Almacenamiento</span><span class="sxs-lookup"><span data-stu-id="104de-104">Storage</span></span>

<span data-ttu-id="104de-105">Use el panel **almacenamiento** para inspeccionar y administrar diversos datos de la caché local, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="104de-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>

 - <span data-ttu-id="104de-106">Pares de clave y valor de [almacenamiento web](#local-and-session-storage-managers) (almacenamiento*local* y de *sesión* )</span><span class="sxs-lookup"><span data-stu-id="104de-106">[Web storage](#local-and-session-storage-managers) (*Local* and *Session* storage) key/values pairs</span></span>
 - <span data-ttu-id="104de-107">Datos estructurados de la base de datos [indizados](#indexeddb-manager)</span><span class="sxs-lookup"><span data-stu-id="104de-107">[Indexed DB](#indexeddb-manager) structured data</span></span>
 - <span data-ttu-id="104de-108">[Cookies](#cookies-list) para el dominio</span><span class="sxs-lookup"><span data-stu-id="104de-108">[Cookies](#cookies-list) for the domain</span></span>
 - <span data-ttu-id="104de-109">[Caché](#cache-manager) (pares de solicitud y respuesta) para la depuración de trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="104de-109">[Cache](#cache-manager) (request/response pairs) for service worker debugging</span></span>

<span data-ttu-id="104de-110">Expanda cualquiera de estas categorías y haga clic en una entrada secundaria para abrir su ficha de administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="104de-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>

## <span data-ttu-id="104de-111">Administradores de almacenamiento local y de sesión</span><span class="sxs-lookup"><span data-stu-id="104de-111">Local and Session storage managers</span></span>

<span data-ttu-id="104de-112">Use el *Administrador* de almacenamiento local y el *Administrador de almacenamiento de sesión* para inspeccionar y administrar el almacenamiento Web de la página.</span><span class="sxs-lookup"><span data-stu-id="104de-112">Use the *Local Storage manager* and *Session Storage manager* to inspect and manage the web storage for  your page.</span></span> 

<span data-ttu-id="104de-113">Las carpetas **almacenamiento local** y **almacenamiento de sesión** en el selector de [*recursos*](./debugger.md#resource-picker) del panel de almacenamiento muestran una lista de orígenes de la página.</span><span class="sxs-lookup"><span data-stu-id="104de-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [*Resource picker*](./debugger.md#resource-picker) display a list of origins for the page.</span></span> <span data-ttu-id="104de-114">Al seleccionar uno de estos marcos, se abre una tabla editable de los pares de clave y valor actuales establecido a través de [window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) o [window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivamente (o establecido directamente desde la [lista de almacenamiento](#storage-list)de DevTools).</span><span class="sxs-lookup"><span data-stu-id="104de-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively (and/or set directly from the  DevTools [Storage list](#storage-list)).</span></span>

![DevTools local Storage Manager](./media/storage_web_storage.png)

<span data-ttu-id="104de-116">En las pestañas *almacenamiento local* y *almacenamiento de sesiones* , puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="104de-116">From the *Local Storage* and *Session Storage* tabs you can:</span></span>

 - <span data-ttu-id="104de-117">**Refresh** ( `Ctrl+F5` ) la [lista de almacenamiento](#cookies-list) para ver el conjunto actual de pares clave/valor para el dominio dado.</span><span class="sxs-lookup"><span data-stu-id="104de-117">**Refresh** (`Ctrl+F5`) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span> <span data-ttu-id="104de-118">(La lista no se actualiza automáticamente en las actualizaciones de script).</span><span class="sxs-lookup"><span data-stu-id="104de-118">(The list does not auto-refresh upon script updates.)</span></span>
 - <span data-ttu-id="104de-119">**Simular alcanzar el límite de almacenamiento** para almacenamiento Web Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="104de-119">**Simulate reaching the storage limit** for Microsoft Edge web storage.</span></span> <span data-ttu-id="104de-120">Cada dominio y subdominio tiene su propia área de almacenamiento, pero hay un límite combinado:</span><span class="sxs-lookup"><span data-stu-id="104de-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>
    - <span data-ttu-id="104de-121">**Subdominios:** hasta 5 MB de espacio</span><span class="sxs-lookup"><span data-stu-id="104de-121">**Subdomains:** up to 5 MBs of space</span></span>
    - <span data-ttu-id="104de-122">**Dominios:** hasta 10 MB de espacio</span><span class="sxs-lookup"><span data-stu-id="104de-122">**Domains:** up to 10 MBs of space</span></span>
    - <span data-ttu-id="104de-123">**Total para todos los dominios:** hasta 50 MB de espacio</span><span class="sxs-lookup"><span data-stu-id="104de-123">**Total for all domains:** up to 50 MBs of space</span></span>

   <span data-ttu-id="104de-124">El almacenamiento de sesión se borra tan pronto como se cierre la última ficha del explorador que hace referencia a su origen.</span><span class="sxs-lookup"><span data-stu-id="104de-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span> <span data-ttu-id="104de-125">Las entradas de almacenamiento local continúan de forma indefinida hasta que la página la borra mediante programación o manualmente por el usuario:</span><span class="sxs-lookup"><span data-stu-id="104de-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>

   <span data-ttu-id="104de-126">**Configuración**  >  **Borrar datos**  >  de exploración **Cookies y datos de sitios web guardados**</span><span class="sxs-lookup"><span data-stu-id="104de-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

![Desactivar la navegación de datos desde el panel de configuración de Microsoft Edge](./media/settings_clear_browsing_data.png)

### <span data-ttu-id="104de-128">Lista de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="104de-128">Storage list</span></span>

<span data-ttu-id="104de-129">En la tabla *lista de almacenamiento* , puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="104de-129">From the *Storage list* table you can:</span></span>

 - <span data-ttu-id="104de-130">**Inspeccione y ordene** las parejas de clave y valor haciendo clic en uno de los nombres de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="104de-130">**Inspect and sort** your key/value pairs by clicking on either column name in the table.</span></span>
 - <span data-ttu-id="104de-131">**Edite** la *clave* y el *valor* de una entrada existente haciendo clic en la celda.</span><span class="sxs-lookup"><span data-stu-id="104de-131">**Edit** the *Key* and *Value* of an existing entry by clicking in the cell.</span></span>
 - <span data-ttu-id="104de-132">**Eliminar** ( `Del` ) una entrada de la opción del menú contextual de clic derecho, *Eliminar elemento*.</span><span class="sxs-lookup"><span data-stu-id="104de-132">**Delete** (`Del`) an entry from the right-click context menu option, *Delete item*.</span></span>
 - <span data-ttu-id="104de-133">**Agregue** un nuevo par de clave/valor haciendo clic en la fila vacía de la parte inferior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="104de-133">**Add** a new key/value pair by clicking on the empty row at the bottom of the table.</span></span>


### <span data-ttu-id="104de-134">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="104de-134">Shortcuts</span></span>

| <span data-ttu-id="104de-135">Acción</span><span class="sxs-lookup"><span data-stu-id="104de-135">Action</span></span>              | <span data-ttu-id="104de-136">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="104de-136">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="104de-137">Actualizar</span><span class="sxs-lookup"><span data-stu-id="104de-137">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="104de-138">Eliminar elemento</span><span class="sxs-lookup"><span data-stu-id="104de-138">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="104de-139">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="104de-139">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="104de-140">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="104de-140">Select all</span></span>          | `Ctrl` + `A`  |


## <span data-ttu-id="104de-141">IndexedDB Manager</span><span class="sxs-lookup"><span data-stu-id="104de-141">IndexedDB manager</span></span>

<span data-ttu-id="104de-142">Use la pestaña **IndexedDB** para inspeccionar y administrar los datos estructurados almacenados de forma local en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="104de-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span> <span data-ttu-id="104de-143">En concreto, puede inspeccionar/ordenar y actualizar los índices y los almacenes de objetos, así como eliminar entradas de clave y valor individuales.</span><span class="sxs-lookup"><span data-stu-id="104de-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>

> [!TIP]
> <span data-ttu-id="104de-144">Puede usar nuestra demostración de [mezclador de audio](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) para probar el *Administrador de IndexedDB* en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="104de-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>

<span data-ttu-id="104de-145">Para eliminar todos los datos de IndexedDB almacenados para el usuario actual en Microsoft Edge, usa el menú de *configuración* de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="104de-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge *Settings* menu:</span></span>

<span data-ttu-id="104de-146">**...** >  **Configuración**  >  **Borrar datos**  >  de exploración **Cookies y datos de sitios web guardados**</span><span class="sxs-lookup"><span data-stu-id="104de-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

<span data-ttu-id="104de-147">La carpeta **IndexedDB** dentro del [*selector de recursos*](./debugger.md#resource-picker) del depurador muestra una lista de orígenes de los recursos cargados por la página.</span><span class="sxs-lookup"><span data-stu-id="104de-147">The **IndexedDB** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="104de-148">Todas las bases de datos IndexedDB (IDB) aparecerán debajo del origen, junto con sus almacenes de objetos.</span><span class="sxs-lookup"><span data-stu-id="104de-148">Any IndexedDB (IDB) databases will be listed under the origin, along with their object stores.</span></span> 

![DevTools IndexedDB Manager](./media/storage_indexeddb.png)

### <span data-ttu-id="104de-150">Barra de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="104de-150">IndexedDB Toolbar</span></span>

<span data-ttu-id="104de-151">Desde la barra de herramientas de *IndexedDB* puedes hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="104de-151">From the *IndexedDB* toolbar you can:</span></span>

 - <span data-ttu-id="104de-152">**Actualizar** ( `Ctrl+F5` ) para ver las entradas actuales en el almacén de objetos o el índice de su base de datos.</span><span class="sxs-lookup"><span data-stu-id="104de-152">**Refresh** (`Ctrl+F5`) to see the current entries in the object store or index of your database.</span></span> <span data-ttu-id="104de-153">El administrador de IndexedDB no se actualiza automáticamente cuando se realizan cambios en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="104de-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>

### <span data-ttu-id="104de-154">Lista de entradas del almacén de objetos</span><span class="sxs-lookup"><span data-stu-id="104de-154">Object store entries list</span></span>

<span data-ttu-id="104de-155">Desde la tabla *almacén de objetos* o *Índice* , puede:</span><span class="sxs-lookup"><span data-stu-id="104de-155">From the *Object store* or *Index* table you can:</span></span>

 - <span data-ttu-id="104de-156">**Inspeccione y ordene** los pares clave-valor haciendo clic en cualquier nombre de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="104de-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="104de-157">**Actualizar** ( `Ctrl+F5` )</span><span class="sxs-lookup"><span data-stu-id="104de-157">**Refresh** (`Ctrl+F5`)</span></span>
 - <span data-ttu-id="104de-158">**Eliminar elemento** ( `Del` ) para quitar la entrada seleccionada en el almacén de objetos o en el índice.</span><span class="sxs-lookup"><span data-stu-id="104de-158">**Delete item** (`Del`) to remove the selected entry in your object store or index.</span></span> <span data-ttu-id="104de-159">También puede hacer esto desde la opción del [menú contextual](#context-menu) al hacer clic con el botón derecho, *Eliminar elemento*.</span><span class="sxs-lookup"><span data-stu-id="104de-159">You can also do this from the right-click [context menu](#context-menu) option, *Delete item*.</span></span>
 - <span data-ttu-id="104de-160">**Copiar elementos seleccionados** ( `Ctrl+C` ) para copiar el elemento seleccionado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="104de-160">**Copy selected items** (`Ctrl+C`) to copy the selected item to your clipboard.</span></span> <span data-ttu-id="104de-161">También puede hacer esto desde la opción del [menú contextual](#context-menu) al hacer clic con el botón derecho, *copiar el elemento seleccionado*.</span><span class="sxs-lookup"><span data-stu-id="104de-161">You can also do this from the right-click [context menu](#context-menu) option, *Copy selected item*.</span></span>
 - <span data-ttu-id="104de-162">**Seleccione todos** ( `Ctrl+A` ) para seleccionar todas las entradas del almacén de objetos o del índice.</span><span class="sxs-lookup"><span data-stu-id="104de-162">**Select all** (`Ctrl+A`) to select all the entries in your object store or index.</span></span> <span data-ttu-id="104de-163">También puede hacer esto desde la opción del [menú contextual](#context-menu) de clic derecho, *seleccionar todo*.</span><span class="sxs-lookup"><span data-stu-id="104de-163">You can also do this from the right-click [context menu](#context-menu) option, *Select all*.</span></span>

<span data-ttu-id="104de-164">Las columnas de la tabla de *Índice* o el *almacén de objetos* se pueden ordenar:</span><span class="sxs-lookup"><span data-stu-id="104de-164">The columns of the *Object store* or *Index* table are sortable:</span></span>

<span data-ttu-id="104de-165">Columna</span><span class="sxs-lookup"><span data-stu-id="104de-165">Column</span></span> | <span data-ttu-id="104de-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="104de-166">Description</span></span>
:------------ | :-------------
<span data-ttu-id="104de-167">Key</span><span class="sxs-lookup"><span data-stu-id="104de-167">Key</span></span> | <span data-ttu-id="104de-168">Nombre del par clave-valor (igual que la *clave principal*) al recorrer en iteración un almacén de objetos; Nombre de la clave de índice (clave actual del cursor) cuando se recorre en iteración un índice</span><span class="sxs-lookup"><span data-stu-id="104de-168">Name of the key-value pair (same as *Primary Key*) when iterating over an object store; Name of the index key (cursor's current key) when iterating over an index</span></span>
<span data-ttu-id="104de-169">Clave principal</span><span class="sxs-lookup"><span data-stu-id="104de-169">Primary Key</span></span> | <span data-ttu-id="104de-170">Nombre del par clave-valor (vea los *documentos web de MDN* para obtener más información sobre [las claves](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)de la IDB)</span><span class="sxs-lookup"><span data-stu-id="104de-170">Name of the key-value pair (see *MDN web docs* for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database))</span></span>
<span data-ttu-id="104de-171">Valor</span><span class="sxs-lookup"><span data-stu-id="104de-171">Value</span></span> | <span data-ttu-id="104de-172">Valor del par clave-valor</span><span class="sxs-lookup"><span data-stu-id="104de-172">Value of the key-value pair</span></span>

<span data-ttu-id="104de-173">Consulte los *documentos web de MDN* para obtener más información sobre los [conceptos y el uso de IndexedDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span><span class="sxs-lookup"><span data-stu-id="104de-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>

### <span data-ttu-id="104de-174">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="104de-174">Context menu</span></span>

<span data-ttu-id="104de-175">Además de la [barra de herramientas *IndexedDB* ](#indexeddb-toolbar), también puede administrar los datos en almacenes o índices de objetos desde el **menú contextual** o los [métodos abreviados](#shortcuts)de teclado del botón secundario del ratón.</span><span class="sxs-lookup"><span data-stu-id="104de-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="104de-176">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="104de-176">Shortcuts</span></span>

<span data-ttu-id="104de-177">Acción</span><span class="sxs-lookup"><span data-stu-id="104de-177">Action</span></span> | <span data-ttu-id="104de-178">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="104de-178">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="104de-179">Actualizar</span><span class="sxs-lookup"><span data-stu-id="104de-179">Refresh</span></span> | `Ctrl` + `F5`
<span data-ttu-id="104de-180">Eliminar par clave-valor</span><span class="sxs-lookup"><span data-stu-id="104de-180">Delete key-value pair</span></span> | `Del`
<span data-ttu-id="104de-181">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="104de-181">Copy selected items</span></span> | `Ctrl` + `C`
<span data-ttu-id="104de-182">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="104de-182">Select all</span></span> | `Ctrl` + `A`

## <span data-ttu-id="104de-183">Administrador de cookies</span><span class="sxs-lookup"><span data-stu-id="104de-183">Cookies manager</span></span>

<span data-ttu-id="104de-184">Use el *Administrador de cookies* para inspeccionar y administrar las cookies para el dominio dado.</span><span class="sxs-lookup"><span data-stu-id="104de-184">Use the *Cookies manager* to inspect and manage the cookies for the given domain.</span></span> 

<span data-ttu-id="104de-185">La carpeta **cookies** dentro del selector de [*recursos*](./debugger.md#resource-picker) del depurador muestra una lista de orígenes de los recursos cargados por la página.</span><span class="sxs-lookup"><span data-stu-id="104de-185">The **Cookies** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="104de-186">Al seleccionar uno de estos marcos, se abre una tabla que representa las cookies actuales que ha establecido el encabezado [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) o mediante una secuencia de comandos con [Document. cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span><span class="sxs-lookup"><span data-stu-id="104de-186">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>

![Administrador de cookies de DevTools](./media/storage_cookies.png)

<span data-ttu-id="104de-188">En la barra de herramientas de la pestaña *cookies* puede:</span><span class="sxs-lookup"><span data-stu-id="104de-188">From the *Cookies* tab toolbar you can:</span></span>

 - <span data-ttu-id="104de-189">**Actualizar** ( `Ctrl+F5` ) la [lista de cookies](#cookies-list) para ver el conjunto actual de cookies para el dominio dado.</span><span class="sxs-lookup"><span data-stu-id="104de-189">**Refresh** (`Ctrl+F5`) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span> <span data-ttu-id="104de-190">(La lista no se actualiza automáticamente).</span><span class="sxs-lookup"><span data-stu-id="104de-190">(The list does not auto-refresh.)</span></span>
 - <span data-ttu-id="104de-191">**Elimine todas las cookies** ( `Ctrl+Shift+Del` sesión y permanente) de la ruta de acceso de la página actual.</span><span class="sxs-lookup"><span data-stu-id="104de-191">**Delete all cookies** (`Ctrl+Shift+Del`) (session and permanent) for the path of the current page.</span></span>
 - <span data-ttu-id="104de-192">**Elimine todas las cookies de sesión** ( `Ctrl+Del` ) de la ruta de acceso de la página actual.</span><span class="sxs-lookup"><span data-stu-id="104de-192">**Delete all session cookies** (`Ctrl+Del`) for the path of the current page.</span></span>

<span data-ttu-id="104de-193">Para borrar por completo la *lista de cookies*, es posible que tenga que **borrar todas las cookies del dominio** en la barra de herramientas del panel [**red**](./network.md#toolbar) .</span><span class="sxs-lookup"><span data-stu-id="104de-193">To completely clear your *Cookies list*, you might need to **Clear all cookies for the domain** from the [**Network**](./network.md#toolbar) panel toolbar.</span></span>

### <span data-ttu-id="104de-194">Lista de cookies</span><span class="sxs-lookup"><span data-stu-id="104de-194">Cookies list</span></span>

<span data-ttu-id="104de-195">En la tabla *lista de cookies* puede:</span><span class="sxs-lookup"><span data-stu-id="104de-195">From the *Cookies list* table you can:</span></span>

 - <span data-ttu-id="104de-196">**Inspeccione y ordene** las cookies haciendo clic en cualquier nombre de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="104de-196">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="104de-197">**Edite** el *nombre* y el *valor* de una cookie existente haciendo clic en la celda.</span><span class="sxs-lookup"><span data-stu-id="104de-197">**Edit** the *Name* and *Value* of an existing cookie by clicking in the cell.</span></span>
 - <span data-ttu-id="104de-198">**Eliminar** ( `Del` ) una cookie de la opción de [menú contextual](#context-menu) de clic derecho, *eliminar cookie*.</span><span class="sxs-lookup"><span data-stu-id="104de-198">**Delete** (`Del`) a cookie from the right-click [context menu](#context-menu) option, *Delete cookie*.</span></span>
 - <span data-ttu-id="104de-199">**Agregue** una nueva cookie de sesión para el *dominio o la ruta de acceso* dada haciendo clic en la fila vacía situada en la parte inferior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="104de-199">**Add** a new session cookie for the given *Domain/Path* by clicking on the empty row at the bottom of the table.</span></span> <span data-ttu-id="104de-200">Esto solo funciona para las cookies de sesión; las cookies permanentes (con fechas de vencimiento específicas) deben establecerse en métodos tradicionales.</span><span class="sxs-lookup"><span data-stu-id="104de-200">This only works for session cookies; permanent cookies (with specific expiry dates) must be set with traditional methods.</span></span> <span data-ttu-id="104de-201">Los valores de *dominio* y *ruta* se rellenan automáticamente según la ubicación de la página.</span><span class="sxs-lookup"><span data-stu-id="104de-201">The *Domain* and *Path* values are auto-filled according to the location of the page.</span></span>

<span data-ttu-id="104de-202">Las columnas de la *lista de cookies* se pueden ordenar:</span><span class="sxs-lookup"><span data-stu-id="104de-202">The columns of the *Cookies list* are sortable:</span></span>

<span data-ttu-id="104de-203">Columna</span><span class="sxs-lookup"><span data-stu-id="104de-203">Column</span></span> | <span data-ttu-id="104de-204">Descripción</span><span class="sxs-lookup"><span data-stu-id="104de-204">Description</span></span>
:------------ | :-------------
<span data-ttu-id="104de-205">Name</span><span class="sxs-lookup"><span data-stu-id="104de-205">Name</span></span> | <span data-ttu-id="104de-206">Nombre de la cookie</span><span class="sxs-lookup"><span data-stu-id="104de-206">Name of the cookie</span></span>
<span data-ttu-id="104de-207">Valor</span><span class="sxs-lookup"><span data-stu-id="104de-207">Value</span></span> | <span data-ttu-id="104de-208">Valor de la cookie</span><span class="sxs-lookup"><span data-stu-id="104de-208">Value of the cookie</span></span>
<span data-ttu-id="104de-209">Dominio</span><span class="sxs-lookup"><span data-stu-id="104de-209">Domain</span></span> | <span data-ttu-id="104de-210">Nombre de host de la cookie (puede estar vacío)</span><span class="sxs-lookup"><span data-stu-id="104de-210">Host name of the cookie (may be empty)</span></span>
<span data-ttu-id="104de-211">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="104de-211">Path</span></span> | <span data-ttu-id="104de-212">Dirección URL de la cookie (puede estar vacía)</span><span class="sxs-lookup"><span data-stu-id="104de-212">URL path for the cookie (may be empty)</span></span>
<span data-ttu-id="104de-213">Expira</span><span class="sxs-lookup"><span data-stu-id="104de-213">Expires</span></span> | <span data-ttu-id="104de-214">Vigencia máxima de la cookie como marca de tiempo de fecha HTTP.</span><span class="sxs-lookup"><span data-stu-id="104de-214">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span> <span data-ttu-id="104de-215">Si no `Expires` se `Max-Age` ha establecido ninguna o se ha establecido, la entrada se considera una cookie de *sesión* .</span><span class="sxs-lookup"><span data-stu-id="104de-215">If no `Expires` or `Max-Age` was set, the entry is considered a *Session* cookie.</span></span>
<span data-ttu-id="104de-216">Solo HTTP</span><span class="sxs-lookup"><span data-stu-id="104de-216">HTTP only</span></span> | <span data-ttu-id="104de-217">Indica si la cookie se ha establecido en una `HttpOnly` Directiva, lo que indica que es inaccesible desde JavaScript</span><span class="sxs-lookup"><span data-stu-id="104de-217">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span>
<span data-ttu-id="104de-218">Seguro</span><span class="sxs-lookup"><span data-stu-id="104de-218">Secure</span></span> | <span data-ttu-id="104de-219">Indica si la cookie se estableció con la `Secure` Directiva, lo que indica que solo se enviará al servidor desde una solicitud mediante SSL y el protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="104de-219">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>

<span data-ttu-id="104de-220">Para obtener más información sobre las propiedades de las cookies, consulte la documentación del [conjunto de](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) **documentos web de MDN** .</span><span class="sxs-lookup"><span data-stu-id="104de-220">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>

### <span data-ttu-id="104de-221">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="104de-221">Context menu</span></span>

<span data-ttu-id="104de-222">Además de la [barra de herramientas](#cookies-manager)de la pestaña *cookies* , también puede administrar las cookies desde el **menú contextual** o los [métodos abreviados](#shortcuts)de teclado del botón secundario.</span><span class="sxs-lookup"><span data-stu-id="104de-222">In addition to the *Cookies* tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="104de-223">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="104de-223">Shortcuts</span></span>

| <span data-ttu-id="104de-224">Acción</span><span class="sxs-lookup"><span data-stu-id="104de-224">Action</span></span>                     | <span data-ttu-id="104de-225">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="104de-225">Shortcut</span></span>                 |
|:---------------------------|:-------------------------|
| <span data-ttu-id="104de-226">Actualizar</span><span class="sxs-lookup"><span data-stu-id="104de-226">Refresh</span></span>                    | `Ctrl` + `F5`            |
| <span data-ttu-id="104de-227">Eliminar cookie</span><span class="sxs-lookup"><span data-stu-id="104de-227">Delete cookie</span></span>              | `Del`                    |
| <span data-ttu-id="104de-228">Eliminar todas las cookies</span><span class="sxs-lookup"><span data-stu-id="104de-228">Delete all cookies</span></span>         | `Ctrl` + `Shift` + `Del` |
| <span data-ttu-id="104de-229">Eliminar todas las cookies de sesión</span><span class="sxs-lookup"><span data-stu-id="104de-229">Delete all session cookies</span></span> | `Ctrl` + `Del`           |
| <span data-ttu-id="104de-230">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="104de-230">Copy selected items</span></span>        | `Ctrl` + `C`             |
| <span data-ttu-id="104de-231">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="104de-231">Select all</span></span>                 | `Ctrl` + `A`             |

### <span data-ttu-id="104de-232">Administrador de caché</span><span class="sxs-lookup"><span data-stu-id="104de-232">Cache manager</span></span>

<span data-ttu-id="104de-233">Al hacer clic en una entrada de caché específica, se abrirá el administrador de **caché** de trabajadores del servicio, donde puede inspeccionar y, opcionalmente, eliminar entradas de la memoria caché (pares de clave y valor de*solicitud* y *respuesta* ):</span><span class="sxs-lookup"><span data-stu-id="104de-233">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs):</span></span>

![Administrador de caché](./media/storage_cache.png)

### <span data-ttu-id="104de-235">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="104de-235">Shortcuts</span></span>

#### <span data-ttu-id="104de-236">Administrador de caché</span><span class="sxs-lookup"><span data-stu-id="104de-236">Cache manager</span></span>

| <span data-ttu-id="104de-237">Acción</span><span class="sxs-lookup"><span data-stu-id="104de-237">Action</span></span>              | <span data-ttu-id="104de-238">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="104de-238">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="104de-239">Actualizar</span><span class="sxs-lookup"><span data-stu-id="104de-239">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="104de-240">Eliminar elemento</span><span class="sxs-lookup"><span data-stu-id="104de-240">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="104de-241">Copiar elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="104de-241">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="104de-242">Seleccionar todos</span><span class="sxs-lookup"><span data-stu-id="104de-242">Select all</span></span>          | `Ctrl` + `A`  |
