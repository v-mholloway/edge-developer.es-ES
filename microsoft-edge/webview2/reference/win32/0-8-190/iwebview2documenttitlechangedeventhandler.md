---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 0dc9886bc2282d08855ccb40cb8b06b4ffadb659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886118"
---
# <span data-ttu-id="471eb-104">0.8.355: IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="471eb-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="471eb-105">La persona que llama implementa esta interfaz para recibir eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="471eb-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="471eb-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="471eb-106">Summary</span></span>

 <span data-ttu-id="471eb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="471eb-107">Members</span></span>                        | <span data-ttu-id="471eb-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="471eb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="471eb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="471eb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="471eb-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="471eb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="471eb-111">Use la propiedad DocumentTitle para obtener el título modificado.</span><span class="sxs-lookup"><span data-stu-id="471eb-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="471eb-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="471eb-112">Members</span></span>

#### <span data-ttu-id="471eb-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="471eb-113">Invoke</span></span> 

<span data-ttu-id="471eb-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="471eb-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="471eb-115">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="471eb-115">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="471eb-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="471eb-116">There are no event args and the args parameter will be null.</span></span>

