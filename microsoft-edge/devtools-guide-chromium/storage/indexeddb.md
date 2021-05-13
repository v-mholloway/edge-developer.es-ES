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
# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a>Ver y cambiar datos IndexedDB con Microsoft Edge DevTools  

En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] ver y cambiar [los datos de IndexedDB.][MDNIndexedDBAPI]  Se supone que está familiarizado con DevTools.  También supone que está familiarizado con IndexedDB.  Si no es así, vaya [a Using IndexedDB][MDNUsingIndexedDB].  

## <a name="view-indexeddb-data"></a>Ver datos indexadosDB  

1.  Elija la **pestaña** Aplicación para abrir la **herramienta** Aplicación.  El **panel Manifiesto** normalmente se abre de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Panel **Manifiesto**  
    :::image-end:::  
    
1.  Expanda el **menú IndexedDB** para revisar qué bases de datos están disponibles.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Menú IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Menú **IndexedDB**  
    :::image-end:::  
    
    *   \( Icono de base de datos \) representa una base de datos, donde es el nombre de la base de datos y es el origen que ![ tiene acceso a la base de ](../media/database-icon.msft.png) `notes - https://mdn.github.io` `notes` `https://mdn.github.io` datos.  
    *   \( ![ Icono del almacén de objetos ](../media/object-store-icon.msft.png) \) es un almacén de `notes` objetos.  
    *   **title** y **body** son [índices][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitación conocida**  Las bases de datos de terceros no están visibles.  Por ejemplo, si usas un anuncio para insertar un anuncio en tu página y la red de anuncios usa IndexedDB, los datos indexados de la red de anuncios no `<iframe>` estarán visibles.  Vaya a [emitir #943770][ChromiumIssue943770].  
    
1.  Elija una base de datos para revisar el origen y el número de versión.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="La base de datos de notas" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       La **base de datos de notas**  
    :::image-end:::  
    
1.  Elija un almacén de objetos para revisar los pares clave-valor.  
    
    > [!NOTE]
    > Los datos indexadosDB no se actualizan en tiempo real.  Vaya a [Actualizar datos indexadosDB](#refresh-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="El almacén de objetos de notas" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       El **almacén de objetos de** notas  
    :::image-end:::  
    
    *   **El número total de entradas** es el número total de pares clave-valor en el almacén de objetos.  
    *   **El valor del generador de** claves es la siguiente clave disponible.  El campo solo se muestra cuando se usan [generadores de claves][MDNBasicConceptsKeyGenerator].  
    
1.  Elija una celda en la **columna Valor** para expandir el valor.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Ver un valor IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Ver un **valor IndexedDB**  
    :::image-end:::  
    
1.  Elija un índice, como **el título** **o** el cuerpo de la siguiente figura, para ordenar el almacén de objetos según los valores de ese índice.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Ordenar un almacén de objetos por un índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Ordenar un almacén de objetos por un índice  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a>Actualizar datos indexadosDB  

Los valores indexadosDB en **la herramienta Aplicación** no se actualizan en tiempo real.  Elija **Actualizar** \( Actualizar \) al ver un almacén de objetos para actualizar los datos o ver una base de datos y elegir Actualizar base de datos para ![ actualizar todos los ](../media/reload-icon.msft.png) datos. ****  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Ver una base de datos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Ver una base de datos  
:::image-end:::  

## <a name="edit-indexeddb-data"></a>Editar datos indexadosDB  

Las claves indexadasDB y los valores no se pueden editar desde la **herramienta Aplicación.**  Sin embargo, dado que DevTools tiene acceso al contexto de página, puede ejecutar código JavaScript en DevTools para editar datos indexadosDB.  

### <a name="edit-indexeddb-data-with-snippets"></a>Editar datos IndexedDB con fragmentos de código  

[Los fragmentos][DevtoolsJavascriptSnippets] de código son una forma de almacenar y ejecutar bloques de código JavaScript en DevTools.  Al ejecutar un fragmento de código, el resultado se registra en la **consola**.  Puede usar un fragmento de código para ejecutar código JavaScript para editar una base de datos IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar un fragmento de código para interactuar con IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Usar un fragmento de código para interactuar con IndexedDB  
:::image-end:::  

## <a name="delete-indexeddb-data"></a>Eliminar datos indexadosDB  

### <a name="delete-an-indexeddb-key-value-pair"></a>Eliminar un par clave-valor IndexedDB  

1.  [Ver un almacén de objetos IndexedDB](#view-indexeddb-data).  
1.  Elija el par clave-valor que desea eliminar.  DevTools lo resalta para indicar que está seleccionado.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Elegir un par clave-valor para eliminarlo" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Elegir un par clave-valor para eliminarlo  
    :::image-end:::  
    
1.  Seleccione la `Delete` clave o elija Eliminar **seleccionado** \( Eliminar ![ seleccionado ](../media/delete-icon.msft.png) \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Cómo se ve el almacén de objetos después de eliminar el par clave-valor" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Cómo se ve el almacén de objetos después de eliminar el par clave-valor  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a>Eliminar todos los pares clave-valor de un almacén de objetos  

1.  [Ver un almacén de objetos IndexedDB](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Ver un almacén de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Ver un almacén de objetos  
    :::image-end:::  
    
1.  Elija **Borrar almacén de objetos** \( Borrar almacén de objetos ![ ](../media/clear-icon.msft.png) \).  
    
### <a name="delete-an-indexeddb-database"></a>Eliminar una base de datos IndexedDB  

1.  [Vea la base de datos IndexedDB](#view-indexeddb-data) que desea eliminar.  
1.  Elija **Eliminar base de datos**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Botón Eliminar base de datos" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Botón **Eliminar base de datos**  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a>Eliminar todo el almacenamiento de IndexedDB  

1.  Abra el **panel Borrar** almacenamiento.  
1.  Asegúrese de que la **casilla IndexedDB** está habilitada.  
1.  Elija **Borrar datos del sitio**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="El panel Despejar almacenamiento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       El **panel Despejar almacenamiento**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
