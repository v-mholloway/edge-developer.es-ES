---
description: Usar el panel de almacenamiento para inspeccionar el almacenamiento Web, IndexedDB, cookies y las memorias caché de solicitudes/respuestas
title: 'DevTools: almacenamiento'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, almacenamiento Web, almacenamiento local, almacenamiento de sesión, IndexedDB, cookies, trabajo de servicio, caché
ms.custom: seodec18
ms.openlocfilehash: 8de6e1f90f86fa09b116646918c6be1d8cfb0a72
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573789"
---
# Almacenamiento

Use el panel **almacenamiento** para inspeccionar y administrar diversos datos de la caché local, entre los que se incluyen:

 - Pares de clave y valor de [almacenamiento web](#local-and-session-storage-managers) (almacenamiento*local* y de *sesión* )
 - Datos estructurados de la base de datos [indizados](#indexeddb-manager)
 - [Cookies](#cookies-list) para el dominio
 - [Caché](#cache-manager) (pares de solicitud y respuesta) para la depuración de trabajos de servicio

Expanda cualquiera de estas categorías y haga clic en una entrada secundaria para abrir su ficha de administrador de recursos.

## Administradores de almacenamiento local y de sesión

Use el *Administrador* de almacenamiento local y el *Administrador de almacenamiento de sesión* para inspeccionar y administrar el almacenamiento Web de la página. 

Las carpetas **almacenamiento local** y **almacenamiento de sesión** en el selector de [*recursos*](./debugger.md#resource-picker) del panel de almacenamiento muestran una lista de orígenes de la página. Al seleccionar uno de estos marcos, se abre una tabla editable de los pares de clave y valor actuales establecido a través de [window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) o [window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivamente (o establecido directamente desde la [lista de almacenamiento](#storage-list)de DevTools).

![Administrador de cookies de DevTools](./media/storage_web_storage.png)

En las pestañas *almacenamiento local* y *almacenamiento de sesiones* , puede hacer lo siguiente:

 - **Refresh** ( `Ctrl+F5` ) la [lista de almacenamiento](#cookies-list) para ver el conjunto actual de pares clave/valor para el dominio dado. (La lista no se actualiza automáticamente en las actualizaciones de script).
 - **Simular alcanzar el límite de almacenamiento** para almacenamiento Web Microsoft Edge. Cada dominio y subdominio tiene su propia área de almacenamiento, pero hay un límite combinado:
    - **Subdominios:** hasta 5 MB de espacio
    - **Dominios:** hasta 10 MB de espacio
    - **Total para todos los dominios:** hasta 50 MB de espacio

   El almacenamiento de sesión se borra tan pronto como se cierre la última ficha del explorador que hace referencia a su origen. Las entradas de almacenamiento local continúan de forma indefinida hasta que la página la borra mediante programación o manualmente por el usuario:

   **Configuración**  >  **Borrar datos**  >  de exploración **Cookies y datos de sitios web guardados**

![Desactivar la navegación de datos desde el panel de configuración de Microsoft Edge](./media/settings_clear_browsing_data.png)

### Lista de almacenamiento

En la tabla *lista de almacenamiento* , puede hacer lo siguiente:

 - **Inspeccione y ordene** las parejas de clave y valor haciendo clic en uno de los nombres de columna de la tabla.
 - **Edite** la *clave* y el *valor* de una entrada existente haciendo clic en la celda.
 - **Eliminar** ( `Del` ) una entrada de la opción del menú contextual de clic derecho, *Eliminar elemento*.
 - **Agregue** un nuevo par de clave/valor haciendo clic en la fila vacía de la parte inferior de la tabla.


### Abreviados

| Acción              | Método abreviado      |
|:--------------------|:--------------|
| Actualizar             | `Ctrl` + `F5` |
| Eliminar elemento         | `Del`         |
| Copiar elementos seleccionados | `Ctrl` + `C`  |
| Seleccionar todos          | `Ctrl` + `A`  |


## IndexedDB Manager

Use la pestaña **IndexedDB** para inspeccionar y administrar los datos estructurados almacenados de forma local en un equipo cliente. En concreto, puede inspeccionar/ordenar y actualizar los índices y los almacenes de objetos, así como eliminar entradas de clave y valor individuales.

> [!TIP]
> Puede usar nuestra demostración de [mezclador de audio](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) para probar el *Administrador de IndexedDB* en Microsoft Edge DevTools.

Para eliminar todos los datos de IndexedDB almacenados para el usuario actual en Microsoft Edge, usa el menú de *configuración* de Microsoft Edge:

**...** >  **Configuración**  >  **Borrar datos**  >  de exploración **Cookies y datos de sitios web guardados**

La carpeta **IndexedDB** dentro del [*selector de recursos*](./debugger.md#resource-picker) del depurador muestra una lista de orígenes de los recursos cargados por la página. Todas las bases de datos IndexedDB (IDB) aparecerán debajo del origen, junto con sus almacenes de objetos. 

![DevTools IndexedDB Manager](./media/storage_indexeddb.png)

### Barra de IndexedDB

Desde la barra de herramientas de *IndexedDB* puedes hacer lo siguiente:

 - **Actualizar** ( `Ctrl+F5` ) para ver las entradas actuales en el almacén de objetos o el índice de su base de datos. El administrador de IndexedDB no se actualiza automáticamente cuando se realizan cambios en la base de datos.

### Lista de entradas del almacén de objetos

Desde la tabla *almacén de objetos* o *Índice* , puede:

 - **Inspeccione y ordene** los pares clave-valor haciendo clic en cualquier nombre de columna de la tabla.
 - **Actualizar** ( `Ctrl+F5` )
 - **Eliminar elemento** ( `Del` ) para quitar la entrada seleccionada en el almacén de objetos o en el índice. También puede hacer esto desde la opción del [menú contextual](#context-menu) al hacer clic con el botón derecho, *Eliminar elemento*.
 - **Copiar elementos seleccionados** ( `Ctrl+C` ) para copiar el elemento seleccionado en el portapapeles. También puede hacer esto desde la opción del [menú contextual](#context-menu) al hacer clic con el botón derecho, *copiar el elemento seleccionado*.
 - **Seleccione todos** ( `Ctrl+A` ) para seleccionar todas las entradas del almacén de objetos o del índice. También puede hacer esto desde la opción del [menú contextual](#context-menu) de clic derecho, *seleccionar todo*.

Las columnas de la tabla de *Índice* o el *almacén de objetos* se pueden ordenar:

Columna | Descripción
:------------ | :-------------
Key | Nombre del par clave-valor (igual que la *clave principal*) al recorrer en iteración un almacén de objetos; Nombre de la clave de índice (clave actual del cursor) cuando se recorre en iteración un índice
Clave principal | Nombre del par clave-valor (vea los *documentos web de MDN* para obtener más información sobre [las claves](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)de la IDB)
Valor | Valor del par clave-valor

Consulte los *documentos web de MDN* para obtener más información sobre los [conceptos y el uso de IndexedDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).

### Menú contextual

Además de la [barra de herramientas *IndexedDB* ](#indexeddb-toolbar), también puede administrar los datos en almacenes o índices de objetos desde el **menú contextual** o los [métodos abreviados](#shortcuts)de teclado del botón secundario del ratón.

### Abreviados

Acción | Método abreviado
:------------ | :-------------
Actualizar | `Ctrl` + `F5`
Eliminar par clave-valor | `Del`
Copiar elementos seleccionados | `Ctrl` + `C`
Seleccionar todos | `Ctrl` + `A`

## Administrador de cookies

Use el *Administrador de cookies* para inspeccionar y administrar las cookies para el dominio dado. 

La carpeta **cookies** dentro del selector de [*recursos*](./debugger.md#resource-picker) del depurador muestra una lista de orígenes de los recursos cargados por la página. Al seleccionar uno de estos marcos, se abre una tabla que representa las cookies actuales que ha establecido el encabezado [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) o mediante una secuencia de comandos con [Document. cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).

![Administrador de cookies de DevTools](./media/storage_cookies.png)

En la barra de herramientas de la pestaña *cookies* puede:

 - **Actualizar** ( `Ctrl+F5` ) la [lista de cookies](#cookies-list) para ver el conjunto actual de cookies para el dominio dado. (La lista no se actualiza automáticamente).
 - **Elimine todas las cookies** ( `Ctrl+Shift+Del` sesión y permanente) de la ruta de acceso de la página actual.
 - **Elimine todas las cookies de sesión** ( `Ctrl+Del` ) de la ruta de acceso de la página actual.

Para borrar por completo la *lista de cookies*, es posible que tenga que **borrar todas las cookies del dominio** en la barra de herramientas del panel [**red**](./network.md#toolbar) .

### Lista de cookies

En la tabla *lista de cookies* puede:

 - **Inspeccione y ordene** las cookies haciendo clic en cualquier nombre de columna de la tabla.
 - **Edite** el *nombre* y el *valor* de una cookie existente haciendo clic en la celda.
 - **Eliminar** ( `Del` ) una cookie de la opción de [menú contextual](#context-menu) de clic derecho, *eliminar cookie*.
 - **Agregue** una nueva cookie de sesión para el *dominio o la ruta de acceso* dada haciendo clic en la fila vacía situada en la parte inferior de la tabla. Esto solo funciona para las cookies de sesión; las cookies permanentes (con fechas de vencimiento específicas) deben establecerse en métodos tradicionales. Los valores de *dominio* y *ruta* se rellenan automáticamente según la ubicación de la página.

Las columnas de la *lista de cookies* se pueden ordenar:

Columna | Descripción
:------------ | :-------------
Name | Nombre de la cookie
Valor | Valor de la cookie
Dominio | Nombre de host de la cookie (puede estar vacío)
Ruta de acceso | Dirección URL de la cookie (puede estar vacía)
Expira | Vigencia máxima de la cookie como marca de tiempo de fecha HTTP. Si no `Expires` se `Max-Age` ha establecido ninguna o se ha establecido, la entrada se considera una cookie de *sesión* .
Solo HTTP | Indica si la cookie se ha establecido en una `HttpOnly` Directiva, lo que indica que es inaccesible desde JavaScript
Proteger | Indica si la cookie se estableció con la `Secure` Directiva, lo que indica que solo se enviará al servidor desde una solicitud mediante SSL y el protocolo HTTPS.

Para obtener más información sobre las propiedades de las cookies, consulte la documentación del [conjunto de](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) **documentos web de MDN** .

### Menú contextual

Además de la [barra de herramientas](#cookies-manager)de la pestaña *cookies* , también puede administrar las cookies desde el **menú contextual** o los [métodos abreviados](#shortcuts)de teclado del botón secundario.

### Abreviados

| Acción                     | Método abreviado                 |
|:---------------------------|:-------------------------|
| Actualizar                    | `Ctrl` + `F5`            |
| Eliminar cookie              | `Del`                    |
| Eliminar todas las cookies         | `Ctrl` + `Shift` + `Del` |
| Eliminar todas las cookies de sesión | `Ctrl` + `Del`           |
| Copiar elementos seleccionados        | `Ctrl` + `C`             |
| Seleccionar todos                 | `Ctrl` + `A`             |

### Administrador de caché

Al hacer clic en una entrada de caché específica, se abrirá el administrador de **caché** de trabajadores del servicio, donde puede inspeccionar y, opcionalmente, eliminar entradas de la memoria caché (pares de clave y valor de*solicitud* y *respuesta* ):

![Administrador de caché](./media/storage_cache.png)

### Abreviados

#### Administrador de caché

| Acción              | Método abreviado      |
|:--------------------|:--------------|
| Actualizar             | `Ctrl` + `F5` |
| Eliminar elemento         | `Del`         |
| Copiar elementos seleccionados | `Ctrl` + `C`  |
| Seleccionar todos          | `Ctrl` + `A`  |
