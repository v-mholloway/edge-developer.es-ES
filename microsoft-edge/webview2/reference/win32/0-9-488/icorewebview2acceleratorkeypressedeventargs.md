---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 10311cf26b66e824447461530f1ce0870ea01ceb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655187"
---
# <span data-ttu-id="9c239-104">interfaz ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9c239-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="9c239-105">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="9c239-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="9c239-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="9c239-106">Summary</span></span>

 <span data-ttu-id="9c239-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c239-107">Members</span></span>                        | <span data-ttu-id="9c239-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9c239-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9c239-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="9c239-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="9c239-110">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="9c239-110">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="9c239-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="9c239-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="9c239-112">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="9c239-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="9c239-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="9c239-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="9c239-114">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="9c239-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="9c239-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="9c239-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="9c239-116">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9c239-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="9c239-117">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="9c239-117">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="9c239-118">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="9c239-118">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="9c239-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="9c239-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="9c239-120">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="9c239-120">Sets the Handled property.</span></span>

## <span data-ttu-id="9c239-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c239-121">Members</span></span>

#### <span data-ttu-id="9c239-122">get_Handled</span><span class="sxs-lookup"><span data-stu-id="9c239-122">get_Handled</span></span> 

<span data-ttu-id="9c239-123">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="9c239-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="9c239-124">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="9c239-124">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="9c239-125">Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="9c239-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="9c239-126">De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="9c239-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="9c239-127">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="9c239-127">get_KeyEventKind</span></span> 

<span data-ttu-id="9c239-128">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="9c239-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="9c239-129">[get_KeyEventKind](#get_keyeventkind)de HRESULT público (COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="9c239-129">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="9c239-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="9c239-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="9c239-131">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="9c239-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="9c239-132">[get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="9c239-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="9c239-133">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="9c239-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="9c239-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="9c239-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="9c239-135">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9c239-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="9c239-136">[get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="9c239-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="9c239-137">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="9c239-137">get_VirtualKey</span></span> 

<span data-ttu-id="9c239-138">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="9c239-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="9c239-139">[get_VirtualKey](#get_virtualkey)pública HRESULT (uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="9c239-139">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="9c239-140">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="9c239-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="9c239-141">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="9c239-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="9c239-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="9c239-142">put_Handled</span></span> 

<span data-ttu-id="9c239-143">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="9c239-143">Sets the Handled property.</span></span>

> <span data-ttu-id="9c239-144">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="9c239-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

