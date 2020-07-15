---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ecf68bfc338d06fdd2d1a104126685ca105810b0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879383"
---
# <span data-ttu-id="35640-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="35640-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="35640-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="35640-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="35640-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="35640-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="35640-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="35640-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="35640-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="35640-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="35640-109">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="35640-109">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="35640-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="35640-110">Summary</span></span>

 <span data-ttu-id="35640-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="35640-111">Members</span></span>                        | <span data-ttu-id="35640-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="35640-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35640-113">Handled</span><span class="sxs-lookup"><span data-stu-id="35640-113">Handled</span></span>](#handled) | <span data-ttu-id="35640-114">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="35640-114">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="35640-115">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="35640-115">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="35640-116">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="35640-116">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="35640-117">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="35640-117">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="35640-118">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="35640-118">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="35640-119">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="35640-119">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="35640-120">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="35640-120">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="35640-121">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="35640-121">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="35640-122">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="35640-122">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="35640-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="35640-123">Members</span></span>

#### <span data-ttu-id="35640-124">Handled</span><span class="sxs-lookup"><span data-stu-id="35640-124">Handled</span></span> 

<span data-ttu-id="35640-125">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="35640-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="35640-126">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="35640-126">public bool [Handled](#handled)</span></span>

<span data-ttu-id="35640-127">Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="35640-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="35640-128">De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="35640-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="35640-129">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="35640-129">KeyEventKind</span></span> 

<span data-ttu-id="35640-130">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="35640-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="35640-131">[CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) pública [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="35640-131">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="35640-132">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="35640-132">KeyEventLParam</span></span> 

<span data-ttu-id="35640-133">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="35640-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="35640-134">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="35640-134">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="35640-135">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="35640-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="35640-136">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="35640-136">PhysicalKeyStatus</span></span> 

<span data-ttu-id="35640-137">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="35640-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="35640-138">[CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) pública [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="35640-138">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="35640-139">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="35640-139">VirtualKey</span></span> 

<span data-ttu-id="35640-140">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="35640-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="35640-141">uint pública [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="35640-141">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="35640-142">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="35640-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="35640-143">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="35640-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

