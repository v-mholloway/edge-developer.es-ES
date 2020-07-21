---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 9c2b5568e6a276b07dc91bd639c730b2009aa9e5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884284"
---
# <span data-ttu-id="e7019-104">0.9.430: ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e7019-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e7019-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Host creado a través de CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="e7019-105">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="e7019-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e7019-106">Summary</span></span>

 <span data-ttu-id="e7019-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7019-107">Members</span></span>                        | <span data-ttu-id="e7019-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e7019-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e7019-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e7019-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e7019-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e7019-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e7019-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7019-111">Members</span></span>

#### <span data-ttu-id="e7019-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e7019-112">Invoke</span></span> 

<span data-ttu-id="e7019-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e7019-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e7019-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="e7019-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>

