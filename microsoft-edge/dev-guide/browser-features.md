---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Guías para las características del explorador en Microsoft Edge.
title: Guía para desarrolladores y exploradores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 854b0e8ac057db3cc8b53af6205404d0841dfdb4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942039"
---
# <span data-ttu-id="d2c77-104">Características del explorador</span><span class="sxs-lookup"><span data-stu-id="d2c77-104">Browser features</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## <span data-ttu-id="d2c77-105">Directivas de reproducción automática</span><span class="sxs-lookup"><span data-stu-id="d2c77-105">Autoplay policies</span></span>  

 <span data-ttu-id="d2c77-106">Microsoft Edge proporciona a los clientes la posibilidad de personalizar sus preferencias de navegación en sitios web con sonido de reproducción automática con el fin de minimizar las distracciones en la web y ahorrar ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="d2c77-106">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="d2c77-107">Los usuarios pueden personalizar el comportamiento de los medios con controles de reproducción automática globales y por sitio.</span><span class="sxs-lookup"><span data-stu-id="d2c77-107">Users can customize media behavior with both global and per-site autoplay controls.</span></span>  <span data-ttu-id="d2c77-108">Además, Microsoft Edge elimina automáticamente la reproducción automática de los elementos multimedia en las pestañas de fondo.</span><span class="sxs-lookup"><span data-stu-id="d2c77-108">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="d2c77-109">Consulte [directivas de reproducción automática](./browser-features/autoplay-policies.md) para obtener detalles y procedimientos recomendados para garantizar una buena experiencia de usuario con los elementos multimedia hospedados en su sitio.</span><span class="sxs-lookup"><span data-stu-id="d2c77-109">Check out [Autoplay policies](./browser-features/autoplay-policies.md) for details and best practices to ensure a good user experience with media hosted on your site.</span></span>  

## <span data-ttu-id="d2c77-110">Flash</span><span class="sxs-lookup"><span data-stu-id="d2c77-110">Flash</span></span>  

<span data-ttu-id="d2c77-111">Si se usa Flash en la página pero el usuario no lo ha habilitado, Microsoft Edge normalmente mostrará un icono de pieza de Puzzle en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d2c77-111">If Flash is used on your page but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar.</span></span>  <span data-ttu-id="d2c77-112">Si va a agregar dinámicamente el control de flash después de que se cargue la página, es posible que no se muestre el icono del rompecabezas, en cuyo caso deseará [comprobar si flash está cargado y proporcionar una experiencia de reserva correcta](./browser-features/flash.md) si no está presente.</span><span class="sxs-lookup"><span data-stu-id="d2c77-112">If you are dynamically adding the Flash control after the page is loaded, the puzzle icon may not display, in which case you'll want to [test if Flash is loaded and provide a graceful fallback experience](./browser-features/flash.md) if its not present.</span></span>  

## <span data-ttu-id="d2c77-113">Vista de lectura</span><span class="sxs-lookup"><span data-stu-id="d2c77-113">Reading view</span></span>  

<span data-ttu-id="d2c77-114">Microsoft Edge ofrece una [vista de lectura](./browser-features/reading-view.md) para obtener una experiencia de lectura más fluida, como las páginas web, sin la distracción de contenido no relacionado u otro contenido secundario en la página.</span><span class="sxs-lookup"><span data-stu-id="d2c77-114">Microsoft Edge provides a [reading view](./browser-features/reading-view.md) for a more streamlined, book-like reading experience of webpages, without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="d2c77-115">Estas son algunas sugerencias sobre cómo garantizar una estupenda experiencia de lectura con el sitio, así como instrucciones para que el sitio quede fuera de la vista de lectura.</span><span class="sxs-lookup"><span data-stu-id="d2c77-115">Here are tips on how to ensure a great reading view experience with your site and also instructions for opting your site out of reading view.</span></span>  

## <span data-ttu-id="d2c77-116">Búsqueda de detección de proveedor</span><span class="sxs-lookup"><span data-stu-id="d2c77-116">Search provider discovery</span></span>  

<span data-ttu-id="d2c77-117">La barra de direcciones de Microsoft Edge está integrada en la integración de búsqueda enriquecida, incluidas las sugerencias de búsqueda, los resultados de la web, el historial de exploración y los favoritos.</span><span class="sxs-lookup"><span data-stu-id="d2c77-117">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="d2c77-118">[Aquí tienes más información sobre los proveedores de búsqueda](./browser-features/search-provider-discovery.md) que desean proporcionar soporte técnico para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d2c77-118">[Here's more info for search providers](./browser-features/search-provider-discovery.md) looking to provide support for Microsoft Edge.</span></span>  
