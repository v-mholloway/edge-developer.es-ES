---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: 482137fd0ffa10c60381d5b0f3dc3d7db6f9fdf7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011296"
---
# <span data-ttu-id="adf87-104">0.9.579: ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="adf87-104">0.9.579 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="adf87-105">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="adf87-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="adf87-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="adf87-106">Summary</span></span>

 <span data-ttu-id="adf87-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="adf87-107">Members</span></span>                        | <span data-ttu-id="adf87-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="adf87-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="adf87-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="adf87-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="adf87-110">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="adf87-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="adf87-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="adf87-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="adf87-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="adf87-112">The ID of the navigation.</span></span>
[<span data-ttu-id="adf87-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="adf87-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="adf87-114">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="adf87-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="adf87-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="adf87-115">Members</span></span>

#### <span data-ttu-id="adf87-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="adf87-116">get_IsSuccess</span></span> 

<span data-ttu-id="adf87-117">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="adf87-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="adf87-118">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="adf87-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="adf87-119">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="adf87-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="adf87-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="adf87-120">get_NavigationId</span></span> 

<span data-ttu-id="adf87-121">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="adf87-121">The ID of the navigation.</span></span>

> <span data-ttu-id="adf87-122">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="adf87-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="adf87-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="adf87-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="adf87-124">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="adf87-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="adf87-125">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="adf87-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

