---
description: Representa una cadena de notificación pasada desde el contenido de WebView a la aplicación.
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572894"
---
# <span data-ttu-id="c96b2-104">Objeto ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="c96b2-104">ScriptNotifyEvent object</span></span>

<span data-ttu-id="c96b2-105">Un objeto que representa un evento que se desencadena cuando el contenido incluido en la [vista en WebView](../webview.md) pasa una cadena a la aplicación mediante JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c96b2-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>

## <span data-ttu-id="c96b2-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c96b2-106">Properties</span></span>
    
### <span data-ttu-id="c96b2-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="c96b2-107">callingUri</span></span>

<span data-ttu-id="c96b2-108">Obtiene el identificador uniforme de recursos (URI) de la página que contiene el script que ha provocado el **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="c96b2-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>

<span data-ttu-id="c96b2-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c96b2-109">This property is read-only.</span></span>

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### <span data-ttu-id="c96b2-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c96b2-110">Property value</span></span>
<span data-ttu-id="c96b2-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="c96b2-111">Type: **DOMString**</span></span>

### <span data-ttu-id="c96b2-112">value</span><span class="sxs-lookup"><span data-stu-id="c96b2-112">value</span></span>

<span data-ttu-id="c96b2-113">El nombre del método como se pasó a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c96b2-113">The method name as passed to the application.</span></span>

<span data-ttu-id="c96b2-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c96b2-114">This property is read-only.</span></span>

```js
var value = ScriptNotifyEvent.value;
```

#### <span data-ttu-id="c96b2-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c96b2-115">Property value</span></span>
<span data-ttu-id="c96b2-116">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="c96b2-116">Type: **DOMString**</span></span>