---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 215297bf56234452aad33e135cfb03ec079a049b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877976"
---
# <span data-ttu-id="8d050-104">0.9.430: ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d050-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="8d050-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="8d050-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8d050-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="8d050-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="8d050-107">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="8d050-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="8d050-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="8d050-108">Summary</span></span>

 <span data-ttu-id="8d050-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d050-109">Members</span></span>                        | <span data-ttu-id="8d050-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8d050-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8d050-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="8d050-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="8d050-112">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="8d050-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="8d050-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="8d050-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="8d050-114">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="8d050-114">The error code if the navigation failed.</span></span>
[<span data-ttu-id="8d050-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="8d050-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="8d050-116">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="8d050-116">The ID of the navigation.</span></span>

## <span data-ttu-id="8d050-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d050-117">Members</span></span>

#### <span data-ttu-id="8d050-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="8d050-118">get_IsSuccess</span></span> 

<span data-ttu-id="8d050-119">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="8d050-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="8d050-120">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="8d050-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="8d050-121">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="8d050-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="8d050-122">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="8d050-122">get_WebErrorStatus</span></span> 

<span data-ttu-id="8d050-123">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="8d050-123">The error code if the navigation failed.</span></span>

> <span data-ttu-id="8d050-124">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="8d050-124">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="8d050-125">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="8d050-125">get_NavigationId</span></span> 

<span data-ttu-id="8d050-126">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="8d050-126">The ID of the navigation.</span></span>

> <span data-ttu-id="8d050-127">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="8d050-127">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

