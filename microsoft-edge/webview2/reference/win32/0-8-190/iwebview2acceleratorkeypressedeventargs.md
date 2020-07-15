---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5d052488d23f3d016ba2fd71eb929d5aa2ebea6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877367"
---
# <span data-ttu-id="537d5-104">0.8.355: IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="537d5-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="537d5-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="537d5-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="537d5-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="537d5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="537d5-107">Argumentos de evento para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="537d5-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="537d5-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="537d5-108">Summary</span></span>

 <span data-ttu-id="537d5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="537d5-109">Members</span></span>                        | <span data-ttu-id="537d5-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="537d5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="537d5-111">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="537d5-111">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="537d5-112">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="537d5-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="537d5-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="537d5-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="537d5-114">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="537d5-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="537d5-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="537d5-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="537d5-116">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="537d5-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="537d5-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="537d5-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="537d5-118">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="537d5-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="537d5-119">Indicador</span><span class="sxs-lookup"><span data-stu-id="537d5-119">Handle</span></span>](#handle) | <span data-ttu-id="537d5-120">Al llamar, se permitirá que continúe el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="537d5-120">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="537d5-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="537d5-121">Members</span></span>

#### <span data-ttu-id="537d5-122">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="537d5-122">get_KeyEventType</span></span> 

<span data-ttu-id="537d5-123">El tipo de evento de clave que causó el evento que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="537d5-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="537d5-124">[get_KeyEventType](#get_keyeventtype)de HRESULT público (WEBVIEW2_KEY_EVENT_TYPE \* KeyEventType)</span><span class="sxs-lookup"><span data-stu-id="537d5-124">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="537d5-125">Esta es una de WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN o WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="537d5-125">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="537d5-126">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="537d5-126">get_VirtualKey</span></span> 

<span data-ttu-id="537d5-127">El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.</span><span class="sxs-lookup"><span data-stu-id="537d5-127">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="537d5-128">[get_VirtualKey](#get_virtualkey)pública HRESULT (uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="537d5-128">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="537d5-129">Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A".</span><span class="sxs-lookup"><span data-stu-id="537d5-129">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="537d5-130">Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="537d5-130">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="537d5-131">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="537d5-131">get_KeyEventLParam</span></span> 

<span data-ttu-id="537d5-132">El valor LPARAM que acompañaba al mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="537d5-132">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="537d5-133">[get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="537d5-133">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="537d5-134">Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="537d5-134">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="537d5-135">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="537d5-135">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="537d5-136">Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.</span><span class="sxs-lookup"><span data-stu-id="537d5-136">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="537d5-137">[get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="537d5-137">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="537d5-138">Indicador</span><span class="sxs-lookup"><span data-stu-id="537d5-138">Handle</span></span> 

<span data-ttu-id="537d5-139">Al llamar, se permitirá que continúe el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="537d5-139">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="537d5-140">[identificador](#handle)de HRESULT público (bool Handled)</span><span class="sxs-lookup"><span data-stu-id="537d5-140">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="537d5-141">Si se pasa TRUE, el explorador no podrá realizar la acción predeterminada para esta tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="537d5-141">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="537d5-142">Si el controlador de eventos vuelve sin llamar al [controlador ()](#handle), es equivalente a llamar a handle (false).</span><span class="sxs-lookup"><span data-stu-id="537d5-142">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="537d5-143">Llamar a [HANDLE ()](#handle) después de que ya se ha llamado o el controlador de eventos se ha devuelto no hará nada.</span><span class="sxs-lookup"><span data-stu-id="537d5-143">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

