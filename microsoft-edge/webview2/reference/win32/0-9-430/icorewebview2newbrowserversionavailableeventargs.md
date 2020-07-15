---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877857"
---
# <span data-ttu-id="4e48b-104">0.9.430: ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="4e48b-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4e48b-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4e48b-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4e48b-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="4e48b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="4e48b-107">Argumentos de evento para el evento NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="4e48b-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="4e48b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="4e48b-108">Summary</span></span>

 <span data-ttu-id="4e48b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e48b-109">Members</span></span>                        | <span data-ttu-id="4e48b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4e48b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4e48b-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="4e48b-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="4e48b-112">Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="4e48b-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="4e48b-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e48b-113">Members</span></span>

#### <span data-ttu-id="4e48b-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="4e48b-114">get_NewVersion</span></span> 

<span data-ttu-id="4e48b-115">Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="4e48b-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="4e48b-116">[get_NewVersion](#get_newversion)de HRESULT público (LPWStr \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="4e48b-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

