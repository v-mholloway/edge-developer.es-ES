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
ms.openlocfilehash: 0555c9f8bb145b75dcbcf042642d9d9102f573cb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699390"
---
# <span data-ttu-id="6fd05-104">interfaz ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6fd05-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="6fd05-105">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="6fd05-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="6fd05-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6fd05-106">Summary</span></span>

 <span data-ttu-id="6fd05-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6fd05-107">Members</span></span>                        | <span data-ttu-id="6fd05-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6fd05-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6fd05-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6fd05-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="6fd05-110">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="6fd05-110">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="6fd05-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="6fd05-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="6fd05-112">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="6fd05-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="6fd05-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6fd05-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="6fd05-114">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="6fd05-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="6fd05-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6fd05-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="6fd05-116">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6fd05-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="6fd05-117">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6fd05-117">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="6fd05-118">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="6fd05-118">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="6fd05-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6fd05-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="6fd05-120">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="6fd05-120">Sets the Handled property.</span></span>

## <span data-ttu-id="6fd05-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="6fd05-121">Members</span></span>

#### <span data-ttu-id="6fd05-122">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6fd05-122">get_Handled</span></span> 

<span data-ttu-id="6fd05-123">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="6fd05-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="6fd05-124">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="6fd05-124">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="6fd05-125">Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="6fd05-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="6fd05-126">De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="6fd05-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="6fd05-127">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="6fd05-127">get_KeyEventKind</span></span> 

<span data-ttu-id="6fd05-128">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="6fd05-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="6fd05-129">[get_KeyEventKind](#get_keyeventkind)de HRESULT público (COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="6fd05-129">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="6fd05-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6fd05-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="6fd05-131">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="6fd05-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="6fd05-132">[get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="6fd05-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="6fd05-133">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="6fd05-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="6fd05-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6fd05-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="6fd05-135">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6fd05-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="6fd05-136">[get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="6fd05-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="6fd05-137">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6fd05-137">get_VirtualKey</span></span> 

<span data-ttu-id="6fd05-138">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="6fd05-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="6fd05-139">[get_VirtualKey](#get_virtualkey)pública HRESULT (uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="6fd05-139">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="6fd05-140">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="6fd05-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="6fd05-141">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="6fd05-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="6fd05-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6fd05-142">put_Handled</span></span> 

<span data-ttu-id="6fd05-143">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="6fd05-143">Sets the Handled property.</span></span>

> <span data-ttu-id="6fd05-144">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="6fd05-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

