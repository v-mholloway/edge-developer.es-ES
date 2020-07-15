---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 0df2ea043a95c8cca24c0b9bbe3091c490b4ea3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878606"
---
# <span data-ttu-id="5dca0-104">0.8.355: IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5dca0-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="5dca0-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="5dca0-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="5dca0-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="5dca0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="5dca0-107">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="5dca0-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="5dca0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="5dca0-108">Summary</span></span>

 <span data-ttu-id="5dca0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5dca0-109">Members</span></span>                        | <span data-ttu-id="5dca0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5dca0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5dca0-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="5dca0-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="5dca0-112">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="5dca0-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="5dca0-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="5dca0-113">Members</span></span>

#### <span data-ttu-id="5dca0-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="5dca0-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="5dca0-115">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="5dca0-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="5dca0-116">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="5dca0-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

