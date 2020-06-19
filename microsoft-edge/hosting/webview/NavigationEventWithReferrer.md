---
description: Contiene información de referencia sobre la navegación
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752132"
---
# <span data-ttu-id="6d036-104">Objeto NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="6d036-104">NavigationEventWithReferrer object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="6d036-105">Un objeto que representa un evento que se desencadena cuando se inicia la navegación y la navegación contiene una referencia.</span><span class="sxs-lookup"><span data-stu-id="6d036-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>  

## <span data-ttu-id="6d036-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6d036-106">Properties</span></span>  

### <span data-ttu-id="6d036-107">Referer</span><span class="sxs-lookup"><span data-stu-id="6d036-107">referer</span></span>

<span data-ttu-id="6d036-108">Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.</span><span class="sxs-lookup"><span data-stu-id="6d036-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="6d036-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d036-109">This property is read-only.</span></span>  

#### <span data-ttu-id="6d036-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d036-110">Property value</span></span>  

<span data-ttu-id="6d036-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="6d036-111">Type: **DOMString**</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### <span data-ttu-id="6d036-112">uri</span><span class="sxs-lookup"><span data-stu-id="6d036-112">uri</span></span>  

<span data-ttu-id="6d036-113">Identificador uniforme de recursos (URI) del destino de la navegación.</span><span class="sxs-lookup"><span data-stu-id="6d036-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="6d036-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d036-114">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="6d036-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d036-115">Property value</span></span>  

<span data-ttu-id="6d036-116">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="6d036-116">Type: **DOMString**</span></span>  
