---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 116679e5b4168803af1c7e2909eb590af2378623
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012699"
---
# <span data-ttu-id="e9303-104">interfaz ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9303-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e9303-105">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="e9303-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="e9303-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e9303-106">Summary</span></span>

 <span data-ttu-id="e9303-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9303-107">Members</span></span>                        | <span data-ttu-id="e9303-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e9303-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e9303-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9303-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e9303-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e9303-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e9303-111">Usa la propiedad ICoreWebView2Controller. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="e9303-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="e9303-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9303-112">Members</span></span>

#### <span data-ttu-id="e9303-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9303-113">Invoke</span></span> 

<span data-ttu-id="e9303-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e9303-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e9303-115">invocación [Invoke](#invoke)pública de HRESULT (ICoreWebView2Controller \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e9303-115">public HRESULT [Invoke](#invoke)(ICoreWebView2Controller \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="e9303-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="e9303-116">There are no event args and the args parameter will be null.</span></span>

