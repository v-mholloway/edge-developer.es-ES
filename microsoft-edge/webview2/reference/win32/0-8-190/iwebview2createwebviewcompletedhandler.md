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
ms.openlocfilehash: 2788a18898da1f878520f4c4eb072c1a8b43375b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655089"
---
# <span data-ttu-id="53293-104">interfaz IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="53293-104">interface IWebView2CreateWebViewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="53293-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="53293-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="53293-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="53293-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="53293-107">La persona que llama implementa esta interfaz para recibir la vista en WebView creada a través de CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="53293-107">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="53293-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="53293-108">Summary</span></span>

 <span data-ttu-id="53293-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="53293-109">Members</span></span>                        | <span data-ttu-id="53293-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="53293-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="53293-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="53293-111">Invoke</span></span>](#invoke) | <span data-ttu-id="53293-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53293-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="53293-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="53293-113">Members</span></span>

#### <span data-ttu-id="53293-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="53293-114">Invoke</span></span> 

<span data-ttu-id="53293-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53293-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="53293-116">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[IWebView2WebView](IWebView2WebView.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="53293-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>

