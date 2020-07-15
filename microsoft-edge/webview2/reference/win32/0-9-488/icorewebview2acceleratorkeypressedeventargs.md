---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1a5330a9217430595acd708d565f38ca88f879f0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880944"
---
# <span data-ttu-id="caff0-104">0.9.515: ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="caff0-104">0.9.515 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="caff0-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="caff0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="caff0-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="caff0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="caff0-107">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="caff0-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="caff0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="caff0-108">Summary</span></span>

 <span data-ttu-id="caff0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="caff0-109">Members</span></span>                        | <span data-ttu-id="caff0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="caff0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="caff0-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="caff0-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="caff0-112">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="caff0-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="caff0-113">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="caff0-113">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="caff0-114">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="caff0-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="caff0-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="caff0-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="caff0-116">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="caff0-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="caff0-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="caff0-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="caff0-118">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="caff0-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="caff0-119">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="caff0-119">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="caff0-120">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="caff0-120">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="caff0-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="caff0-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="caff0-122">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="caff0-122">Sets the Handled property.</span></span>

## <span data-ttu-id="caff0-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="caff0-123">Members</span></span>

#### <span data-ttu-id="caff0-124">get_Handled</span><span class="sxs-lookup"><span data-stu-id="caff0-124">get_Handled</span></span> 

<span data-ttu-id="caff0-125">Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.</span><span class="sxs-lookup"><span data-stu-id="caff0-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="caff0-126">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="caff0-126">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="caff0-127">Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="caff0-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="caff0-128">De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="caff0-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="caff0-129">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="caff0-129">get_KeyEventKind</span></span> 

<span data-ttu-id="caff0-130">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="caff0-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="caff0-131">[get_KeyEventKind](#get_keyeventkind)de HRESULT público (COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="caff0-131">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="caff0-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="caff0-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="caff0-133">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="caff0-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="caff0-134">[get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="caff0-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="caff0-135">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="caff0-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="caff0-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="caff0-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="caff0-137">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="caff0-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="caff0-138">[get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="caff0-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="caff0-139">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="caff0-139">get_VirtualKey</span></span> 

<span data-ttu-id="caff0-140">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="caff0-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="caff0-141">[get_VirtualKey](#get_virtualkey)pública HRESULT (uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="caff0-141">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="caff0-142">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="caff0-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="caff0-143">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="caff0-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="caff0-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="caff0-144">put_Handled</span></span> 

<span data-ttu-id="caff0-145">Establece la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="caff0-145">Sets the Handled property.</span></span>

> <span data-ttu-id="caff0-146">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="caff0-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

