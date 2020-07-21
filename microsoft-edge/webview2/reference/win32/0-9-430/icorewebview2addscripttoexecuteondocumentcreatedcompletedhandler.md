---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 3c34c75e62fd73530d338e618469e071648f2fcb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884347"
---
# <span data-ttu-id="81e52-104">0.9.430: ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="81e52-104">0.9.430 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="81e52-105">La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="81e52-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="81e52-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="81e52-106">Summary</span></span>

 <span data-ttu-id="81e52-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="81e52-107">Members</span></span>                        | <span data-ttu-id="81e52-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="81e52-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="81e52-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="81e52-109">Invoke</span></span>](#invoke) | <span data-ttu-id="81e52-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="81e52-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="81e52-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="81e52-111">Members</span></span>

#### <span data-ttu-id="81e52-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="81e52-112">Invoke</span></span> 

<span data-ttu-id="81e52-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="81e52-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="81e52-114">invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="81e52-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>

