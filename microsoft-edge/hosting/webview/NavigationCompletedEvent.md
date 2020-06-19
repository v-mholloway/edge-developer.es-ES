---
description: Contiene información sobre la navegación de WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752145"
---
# <span data-ttu-id="2b6ee-104">Objeto NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="2b6ee-104">NavigationCompletedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="2b6ee-105">Un objeto que representa un evento que se desencadena cuando [WebView](../webview.md) ha terminado de cargar el contenido actual o si se ha producido un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>  

## <span data-ttu-id="2b6ee-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b6ee-106">Properties</span></span>  

### <span data-ttu-id="2b6ee-107">uri</span><span class="sxs-lookup"><span data-stu-id="2b6ee-107">uri</span></span>  

<span data-ttu-id="2b6ee-108">Identificador uniforme de recursos (URI) de la navegación.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>  

<span data-ttu-id="2b6ee-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-109">This property is read-only.</span></span>  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### <span data-ttu-id="2b6ee-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b6ee-110">Property value</span></span>  

<span data-ttu-id="2b6ee-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="2b6ee-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="2b6ee-112">isSuccess</span><span class="sxs-lookup"><span data-stu-id="2b6ee-112">isSuccess</span></span>  

<span data-ttu-id="2b6ee-113">Obtiene un valor que indica si la navegación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-113">Gets a value that indicates whether the navigation completed successfully.</span></span>  

<span data-ttu-id="2b6ee-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-114">This property is read-only.</span></span>  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### <span data-ttu-id="2b6ee-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b6ee-115">Property value</span></span>  

<span data-ttu-id="2b6ee-116">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b6ee-116">Type: **Boolean**</span></span>  

### <span data-ttu-id="2b6ee-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="2b6ee-117">webErrorStatus</span></span>  

<span data-ttu-id="2b6ee-118">Si la navegación no se realizó correctamente, obtiene un valor que indica por qué.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>  

<span data-ttu-id="2b6ee-119">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-119">This property is read-only.</span></span>  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### <span data-ttu-id="2b6ee-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b6ee-120">Property value</span></span>  

<span data-ttu-id="2b6ee-121">Tipo: **largo sin signo**</span><span class="sxs-lookup"><span data-stu-id="2b6ee-121">Type: **unsigned long**</span></span>  
