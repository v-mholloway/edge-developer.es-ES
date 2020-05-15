---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 480b79cce673be530219718fb7f4920f5d1e80ae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655404"
---
# <span data-ttu-id="02dbe-104">interfaz ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="02dbe-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="02dbe-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="02dbe-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="02dbe-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="02dbe-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="02dbe-107">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="02dbe-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="02dbe-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="02dbe-108">Summary</span></span>

 <span data-ttu-id="02dbe-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="02dbe-109">Members</span></span>                        | <span data-ttu-id="02dbe-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="02dbe-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="02dbe-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="02dbe-111">Invoke</span></span>](#invoke) | <span data-ttu-id="02dbe-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="02dbe-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="02dbe-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="02dbe-113">Members</span></span>

#### <span data-ttu-id="02dbe-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="02dbe-114">Invoke</span></span> 

<span data-ttu-id="02dbe-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="02dbe-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="02dbe-116">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="02dbe-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

