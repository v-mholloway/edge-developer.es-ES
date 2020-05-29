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
# <span data-ttu-id="eb568-104">Detección de proveedores de búsqueda</span><span class="sxs-lookup"><span data-stu-id="eb568-104">Search provider discovery</span></span>


<span data-ttu-id="eb568-105">La barra de direcciones de Microsoft Edge está integrada en la integración de búsqueda enriquecida, incluidas las sugerencias de búsqueda, los resultados de la web, el historial de exploración y los favoritos.</span><span class="sxs-lookup"><span data-stu-id="eb568-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span> <span data-ttu-id="eb568-106">Microsoft Edge sigue la especificación de [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) para descubrir y usar proveedores de búsqueda web.</span><span class="sxs-lookup"><span data-stu-id="eb568-106">Microsoft Edge follows the [OpenSearch 1.1](https://go.microsoft.com/fwlink/p/?LinkID=208582) specification to discover and use web search providers.</span></span> <span data-ttu-id="eb568-107">Si eres un proveedor de búsqueda, esta es la manera de asegurarte de que Microsoft Edge sea compatible con tu servicio.</span><span class="sxs-lookup"><span data-stu-id="eb568-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>

**<span data-ttu-id="eb568-108">Para la seguridad y la privacidad de los usuarios, Microsoft Edge requiere que todas las búsquedas se realicen a través de SSL.</span><span class="sxs-lookup"><span data-stu-id="eb568-108">For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>** <span data-ttu-id="eb568-109">Los siguientes recursos deben especificarse como `https` direcciones URL para habilitar la integración de Microsoft Edge de su motor de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="eb568-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>
* <span data-ttu-id="eb568-110">El sitio que contiene la referencia al documento de Descripción</span><span class="sxs-lookup"><span data-stu-id="eb568-110">The site that contains the reference to the description document</span></span>
* <span data-ttu-id="eb568-111">La dirección URL para el propio documento de Descripción</span><span class="sxs-lookup"><span data-stu-id="eb568-111">The URL to the description document itself</span></span>
* <span data-ttu-id="eb568-112">Plantilla de consulta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="eb568-112">The search query template</span></span> 

1.  <span data-ttu-id="eb568-113">Proporcione un archivo de descripción de OpenSearch, que contiene el nombre del proveedor de búsqueda y la plantilla que se va a usar para crear la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="eb568-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span> <span data-ttu-id="eb568-114">Este es un documento de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="eb568-114">Here is an example document:</span></span>

    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```

2.  <span data-ttu-id="eb568-115">Incluya una referencia a su archivo de descripción de OpenSearch en la sección de encabezado de las páginas (normalmente se incluye la Página principal del sitio y las páginas de resultados de búsqueda), por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="eb568-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>

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

<span data-ttu-id="eb568-116">Cuando un usuario Explore el servicio de búsqueda, tu descripción de OpenSearch se seleccionará y se guardará automáticamente para usarla más adelante.</span><span class="sxs-lookup"><span data-stu-id="eb568-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span> <span data-ttu-id="eb568-117">El usuario podrá ir a la configuración de Microsoft Edge y elegir agregar el servicio de búsqueda a su lista de proveedores de búsqueda para la barra de direcciones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="eb568-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>

<span data-ttu-id="eb568-118">Para obtener más información sobre cómo crear un documento de descripción de OpenSearch, consulta la especificación de [opensearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) .</span><span class="sxs-lookup"><span data-stu-id="eb568-118">See the [OpenSearch 1.1](https://go.microsoft.com/fwlink/p/?LinkID=208582) specification for further details on creating your OpenSearch description document.</span></span>
