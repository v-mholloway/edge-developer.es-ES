---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 3a9af31477e7b4155bece55ec2faef85efccbd0d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884984"
---
# <span data-ttu-id="e3795-104">0.8.355: IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="e3795-104">0.8.355 - interface IWebView2NewVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="e3795-105">La persona que llama implementa esta interfaz para recibir eventos NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="e3795-105">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="e3795-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e3795-106">Summary</span></span>

 <span data-ttu-id="e3795-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3795-107">Members</span></span>                        | <span data-ttu-id="e3795-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e3795-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e3795-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e3795-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e3795-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e3795-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e3795-111">Use el método get_NewVersion de [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) para obtener el nuevo número de versión.</span><span class="sxs-lookup"><span data-stu-id="e3795-111">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="e3795-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3795-112">Members</span></span>

#### <span data-ttu-id="e3795-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e3795-113">Invoke</span></span> 

<span data-ttu-id="e3795-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e3795-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e3795-115">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e3795-115">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

