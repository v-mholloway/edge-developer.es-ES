---
description: Un evento que se desencadena cuando se realiza una solicitud HTTP.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751985"
---
# <span data-ttu-id="76892-104">Objeto WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="76892-104">WebResourceRequestedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="76892-105">Un evento que se desencadena cuando se realiza una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="76892-105">An event that is fired when an HTTP request is made.</span></span>  

## <span data-ttu-id="76892-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="76892-106">Properties</span></span>  

### <span data-ttu-id="76892-107">EventArgs</span><span class="sxs-lookup"><span data-stu-id="76892-107">args</span></span>  

<span data-ttu-id="76892-108">Información sobre la solicitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="76892-108">Information about the resource request.</span></span>  <span data-ttu-id="76892-109">Este es un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="76892-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>  

<span data-ttu-id="76892-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76892-110">This property is read-only.</span></span>  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### <span data-ttu-id="76892-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="76892-111">Property value</span></span>  

<span data-ttu-id="76892-112">Escriba lo siguiente: **cualquiera**</span><span class="sxs-lookup"><span data-stu-id="76892-112">Type: **any**</span></span>  
