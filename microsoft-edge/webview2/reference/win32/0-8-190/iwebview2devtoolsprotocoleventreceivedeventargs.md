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
ms.openlocfilehash: cf321ff1091883827b7ce6cda7248a06f1128867
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655322"
---
# <span data-ttu-id="a0b9c-104">interfaz IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0b9c-104">interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a0b9c-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a0b9c-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a0b9c-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a0b9c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="a0b9c-107">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="a0b9c-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="a0b9c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a0b9c-108">Summary</span></span>

 <span data-ttu-id="a0b9c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0b9c-109">Members</span></span>                        | <span data-ttu-id="a0b9c-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a0b9c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0b9c-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="a0b9c-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="a0b9c-112">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="a0b9c-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="a0b9c-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0b9c-113">Members</span></span>

#### <span data-ttu-id="a0b9c-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="a0b9c-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="a0b9c-115">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="a0b9c-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="a0b9c-116">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="a0b9c-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

