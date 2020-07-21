---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 5a74464f841a0c8320bef7f81c83567d58f6caca
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884480"
---
# <span data-ttu-id="53a70-104">0.9.515: ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="53a70-104">0.9.515 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="53a70-105">La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="53a70-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="53a70-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="53a70-106">Summary</span></span>

 <span data-ttu-id="53a70-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="53a70-107">Members</span></span>                        | <span data-ttu-id="53a70-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="53a70-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="53a70-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="53a70-109">Invoke</span></span>](#invoke) | <span data-ttu-id="53a70-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53a70-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="53a70-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="53a70-111">Members</span></span>

#### <span data-ttu-id="53a70-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="53a70-112">Invoke</span></span> 

<span data-ttu-id="53a70-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53a70-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="53a70-114">invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="53a70-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

