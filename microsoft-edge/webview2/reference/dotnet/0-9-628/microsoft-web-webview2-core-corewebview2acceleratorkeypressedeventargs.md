---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: 16af4247c494d1d09155110755d7936487f2e84e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012684"
---
# <span data-ttu-id="6f263-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6f263-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

<span data-ttu-id="6f263-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6f263-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6f263-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6f263-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6f263-107">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="6f263-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="6f263-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6f263-108">Summary</span></span>

 <span data-ttu-id="6f263-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f263-109">Members</span></span>                        | <span data-ttu-id="6f263-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6f263-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6f263-111">Handled</span><span class="sxs-lookup"><span data-stu-id="6f263-111">Handled</span></span>](#handled) | <span data-ttu-id="6f263-112">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="6f263-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="6f263-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="6f263-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="6f263-114">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="6f263-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="6f263-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6f263-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="6f263-116">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="6f263-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="6f263-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6f263-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="6f263-118">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6f263-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="6f263-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6f263-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="6f263-120">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="6f263-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="6f263-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f263-121">Members</span></span>

#### <span data-ttu-id="6f263-122">Handled</span><span class="sxs-lookup"><span data-stu-id="6f263-122">Handled</span></span> 

<span data-ttu-id="6f263-123">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="6f263-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="6f263-124">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="6f263-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="6f263-125">Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="6f263-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="6f263-126">De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="6f263-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="6f263-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="6f263-127">KeyEventKind</span></span> 

<span data-ttu-id="6f263-128">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="6f263-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="6f263-129">[CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) pública [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="6f263-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="6f263-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6f263-130">KeyEventLParam</span></span> 

<span data-ttu-id="6f263-131">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="6f263-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="6f263-132">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="6f263-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="6f263-133">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="6f263-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="6f263-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6f263-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="6f263-135">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6f263-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="6f263-136">[CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) pública [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="6f263-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="6f263-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6f263-137">VirtualKey</span></span> 

<span data-ttu-id="6f263-138">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="6f263-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="6f263-139">uint pública [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="6f263-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="6f263-140">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="6f263-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="6f263-141">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="6f263-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

