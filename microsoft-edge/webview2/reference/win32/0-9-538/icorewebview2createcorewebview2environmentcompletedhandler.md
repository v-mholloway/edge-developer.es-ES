---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: dbc1a3e05f9cdc5b5ced2e0b7d489b06392e6100
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699366"
---
# <span data-ttu-id="f2f35-104">interfaz ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f2f35-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f2f35-105">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="f2f35-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="f2f35-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="f2f35-106">Summary</span></span>

 <span data-ttu-id="f2f35-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2f35-107">Members</span></span>                        | <span data-ttu-id="f2f35-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f2f35-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f2f35-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f2f35-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f2f35-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f2f35-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f2f35-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2f35-111">Members</span></span>

#### <span data-ttu-id="f2f35-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f2f35-112">Invoke</span></span> 

<span data-ttu-id="f2f35-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f2f35-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f2f35-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="f2f35-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

