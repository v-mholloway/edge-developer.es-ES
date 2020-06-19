---
description: Define las propiedades que habilitan o deshabilitan características de WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752181"
---
# <span data-ttu-id="d12a7-104">Objeto MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="d12a7-104">MSWebViewSettings object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="d12a7-105">Define las propiedades que habilitan o deshabilitan características de [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="d12a7-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>  

## <span data-ttu-id="d12a7-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d12a7-106">Properties</span></span>  

### <span data-ttu-id="d12a7-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="d12a7-107">isIndexedDBEnabled</span></span>  

<span data-ttu-id="d12a7-108">Obtiene o establece un valor que indica si se permite el uso de IndexedDB en [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="d12a7-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### <span data-ttu-id="d12a7-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d12a7-109">Property value</span></span>  

<span data-ttu-id="d12a7-110">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d12a7-110">Type: **boolean**</span></span>  

<span data-ttu-id="d12a7-111">**Verdadero** si IndexedDB está permitido en la **vista de vista**de usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d12a7-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span>  

### <span data-ttu-id="d12a7-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d12a7-112">isJavaScriptEnabled</span></span>  

<span data-ttu-id="d12a7-113">Obtiene o establece un valor que indica si se permite el uso de JavaScript en [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="d12a7-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### <span data-ttu-id="d12a7-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d12a7-114">Property value</span></span>  

<span data-ttu-id="d12a7-115">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d12a7-115">Type: **boolean**</span></span>  

<span data-ttu-id="d12a7-116">**Verdadero** Se permite JavaScript en la [vista](../webview.md)de usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d12a7-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  

### <span data-ttu-id="d12a7-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="d12a7-117">isScriptNotifyAllowed</span></span>  

<span data-ttu-id="d12a7-118">Obtiene o establece un valor que indica si se permite el uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) en [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="d12a7-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### <span data-ttu-id="d12a7-119">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d12a7-119">Property value</span></span>  

<span data-ttu-id="d12a7-120">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d12a7-120">Type: **boolean**</span></span>  

<span data-ttu-id="d12a7-121">Se permite **verdadero** [ScriptNotifyEvent](ScriptNotifyEvent.md) en la [vista](../webview.md)de usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d12a7-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  
