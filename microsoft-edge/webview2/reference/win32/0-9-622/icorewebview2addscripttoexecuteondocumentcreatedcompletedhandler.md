---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
ms.openlocfilehash: 1580f119a83a171f304b7b05ecbc88edfe31e26d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012740"
---
# <span data-ttu-id="66410-104">interfaz ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="66410-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="66410-105">La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="66410-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="66410-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="66410-106">Summary</span></span>

 <span data-ttu-id="66410-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="66410-107">Members</span></span>                        | <span data-ttu-id="66410-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="66410-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66410-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="66410-109">Invoke</span></span>](#invoke) | <span data-ttu-id="66410-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="66410-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="66410-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="66410-111">Members</span></span>

#### <span data-ttu-id="66410-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="66410-112">Invoke</span></span> 

<span data-ttu-id="66410-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="66410-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="66410-114">invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="66410-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

