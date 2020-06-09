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
ms.openlocfilehash: a3dde4581692fb30cada16d9166bda62a0d69179
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699353"
---
# <span data-ttu-id="17302-104">interfaz ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="17302-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="17302-105">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="17302-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="17302-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="17302-106">Summary</span></span>

 <span data-ttu-id="17302-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="17302-107">Members</span></span>                        | <span data-ttu-id="17302-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17302-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17302-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="17302-109">Invoke</span></span>](#invoke) | <span data-ttu-id="17302-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17302-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="17302-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="17302-111">Members</span></span>

#### <span data-ttu-id="17302-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="17302-112">Invoke</span></span> 

<span data-ttu-id="17302-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17302-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="17302-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="17302-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

