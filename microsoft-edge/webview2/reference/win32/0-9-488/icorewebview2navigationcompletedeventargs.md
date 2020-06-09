---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 83f55e19c8c8c0f2fb075ff47e95e34be27c6602
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697339"
---
# <span data-ttu-id="8117c-104">interfaz ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8117c-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="8117c-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="8117c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8117c-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="8117c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="8117c-107">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="8117c-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="8117c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="8117c-108">Summary</span></span>

 <span data-ttu-id="8117c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8117c-109">Members</span></span>                        | <span data-ttu-id="8117c-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8117c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8117c-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="8117c-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="8117c-112">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="8117c-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="8117c-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="8117c-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="8117c-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="8117c-114">The ID of the navigation.</span></span>
[<span data-ttu-id="8117c-115">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="8117c-115">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="8117c-116">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="8117c-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="8117c-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="8117c-117">Members</span></span>

#### <span data-ttu-id="8117c-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="8117c-118">get_IsSuccess</span></span> 

<span data-ttu-id="8117c-119">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="8117c-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="8117c-120">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="8117c-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="8117c-121">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="8117c-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="8117c-122">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="8117c-122">get_NavigationId</span></span> 

<span data-ttu-id="8117c-123">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="8117c-123">The ID of the navigation.</span></span>

> <span data-ttu-id="8117c-124">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="8117c-124">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="8117c-125">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="8117c-125">get_WebErrorStatus</span></span> 

<span data-ttu-id="8117c-126">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="8117c-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="8117c-127">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="8117c-127">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

