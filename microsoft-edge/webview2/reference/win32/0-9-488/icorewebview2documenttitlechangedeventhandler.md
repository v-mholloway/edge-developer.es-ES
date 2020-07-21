---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 486218dcb54281da559fb5b5f69314248a0d2cad
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883822"
---
# <span data-ttu-id="ccd60-104">0.9.515: ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ccd60-104">0.9.515 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ccd60-105">La persona que llama implementa esta interfaz para recibir eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="ccd60-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="ccd60-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ccd60-106">Summary</span></span>

 <span data-ttu-id="ccd60-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ccd60-107">Members</span></span>                        | <span data-ttu-id="ccd60-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ccd60-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ccd60-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ccd60-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ccd60-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ccd60-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ccd60-111">Use la propiedad DocumentTitle para obtener el título modificado.</span><span class="sxs-lookup"><span data-stu-id="ccd60-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="ccd60-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="ccd60-112">Members</span></span>

#### <span data-ttu-id="ccd60-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="ccd60-113">Invoke</span></span> 

<span data-ttu-id="ccd60-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ccd60-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ccd60-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ccd60-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ccd60-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="ccd60-116">There are no event args and the args parameter will be null.</span></span>

