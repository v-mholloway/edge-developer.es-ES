---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: f0b90cec451a80225f657386fa06b8740d6e1385
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699426"
---
# <span data-ttu-id="6b9bc-104">interfaz ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6b9bc-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6b9bc-105">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="6b9bc-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6b9bc-106">Summary</span></span>

 <span data-ttu-id="6b9bc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b9bc-107">Members</span></span>                        | <span data-ttu-id="6b9bc-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6b9bc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6b9bc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6b9bc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6b9bc-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6b9bc-111">Usa la propiedad ICoreWebView2Controller. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="6b9bc-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b9bc-112">Members</span></span>

#### <span data-ttu-id="6b9bc-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="6b9bc-113">Invoke</span></span> 

<span data-ttu-id="6b9bc-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6b9bc-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6b9bc-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="6b9bc-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-116">There are no event args and the args parameter will be null.</span></span>

