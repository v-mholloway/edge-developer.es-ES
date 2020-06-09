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
ms.openlocfilehash: 45ac3cf4728f8b09f9ce65a30b53506fc2829c9d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699373"
---
# <span data-ttu-id="4cbd0-104">interfaz ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="4cbd0-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="4cbd0-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="4cbd0-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="4cbd0-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="4cbd0-106">Summary</span></span>

 <span data-ttu-id="4cbd0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4cbd0-107">Members</span></span>                        | <span data-ttu-id="4cbd0-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4cbd0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4cbd0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4cbd0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4cbd0-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4cbd0-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="4cbd0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4cbd0-111">Members</span></span>

#### <span data-ttu-id="4cbd0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4cbd0-112">Invoke</span></span> 

<span data-ttu-id="4cbd0-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4cbd0-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="4cbd0-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="4cbd0-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

