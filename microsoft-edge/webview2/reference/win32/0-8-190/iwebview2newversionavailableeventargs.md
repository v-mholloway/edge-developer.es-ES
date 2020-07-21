---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 4271cc1002de70db2803a5bd6d4be73748bf5bbb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885873"
---
# <span data-ttu-id="8cb7e-104">0.8.355: IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="8cb7e-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="8cb7e-105">Argumentos de evento para el evento NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="8cb7e-105">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="8cb7e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8cb7e-106">Summary</span></span>

 <span data-ttu-id="8cb7e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8cb7e-107">Members</span></span>                        | <span data-ttu-id="8cb7e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8cb7e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8cb7e-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="8cb7e-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="8cb7e-110">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="8cb7e-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="8cb7e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8cb7e-111">Members</span></span>

#### <span data-ttu-id="8cb7e-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="8cb7e-112">get_NewVersion</span></span> 

<span data-ttu-id="8cb7e-113">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.</span><span class="sxs-lookup"><span data-stu-id="8cb7e-113">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="8cb7e-114">[get_NewVersion](#get_newversion)de HRESULT público (LPWStr \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="8cb7e-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

