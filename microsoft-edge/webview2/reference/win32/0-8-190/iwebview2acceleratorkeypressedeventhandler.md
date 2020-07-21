---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 7d510a547e43a4f04ef517c393ceeb3040d914e7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885034"
---
# <span data-ttu-id="dec76-104">0.8.355: IWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="dec76-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="dec76-105">La persona que llama implementa esta interfaz para recibir el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="dec76-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="dec76-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="dec76-106">Summary</span></span>

 <span data-ttu-id="dec76-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dec76-107">Members</span></span>                        | <span data-ttu-id="dec76-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="dec76-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dec76-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="dec76-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dec76-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dec76-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="dec76-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="dec76-111">Members</span></span>

#### <span data-ttu-id="dec76-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="dec76-112">Invoke</span></span> 

<span data-ttu-id="dec76-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dec76-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dec76-114">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="dec76-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

