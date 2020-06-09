---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ac2f17c621dc6ad5093bacac685e01688a663cb1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697955"
---
# <span data-ttu-id="c62fc-104">interfaz ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c62fc-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c62fc-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c62fc-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c62fc-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="c62fc-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c62fc-107">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="c62fc-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c62fc-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c62fc-108">Summary</span></span>

 <span data-ttu-id="c62fc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c62fc-109">Members</span></span>                        | <span data-ttu-id="c62fc-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c62fc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c62fc-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c62fc-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c62fc-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c62fc-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c62fc-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="c62fc-113">Members</span></span>

#### <span data-ttu-id="c62fc-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c62fc-114">Invoke</span></span> 

<span data-ttu-id="c62fc-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c62fc-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c62fc-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c62fc-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

