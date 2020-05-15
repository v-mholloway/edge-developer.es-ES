---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e7fbc952a44bdd38e6e59c46adafb8e71b7904b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655345"
---
# <span data-ttu-id="86f6c-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="86f6c-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="86f6c-105">Argumentos de evento para el evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="86f6c-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="86f6c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="86f6c-106">Summary</span></span>

 <span data-ttu-id="86f6c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="86f6c-107">Members</span></span>                        | <span data-ttu-id="86f6c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="86f6c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86f6c-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="86f6c-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="86f6c-110">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="86f6c-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="86f6c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="86f6c-111">Members</span></span>

#### <span data-ttu-id="86f6c-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="86f6c-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="86f6c-113">El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="86f6c-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="86f6c-114">[get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="86f6c-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

