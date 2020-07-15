---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878347"
---
# <span data-ttu-id="7a9ec-104">0.8.355: IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="7a9ec-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7a9ec-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="7a9ec-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="7a9ec-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="7a9ec-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="7a9ec-107">Argumentos de evento para el evento NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="7a9ec-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="7a9ec-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7a9ec-108">Summary</span></span>

 <span data-ttu-id="7a9ec-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a9ec-109">Members</span></span>                        | <span data-ttu-id="7a9ec-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7a9ec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a9ec-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="7a9ec-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="7a9ec-112">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="7a9ec-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="7a9ec-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a9ec-113">Members</span></span>

#### <span data-ttu-id="7a9ec-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="7a9ec-114">get_NewVersion</span></span> 

<span data-ttu-id="7a9ec-115">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="7a9ec-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="7a9ec-116">[get_NewVersion](#get_newversion)de HRESULT público (LPWStr \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="7a9ec-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

