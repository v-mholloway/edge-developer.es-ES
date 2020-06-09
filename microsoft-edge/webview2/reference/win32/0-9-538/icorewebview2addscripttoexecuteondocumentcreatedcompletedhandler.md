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
ms.openlocfilehash: 9777a27c1b9252d0d1a5f91a4692b9043fffc569
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699385"
---
# <span data-ttu-id="2d466-104">interfaz ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2d466-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="2d466-105">La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2d466-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="2d466-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="2d466-106">Summary</span></span>

 <span data-ttu-id="2d466-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d466-107">Members</span></span>                        | <span data-ttu-id="2d466-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2d466-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d466-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2d466-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2d466-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2d466-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="2d466-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d466-111">Members</span></span>

#### <span data-ttu-id="2d466-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2d466-112">Invoke</span></span> 

<span data-ttu-id="2d466-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2d466-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="2d466-114">invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2d466-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

