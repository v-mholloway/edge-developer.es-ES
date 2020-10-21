---
description: Cómo ver y cambiar los datos de IndexedDB con el panel de aplicación y los fragmentos de código.
title: Ver y cambiar datos de IndexedDB con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 54d232780e5e071ce34cdfb55e12daed6f631491
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125436"
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

# Ver y cambiar datos de IndexedDB con Microsoft Edge DevTools  

En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver y cambiar los datos de [IndexedDB][MDNIndexedDBAPI] .  Se da por sentado que estás familiarizado con DevTools.  También se supone que estás familiarizado con IndexedDB.  En caso contrario, vaya a [usar IndexedDB][MDNUsingIndexedDB].  

## Ver datos de IndexedDB  

1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** generalmente se abre de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       El panel **manifiesto**  
    :::image-end:::  
    
1.  Expanda el menú **IndexedDB** para ver qué bases de datos están disponibles.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       El menú **IndexedDB**  
    :::image-end:::  
    
    *   \ ( ![ Icono de base de datos ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` representa una base de datos, donde `notes` es el nombre de la base de datos y `https://mdn.github.io` es el origen que tiene acceso a la base de datos.  
    *   \ ( ![ Icono del almacén de objetos ][ImageObjectStoreIcon] \) `notes` es un almacén de objetos.  
    *   el **título** y el **cuerpo** son [índices][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitación conocida**  Las bases de datos de terceros no están visibles.  Por ejemplo, si usa una `<iframe>` para insertar un anuncio en la página y su red de anuncios usa IndexedDB, los datos de IndexedDB de la red de anuncios no estarán visibles.  Consulte el [problema #943770][ChromiumIssue943770].  
    
1.  Seleccione una base de datos para ver el origen y el número de versión.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       La base de datos de **Notes**  
    :::image-end:::  
    
1.  Seleccione un almacén de objetos para ver los pares de clave y valor.  
    
    > [!NOTE]
    > Los datos de IndexedDB no se actualizan en tiempo real.  Consulte [actualizar datos de IndexedDB](#refresh-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       El almacén de objetos de **Notes**  
    :::image-end:::  
    
    *   **Entradas totales** es el número total de pares de clave y valor en el almacén de objetos.  
    *   El **valor del generador de claves** es la siguiente clave disponible.  Este campo solo se muestra al usar [generadores de claves][MDNBasicConceptsKeyGenerator].  
    
1.  Seleccione una celda en la columna **valor** para expandir ese valor.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Ver un valor de **IndexedDB**  
    :::image-end:::  
    
1.  Seleccione un índice, como **título** o **cuerpo** en la siguiente ilustración, para ordenar el objeto almacén según los valores de ese índice.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Ordenar un objeto por un índice  
    :::image-end:::  
    
## Actualizar datos de IndexedDB  

Los valores de IndexedDB en el panel de **aplicaciones** no se actualizan en tiempo real.  Elija **Actualizar** \ ( ![ actualizar ][ImageReloadIcon] \) al ver un almacén de objetos para actualizar los datos, o ver una base de datos y elegir **actualizar la base** de datos para actualizar todos los datos.  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Ver una base de datos  
:::image-end:::  

## Editar datos de IndexedDB  

Las claves y los valores de IndexedDB no se pueden modificar en el panel de la **aplicación** .  Como DevTools tiene acceso al contexto de la página, puede ejecutar el código de JavaScript dentro de DevTools para editar los datos de IndexedDB.  

### Editar datos de IndexedDB con fragmentos de código  

Los recortes [son una][DevtoolsJavascriptSnippets] forma de almacenar y ejecutar bloques de código JavaScript dentro de DevTools.  Al ejecutar un fragmento de código, el resultado se registra en la **consola**.  Puede usar un fragmento de código de JavaScript para editar una base de datos IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Usar un fragmento de código para interactuar con IndexedDB  
:::image-end:::  

## Eliminar datos de IndexedDB  

### Eliminar un par de clave y valor de IndexedDB  

1.  [Ver un almacén de objetos IndexedDB](#view-indexeddb-data).  
1.  Seleccione el par de clave y valor que desea eliminar.  DevTools lo resalta para indicar que está seleccionado.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Seleccione un par clave-valor para eliminarlo.  
    :::image-end:::  
    
1.  Presione la `Delete` tecla o elija **eliminar seleccionado** \ ( ![ eliminar seleccionado ][ImageDeleteIcon] \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Aspecto del almacén de objetos después de eliminar el par de clave y valor  
    :::image-end:::  
    
### Eliminar todos los pares clave-valor en un almacén de objetos  

1.  [Ver un almacén de objetos IndexedDB](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Ver un almacén de objetos  
    :::image-end:::  
    
1.  Elija **Borrar almacén de objetos** \ ( ![ Borrar almacén de objetos ][ImageClearIcon] \).  
    
### Eliminar una base de datos de IndexedDB  

1.  [Vea la base de datos IndexedDB](#view-indexeddb-data) que desea eliminar.  
1.  Elija **eliminar base de datos**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       El botón **eliminar base de datos**  
    :::image-end:::  
    
### Eliminar todo el almacenamiento de IndexedDB  

1.  Abra el panel **Borrar almacenamiento** .  
1.  Asegúrese de que la casilla de verificación **IndexedDB** está habilitada.  
1.  Elija **Borrar datos del sitio**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="El panel manifiesto" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       El panel **Borrar almacenamiento**  
    :::image-end:::  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: Mostrar bases de datos de IndexedDB de iframe, cromo-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Generador de claves: conceptos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API de IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Uso de IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usar un índice-Using IndexedDB | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
