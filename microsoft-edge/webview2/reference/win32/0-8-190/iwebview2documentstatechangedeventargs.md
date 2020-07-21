---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 75741c1ba1d835d1c26c7d1db0845071216e0705
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886125"
---
# <span data-ttu-id="45d57-104">0.8.355: IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="45d57-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="45d57-105">Argumentos de evento para el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="45d57-105">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="45d57-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="45d57-106">Summary</span></span>

 <span data-ttu-id="45d57-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="45d57-107">Members</span></span>                        | <span data-ttu-id="45d57-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="45d57-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="45d57-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="45d57-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="45d57-110">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="45d57-110">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="45d57-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="45d57-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="45d57-112">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="45d57-112">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="45d57-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="45d57-113">Members</span></span>

#### <span data-ttu-id="45d57-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="45d57-114">get_IsNewDocument</span></span> 

<span data-ttu-id="45d57-115">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="45d57-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="45d57-116">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="45d57-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="45d57-117">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="45d57-117">get_IsErrorPage</span></span> 

<span data-ttu-id="45d57-118">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="45d57-118">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="45d57-119">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="45d57-119">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

