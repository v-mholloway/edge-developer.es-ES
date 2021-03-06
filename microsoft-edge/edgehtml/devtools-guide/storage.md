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
# <a name="storage"></a>Almacenamiento

Use el panel **Almacenamiento** para inspeccionar y administrar varios datos almacenados en caché localmente, incluidos:  

*   [Pares de clave y](#local-and-session-storage-managers) valores de almacenamiento web \(Almacenamiento local y de sesión\)  
*   [Datos estructurados de base de datos](#indexeddb-manager) indizados  
*   [Cookies](#cookies-list) para el dominio  
*   [Caché](#cache-manager) \(pares de solicitud/respuesta\) para la depuración del trabajador de servicio  

Expanda cualquiera de estas categorías y haga clic en una entrada secundaria para abrir su pestaña administrador de recursos.  

## <a name="local-and-session-storage-managers"></a>Administradores de almacenamiento local y de sesión  

Use el administrador de almacenamiento local y el administrador de almacenamiento de sesiones para inspeccionar y administrar el almacenamiento web de la página.  

Las **carpetas** Almacenamiento local y **Almacenamiento de** sesiones dentro del selector De recursos del panel almacenamiento muestran una lista de orígenes de la página. [](./debugger.md#resource-picker)  Al seleccionar uno de estos marcos, se abre una tabla editable de los pares clave/valor actuales establecidos a través de [](#storage-list) [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) o [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivamente \(y/o establecido directamente desde la lista Almacenamiento de DevTools \).  

![Administrador de almacenamiento de DevTools](./media/storage_web_storage.png)  

En las pestañas Almacenamiento local y Almacenamiento de sesiones puede:  

*   **Actualice** \( \) la lista de almacenamiento para ver el conjunto actual de pares `Ctrl+F5` clave/valores para el dominio determinado. [](#cookies-list)  \(La lista no se actualiza automáticamente tras las actualizaciones de scripts.\)  
*   **Simular alcanzar el límite de almacenamiento**  para el almacenamiento web de Microsoft Edge.  Cada dominio y subdominio tiene su propio área de almacenamiento, pero hay un límite combinado:  
    *   **Subdominios:** hasta 5 MB de espacio  
    *   **Dominios:** hasta 10 MB de espacio  
    *   **Total para todos los dominios:** hasta 50 MB de espacio  

   El almacenamiento de sesión se borra tan pronto como se cierra la última pestaña del explorador que hace referencia a su origen.  Las entradas de almacenamiento local persisten indefinidamente hasta que el usuario lo borra mediante programación o manualmente:  

   **Configuración**  >  **Borrar datos de exploración**  >  **Cookies y datos guardados del sitio web**  

![Borrar datos de exploración desde el panel Configuración de Microsoft Edge](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a>Lista de almacenamiento  

En la tabla de lista Almacenamiento puede:  

*   **Inspeccione y ordene** `key/value` los pares haciendo clic en el nombre de columna de la tabla.  
*   **Edite** `Key` el y de una entrada existente haciendo clic en la `Value` celda.  
*   **Eliminar** \( \) una entrada de la opción del menú contextual con el botón `Del` secundario, **Eliminar elemento**.  
*   **Agregue** un par `key/value` nuevo haciendo clic en la fila vacía de la parte inferior de la tabla.  

### <a name="shortcuts"></a>Accesos directos

| Acción | Acceso directo |  
|:--- |:--- |  
| Actualizar | `Ctrl`+`F5` |  
| Eliminar elemento | `Del` |  
| Copiar elementos seleccionados | `Ctrl`+`C` |  
| Seleccionar todos | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a>Administrador de IndexedDB  

Use la **pestaña IndexedDB** para inspeccionar y administrar los datos estructurados almacenados localmente en un equipo cliente.  En concreto, puede inspeccionar/ordenar y actualizar los almacenes e índices de objetos, y también eliminar entradas de clave-valor individuales.  

> [!TIP]
> Puede usar nuestra demostración [del mezclador de audio](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) para probar la unidad del administrador de *IndexedDB* en Microsoft Edge DevTools.  

Para eliminar todos los datos IndexedDB almacenados para el usuario actual en Microsoft Edge, use el menú Configuración **de** Microsoft Edge:  

**...** >  **Configuración**  >  **Borrar datos de exploración**  >  **Cookies y datos guardados del sitio web**  

La carpeta dentro del selector de recursos del depurador muestra una lista de orígenes de `IndexedDB` los recursos cargados por la página. [](./debugger.md#resource-picker)  Las bases de datos IndexedDB \(IDB\) aparecerán en el origen, junto con sus almacenes de objetos.  

![Administrador de IndexedDB de DevTools](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a>Barra de herramientas IndexedDB  

Desde la barra de herramientas IndexedDB puede:  

*   **Actualice** \( `Ctrl` + `F5` \) para ver las entradas actuales en el almacén de objetos o el índice de la base de datos.  El administrador de IndexedDB no se actualiza automáticamente cuando se realizan cambios en la base de datos.  

### <a name="object-store-entries-list"></a>Lista de entradas del almacén de objetos  

Desde el almacén de objetos o la tabla Índice puede:  

*   **Inspeccione y ordene** los pares clave-valor haciendo clic en cualquier nombre de columna de la tabla.  
*   **Actualizar** \( `Ctrl` + `F5` \)  
*   **Eliminar elemento** \( `Del` \) para quitar la entrada seleccionada en el índice o el almacén de objetos.  También puede hacerlo desde la opción de menú [contextual](#context-menu) Clic con el botón secundario, **Eliminar elemento**.  
*   **Copie los elementos seleccionados** `Ctrl` + `C` \( \) para copiar el elemento seleccionado en el portapapeles.  También puede hacerlo desde la opción de menú [contextual](#context-menu) clic con el botón derecho, **Copiar elemento seleccionado**.  
*   **Seleccione todo** \( \) para seleccionar todas las entradas del índice o `Ctrl` + `A` almacén de objetos.  También puede hacerlo desde la opción de menú [contextual](#context-menu) clic con el botón derecho, **Seleccionar todo**.  

Las columnas del almacén de objetos o la tabla Index se pueden ordenar:  

| Columna | Descripción |  
|:--- |:--- |  
| Key | Nombre del par clave-valor \(igual que **la clave principal**\) al iterar por un almacén de objetos; Nombre de la clave de índice \(tecla actual del cursor\) al iterar sobre un índice |  
| Clave principal | Nombre del par clave-valor \(see **MDN web docs** for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\) |  
| Valor | Valor del par clave-valor |  

Consulte *documentos web de MDN* para obtener más información sobre los conceptos y el uso [de IndexedDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).  

### <a name="context-menu"></a>Menú contextual  

Además de la barra de herramientas [ *IndexedDB,* ](#indexeddb-toolbar)también puede administrar los datos **** en almacenes de objetos o índices desde el menú Contextual y/o los [métodos abreviados de teclado](#shortcuts).  

### <a name="shortcuts"></a>Accesos directos

| Acción | Acceso directo |  
|:--- |:--- |  
| Actualizar | `Ctrl`+`F5` |  
| Eliminar par clave-valor | `Del` |  
| Copiar elementos seleccionados | `Ctrl`+`C` |  
| Seleccionar todos | `Ctrl +`A' |  

## <a name="cookies-manager"></a>Administrador de cookies  

Use el administrador de cookies para inspeccionar y administrar las cookies del dominio determinado.  

La carpeta dentro del selector de recursos del depurador muestra una lista de orígenes de `Cookies` los recursos cargados por la página. [](./debugger.md#resource-picker)  Al seleccionar uno de estos fotogramas se abre una tabla que representa las cookies actuales establecidas por el encabezado [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) o mediante un script [con Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).  

![Administrador de cookies de DevTools](./media/storage_cookies.png)  

En la barra de herramientas de la pestaña Cookies puede:  

*   **Actualice** \( `Ctrl` + `F5` \) la lista [cookies](#cookies-list) para ver el conjunto actual de cookies para el dominio determinado.  \(La lista no se actualiza automáticamente.\)  
*   **Elimine todas las cookies** `Ctrl` + `Shift` + `Del` \( \) \(session y permanent\) de la ruta de acceso de la página actual.  
*   **Elimine todas las cookies de sesión** `Ctrl` + `Del` \( \) de la ruta de acceso de la página actual.  

Para borrar completamente la lista de cookies, es posible que deba borrar todas **las cookies** del dominio desde la barra de [herramientas del](./network.md#toolbar) panel Red.  

### <a name="cookies-list"></a>Lista de cookies  

En la tabla de lista Cookies puede:  

*   **Inspeccione y ordene** las cookies haciendo clic en cualquier nombre de columna de la tabla.  
*   **Edite** `Name` el y de una cookie existente haciendo clic en la `Value` celda.  
*   **Eliminar** \( \) una cookie de la opción del menú contextual con el botón `Del` secundario, [](#context-menu) `Delete cookie` .  
*   **Agregue** una nueva cookie de sesión para el dado `Domain/Path` haciendo clic en la fila vacía en la parte inferior de la tabla.  Esto solo funciona para las cookies de sesión; las cookies permanentes \(con fechas de expiración específicas\) deben establecerse con métodos tradicionales.  Los `Domain` valores y se `Path` rellenan automáticamente según la ubicación de la página.  

Las columnas de la lista cookies se pueden ordenar:

| Columna | Descripción |  
| :--- | :--- |  
| Name | Nombre de la cookie |  
| Valor | Valor de la cookie |  
| Dominio | Nombre de host de la cookie \(puede estar vacío\) |  
| Ruta de acceso | Ruta de acceso url para la cookie \(puede estar vacía\) |  
| Expira | Duración máxima de la cookie como marca de tiempo de fecha HTTP.  Si no `Expires` se `Max-Age` estableció o no, la entrada se considera una cookie de sesión.  |  
| Solo HTTP | Indica si la cookie se estableció con directiva, lo que indica que no es `HttpOnly` accesible desde JavaScript |  
| Seguro | Indica si la cookie se estableció con la directiva, lo que indica que solo se enviará al servidor desde una solicitud mediante SSL y `Secure` el protocolo HTTPS.  |  

Consulta la referencia [set-cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) de documentos web de **MDN** para obtener más información sobre las propiedades de las cookies.  

### <a name="context-menu"></a>Menú contextual  

Además de la barra de herramientas [de](#cookies-manager)la pestaña Cookies, también puede administrar las cookies desde el menú contextual y/o los [métodos abreviados de teclado.](#shortcuts) ****  

### <a name="shortcuts"></a>Accesos directos  

| Acción | Acceso directo |  
|:--- |:--- |  
| Actualizar | `Ctrl`+`F5` |  
| Eliminar cookie | `Del` |  
| Eliminar todas las cookies | `Ctrl`+`Shift`+`Del` |  
| Eliminar todas las cookies de sesión | `Ctrl`+`Del` |  
| Copiar elementos seleccionados | `Ctrl`+`C` |  
| Seleccionar todos | `Ctrl`+`A` |  

### <a name="cache-manager"></a>Administrador de caché  

Al hacer clic en una entrada **** de caché específica, se abrirá el administrador de caché de trabajo de servicio, donde puede inspeccionar y eliminar opcionalmente entradas de caché \( y pares `Request` `Response` clave/valor\):  

![Administrador de caché](./media/storage_cache.png)  

### <a name="shortcuts"></a>Accesos directos  

#### <a name="cache-manager"></a>Administrador de caché  

| Acción | Acceso directo |  
|:--- |:--- |  
| Actualizar | `Ctrl`+`F5` |  
| Eliminar elemento | `Del` |  
| Copiar elementos seleccionados | `Ctrl`+`C` |  
| Seleccionar todos | `Ctrl`+`A` |  
