---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 42031b966f799b788a94938d88d9dec6f4542288
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878543"
---
# <span data-ttu-id="04c14-104">0.8.355: IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="04c14-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="04c14-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="04c14-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="04c14-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="04c14-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="04c14-107">La persona que llama implementa esta interfaz para recibir eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="04c14-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="04c14-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="04c14-108">Summary</span></span>

 <span data-ttu-id="04c14-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="04c14-109">Members</span></span>                        | <span data-ttu-id="04c14-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="04c14-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04c14-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="04c14-111">Invoke</span></span>](#invoke) | <span data-ttu-id="04c14-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="04c14-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="04c14-113">Use la propiedad DocumentTitle para obtener el título modificado.</span><span class="sxs-lookup"><span data-stu-id="04c14-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="04c14-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="04c14-114">Members</span></span>

#### <span data-ttu-id="04c14-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="04c14-115">Invoke</span></span> 

<span data-ttu-id="04c14-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="04c14-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="04c14-117">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="04c14-117">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="04c14-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="04c14-118">There are no event args and the args parameter will be null.</span></span>

