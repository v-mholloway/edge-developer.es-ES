---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 885ad6b161fbde6721e1812735ab50d7e0c3e8d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885055"
---
# <span data-ttu-id="4cf52-104">0.8.355: IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4cf52-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="4cf52-105">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="4cf52-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="4cf52-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="4cf52-106">Summary</span></span>

 <span data-ttu-id="4cf52-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4cf52-107">Members</span></span>                        | <span data-ttu-id="4cf52-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4cf52-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4cf52-109">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="4cf52-109">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="4cf52-110">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="4cf52-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="4cf52-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="4cf52-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="4cf52-112">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="4cf52-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="4cf52-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="4cf52-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="4cf52-114">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="4cf52-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="4cf52-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="4cf52-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="4cf52-116">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="4cf52-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="4cf52-117">Indicador</span><span class="sxs-lookup"><span data-stu-id="4cf52-117">Handle</span></span>](#handle) | <span data-ttu-id="4cf52-118">Al llamar, se permitirá que continúe el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="4cf52-118">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="4cf52-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="4cf52-119">Members</span></span>

#### <span data-ttu-id="4cf52-120">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="4cf52-120">get_KeyEventType</span></span> 

<span data-ttu-id="4cf52-121">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="4cf52-121">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="4cf52-122">[get_KeyEventType](#get_keyeventtype)de HRESULT público (WEBVIEW2_KEY_EVENT_TYPE \* KeyEventType)</span><span class="sxs-lookup"><span data-stu-id="4cf52-122">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="4cf52-123">Esta es una de WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN o WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="4cf52-123">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="4cf52-124">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="4cf52-124">get_VirtualKey</span></span> 

<span data-ttu-id="4cf52-125">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="4cf52-125">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="4cf52-126">[get_VirtualKey](#get_virtualkey)pública HRESULT (uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="4cf52-126">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="4cf52-127">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="4cf52-127">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="4cf52-128">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="4cf52-128">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="4cf52-129">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="4cf52-129">get_KeyEventLParam</span></span> 

<span data-ttu-id="4cf52-130">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="4cf52-130">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="4cf52-131">[get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="4cf52-131">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="4cf52-132">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="4cf52-132">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="4cf52-133">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="4cf52-133">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="4cf52-134">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="4cf52-134">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="4cf52-135">[get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="4cf52-135">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="4cf52-136">Indicador</span><span class="sxs-lookup"><span data-stu-id="4cf52-136">Handle</span></span> 

<span data-ttu-id="4cf52-137">Al llamar, se permitirá que continúe el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="4cf52-137">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="4cf52-138">[identificador](#handle)de HRESULT público (bool Handled)</span><span class="sxs-lookup"><span data-stu-id="4cf52-138">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="4cf52-139">Si se pasa TRUE, el explorador no podrá realizar la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="4cf52-139">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="4cf52-140">Si el controlador de eventos vuelve sin llamar al [controlador ()](#handle), es equivalente a llamar a handle (false).</span><span class="sxs-lookup"><span data-stu-id="4cf52-140">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="4cf52-141">Llamar a [HANDLE ()](#handle) después de que ya se ha llamado o el controlador de eventos se ha devuelto no hará nada.</span><span class="sxs-lookup"><span data-stu-id="4cf52-141">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

