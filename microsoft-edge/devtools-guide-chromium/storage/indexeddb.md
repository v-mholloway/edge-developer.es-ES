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





# Ver y cambiar datos de IndexedDB con Microsoft Edge DevTools   

  

En esta guía se muestra cómo usar [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para ver y cambiar los datos de [IndexedDB][MDNIndexedDBAPI] .  Se da por sentado que estás familiarizado con DevTools.  También se supone que estás familiarizado con IndexedDB.  Si no es así, vea [usar IndexedDB][MDNUsingIndexedDB].  

## Ver datos de IndexedDB   

1.  Seleccione la pestaña **aplicación** para abrir el panel de **aplicaciones** .  El panel **manifiesto** generalmente se abre de forma predeterminada.  
    
    > ##### Figura 1  
    > El panel manifiesto  
    > ![El panel manifiesto][ImageManifest]  

1.  Expanda el menú **IndexedDB** para ver qué bases de datos están disponibles.  
    
    > ##### Figura 2  
    > El menú **IndexedDB**  
    > ![El menú IndexedDB][ImageIndexedDBMenu]  
    
    *   ![El icono ][ImageDatabaseIcon] `notes - https://mdn.github.io` de base de datos representa una base de datos, donde `notes` es el nombre de la base de datos y `https://mdn.github.io` es el origen que tiene acceso a la base de datos.  
    *   ![El icono de almacén de objetos ][ImageObjectStoreIcon] `notes` es un almacén de objetos.  
    *   el **título** y el **cuerpo** son [índices][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitación conocida**  Las bases de datos de terceros no están visibles.  Por ejemplo, si usa una `<iframe>` para insertar un anuncio en la página y su red de anuncios usa IndexedDB, los datos de IndexedDB de la red de anuncios no estarán visibles.  Consulte el [problema #943770][ChromiumIssue943770].  
    
1.  Seleccione una base de datos para ver el origen y el número de versión.  
    
    > ##### Imagen 3  
    > La base de datos de **Notes**  
    > ![La base de datos de Notes][ImageIndexedDBDatabase]  
    
1.  Seleccione un almacén de objetos para ver los pares de clave y valor.  
    
    > [!NOTE]
    > Los datos de IndexedDB no se actualizan en tiempo real.  Consulte [actualizar datos de IndexedDB](#refresh-indexeddb-data).  
    
    > ##### Imagen 4  
    > El almacén de objetos de **Notes**  
    > ![El almacén de objetos de Notes][ImageIndexedDBObjectStore]  

    *   **Entradas totales** es el número total de pares de clave y valor en el almacén de objetos.  
    *   El **valor del generador de claves** es la siguiente clave disponible.  Este campo solo se muestra al usar [generadores de claves][MDNBasicConceptsKeyGenerator].  

1.  Seleccione una celda en la columna **valor** para expandir ese valor.  
    
    > ##### Imagen 5  
    > Visualización de un valor de IndexedDB  
    > ![Visualización de un valor de IndexedDB][ImageIndexedBDValue]  
    
1.  Seleccione un índice, como **título** o **cuerpo** en la [figura 6](#figure-6), para ordenar el objeto almacén según los valores de ese índice.  
   
    > ##### Imagen 6  
    > Un almacén de objetos ordenado alfabéticamente según la clave de **título**  
    > ![Ordenar un objeto por un índice][ImageIndexedDBIndex]  

## Actualizar datos de IndexedDB   

Los valores de IndexedDB en el panel de **aplicaciones** no se actualizan en tiempo real.  Seleccione **Actualizar** ![ actualización ][ImageReloadIcon] al ver un almacén de objetos para actualizar los datos, o ver una base de datos y haga clic en **actualizar la base** de datos para actualizar todos los datos.  

> ##### Imagen 7  
> Ver una base de datos  
> ![Ver una base de datos][ImageIndexedDBDatabase2]  

## Editar datos de IndexedDB   

Las claves y los valores de IndexedDB no se pueden modificar en el panel de la **aplicación** .  Como DevTools tiene acceso al contexto de la página, puede ejecutar el código de JavaScript dentro de DevTools para editar los datos de IndexedDB.  

### Editar datos de IndexedDB con fragmentos de código   

Los recortes [son una][DevtoolsJavascriptSnippets] forma de almacenar y ejecutar bloques de código JavaScript dentro de DevTools.  Al ejecutar un fragmento de código, el resultado se registra en la **consola**.  Puede usar un fragmento de código de JavaScript para editar una base de datos IndexedDB.  

> ##### Imagen 8  
> Uso de un fragmento de código para interactuar con IndexedDB  
> ![Uso de un fragmento de código para interactuar con IndexedDB][ImageIndexedDBSnippet]  

## Eliminar datos de IndexedDB   

### Eliminar un par de clave y valor de IndexedDB   

1.  [Ver un almacén de objetos IndexedDB](#view-indexeddb-data).  
1.  Seleccione el par de clave y valor que desea eliminar.  DevTools lo resalta para indicar que está seleccionado.  
    
    > ##### Imagen 9  
    > Selección de un par clave-valor para eliminarlo  
    > ![Selección de un par clave-valor para eliminarlo][ImageIndexedDBKeyValuePair]  

1.  Presione la `Delete` tecla o haga clic en **eliminar** selección ![ eliminar seleccionados ][ImageDeleteIcon] .  
    
    > ##### Imagen 10  
    > Aspecto del almacén de objetos después de eliminar el par de clave y valor  
    > ![Aspecto del almacén de objetos después de eliminar el par de clave y valor][ImageIndexedDBKeyValuePairDeleted]  

### Eliminar todos los pares clave-valor en un almacén de objetos   

1.  [Ver un almacén de objetos IndexedDB](#view-indexeddb-data).  
    
    > ##### Imagen 11  
    > Visualización de un almacén de objetos  
    > ![Visualización de un almacén de objetos][ImageIndexedDBObjectStore]  

1.  Seleccione Borrar almacén de objetos borrar **almacén de objetos** ![ ][ImageClearIcon] .  

### Eliminar una base de datos de IndexedDB   

1.  [Vea la base de datos IndexedDB](#view-indexeddb-data) que desea eliminar.  
1.  Seleccione **eliminar base de datos**.  
    
    > ##### Imagen 12  
    > El botón **eliminar base de datos**  
    > ![El botón Eliminar base de datos][ImageIndexedDBDatabase]  

### Eliminar todo el almacenamiento de IndexedDB   

1.  Abra el panel **Borrar almacenamiento** .  

1.  Asegúrese de que la casilla de verificación **IndexedDB** está habilitada.  

1.  Seleccione **Borrar datos del sitio**.  
    
    > ##### Imagen 13  
    > El panel **Borrar almacenamiento** ![ el panel borrar almacenamiento][ImageIndexedDBClearStorage]  

 



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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
