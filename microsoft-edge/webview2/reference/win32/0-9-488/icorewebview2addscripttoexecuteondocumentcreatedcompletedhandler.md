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
ms.openlocfilehash: e9f98b43463fe5259d2f9f723b62b78c1d1a4758
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655370"
---
# <span data-ttu-id="897a5-104">interfaz ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="897a5-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="897a5-105">La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="897a5-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="897a5-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="897a5-106">Summary</span></span>

 <span data-ttu-id="897a5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="897a5-107">Members</span></span>                        | <span data-ttu-id="897a5-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="897a5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="897a5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="897a5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="897a5-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="897a5-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="897a5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="897a5-111">Members</span></span>

#### <span data-ttu-id="897a5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="897a5-112">Invoke</span></span> 

<span data-ttu-id="897a5-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="897a5-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="897a5-114">invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="897a5-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

