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
ms.openlocfilehash: 889728489b6c4b06cd224915a0e12ee0a4144653
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655119"
---
# <span data-ttu-id="38fc2-104">interfaz ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="38fc2-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="38fc2-105">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="38fc2-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="38fc2-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="38fc2-106">Summary</span></span>

 <span data-ttu-id="38fc2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="38fc2-107">Members</span></span>                        | <span data-ttu-id="38fc2-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="38fc2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="38fc2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="38fc2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="38fc2-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="38fc2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="38fc2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="38fc2-111">Members</span></span>

#### <span data-ttu-id="38fc2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="38fc2-112">Invoke</span></span> 

<span data-ttu-id="38fc2-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="38fc2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="38fc2-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="38fc2-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="38fc2-115">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="38fc2-115">There are no event args and the args parameter will be null.</span></span>

