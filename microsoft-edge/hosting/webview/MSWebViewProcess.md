---
description: Representa un proceso de WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573370"
---
# <span data-ttu-id="e3ab4-104">Objeto MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="e3ab4-104">MSWebViewProcess object</span></span>

<span data-ttu-id="e3ab4-105">Representa un proceso de [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="e3ab4-105">Represents a [webview](../webview.md) process.</span></span>

```js
var wvprocess = new MSWebViewProcess();
```

## <span data-ttu-id="e3ab4-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3ab4-106">Properties</span></span>

### <span data-ttu-id="e3ab4-107">enterpriseId</span><span class="sxs-lookup"><span data-stu-id="e3ab4-107">enterpriseId</span></span>

<span data-ttu-id="e3ab4-108">IDENTIFICADOR de empresa del proceso.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-108">The enterprise ID of the process.</span></span>

```js
var enterpriseId = wvprocess.enterpriseId;
```

<span data-ttu-id="e3ab4-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-109">This property is read-only.</span></span>

#### <span data-ttu-id="e3ab4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3ab4-110">Property value</span></span>
<span data-ttu-id="e3ab4-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="e3ab4-111">Type: **DOMString**</span></span>

### <span data-ttu-id="e3ab4-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="e3ab4-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>

<span data-ttu-id="e3ab4-113">Obtiene un valor que indica si el proceso de [WebView](../webview.md) tiene la [declaración de funcionalidades](/windows/uwp/packaging/app-capability-declarations) de la aplicación universal de Windows *(cliente & servidor)* habilitada en el manifiesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

<span data-ttu-id="e3ab4-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-114">This property is read-only.</span></span>

#### <span data-ttu-id="e3ab4-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3ab4-115">Property value</span></span>
<span data-ttu-id="e3ab4-116">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e3ab4-116">Type: **Boolean**</span></span>

## <span data-ttu-id="e3ab4-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3ab4-117">Methods</span></span>

### <span data-ttu-id="e3ab4-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="e3ab4-118">CreateWebViewAsync</span></span>

<span data-ttu-id="e3ab4-119">Crea un [WebView](../webview.md) en un proceso específico.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-119">Creates a [webview](../webview.md) in a specific process.</span></span>

```js
wvprocess.createWebviewAsync();
```

#### <span data-ttu-id="e3ab4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3ab4-120">Return value</span></span>

<span data-ttu-id="e3ab4-121">Escrita**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="e3ab4-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="e3ab4-122">GetWebViews</span><span class="sxs-lookup"><span data-stu-id="e3ab4-122">GetWebViews</span></span>

<span data-ttu-id="e3ab4-123">Devuelve una secuencia de objetos **MSWebViewProcess** hospedados en el proceso.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>

#### <span data-ttu-id="e3ab4-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3ab4-124">Return value</span></span>

<span data-ttu-id="e3ab4-125">Escrita**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="e3ab4-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="e3ab4-126">Detiene</span><span class="sxs-lookup"><span data-stu-id="e3ab4-126">Terminate</span></span>

<span data-ttu-id="e3ab4-127">Finaliza el proceso.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-127">Terminates the process.</span></span>

```js
wvprocess.terminate();
```

#### <span data-ttu-id="e3ab4-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3ab4-128">Return value</span></span>

<span data-ttu-id="e3ab4-129">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e3ab4-129">This method does not return a value.</span></span>
