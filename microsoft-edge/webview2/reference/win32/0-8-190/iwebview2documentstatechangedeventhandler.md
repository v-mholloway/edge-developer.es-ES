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
ms.openlocfilehash: 062d6d3201acc71e58ab4cedd85f697f560bb7c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655315"
---
# <span data-ttu-id="580ef-104">interfaz IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="580ef-104">interface IWebView2DocumentStateChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="580ef-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="580ef-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="580ef-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="580ef-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="580ef-107">La persona que llama implementa esta interfaz para recibir el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="580ef-107">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="580ef-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="580ef-108">Summary</span></span>

 <span data-ttu-id="580ef-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="580ef-109">Members</span></span>                        | <span data-ttu-id="580ef-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="580ef-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="580ef-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="580ef-111">Invoke</span></span>](#invoke) | <span data-ttu-id="580ef-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="580ef-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="580ef-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="580ef-113">Members</span></span>

#### <span data-ttu-id="580ef-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="580ef-114">Invoke</span></span> 

<span data-ttu-id="580ef-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="580ef-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="580ef-116">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="580ef-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>

