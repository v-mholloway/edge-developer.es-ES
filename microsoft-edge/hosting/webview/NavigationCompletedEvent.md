---
description: Contiene información sobre la navegación de WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573367"
---
# <span data-ttu-id="eec67-104">Objeto NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="eec67-104">NavigationCompletedEvent object</span></span>

<span data-ttu-id="eec67-105">Un objeto que representa un evento que se desencadena cuando [WebView](../webview.md) ha terminado de cargar el contenido actual o si se ha producido un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="eec67-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>

## <span data-ttu-id="eec67-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eec67-106">Properties</span></span>
    
### <span data-ttu-id="eec67-107">uri</span><span class="sxs-lookup"><span data-stu-id="eec67-107">uri</span></span>

<span data-ttu-id="eec67-108">Identificador uniforme de recursos (URI) de la navegación.</span><span class="sxs-lookup"><span data-stu-id="eec67-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>

<span data-ttu-id="eec67-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eec67-109">This property is read-only.</span></span>

```js
var uri = NavigationCompletedEvent.uri;
```

#### <span data-ttu-id="eec67-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eec67-110">Property value</span></span>
<span data-ttu-id="eec67-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="eec67-111">Type: **DOMString**</span></span>

### <span data-ttu-id="eec67-112">isSuccess</span><span class="sxs-lookup"><span data-stu-id="eec67-112">isSuccess</span></span>

<span data-ttu-id="eec67-113">Obtiene un valor que indica si la navegación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="eec67-113">Gets a value that indicates whether the navigation completed successfully.</span></span>

<span data-ttu-id="eec67-114">Esta propiedad es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="eec67-114">This property is read-only</span></span>

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### <span data-ttu-id="eec67-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eec67-115">Property value</span></span>
<span data-ttu-id="eec67-116">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eec67-116">Type: **Boolean**</span></span>

### <span data-ttu-id="eec67-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="eec67-117">webErrorStatus</span></span>

<span data-ttu-id="eec67-118">Si la navegación no se realizó correctamente, obtiene un valor que indica por qué.</span><span class="sxs-lookup"><span data-stu-id="eec67-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>

<span data-ttu-id="eec67-119">Esta propiedad es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="eec67-119">This property is read-only</span></span>

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### <span data-ttu-id="eec67-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eec67-120">Property value</span></span>
<span data-ttu-id="eec67-121">Tipo: **largo sin signo**</span><span class="sxs-lookup"><span data-stu-id="eec67-121">Type: **unsigned long**</span></span>
