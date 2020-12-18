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
# <span data-ttu-id="dffcd-104">Búsqueda de detección de proveedor</span><span class="sxs-lookup"><span data-stu-id="dffcd-104">Search provider discovery</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="dffcd-105">La barra de direcciones de Microsoft Edge está integrada en la integración de búsqueda enriquecida, incluidas las sugerencias de búsqueda, los resultados de la web, el historial de exploración y los favoritos.</span><span class="sxs-lookup"><span data-stu-id="dffcd-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="dffcd-106">Microsoft Edge sigue la especificación de [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) para descubrir y usar proveedores de búsqueda web.</span><span class="sxs-lookup"><span data-stu-id="dffcd-106">Microsoft Edge follows the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification to discover and use web search providers.</span></span>  <span data-ttu-id="dffcd-107">Si eres un proveedor de búsqueda, esta es la manera de asegurarte de que Microsoft Edge sea compatible con tu servicio.</span><span class="sxs-lookup"><span data-stu-id="dffcd-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="dffcd-108">Para la seguridad y la privacidad de los usuarios, Microsoft Edge requiere que todas las búsquedas se realicen a través de SSL.</span><span class="sxs-lookup"><span data-stu-id="dffcd-108">For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>  

<span data-ttu-id="dffcd-109">Los siguientes recursos deben especificarse como `https` direcciones URL para habilitar la integración de Microsoft Edge de su motor de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="dffcd-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>  

*   <span data-ttu-id="dffcd-110">El sitio que contiene la referencia al documento de Descripción</span><span class="sxs-lookup"><span data-stu-id="dffcd-110">The site that contains the reference to the description document</span></span>  
*   <span data-ttu-id="dffcd-111">La dirección URL para el propio documento de Descripción</span><span class="sxs-lookup"><span data-stu-id="dffcd-111">The URL to the description document itself</span></span>  
*   <span data-ttu-id="dffcd-112">Plantilla de consulta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="dffcd-112">The search query template</span></span>  
    
1.  <span data-ttu-id="dffcd-113">Proporcione un archivo de descripción de OpenSearch, que contiene el nombre del proveedor de búsqueda y la plantilla que se va a usar para crear la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="dffcd-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span>  <span data-ttu-id="dffcd-114">Este es un documento de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dffcd-114">Here is an example document:</span></span>  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  <span data-ttu-id="dffcd-115">Incluya una referencia a su archivo de descripción de OpenSearch en la sección de encabezado de las páginas (normalmente se incluye la Página principal del sitio y las páginas de resultados de búsqueda), por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dffcd-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>  
    
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
    
<span data-ttu-id="dffcd-116">Cuando un usuario Explore el servicio de búsqueda, tu descripción de OpenSearch se seleccionará y se guardará automáticamente para usarla más adelante.</span><span class="sxs-lookup"><span data-stu-id="dffcd-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span>  <span data-ttu-id="dffcd-117">El usuario podrá ir a la configuración de Microsoft Edge y elegir agregar el servicio de búsqueda a su lista de proveedores de búsqueda para la barra de direcciones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dffcd-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>  

<span data-ttu-id="dffcd-118">Para obtener más información sobre cómo crear un documento de descripción de OpenSearch, consulta la especificación de [opensearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) .</span><span class="sxs-lookup"><span data-stu-id="dffcd-118">See the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification for further details on creating your OpenSearch description document.</span></span>  
