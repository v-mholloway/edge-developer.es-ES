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
ms.openlocfilehash: 30fc5e258c73b880009bc48e9213c647a5542917
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655250"
---
# <span data-ttu-id="5392f-104">interfaz ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5392f-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="5392f-105">La persona que llama implementa esta interfaz para recibir eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="5392f-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="5392f-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="5392f-106">Summary</span></span>

 <span data-ttu-id="5392f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5392f-107">Members</span></span>                        | <span data-ttu-id="5392f-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5392f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5392f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5392f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5392f-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5392f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="5392f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5392f-111">Members</span></span>

#### <span data-ttu-id="5392f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5392f-112">Invoke</span></span> 

<span data-ttu-id="5392f-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5392f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5392f-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5392f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>

