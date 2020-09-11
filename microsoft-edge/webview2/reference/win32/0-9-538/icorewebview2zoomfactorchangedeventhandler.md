---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: c941629ab8ee87c0c964b00798878bb69265669a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011394"
---
# <span data-ttu-id="2dcbe-104">0.9.579: ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2dcbe-104">0.9.579 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="2dcbe-105">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="2dcbe-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="2dcbe-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="2dcbe-106">Summary</span></span>

 <span data-ttu-id="2dcbe-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2dcbe-107">Members</span></span>                        | <span data-ttu-id="2dcbe-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2dcbe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2dcbe-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2dcbe-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2dcbe-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2dcbe-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2dcbe-111">Usa la propiedad ICoreWebView2Controller. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="2dcbe-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="2dcbe-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="2dcbe-112">Members</span></span>

#### <span data-ttu-id="2dcbe-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="2dcbe-113">Invoke</span></span> 

<span data-ttu-id="2dcbe-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2dcbe-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2dcbe-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2dcbe-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="2dcbe-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="2dcbe-116">There are no event args and the args parameter will be null.</span></span>

