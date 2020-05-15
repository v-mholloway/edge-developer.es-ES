---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 1d2956aee178c2bdc581d51a93006e14cfb539e3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655235"
---
# <span data-ttu-id="e4cac-104">interfaz ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e4cac-104">interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e4cac-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e4cac-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e4cac-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="e4cac-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e4cac-107">La persona que llama implementa esta interfaz para recibir el CoreWebView2Host creado a través de CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="e4cac-107">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="e4cac-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e4cac-108">Summary</span></span>

 <span data-ttu-id="e4cac-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4cac-109">Members</span></span>                        | <span data-ttu-id="e4cac-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e4cac-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4cac-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e4cac-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e4cac-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e4cac-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e4cac-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4cac-113">Members</span></span>

#### <span data-ttu-id="e4cac-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e4cac-114">Invoke</span></span> 

<span data-ttu-id="e4cac-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e4cac-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e4cac-116">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="e4cac-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>

