---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655410"
---
# <span data-ttu-id="ddc7a-104">interfaz IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="ddc7a-104">interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="ddc7a-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="ddc7a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ddc7a-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="ddc7a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="ddc7a-107">Argumentos de evento para el evento NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="ddc7a-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="ddc7a-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="ddc7a-108">Summary</span></span>

 <span data-ttu-id="ddc7a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ddc7a-109">Members</span></span>                        | <span data-ttu-id="ddc7a-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ddc7a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ddc7a-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="ddc7a-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="ddc7a-112">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="ddc7a-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="ddc7a-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="ddc7a-113">Members</span></span>

#### <span data-ttu-id="ddc7a-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="ddc7a-114">get_NewVersion</span></span> 

<span data-ttu-id="ddc7a-115">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="ddc7a-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="ddc7a-116">[get_NewVersion](#get_newversion)de HRESULT público (LPWStr \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="ddc7a-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

