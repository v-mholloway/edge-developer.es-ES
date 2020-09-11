---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: b45920cfdab8a01d1288fbaf566748545b8a2c98
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012655"
---
# <span data-ttu-id="031b5-104">interfaz ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="031b5-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="031b5-105">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="031b5-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="031b5-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="031b5-106">Summary</span></span>

 <span data-ttu-id="031b5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="031b5-107">Members</span></span>                        | <span data-ttu-id="031b5-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="031b5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="031b5-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="031b5-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="031b5-110">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="031b5-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="031b5-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="031b5-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="031b5-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="031b5-112">The ID of the navigation.</span></span>
[<span data-ttu-id="031b5-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="031b5-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="031b5-114">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="031b5-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="031b5-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="031b5-115">Members</span></span>

#### <span data-ttu-id="031b5-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="031b5-116">get_IsSuccess</span></span> 

<span data-ttu-id="031b5-117">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="031b5-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="031b5-118">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="031b5-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="031b5-119">Esto es falso para una navegación que finalizó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso para escenarios adicionales como Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="031b5-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional scenarios such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="031b5-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="031b5-120">get_NavigationId</span></span> 

<span data-ttu-id="031b5-121">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="031b5-121">The ID of the navigation.</span></span>

> <span data-ttu-id="031b5-122">[get_NavigationId](#get_navigationid)(HRESULT) público (UINT64 \* NavigationId)</span><span class="sxs-lookup"><span data-stu-id="031b5-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

#### <span data-ttu-id="031b5-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="031b5-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="031b5-124">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="031b5-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="031b5-125">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (COREWEBVIEW2_WEB_ERROR_STATUS \* WebErrorStatus)</span><span class="sxs-lookup"><span data-stu-id="031b5-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* webErrorStatus)</span></span>

