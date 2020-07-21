---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884865"
---
# <span data-ttu-id="e631e-104">0.9.430: ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="e631e-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="e631e-105">Argumentos de evento para el evento NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="e631e-105">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="e631e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e631e-106">Summary</span></span>

 <span data-ttu-id="e631e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e631e-107">Members</span></span>                        | <span data-ttu-id="e631e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e631e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e631e-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="e631e-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="e631e-110">Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="e631e-110">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="e631e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e631e-111">Members</span></span>

#### <span data-ttu-id="e631e-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="e631e-112">get_NewVersion</span></span> 

<span data-ttu-id="e631e-113">Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="e631e-113">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="e631e-114">[get_NewVersion](#get_newversion)de HRESULT público (LPWStr \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="e631e-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

