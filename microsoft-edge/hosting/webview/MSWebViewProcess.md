---
description: Representa un proceso de WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752160"
---
# <span data-ttu-id="65453-104">Objeto MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="65453-104">MSWebViewProcess object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="65453-105">Representa un proceso de [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="65453-105">Represents a [webview](../webview.md) process.</span></span>  

```javascript
var wvprocess = new MSWebViewProcess();
```  

## <span data-ttu-id="65453-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65453-106">Properties</span></span>  

### <span data-ttu-id="65453-107">enterpriseId</span><span class="sxs-lookup"><span data-stu-id="65453-107">enterpriseId</span></span>  

<span data-ttu-id="65453-108">IDENTIFICADOR de empresa del proceso.</span><span class="sxs-lookup"><span data-stu-id="65453-108">The enterprise ID of the process.</span></span>  

```js
var enterpriseId = wvprocess.enterpriseId;
```  

<span data-ttu-id="65453-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="65453-109">This property is read-only.</span></span>  

#### <span data-ttu-id="65453-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65453-110">Property value</span></span>  

<span data-ttu-id="65453-111">Escriba: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="65453-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="65453-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="65453-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>  

<span data-ttu-id="65453-113">Obtiene un valor que indica si el proceso de [WebView](../webview.md) tiene la [declaración de funcionalidades](/windows/uwp/packaging/app-capability-declarations) de la aplicación universal de Windows *(cliente & servidor)* habilitada en el manifiesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65453-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>  

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

<span data-ttu-id="65453-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="65453-114">This property is read-only.</span></span>  

#### <span data-ttu-id="65453-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65453-115">Property value</span></span>  

<span data-ttu-id="65453-116">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65453-116">Type: **Boolean**</span></span>  

## <span data-ttu-id="65453-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="65453-117">Methods</span></span>  

### <span data-ttu-id="65453-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="65453-118">CreateWebViewAsync</span></span>  

<span data-ttu-id="65453-119">Crea un [WebView](../webview.md) en un proceso específico.</span><span class="sxs-lookup"><span data-stu-id="65453-119">Creates a [webview](../webview.md) in a specific process.</span></span>  

```javascript
wvprocess.createWebviewAsync();
```  

#### <span data-ttu-id="65453-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65453-120">Return value</span></span>  

<span data-ttu-id="65453-121">Escrita**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="65453-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="65453-122">GetWebViews</span><span class="sxs-lookup"><span data-stu-id="65453-122">GetWebViews</span></span>  

<span data-ttu-id="65453-123">Devuelve una secuencia de objetos **MSWebViewProcess** hospedados en el proceso.</span><span class="sxs-lookup"><span data-stu-id="65453-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>  

#### <span data-ttu-id="65453-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65453-124">Return value</span></span>  

<span data-ttu-id="65453-125">Escrita**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="65453-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="65453-126">Detiene</span><span class="sxs-lookup"><span data-stu-id="65453-126">Terminate</span></span>  

<span data-ttu-id="65453-127">Finaliza el proceso.</span><span class="sxs-lookup"><span data-stu-id="65453-127">Terminates the process.</span></span>  

```javascript
wvprocess.terminate();
```  

#### <span data-ttu-id="65453-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65453-128">Return value</span></span>  

<span data-ttu-id="65453-129">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="65453-129">This method does not return a value.</span></span>  
