---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2429c519858aa9c55e52d47bea64fc182b6beb73
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699368"
---
# <span data-ttu-id="89d6e-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="89d6e-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="89d6e-105">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="89d6e-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="89d6e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="89d6e-106">Summary</span></span>

 <span data-ttu-id="89d6e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="89d6e-107">Members</span></span>                        | <span data-ttu-id="89d6e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="89d6e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89d6e-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="89d6e-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="89d6e-110">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="89d6e-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="89d6e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="89d6e-111">Members</span></span>

#### <span data-ttu-id="89d6e-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="89d6e-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="89d6e-113">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="89d6e-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="89d6e-114">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="89d6e-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

