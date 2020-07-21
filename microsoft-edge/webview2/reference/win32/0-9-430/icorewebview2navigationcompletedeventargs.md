---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883731"
---
# <span data-ttu-id="95dc4-104">0.9.430: ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="95dc4-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="95dc4-105">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="95dc4-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="95dc4-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="95dc4-106">Summary</span></span>

 <span data-ttu-id="95dc4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="95dc4-107">Members</span></span>                        | <span data-ttu-id="95dc4-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="95dc4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95dc4-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="95dc4-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="95dc4-110">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="95dc4-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="95dc4-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="95dc4-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="95dc4-112">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="95dc4-112">The error code if the navigation failed.</span></span>
[<span data-ttu-id="95dc4-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="95dc4-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="95dc4-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="95dc4-114">The ID of the navigation.</span></span>

## <span data-ttu-id="95dc4-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="95dc4-115">Members</span></span>

#### <span data-ttu-id="95dc4-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="95dc4-116">get_IsSuccess</span></span> 

<span data-ttu-id="95dc4-117">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="95dc4-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="95dc4-118">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="95dc4-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="95dc4-119">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="95dc4-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="95dc4-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="95dc4-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="95dc4-121">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="95dc4-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="95dc4-122">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="95dc4-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="95dc4-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="95dc4-123">get_NavigationId</span></span> 

<span data-ttu-id="95dc4-124">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="95dc4-124">The ID of the navigation.</span></span>

> <span data-ttu-id="95dc4-125">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="95dc4-125">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

