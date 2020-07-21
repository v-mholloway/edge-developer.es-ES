---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 5cc3ca23dcababc35a73b44a81c54439d0dbe1a3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884312"
---
# <span data-ttu-id="a493c-104">0.9.430: ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a493c-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a493c-105">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="a493c-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="a493c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a493c-106">Summary</span></span>

 <span data-ttu-id="a493c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a493c-107">Members</span></span>                        | <span data-ttu-id="a493c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a493c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a493c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a493c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a493c-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a493c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a493c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a493c-111">Members</span></span>

#### <span data-ttu-id="a493c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a493c-112">Invoke</span></span> 

<span data-ttu-id="a493c-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a493c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a493c-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="a493c-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>

