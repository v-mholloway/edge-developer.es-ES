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
ms.openlocfilehash: b786bae624b5f0649ec443e93f741975d672d0e0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655232"
---
# <span data-ttu-id="0ac48-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0ac48-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0ac48-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="0ac48-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="0ac48-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="0ac48-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="0ac48-107">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="0ac48-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="0ac48-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="0ac48-108">Summary</span></span>

 <span data-ttu-id="0ac48-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ac48-109">Members</span></span>                        | <span data-ttu-id="0ac48-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0ac48-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0ac48-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ac48-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0ac48-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0ac48-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0ac48-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ac48-113">Members</span></span>

#### <span data-ttu-id="0ac48-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ac48-114">Invoke</span></span> 

<span data-ttu-id="0ac48-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0ac48-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0ac48-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0ac48-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>

