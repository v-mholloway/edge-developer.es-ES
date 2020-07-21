---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: aeb6e2e25ca9f8c454f5dff891f2c488591d2a48
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884935"
---
# <span data-ttu-id="e5e45-104">0.8.355: IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e5e45-104">0.8.355 - interface IWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e5e45-105">La persona que llama implementa esta interfaz para recibir el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="e5e45-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="e5e45-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e5e45-106">Summary</span></span>

 <span data-ttu-id="e5e45-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5e45-107">Members</span></span>                        | <span data-ttu-id="e5e45-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e5e45-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5e45-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5e45-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e5e45-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e5e45-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e5e45-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5e45-111">Members</span></span>

#### <span data-ttu-id="e5e45-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5e45-112">Invoke</span></span> 

<span data-ttu-id="e5e45-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e5e45-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e5e45-114">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e5e45-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

