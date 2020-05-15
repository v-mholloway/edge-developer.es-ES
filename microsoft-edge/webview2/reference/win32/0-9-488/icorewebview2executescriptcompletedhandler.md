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
ms.openlocfilehash: da7b12d382776bb1755e90b0ce1c2728b555c8c8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655382"
---
# <span data-ttu-id="5fd1d-104">interfaz ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5fd1d-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5fd1d-105">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="5fd1d-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="5fd1d-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="5fd1d-106">Summary</span></span>

 <span data-ttu-id="5fd1d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5fd1d-107">Members</span></span>                        | <span data-ttu-id="5fd1d-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5fd1d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5fd1d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5fd1d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5fd1d-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5fd1d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="5fd1d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5fd1d-111">Members</span></span>

#### <span data-ttu-id="5fd1d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5fd1d-112">Invoke</span></span> 

<span data-ttu-id="5fd1d-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5fd1d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5fd1d-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="5fd1d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

