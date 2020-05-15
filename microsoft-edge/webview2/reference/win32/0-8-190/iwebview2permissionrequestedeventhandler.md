---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: d669b73edd8def1d8a44491705e0f80888da2b3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655275"
---
# <span data-ttu-id="c125a-104">interfaz IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c125a-104">interface IWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c125a-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c125a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c125a-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="c125a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c125a-107">La persona que llama implementa esta interfaz para recibir el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="c125a-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="c125a-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c125a-108">Summary</span></span>

 <span data-ttu-id="c125a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c125a-109">Members</span></span>                        | <span data-ttu-id="c125a-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c125a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c125a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c125a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c125a-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c125a-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c125a-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="c125a-113">Members</span></span>

#### <span data-ttu-id="c125a-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c125a-114">Invoke</span></span> 

<span data-ttu-id="c125a-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c125a-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c125a-116">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c125a-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

