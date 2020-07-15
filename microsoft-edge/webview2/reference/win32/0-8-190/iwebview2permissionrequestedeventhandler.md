---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 3019f58ab1c0f01a63ddd906b6bd9e3137c0d0ee
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878340"
---
# <span data-ttu-id="acc96-104">0.8.355: IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="acc96-104">0.8.355 - interface IWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="acc96-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="acc96-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="acc96-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="acc96-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="acc96-107">La persona que llama implementa esta interfaz para recibir el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="acc96-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="acc96-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="acc96-108">Summary</span></span>

 <span data-ttu-id="acc96-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="acc96-109">Members</span></span>                        | <span data-ttu-id="acc96-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="acc96-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="acc96-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="acc96-111">Invoke</span></span>](#invoke) | <span data-ttu-id="acc96-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="acc96-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="acc96-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="acc96-113">Members</span></span>

#### <span data-ttu-id="acc96-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="acc96-114">Invoke</span></span> 

<span data-ttu-id="acc96-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="acc96-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="acc96-116">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="acc96-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

