---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 41fac4533a96e39da261516f91b96fbf00775af3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886426"
---
# <span data-ttu-id="791cb-104">0.9.430: ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="791cb-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="791cb-105">La persona que llama implementa esta interfaz para recibir el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="791cb-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="791cb-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="791cb-106">Summary</span></span>

 <span data-ttu-id="791cb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="791cb-107">Members</span></span>                        | <span data-ttu-id="791cb-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="791cb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="791cb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="791cb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="791cb-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="791cb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="791cb-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="791cb-111">Members</span></span>

#### <span data-ttu-id="791cb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="791cb-112">Invoke</span></span> 

<span data-ttu-id="791cb-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="791cb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="791cb-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2PermissionRequestedEventArgs](ICoreWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="791cb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2PermissionRequestedEventArgs](ICoreWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

