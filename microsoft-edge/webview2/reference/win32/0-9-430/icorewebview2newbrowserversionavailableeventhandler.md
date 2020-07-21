---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 04859c0a22e8571a4fe8015a089c9b7d708c1dd3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884879"
---
# <span data-ttu-id="983c8-104">0.9.430: ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="983c8-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="983c8-105">La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="983c8-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="983c8-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="983c8-106">Summary</span></span>

 <span data-ttu-id="983c8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="983c8-107">Members</span></span>                        | <span data-ttu-id="983c8-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="983c8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="983c8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="983c8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="983c8-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="983c8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="983c8-111">Use el método get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) para obtener el nuevo número de versión.</span><span class="sxs-lookup"><span data-stu-id="983c8-111">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="983c8-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="983c8-112">Members</span></span>

#### <span data-ttu-id="983c8-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="983c8-113">Invoke</span></span> 

<span data-ttu-id="983c8-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="983c8-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="983c8-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="983c8-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

