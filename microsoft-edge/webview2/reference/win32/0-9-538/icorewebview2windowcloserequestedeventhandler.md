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
ms.openlocfilehash: 0d02fb1c8605bc6817085748154055cdfa489da8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699427"
---
# <span data-ttu-id="1b35f-104">interfaz ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1b35f-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="1b35f-105">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="1b35f-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="1b35f-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="1b35f-106">Summary</span></span>

 <span data-ttu-id="1b35f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b35f-107">Members</span></span>                        | <span data-ttu-id="1b35f-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1b35f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b35f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b35f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1b35f-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b35f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="1b35f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b35f-111">Members</span></span>

#### <span data-ttu-id="1b35f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b35f-112">Invoke</span></span> 

<span data-ttu-id="1b35f-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b35f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1b35f-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1b35f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="1b35f-115">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="1b35f-115">There are no event args and the args parameter will be null.</span></span>

