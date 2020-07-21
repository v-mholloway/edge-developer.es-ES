---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: e3177f159ff397ee9d4781936aa32f2715d4af02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886090"
---
# <span data-ttu-id="69ffd-104">0.8.355: IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="69ffd-104">0.8.355 - interface IWebView2Environment2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="69ffd-105">Funcionalidad adicional implementada por el objeto de entorno.</span><span class="sxs-lookup"><span data-stu-id="69ffd-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="69ffd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="69ffd-106">Summary</span></span>

 <span data-ttu-id="69ffd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="69ffd-107">Members</span></span>                        | <span data-ttu-id="69ffd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="69ffd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="69ffd-109">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="69ffd-109">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="69ffd-110">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="69ffd-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="69ffd-111">Para obtener más información, consulta la interfaz de [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="69ffd-111">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="69ffd-112">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="69ffd-112">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="69ffd-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="69ffd-113">Members</span></span>

#### <span data-ttu-id="69ffd-114">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="69ffd-114">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="69ffd-115">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="69ffd-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="69ffd-116">[get_BrowserVersionInfo](#get_browserversioninfo)de HRESULT público (LPWStr \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="69ffd-116">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="69ffd-117">Coincide con el formato de la API de GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="69ffd-117">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="69ffd-118">Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.</span><span class="sxs-lookup"><span data-stu-id="69ffd-118">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

