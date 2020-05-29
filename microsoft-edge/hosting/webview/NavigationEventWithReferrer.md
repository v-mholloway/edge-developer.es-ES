---
description: Contiene información de referencia sobre la navegación
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573361"
---
# <span data-ttu-id="819b6-104">Objeto NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="819b6-104">NavigationEventWithReferrer object</span></span>

<span data-ttu-id="819b6-105">Un objeto que representa un evento que se desencadena cuando se inicia la navegación y la navegación contiene una referencia.</span><span class="sxs-lookup"><span data-stu-id="819b6-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>

## <span data-ttu-id="819b6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="819b6-106">Properties</span></span>

### <span data-ttu-id="819b6-107">Referer</span><span class="sxs-lookup"><span data-stu-id="819b6-107">referer</span></span>

<span data-ttu-id="819b6-108">Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.</span><span class="sxs-lookup"><span data-stu-id="819b6-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="819b6-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="819b6-109">This property is read-only.</span></span>

#### <span data-ttu-id="819b6-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="819b6-110">Property value</span></span>
<span data-ttu-id="819b6-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="819b6-111">Type: **DOMString**</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

### <span data-ttu-id="819b6-112">uri</span><span class="sxs-lookup"><span data-stu-id="819b6-112">uri</span></span>

<span data-ttu-id="819b6-113">Identificador uniforme de recursos (URI) del destino de la navegación.</span><span class="sxs-lookup"><span data-stu-id="819b6-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="819b6-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="819b6-114">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="819b6-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="819b6-115">Property value</span></span>
<span data-ttu-id="819b6-116">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="819b6-116">Type: **DOMString**</span></span>
