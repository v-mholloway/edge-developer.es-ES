---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 3ecafb8181b04032bf121a93af3771cfcad8fa91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011170"
---
# <span data-ttu-id="f4b8b-104">0.9.579: ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f4b8b-104">0.9.579 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f4b8b-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="f4b8b-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="f4b8b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="f4b8b-106">Summary</span></span>

 <span data-ttu-id="f4b8b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4b8b-107">Members</span></span>                        | <span data-ttu-id="f4b8b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f4b8b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f4b8b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f4b8b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f4b8b-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f4b8b-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f4b8b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4b8b-111">Members</span></span>

#### <span data-ttu-id="f4b8b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f4b8b-112">Invoke</span></span> 

<span data-ttu-id="f4b8b-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f4b8b-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f4b8b-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="f4b8b-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

