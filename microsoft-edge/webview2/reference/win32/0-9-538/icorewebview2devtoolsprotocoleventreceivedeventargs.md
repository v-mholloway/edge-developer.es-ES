---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: de10adbfe7e74a1679aa8b77cb96775561d87a17
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880132"
---
# <span data-ttu-id="64369-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="64369-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="64369-105">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="64369-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="64369-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="64369-106">Summary</span></span>

 <span data-ttu-id="64369-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="64369-107">Members</span></span>                        | <span data-ttu-id="64369-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="64369-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64369-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="64369-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="64369-110">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="64369-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="64369-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="64369-111">Members</span></span>

#### <span data-ttu-id="64369-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="64369-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="64369-113">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="64369-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="64369-114">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="64369-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

