---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Si eres un proveedor de búsqueda, consulta cómo asegurarte de que Microsoft Edge sea compatible con tu servicio.
title: 'Detección de proveedores de búsqueda: Guía para desarrolladores'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb21182e910cb91658dd4fb204f7f7783843f447
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236569"
---
# Búsqueda de detección de proveedor  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

La barra de direcciones de Microsoft Edge está integrada en la integración de búsqueda enriquecida, incluidas las sugerencias de búsqueda, los resultados de la web, el historial de exploración y los favoritos.  Microsoft Edge sigue la especificación de [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) para descubrir y usar proveedores de búsqueda web.  Si eres un proveedor de búsqueda, esta es la manera de asegurarte de que Microsoft Edge sea compatible con tu servicio.  

> [!IMPORTANT]
> Para la seguridad y la privacidad de los usuarios, Microsoft Edge requiere que todas las búsquedas se realicen a través de SSL.  

Los siguientes recursos deben especificarse como `https` direcciones URL para habilitar la integración de Microsoft Edge de su motor de búsqueda:  

*   El sitio que contiene la referencia al documento de Descripción  
*   La dirección URL para el propio documento de Descripción  
*   Plantilla de consulta de búsqueda  
    
1.  Proporcione un archivo de descripción de OpenSearch, que contiene el nombre del proveedor de búsqueda y la plantilla que se va a usar para crear la búsqueda.  Este es un documento de ejemplo:  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  Incluya una referencia a su archivo de descripción de OpenSearch en la sección de encabezado de las páginas (normalmente se incluye la Página principal del sitio y las páginas de resultados de búsqueda), por ejemplo:  
    
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
    
Cuando un usuario Explore el servicio de búsqueda, tu descripción de OpenSearch se seleccionará y se guardará automáticamente para usarla más adelante.  El usuario podrá ir a la configuración de Microsoft Edge y elegir agregar el servicio de búsqueda a su lista de proveedores de búsqueda para la barra de direcciones de Microsoft Edge.  

Para obtener más información sobre cómo crear un documento de descripción de OpenSearch, consulta la especificación de [opensearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) .  
