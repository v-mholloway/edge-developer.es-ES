---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: d127af61bfdc9bf692fa48489d7982bf2c6cad86
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878550"
---
# <span data-ttu-id="2bcab-104">0.8.355: IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="2bcab-104">0.8.355 - interface IWebView2Environment2</span></span> 

> [!NOTE]
> <span data-ttu-id="2bcab-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="2bcab-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2bcab-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2bcab-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="2bcab-107">Funcionalidad adicional implementada por el objeto de entorno.</span><span class="sxs-lookup"><span data-stu-id="2bcab-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="2bcab-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2bcab-108">Summary</span></span>

 <span data-ttu-id="2bcab-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2bcab-109">Members</span></span>                        | <span data-ttu-id="2bcab-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2bcab-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2bcab-111">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2bcab-111">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="2bcab-112">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="2bcab-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="2bcab-113">Para obtener más información, consulta la interfaz de [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="2bcab-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="2bcab-114">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="2bcab-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="2bcab-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="2bcab-115">Members</span></span>

#### <span data-ttu-id="2bcab-116">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2bcab-116">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="2bcab-117">Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="2bcab-117">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="2bcab-118">[get_BrowserVersionInfo](#get_browserversioninfo)de HRESULT público (LPWStr \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="2bcab-118">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="2bcab-119">Coincide con el formato de la API de GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="2bcab-119">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="2bcab-120">Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.</span><span class="sxs-lookup"><span data-stu-id="2bcab-120">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

