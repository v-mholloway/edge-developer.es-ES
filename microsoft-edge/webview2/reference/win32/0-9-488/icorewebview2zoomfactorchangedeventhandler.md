---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e2469dd9a587735efcf88a48e0ce950cb4f85239
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655364"
---
# <span data-ttu-id="e4c89-104">interfaz ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e4c89-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e4c89-105">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="e4c89-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="e4c89-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e4c89-106">Summary</span></span>

 <span data-ttu-id="e4c89-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4c89-107">Members</span></span>                        | <span data-ttu-id="e4c89-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e4c89-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4c89-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e4c89-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e4c89-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e4c89-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e4c89-111">Usa la propiedad ICoreWebView2Controller. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="e4c89-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="e4c89-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4c89-112">Members</span></span>

#### <span data-ttu-id="e4c89-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e4c89-113">Invoke</span></span> 

<span data-ttu-id="e4c89-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e4c89-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e4c89-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e4c89-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="e4c89-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="e4c89-116">There are no event args and the args parameter will be null.</span></span>

