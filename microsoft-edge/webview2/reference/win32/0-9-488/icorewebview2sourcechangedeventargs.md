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
ms.openlocfilehash: 6d4c5e7893f9be78baca25e8976ca889ef9826c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655419"
---
# <span data-ttu-id="810d0-104">interfaz ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="810d0-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="810d0-105">Argumentos de evento para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="810d0-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="810d0-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="810d0-106">Summary</span></span>

 <span data-ttu-id="810d0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="810d0-107">Members</span></span>                        | <span data-ttu-id="810d0-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="810d0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="810d0-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="810d0-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="810d0-110">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="810d0-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="810d0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="810d0-111">Members</span></span>

#### <span data-ttu-id="810d0-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="810d0-112">get_IsNewDocument</span></span> 

<span data-ttu-id="810d0-113">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="810d0-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="810d0-114">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="810d0-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

