---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
ms.openlocfilehash: 9447420abddfdb44394042d6742ed1dafd299adf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886565"
---
# <span data-ttu-id="602e8-104">interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="602e8-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="602e8-105">Se desencadena cuando se recibe una respuesta para una solicitud de un recurso Web en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="602e8-105">Fires when a response for a request is received for a Web resource in the webview.</span></span>

## <span data-ttu-id="602e8-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="602e8-106">Summary</span></span>

 <span data-ttu-id="602e8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="602e8-107">Members</span></span>                        | <span data-ttu-id="602e8-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="602e8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="602e8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="602e8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="602e8-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="602e8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="602e8-111">El anfitrión puede usar este evento para ver la solicitud y la respuesta reales de un recurso Web.</span><span class="sxs-lookup"><span data-stu-id="602e8-111">Host can use this event to view the actual request and response for a Web resource.</span></span> <span data-ttu-id="602e8-112">Esto incluye cualquier modificación de solicitud o respuesta realizada por la pila de red (como agregar encabezados de autorización) después de que se haya desencadenado el evento WebResourceRequested para la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="602e8-112">This includes any request or response modifications made by the network stack (such as adding of Authorization headers) after the WebResourceRequested event for the associated request has fired.</span></span> <span data-ttu-id="602e8-113">Las modificaciones realizadas en los objetos de solicitud o respuesta se pasan por alto.</span><span class="sxs-lookup"><span data-stu-id="602e8-113">Modifications made to the request or response objects are ignored.</span></span>

## <span data-ttu-id="602e8-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="602e8-114">Members</span></span>

#### <span data-ttu-id="602e8-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="602e8-115">Invoke</span></span> 

<span data-ttu-id="602e8-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="602e8-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="602e8-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Experimental](icorewebview2experimental.md) \* Sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="602e8-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span></span>

