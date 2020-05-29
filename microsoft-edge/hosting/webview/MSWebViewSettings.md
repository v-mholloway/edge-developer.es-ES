---
description: Define las propiedades que habilitan o deshabilitan características de WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573368"
---
# <span data-ttu-id="51da5-104">Objeto MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="51da5-104">MSWebViewSettings object</span></span>

<span data-ttu-id="51da5-105">Define las propiedades que habilitan o deshabilitan características de [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="51da5-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>

## <span data-ttu-id="51da5-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51da5-106">Properties</span></span>

### <span data-ttu-id="51da5-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="51da5-107">isIndexedDBEnabled</span></span>

<span data-ttu-id="51da5-108">Obtiene o establece un valor que indica si se permite el uso de IndexedDB en [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="51da5-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### <span data-ttu-id="51da5-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="51da5-109">Property value</span></span>
<span data-ttu-id="51da5-110">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="51da5-110">Type: **boolean**</span></span>

<span data-ttu-id="51da5-111">**Verdadero** si IndexedDB está permitido en la **vista de vista**de usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="51da5-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span> 

### <span data-ttu-id="51da5-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="51da5-112">isJavaScriptEnabled</span></span>

<span data-ttu-id="51da5-113">Obtiene o establece un valor que indica si se permite el uso de JavaScript en [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="51da5-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### <span data-ttu-id="51da5-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="51da5-114">Property value</span></span>
<span data-ttu-id="51da5-115">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="51da5-115">Type: **boolean**</span></span>

<span data-ttu-id="51da5-116">**Verdadero** Se permite JavaScript en la [vista](../webview.md)de usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="51da5-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 

### <span data-ttu-id="51da5-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="51da5-117">isScriptNotifyAllowed</span></span>

<span data-ttu-id="51da5-118">Obtiene o establece un valor que indica si se permite el uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) en [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="51da5-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### <span data-ttu-id="51da5-119">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="51da5-119">Property value</span></span>
<span data-ttu-id="51da5-120">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="51da5-120">Type: **boolean**</span></span>

<span data-ttu-id="51da5-121">Se permite **verdadero** [ScriptNotifyEvent](ScriptNotifyEvent.md) en la [vista](../webview.md)de usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="51da5-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 
