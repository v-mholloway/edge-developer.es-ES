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
ms.openlocfilehash: 7a4e074d445b4bab11e8e79dc6cfe5346effbb3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655432"
---
# <span data-ttu-id="704e6-104">interfaz IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="704e6-104">interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="704e6-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="704e6-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="704e6-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="704e6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="704e6-107">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="704e6-107">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="704e6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="704e6-108">Summary</span></span>

 <span data-ttu-id="704e6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="704e6-109">Members</span></span>                        | <span data-ttu-id="704e6-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="704e6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="704e6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="704e6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="704e6-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="704e6-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="704e6-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="704e6-113">Members</span></span>

#### <span data-ttu-id="704e6-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="704e6-114">Invoke</span></span> 

<span data-ttu-id="704e6-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="704e6-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="704e6-116">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="704e6-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>

