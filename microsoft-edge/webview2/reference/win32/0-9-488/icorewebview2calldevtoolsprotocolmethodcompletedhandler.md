---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: fda3ab31405a7d6353af1a670a2804e973577c8e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655280"
---
# <span data-ttu-id="5ec6c-104">interfaz ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5ec6c-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5ec6c-105">La persona que llama implementa esta interfaz para recibir resultados de finalización de CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="5ec6c-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="5ec6c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="5ec6c-106">Summary</span></span>

 <span data-ttu-id="5ec6c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ec6c-107">Members</span></span>                        | <span data-ttu-id="5ec6c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5ec6c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5ec6c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5ec6c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5ec6c-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5ec6c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="5ec6c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ec6c-111">Members</span></span>

#### <span data-ttu-id="5ec6c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5ec6c-112">Invoke</span></span> 

<span data-ttu-id="5ec6c-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5ec6c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5ec6c-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="5ec6c-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

