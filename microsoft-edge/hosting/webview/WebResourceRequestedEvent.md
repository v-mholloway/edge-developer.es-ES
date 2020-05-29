---
description: Un evento que se desencadena cuando se realiza una solicitud HTTP.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572890"
---
# <span data-ttu-id="d5b63-104">Objeto WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="d5b63-104">WebResourceRequestedEvent object</span></span>

<span data-ttu-id="d5b63-105">Un evento que se desencadena cuando se realiza una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="d5b63-105">An event that is fired when an HTTP request is made.</span></span>

## <span data-ttu-id="d5b63-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d5b63-106">Properties</span></span>

### <span data-ttu-id="d5b63-107">EventArgs</span><span class="sxs-lookup"><span data-stu-id="d5b63-107">args</span></span>

<span data-ttu-id="d5b63-108">Información sobre la solicitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5b63-108">Information about the resource request.</span></span> <span data-ttu-id="d5b63-109">Este es un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="d5b63-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>

<span data-ttu-id="d5b63-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d5b63-110">This property is read-only.</span></span>

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### <span data-ttu-id="d5b63-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d5b63-111">Property value</span></span>
<span data-ttu-id="d5b63-112">Escriba lo siguiente: **cualquiera**</span><span class="sxs-lookup"><span data-stu-id="d5b63-112">Type: **any**</span></span>

