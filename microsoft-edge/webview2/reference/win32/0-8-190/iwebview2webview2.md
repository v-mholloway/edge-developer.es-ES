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
ms.openlocfilehash: 62daeaab702b431f787bc800ab79664fc183c4ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655068"
---
# <span data-ttu-id="eac6f-104">interfaz IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="eac6f-104">interface IWebView2WebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="eac6f-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="eac6f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="eac6f-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="eac6f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="eac6f-107">Funcionalidad adicional implementada por el objeto WebView principal.</span><span class="sxs-lookup"><span data-stu-id="eac6f-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="eac6f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="eac6f-108">Summary</span></span>

 <span data-ttu-id="eac6f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="eac6f-109">Members</span></span>                        | <span data-ttu-id="eac6f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="eac6f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eac6f-111">Detener</span><span class="sxs-lookup"><span data-stu-id="eac6f-111">Stop</span></span>](#stop) | <span data-ttu-id="eac6f-112">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="eac6f-112">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="eac6f-113">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="eac6f-113">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="eac6f-114">Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="eac6f-114">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="eac6f-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="eac6f-115">Members</span></span>

#### <span data-ttu-id="eac6f-116">Detener</span><span class="sxs-lookup"><span data-stu-id="eac6f-116">Stop</span></span> 

<span data-ttu-id="eac6f-117">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="eac6f-117">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="eac6f-118">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="eac6f-118">public HRESULT [Stop](#stop)()</span></span>

