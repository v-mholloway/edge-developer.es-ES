---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1082ea61b98b953277219d78a2944a2487b47a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884445"
---
# <span data-ttu-id="cf024-104">0.9.515: ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="cf024-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="cf024-105">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="cf024-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="cf024-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="cf024-106">Summary</span></span>

 <span data-ttu-id="cf024-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf024-107">Members</span></span>                        | <span data-ttu-id="cf024-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cf024-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf024-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="cf024-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cf024-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cf024-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="cf024-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf024-111">Members</span></span>

#### <span data-ttu-id="cf024-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="cf024-112">Invoke</span></span> 

<span data-ttu-id="cf024-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cf024-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="cf024-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="cf024-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

