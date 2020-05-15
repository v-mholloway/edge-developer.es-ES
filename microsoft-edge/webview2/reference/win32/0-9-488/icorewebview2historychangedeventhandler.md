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
ms.openlocfilehash: 42e3767ad2a42a1d9e9931efa8a4fe844ea80dba
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655126"
---
# <span data-ttu-id="e897a-104">interfaz ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e897a-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e897a-105">La persona que llama implementa esta interfaz para recibir el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="e897a-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="e897a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e897a-106">Summary</span></span>

 <span data-ttu-id="e897a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e897a-107">Members</span></span>                        | <span data-ttu-id="e897a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e897a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e897a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e897a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e897a-110">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="e897a-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="e897a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e897a-111">Members</span></span>

#### <span data-ttu-id="e897a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e897a-112">Invoke</span></span> 

<span data-ttu-id="e897a-113">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="e897a-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="e897a-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e897a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

