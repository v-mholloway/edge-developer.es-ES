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
ms.openlocfilehash: e80dca6411534968822d9994f9911828a4fddeeb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655301"
---
# <span data-ttu-id="e5b41-104">interfaz ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e5b41-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e5b41-105">La persona que llama implementa este método para recibir los eventos GotFocus y LostFocus.</span><span class="sxs-lookup"><span data-stu-id="e5b41-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="e5b41-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e5b41-106">Summary</span></span>

 <span data-ttu-id="e5b41-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5b41-107">Members</span></span>                        | <span data-ttu-id="e5b41-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e5b41-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5b41-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5b41-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e5b41-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e5b41-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e5b41-111">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e5b41-111">There are no event args for this event.</span></span>

## <span data-ttu-id="e5b41-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5b41-112">Members</span></span>

#### <span data-ttu-id="e5b41-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5b41-113">Invoke</span></span> 

<span data-ttu-id="e5b41-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e5b41-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e5b41-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e5b41-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="e5b41-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="e5b41-116">There are no event args and the args parameter will be null.</span></span>

