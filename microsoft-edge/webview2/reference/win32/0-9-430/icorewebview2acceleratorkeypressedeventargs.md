---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 280df2816696ce4abce118976b3eb9abf76267e3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884417"
---
# <span data-ttu-id="3a493-104">0.9.430: ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3a493-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="3a493-105">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="3a493-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="3a493-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="3a493-106">Summary</span></span>

 <span data-ttu-id="3a493-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a493-107">Members</span></span>                        | <span data-ttu-id="3a493-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3a493-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3a493-109">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="3a493-109">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="3a493-110">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="3a493-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="3a493-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="3a493-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="3a493-112">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="3a493-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="3a493-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="3a493-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="3a493-114">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="3a493-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="3a493-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="3a493-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="3a493-116">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3a493-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="3a493-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="3a493-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="3a493-118">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="3a493-118">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="3a493-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="3a493-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="3a493-120">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="3a493-120">Sets the Handled property.</span></span>

## <span data-ttu-id="3a493-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a493-121">Members</span></span>

#### <span data-ttu-id="3a493-122">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="3a493-122">get_KeyEventKind</span></span> 

<span data-ttu-id="3a493-123">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="3a493-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="3a493-124">[get_KeyEventKind](#get_keyeventkind)de HRESULT público (CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="3a493-124">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="3a493-125">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="3a493-125">get_VirtualKey</span></span> 

<span data-ttu-id="3a493-126">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="3a493-126">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="3a493-127">[get_VirtualKey](#get_virtualkey)pública HRESULT (uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="3a493-127">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="3a493-128">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="3a493-128">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="3a493-129">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="3a493-129">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="3a493-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="3a493-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="3a493-131">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="3a493-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="3a493-132">[get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="3a493-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="3a493-133">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="3a493-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="3a493-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="3a493-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="3a493-135">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3a493-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="3a493-136">[get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="3a493-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="3a493-137">get_Handled</span><span class="sxs-lookup"><span data-stu-id="3a493-137">get_Handled</span></span> 

<span data-ttu-id="3a493-138">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="3a493-138">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="3a493-139">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="3a493-139">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="3a493-140">Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="3a493-140">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="3a493-141">De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="3a493-141">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="3a493-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="3a493-142">put_Handled</span></span> 

<span data-ttu-id="3a493-143">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="3a493-143">Sets the Handled property.</span></span>

> <span data-ttu-id="3a493-144">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="3a493-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

