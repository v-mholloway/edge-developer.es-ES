---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 6a707465fa08667e9915a77fdc93ee018e0f9631
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881126"
---
# <span data-ttu-id="39ec9-104">0.9.430: ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="39ec9-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="39ec9-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="39ec9-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="39ec9-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="39ec9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="39ec9-107">La persona que llama implementa esta interfaz para recibir el CoreWebView2Host creado a través de CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="39ec9-107">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="39ec9-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="39ec9-108">Summary</span></span>

 <span data-ttu-id="39ec9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="39ec9-109">Members</span></span>                        | <span data-ttu-id="39ec9-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="39ec9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="39ec9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="39ec9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="39ec9-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="39ec9-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="39ec9-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="39ec9-113">Members</span></span>

#### <span data-ttu-id="39ec9-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="39ec9-114">Invoke</span></span> 

<span data-ttu-id="39ec9-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="39ec9-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="39ec9-116">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="39ec9-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>

