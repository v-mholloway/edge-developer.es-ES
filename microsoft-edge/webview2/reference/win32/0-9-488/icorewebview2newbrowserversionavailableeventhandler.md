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
ms.openlocfilehash: 9196f2d9503efbaf9f15b43e7e6d7e80c2de00f7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655330"
---
# <span data-ttu-id="48657-104">interfaz ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="48657-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="48657-105">La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="48657-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="48657-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="48657-106">Summary</span></span>

 <span data-ttu-id="48657-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="48657-107">Members</span></span>                        | <span data-ttu-id="48657-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="48657-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="48657-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="48657-109">Invoke</span></span>](#invoke) | <span data-ttu-id="48657-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="48657-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="48657-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="48657-111">Members</span></span>

#### <span data-ttu-id="48657-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="48657-112">Invoke</span></span> 

<span data-ttu-id="48657-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="48657-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="48657-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="48657-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

