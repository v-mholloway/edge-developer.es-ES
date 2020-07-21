---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2ed75f2a12387b6b8de628ac27ef536cf43fb8b1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885411"
---
# <span data-ttu-id="7436c-104">0.9.515: ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7436c-104">0.9.515 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="7436c-105">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7436c-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="7436c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7436c-106">Summary</span></span>

 <span data-ttu-id="7436c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7436c-107">Members</span></span>                        | <span data-ttu-id="7436c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7436c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7436c-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7436c-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="7436c-110">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="7436c-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="7436c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7436c-111">Members</span></span>

#### <span data-ttu-id="7436c-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7436c-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="7436c-113">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="7436c-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="7436c-114">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="7436c-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

