---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b7c920be1c203fe30174fccbc6736bb76fe389cb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884564"
---
# <span data-ttu-id="a0092-104">0.9.515: ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0092-104">0.9.515 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="a0092-105">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="a0092-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="a0092-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a0092-106">Summary</span></span>

 <span data-ttu-id="a0092-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0092-107">Members</span></span>                        | <span data-ttu-id="a0092-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a0092-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0092-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="a0092-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="a0092-110">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="a0092-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="a0092-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a0092-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="a0092-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="a0092-112">The ID of the navigation.</span></span>
[<span data-ttu-id="a0092-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="a0092-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="a0092-114">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="a0092-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="a0092-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0092-115">Members</span></span>

#### <span data-ttu-id="a0092-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="a0092-116">get_IsSuccess</span></span> 

<span data-ttu-id="a0092-117">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="a0092-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="a0092-118">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="a0092-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="a0092-119">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="a0092-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="a0092-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a0092-120">get_NavigationId</span></span> 

<span data-ttu-id="a0092-121">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="a0092-121">The ID of the navigation.</span></span>

> <span data-ttu-id="a0092-122">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="a0092-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="a0092-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="a0092-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="a0092-124">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="a0092-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="a0092-125">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="a0092-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

