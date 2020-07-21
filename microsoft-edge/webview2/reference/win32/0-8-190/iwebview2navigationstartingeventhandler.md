---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: e6f47382eb3f086618a5d0c46c2eec57a9891ff5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885880"
---
# <span data-ttu-id="9d4da-104">0.8.355: IWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="9d4da-104">0.8.355 - interface IWebView2NavigationStartingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="9d4da-105">La persona que llama implementa esta interfaz para recibir el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d4da-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="9d4da-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="9d4da-106">Summary</span></span>

 <span data-ttu-id="9d4da-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d4da-107">Members</span></span>                        | <span data-ttu-id="9d4da-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d4da-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d4da-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d4da-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9d4da-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9d4da-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9d4da-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d4da-111">Members</span></span>

#### <span data-ttu-id="9d4da-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d4da-112">Invoke</span></span> 

<span data-ttu-id="9d4da-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9d4da-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9d4da-114">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9d4da-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span></span>

