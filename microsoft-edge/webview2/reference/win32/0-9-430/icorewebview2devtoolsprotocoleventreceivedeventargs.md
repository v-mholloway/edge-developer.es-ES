---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c42e353c80335b6dccdad49b470e68fa5ae2f559
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884256"
---
# <span data-ttu-id="da325-104">0.9.430: ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="da325-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="da325-105">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="da325-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="da325-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="da325-106">Summary</span></span>

 <span data-ttu-id="da325-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="da325-107">Members</span></span>                        | <span data-ttu-id="da325-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="da325-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="da325-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="da325-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="da325-110">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="da325-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="da325-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="da325-111">Members</span></span>

#### <span data-ttu-id="da325-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="da325-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="da325-113">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="da325-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="da325-114">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="da325-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

