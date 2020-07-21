---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 91cd4245ff6c75e72457410211deefd9ab7f09d1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883696"
---
# <span data-ttu-id="11687-104">0.9.515: ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="11687-104">0.9.515 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="11687-105">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="11687-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="11687-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="11687-106">Summary</span></span>

 <span data-ttu-id="11687-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="11687-107">Members</span></span>                        | <span data-ttu-id="11687-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="11687-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="11687-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="11687-109">Invoke</span></span>](#invoke) | <span data-ttu-id="11687-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="11687-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="11687-111">Usa la propiedad ICoreWebView2Controller. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="11687-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="11687-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="11687-112">Members</span></span>

#### <span data-ttu-id="11687-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="11687-113">Invoke</span></span> 

<span data-ttu-id="11687-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="11687-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="11687-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="11687-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="11687-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="11687-116">There are no event args and the args parameter will be null.</span></span>

