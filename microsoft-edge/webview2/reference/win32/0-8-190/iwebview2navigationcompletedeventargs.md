---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: fa1debd3b212492eea03e4ecf6e5daff5751f89b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655278"
---
# <span data-ttu-id="fec4f-104">interfaz IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="fec4f-104">interface IWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="fec4f-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="fec4f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="fec4f-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="fec4f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="fec4f-107">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="fec4f-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="fec4f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="fec4f-108">Summary</span></span>

 <span data-ttu-id="fec4f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fec4f-109">Members</span></span>                        | <span data-ttu-id="fec4f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fec4f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fec4f-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="fec4f-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="fec4f-112">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="fec4f-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="fec4f-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="fec4f-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="fec4f-114">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="fec4f-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="fec4f-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="fec4f-115">Members</span></span>

#### <span data-ttu-id="fec4f-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="fec4f-116">get_IsSuccess</span></span> 

<span data-ttu-id="fec4f-117">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="fec4f-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="fec4f-118">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="fec4f-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="fec4f-119">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="fec4f-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="fec4f-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="fec4f-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="fec4f-121">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="fec4f-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="fec4f-122">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="fec4f-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

