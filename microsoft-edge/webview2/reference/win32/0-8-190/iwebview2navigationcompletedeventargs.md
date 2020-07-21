---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: b496c37949e934fadf0af736059566edcab9f5c3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885936"
---
# <span data-ttu-id="b6822-104">0.8.355: IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b6822-104">0.8.355 - interface IWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="b6822-105">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="b6822-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="b6822-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b6822-106">Summary</span></span>

 <span data-ttu-id="b6822-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6822-107">Members</span></span>                        | <span data-ttu-id="b6822-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b6822-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b6822-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b6822-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="b6822-110">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="b6822-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="b6822-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b6822-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="b6822-112">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6822-112">The error code if the navigation failed.</span></span>

## <span data-ttu-id="b6822-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6822-113">Members</span></span>

#### <span data-ttu-id="b6822-114">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b6822-114">get_IsSuccess</span></span> 

<span data-ttu-id="b6822-115">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="b6822-115">True when the navigation is successful.</span></span>

> <span data-ttu-id="b6822-116">[get_IsSuccess](#get_issuccess)de HRESULT público (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="b6822-116">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="b6822-117">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="b6822-117">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="b6822-118">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b6822-118">get_WebErrorStatus</span></span> 

<span data-ttu-id="b6822-119">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6822-119">The error code if the navigation failed.</span></span>

> <span data-ttu-id="b6822-120">[get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="b6822-120">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

