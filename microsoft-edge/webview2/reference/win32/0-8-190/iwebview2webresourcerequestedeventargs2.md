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
ms.openlocfilehash: c23e6bcd18e3b0fe7d2ee9b279e65fc81fe89d3d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655130"
---
# <span data-ttu-id="9d038-104">interfaz IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="9d038-104">interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="9d038-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="9d038-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="9d038-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9d038-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="9d038-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d038-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9d038-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9d038-108">Summary</span></span>

 <span data-ttu-id="9d038-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d038-109">Members</span></span>                        | <span data-ttu-id="9d038-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d038-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d038-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9d038-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="9d038-112">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9d038-112">The web resource request contexts.</span></span>

## <span data-ttu-id="9d038-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d038-113">Members</span></span>

#### <span data-ttu-id="9d038-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9d038-114">get_ResourceContext</span></span> 

<span data-ttu-id="9d038-115">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9d038-115">The web resource request contexts.</span></span>

> <span data-ttu-id="9d038-116">[get_ResourceContext](#get_resourcecontext)de HRESULT público (WEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="9d038-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

