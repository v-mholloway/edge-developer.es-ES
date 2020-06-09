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
ms.openlocfilehash: 8bf8dcf40524425a7ef166c5007d60de738efb67
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699375"
---
# <span data-ttu-id="53efb-104">interfaz ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="53efb-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="53efb-105">La persona que llama implementa esta interfaz para recibir el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="53efb-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="53efb-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="53efb-106">Summary</span></span>

 <span data-ttu-id="53efb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="53efb-107">Members</span></span>                        | <span data-ttu-id="53efb-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="53efb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="53efb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="53efb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="53efb-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53efb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="53efb-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="53efb-111">Members</span></span>

#### <span data-ttu-id="53efb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="53efb-112">Invoke</span></span> 

<span data-ttu-id="53efb-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53efb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="53efb-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="53efb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

