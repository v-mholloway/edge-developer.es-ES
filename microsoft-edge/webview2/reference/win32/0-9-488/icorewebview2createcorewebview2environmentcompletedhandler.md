---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: da49c1762ad7b7f3f366754bb9b05b7d16b861b7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655347"
---
# <span data-ttu-id="d2c41-104">interfaz ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="d2c41-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="d2c41-105">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="d2c41-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="d2c41-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="d2c41-106">Summary</span></span>

 <span data-ttu-id="d2c41-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2c41-107">Members</span></span>                        | <span data-ttu-id="d2c41-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d2c41-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2c41-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d2c41-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d2c41-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d2c41-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="d2c41-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2c41-111">Members</span></span>

#### <span data-ttu-id="d2c41-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d2c41-112">Invoke</span></span> 

<span data-ttu-id="d2c41-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d2c41-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="d2c41-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="d2c41-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

