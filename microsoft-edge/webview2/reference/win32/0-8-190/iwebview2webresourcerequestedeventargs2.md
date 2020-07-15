---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 80ea596f28d1afeb451ce20d495961ca4eed507a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878116"
---
# <span data-ttu-id="3b357-104">0.8.355: IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="3b357-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="3b357-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3b357-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3b357-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="3b357-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="3b357-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3b357-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="3b357-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="3b357-108">Summary</span></span>

 <span data-ttu-id="3b357-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b357-109">Members</span></span>                        | <span data-ttu-id="3b357-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3b357-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3b357-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="3b357-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="3b357-112">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="3b357-112">The web resource request contexts.</span></span>

## <span data-ttu-id="3b357-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b357-113">Members</span></span>

#### <span data-ttu-id="3b357-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="3b357-114">get_ResourceContext</span></span> 

<span data-ttu-id="3b357-115">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="3b357-115">The web resource request contexts.</span></span>

> <span data-ttu-id="3b357-116">[get_ResourceContext](#get_resourcecontext)de HRESULT público (WEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="3b357-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

