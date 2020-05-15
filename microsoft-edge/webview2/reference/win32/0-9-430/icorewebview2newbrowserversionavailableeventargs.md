---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 3ac37f7d90fc03214381b991c8becae602bac738
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655311"
---
# <span data-ttu-id="574c6-104">interfaz ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="574c6-104">interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="574c6-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="574c6-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="574c6-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="574c6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="574c6-107">Argumentos de evento para el evento NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="574c6-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="574c6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="574c6-108">Summary</span></span>

 <span data-ttu-id="574c6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="574c6-109">Members</span></span>                        | <span data-ttu-id="574c6-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="574c6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="574c6-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="574c6-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="574c6-112">Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="574c6-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="574c6-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="574c6-113">Members</span></span>

#### <span data-ttu-id="574c6-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="574c6-114">get_NewVersion</span></span> 

<span data-ttu-id="574c6-115">Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="574c6-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="574c6-116">[get_NewVersion](#get_newversion)de HRESULT público (LPWStr \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="574c6-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

