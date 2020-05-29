---
description: Indica que la vista de la vista previa está intentando descargar un archivo no compatible.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572893"
---
# <span data-ttu-id="530e9-104">Objeto UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="530e9-104">UnviewableContentIdentifiedEvent object</span></span>

<span data-ttu-id="530e9-105">Indica que [WebView](../webview.md) está intentando navegar a un archivo de un tipo de contenido no admitido.</span><span class="sxs-lookup"><span data-stu-id="530e9-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span> 

## <span data-ttu-id="530e9-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="530e9-106">Properties</span></span>

### <span data-ttu-id="530e9-107">Medio</span><span class="sxs-lookup"><span data-stu-id="530e9-107">mediaType</span></span>

<span data-ttu-id="530e9-108">Obtiene el tipo de contenido del contenido que no se ve.</span><span class="sxs-lookup"><span data-stu-id="530e9-108">Gets the content type of the unviewable content.</span></span>

<span data-ttu-id="530e9-109">Esta propiedad es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="530e9-109">This property is read-only</span></span>

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### <span data-ttu-id="530e9-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="530e9-110">Property value</span></span>
<span data-ttu-id="530e9-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="530e9-111">Type: **DOMString**</span></span>

### <span data-ttu-id="530e9-112">Referer</span><span class="sxs-lookup"><span data-stu-id="530e9-112">referer</span></span>

<span data-ttu-id="530e9-113">Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.</span><span class="sxs-lookup"><span data-stu-id="530e9-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="530e9-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530e9-114">This property is read-only.</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

#### <span data-ttu-id="530e9-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="530e9-115">Property value</span></span>
<span data-ttu-id="530e9-116">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="530e9-116">Type: **DOMString**</span></span>

### <span data-ttu-id="530e9-117">uri</span><span class="sxs-lookup"><span data-stu-id="530e9-117">uri</span></span>

<span data-ttu-id="530e9-118">Identificador uniforme de recursos (URI) del destino de la navegación.</span><span class="sxs-lookup"><span data-stu-id="530e9-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="530e9-119">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530e9-119">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="530e9-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="530e9-120">Property value</span></span>
<span data-ttu-id="530e9-121">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="530e9-121">Type: **DOMString**</span></span>
