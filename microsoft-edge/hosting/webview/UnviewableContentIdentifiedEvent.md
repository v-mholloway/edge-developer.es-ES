---
description: Indica que la vista de la vista previa está intentando descargar un archivo no compatible.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752016"
---
# <span data-ttu-id="1bf31-104">Objeto UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="1bf31-104">UnviewableContentIdentifiedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="1bf31-105">Indica que [WebView](../webview.md) está intentando navegar a un archivo de un tipo de contenido no admitido.</span><span class="sxs-lookup"><span data-stu-id="1bf31-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span>  

## <span data-ttu-id="1bf31-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bf31-106">Properties</span></span>  

### <span data-ttu-id="1bf31-107">Medio</span><span class="sxs-lookup"><span data-stu-id="1bf31-107">mediaType</span></span>  

<span data-ttu-id="1bf31-108">Obtiene el tipo de contenido del contenido que no se ve.</span><span class="sxs-lookup"><span data-stu-id="1bf31-108">Gets the content type of the unviewable content.</span></span>  

<span data-ttu-id="1bf31-109">Esta propiedad es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bf31-109">This property is read-only</span></span>  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### <span data-ttu-id="1bf31-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1bf31-110">Property value</span></span>  

<span data-ttu-id="1bf31-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1bf31-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="1bf31-112">Referer</span><span class="sxs-lookup"><span data-stu-id="1bf31-112">referer</span></span>  

<span data-ttu-id="1bf31-113">Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.</span><span class="sxs-lookup"><span data-stu-id="1bf31-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="1bf31-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1bf31-114">This property is read-only.</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### <span data-ttu-id="1bf31-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1bf31-115">Property value</span></span>  

<span data-ttu-id="1bf31-116">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1bf31-116">Type: **DOMString**</span></span>  

### <span data-ttu-id="1bf31-117">uri</span><span class="sxs-lookup"><span data-stu-id="1bf31-117">uri</span></span>  

<span data-ttu-id="1bf31-118">Identificador uniforme de recursos (URI) del destino de la navegación.</span><span class="sxs-lookup"><span data-stu-id="1bf31-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="1bf31-119">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1bf31-119">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="1bf31-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1bf31-120">Property value</span></span>  

<span data-ttu-id="1bf31-121">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1bf31-121">Type: **DOMString**</span></span>  
