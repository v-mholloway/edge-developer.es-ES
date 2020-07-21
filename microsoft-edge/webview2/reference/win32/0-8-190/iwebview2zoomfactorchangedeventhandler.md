---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 237179df5ef704fb88516780696f3a9c10c9a198
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884669"
---
# <span data-ttu-id="6ed8f-104">0.8.355: IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6ed8f-104">0.8.355 - interface IWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6ed8f-105">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="6ed8f-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="6ed8f-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6ed8f-106">Summary</span></span>

 <span data-ttu-id="6ed8f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ed8f-107">Members</span></span>                        | <span data-ttu-id="6ed8f-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6ed8f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6ed8f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6ed8f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6ed8f-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6ed8f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6ed8f-111">Usa la propiedad IWebView2WebView. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="6ed8f-111">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="6ed8f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ed8f-112">Members</span></span>

#### <span data-ttu-id="6ed8f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="6ed8f-113">Invoke</span></span> 

<span data-ttu-id="6ed8f-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6ed8f-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6ed8f-115">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6ed8f-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="6ed8f-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="6ed8f-116">There are no event args and the args parameter will be null.</span></span>

