---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: 079b7840689fbeb2931a22f72ad78c1ce0f590b8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012763"
---
# <span data-ttu-id="6c0bd-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6c0bd-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="6c0bd-105">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="6c0bd-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="6c0bd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6c0bd-106">Summary</span></span>

 <span data-ttu-id="6c0bd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c0bd-107">Members</span></span>                        | <span data-ttu-id="6c0bd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6c0bd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c0bd-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="6c0bd-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="6c0bd-110">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="6c0bd-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="6c0bd-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c0bd-111">Members</span></span>

#### <span data-ttu-id="6c0bd-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="6c0bd-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="6c0bd-113">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="6c0bd-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="6c0bd-114">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="6c0bd-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

