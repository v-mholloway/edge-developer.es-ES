---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
ms.openlocfilehash: 9321f7912cb1217a3b6a28f322469ea12e5820dc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010631"
---
# <span data-ttu-id="61b8a-104">0.9.579: ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="61b8a-104">0.9.579 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="61b8a-105">La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="61b8a-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="61b8a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="61b8a-106">Summary</span></span>

 <span data-ttu-id="61b8a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="61b8a-107">Members</span></span>                        | <span data-ttu-id="61b8a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="61b8a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61b8a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="61b8a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="61b8a-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="61b8a-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="61b8a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="61b8a-111">Members</span></span>

#### <span data-ttu-id="61b8a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="61b8a-112">Invoke</span></span> 

<span data-ttu-id="61b8a-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="61b8a-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="61b8a-114">invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="61b8a-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

