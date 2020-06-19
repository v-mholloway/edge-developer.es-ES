---
description: Representa una cadena de notificación pasada desde el contenido de WebView a la aplicación.
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752027"
---
# <span data-ttu-id="cfda0-104">Objeto ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="cfda0-104">ScriptNotifyEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="cfda0-105">Un objeto que representa un evento que se desencadena cuando el contenido incluido en la [vista en WebView](../webview.md) pasa una cadena a la aplicación mediante JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cfda0-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>  

## <span data-ttu-id="cfda0-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cfda0-106">Properties</span></span>  

### <span data-ttu-id="cfda0-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="cfda0-107">callingUri</span></span>  

<span data-ttu-id="cfda0-108">Obtiene el identificador uniforme de recursos (URI) de la página que contiene el script que ha provocado el **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="cfda0-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>  

<span data-ttu-id="cfda0-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cfda0-109">This property is read-only.</span></span>  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### <span data-ttu-id="cfda0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cfda0-110">Property value</span></span>  

<span data-ttu-id="cfda0-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="cfda0-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="cfda0-112">value</span><span class="sxs-lookup"><span data-stu-id="cfda0-112">value</span></span>  

<span data-ttu-id="cfda0-113">El nombre del método como se pasó a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cfda0-113">The method name as passed to the application.</span></span>  

<span data-ttu-id="cfda0-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cfda0-114">This property is read-only.</span></span>  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### <span data-ttu-id="cfda0-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cfda0-115">Property value</span></span>  

<span data-ttu-id="cfda0-116">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="cfda0-116">Type: **DOMString**</span></span>  
