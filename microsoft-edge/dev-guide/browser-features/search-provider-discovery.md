---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Si eres un proveedor de búsqueda, consulta cómo asegurarte de que Microsoft Edge sea compatible con tu servicio.
title: 'Guía para desarrolladores: detección de proveedores de búsqueda'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: ac23c2c62d436d5772b498208a56ad306eb8cb3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572966"
---
# Detección de proveedores de búsqueda


La barra de direcciones de Microsoft Edge está integrada en la integración de búsqueda enriquecida, incluidas las sugerencias de búsqueda, los resultados de la web, el historial de exploración y los favoritos. Microsoft Edge sigue la especificación de [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) para descubrir y usar proveedores de búsqueda web. Si eres un proveedor de búsqueda, esta es la manera de asegurarte de que Microsoft Edge sea compatible con tu servicio.

**Para la seguridad y la privacidad de los usuarios, Microsoft Edge requiere que todas las búsquedas se realicen a través de SSL.** Los siguientes recursos deben especificarse como `https` direcciones URL para habilitar la integración de Microsoft Edge de su motor de búsqueda:
* El sitio que contiene la referencia al documento de Descripción
* La dirección URL para el propio documento de Descripción
* Plantilla de consulta de búsqueda 

1.  Proporcione un archivo de descripción de OpenSearch, que contiene el nombre del proveedor de búsqueda y la plantilla que se va a usar para crear la búsqueda. Este es un documento de ejemplo:

    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```

2.  Incluya una referencia a su archivo de descripción de OpenSearch en la sección de encabezado de las páginas (normalmente se incluye la Página principal del sitio y las páginas de resultados de búsqueda), por ejemplo:

    ```html
    <html>
        <head>
            <link rel="search" 
                type="application/opensearchdescription+xml"  
                href="https://contoso.com/content-search.xml" 
                title="Contoso search" /> 
        </head> 
        <body> 
        ...
    ```

Cuando un usuario Explore el servicio de búsqueda, tu descripción de OpenSearch se seleccionará y se guardará automáticamente para usarla más adelante. El usuario podrá ir a la configuración de Microsoft Edge y elegir agregar el servicio de búsqueda a su lista de proveedores de búsqueda para la barra de direcciones de Microsoft Edge.

Para obtener más información sobre cómo crear un documento de descripción de OpenSearch, consulta la especificación de [opensearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) .
