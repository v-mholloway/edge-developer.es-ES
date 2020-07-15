---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Controller
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8e0f95f8346f4c4b60b6de2676503b79c743afcb
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880825"
---
# <span data-ttu-id="79d05-104">0.9.515: ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="79d05-104">0.9.515 - interface ICoreWebView2Controller</span></span> 

> [!NOTE]
> <span data-ttu-id="79d05-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="79d05-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="79d05-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="79d05-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Controller
  : public IUnknown
```

<span data-ttu-id="79d05-107">Esta interfaz es el propietario del objeto CoreWebView2 y proporciona compatibilidad para cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.</span><span class="sxs-lookup"><span data-stu-id="79d05-107">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="79d05-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="79d05-108">Summary</span></span>

 <span data-ttu-id="79d05-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="79d05-109">Members</span></span>                        | <span data-ttu-id="79d05-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="79d05-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="79d05-111">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="79d05-111">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="79d05-112">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="79d05-112">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="79d05-113">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-113">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="79d05-114">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-114">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="79d05-115">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-115">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="79d05-116">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-116">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="79d05-117">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="79d05-117">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="79d05-118">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="79d05-118">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="79d05-119">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="79d05-119">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="79d05-120">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="79d05-120">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="79d05-121">Cerrar</span><span class="sxs-lookup"><span data-stu-id="79d05-121">Close</span></span>](#close) | <span data-ttu-id="79d05-122">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="79d05-122">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="79d05-123">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="79d05-123">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="79d05-124">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="79d05-124">The webview bounds.</span></span>
[<span data-ttu-id="79d05-125">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="79d05-125">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="79d05-126">Obtiene el CoreWebView2 asociado a este CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="79d05-126">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>
[<span data-ttu-id="79d05-127">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="79d05-127">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="79d05-128">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-128">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="79d05-129">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="79d05-129">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="79d05-130">La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.</span><span class="sxs-lookup"><span data-stu-id="79d05-130">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="79d05-131">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="79d05-131">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="79d05-132">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-132">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="79d05-133">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-133">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="79d05-134">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-134">Move focus into WebView.</span></span>
[<span data-ttu-id="79d05-135">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="79d05-135">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="79d05-136">Esta es una notificación independiente de los límites que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).</span><span class="sxs-lookup"><span data-stu-id="79d05-136">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="79d05-137">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="79d05-137">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="79d05-138">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="79d05-138">Set the Bounds property.</span></span>
[<span data-ttu-id="79d05-139">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="79d05-139">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="79d05-140">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="79d05-140">Set the IsVisible property.</span></span>
[<span data-ttu-id="79d05-141">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="79d05-141">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="79d05-142">Establezca la ventana principal de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-142">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="79d05-143">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="79d05-143">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="79d05-144">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="79d05-144">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="79d05-145">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="79d05-145">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="79d05-146">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="79d05-146">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="79d05-147">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-147">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="79d05-148">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-148">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="79d05-149">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-149">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="79d05-150">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-150">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="79d05-151">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="79d05-151">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="79d05-152">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="79d05-152">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="79d05-153">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="79d05-153">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="79d05-154">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="79d05-154">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="79d05-155">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="79d05-155">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="79d05-156">Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="79d05-156">Update Bounds and ZoomFactor properties at the same time.</span></span>

<span data-ttu-id="79d05-157">El CoreWebView2Controller es propietario de la CoreWebView2 y, si todas las referencias a CoreWebView2Controller desaparecen, se cerrará la WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-157">The CoreWebView2Controller owns the CoreWebView2, and if all references to the CoreWebView2Controller go away, the WebView will be closed.</span></span>

## <span data-ttu-id="79d05-158">Miembros</span><span class="sxs-lookup"><span data-stu-id="79d05-158">Members</span></span>

#### <span data-ttu-id="79d05-159">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="79d05-159">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="79d05-160">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="79d05-160">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="79d05-161">[add_AcceleratorKeyPressed](#add_acceleratorkeypressed)de HRESULT público ([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="79d05-161">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="79d05-162">AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa.</span><span class="sxs-lookup"><span data-stu-id="79d05-162">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="79d05-163">Una clave se considera un acelerador si:</span><span class="sxs-lookup"><span data-stu-id="79d05-163">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="79d05-164">La tecla Ctrl o Alt se está retenida actualmente, o bien</span><span class="sxs-lookup"><span data-stu-id="79d05-164">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="79d05-165">la tecla presionada no se asigna a un carácter.</span><span class="sxs-lookup"><span data-stu-id="79d05-165">the pressed key does not map to a character.</span></span> <span data-ttu-id="79d05-166">Algunas teclas específicas nunca se consideran aceleradores, como Mayús.</span><span class="sxs-lookup"><span data-stu-id="79d05-166">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="79d05-167">La tecla de escape se considera siempre un acelerador.</span><span class="sxs-lookup"><span data-stu-id="79d05-167">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="79d05-168">Los eventos de teclas autorepetidos que se provocan al mantener presionada la tecla también desencadenan este evento.</span><span class="sxs-lookup"><span data-stu-id="79d05-168">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="79d05-169">Puedes filtrarlos comprobando los argumentos del evento ' KeyEventLParam o PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="79d05-169">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="79d05-170">En el modo de ventana, se llama a este controlador de eventos de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="79d05-170">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="79d05-171">Hasta que llames al controlador () en los argumentos del evento o se devuelva el controlador de eventos, el proceso del explorador se bloqueará y las llamadas COM salientes entre procesos generarán un error con RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="79d05-171">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="79d05-172">Sin embargo, todos los métodos de la API de CoreWebView2 funcionarán.</span><span class="sxs-lookup"><span data-stu-id="79d05-172">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="79d05-173">En el modo sin ventana, se llama al controlador de eventos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="79d05-173">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="79d05-174">La entrada de datos adicionales no llegará al explorador hasta que el controlador de eventos devuelva o se llame a (), pero el proceso del explorador en sí no se bloqueará y las llamadas COM salientes funcionarán normalmente.</span><span class="sxs-lookup"><span data-stu-id="79d05-174">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="79d05-175">Se recomienda que llame al controlador (TRUE) tan pronto como sepa que desea controlar la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="79d05-175">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="79d05-176">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-176">add_GotFocus</span></span> 

<span data-ttu-id="79d05-177">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-177">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="79d05-178">[add_GotFocus](#add_gotfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="79d05-178">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="79d05-179">GotFocus se desencadena cuando WebView tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="79d05-179">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="79d05-180">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-180">add_LostFocus</span></span> 

<span data-ttu-id="79d05-181">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-181">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="79d05-182">[add_LostFocus](#add_lostfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="79d05-182">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="79d05-183">LostFocus se desencadena cuando WebView pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="79d05-183">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="79d05-184">En caso de que se inicie el evento MoveFocusRequested, el foco seguirá en la vista previa cuando se desencadene el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="79d05-184">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="79d05-185">Perder el foco solo se activa cuando el código de la aplicación o la acción predeterminada del evento MoveFocusRequested está lejos de WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-185">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="79d05-186">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="79d05-186">add_MoveFocusRequested</span></span> 

<span data-ttu-id="79d05-187">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="79d05-187">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="79d05-188">[add_MoveFocusRequested](#add_movefocusrequested)de HRESULT público ([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="79d05-188">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="79d05-189">MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista.</span><span class="sxs-lookup"><span data-stu-id="79d05-189">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="79d05-190">El foco de la vista de WebView no ha cambiado cuando se desencadena este evento.</span><span class="sxs-lookup"><span data-stu-id="79d05-190">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="79d05-191">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="79d05-191">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="79d05-192">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="79d05-192">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="79d05-193">[add_ZoomFactorChanged](#add_zoomfactorchanged)de HRESULT público ([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="79d05-193">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="79d05-194">El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="79d05-194">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="79d05-195">El evento se podría activar porque el autor de la llamada modificó la propiedad ZoomFactor o debido a que el usuario modificaba manualmente el zoom.</span><span class="sxs-lookup"><span data-stu-id="79d05-195">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="79d05-196">Cuando el autor de la llamada lo modifica a través de la propiedad ZoomFactor, el factor de zoom interno se actualiza inmediatamente y no se producirá ningún evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="79d05-196">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="79d05-197">La vista Web asocia el último factor de zoom usado para cada sitio.</span><span class="sxs-lookup"><span data-stu-id="79d05-197">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="79d05-198">Por lo tanto, es posible que el factor de zoom cambie al navegar a una página diferente.</span><span class="sxs-lookup"><span data-stu-id="79d05-198">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="79d05-199">Cuando el factor de zoom cambia debido a esto, el evento ZoomFactorChanged se activa justo después del evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="79d05-199">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="79d05-200">Cerrar</span><span class="sxs-lookup"><span data-stu-id="79d05-200">Close</span></span> 

<span data-ttu-id="79d05-201">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="79d05-201">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="79d05-202">HRESULT público [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="79d05-202">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="79d05-203">La limpieza de la instancia del explorador liberará los recursos que se encienden en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="79d05-203">Cleaning up the browser instance will release the resources powering the WebView.</span></span> <span data-ttu-id="79d05-204">La instancia del explorador se cerrará si no hay ninguna otra vista previa con ella.</span><span class="sxs-lookup"><span data-stu-id="79d05-204">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="79d05-205">Después de llamar a Close, todas las llamadas a métodos producirán errores y los controladores de eventos dejarán de activarse.</span><span class="sxs-lookup"><span data-stu-id="79d05-205">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="79d05-206">Específicamente, la WebView liberará sus referencias a los controladores de eventos cuando se llama a Close.</span><span class="sxs-lookup"><span data-stu-id="79d05-206">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="79d05-207">Close se llama de forma implícita cuando CoreWebView2Controller pierde su referencia final y se destruye.</span><span class="sxs-lookup"><span data-stu-id="79d05-207">Close is implicitly called when the CoreWebView2Controller loses its final reference and is destructed.</span></span> <span data-ttu-id="79d05-208">Sin embargo, se recomienda llamar de forma explícita a Close para evitar cualquier ciclo de referencias entre la vista de WebView y el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79d05-208">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="79d05-209">En concreto, si capturas una referencia a la vista de la vista en un controlador de eventos, crearás un ciclo de referencia entre la vista en WebView y el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="79d05-209">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="79d05-210">Al llamar a Close se interrumpirá este ciclo liberando todos los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="79d05-210">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="79d05-211">Pero para evitar esta situación, lo mejor es llamar explícitamente a Close en WebView y no capturar una referencia a WebView para asegurarte de que la WebView pueda limpiarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="79d05-211">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="79d05-212">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="79d05-212">get_Bounds</span></span> 

<span data-ttu-id="79d05-213">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="79d05-213">The webview bounds.</span></span>

> <span data-ttu-id="79d05-214">[get_Boundss](#get_bounds)HRESULT públicos (límites Rect \*)</span><span class="sxs-lookup"><span data-stu-id="79d05-214">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="79d05-215">Los límites son relativos al identificador HWND primario.</span><span class="sxs-lookup"><span data-stu-id="79d05-215">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="79d05-216">La aplicación tiene dos formas en las que puede ubicar una vista en WebView:</span><span class="sxs-lookup"><span data-stu-id="79d05-216">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="79d05-217">Cree un HWND secundario que sea el objeto HWND de la vista < View.</span><span class="sxs-lookup"><span data-stu-id="79d05-217">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="79d05-218">Coloque esta ventana donde debería estar la vista en la vista.</span><span class="sxs-lookup"><span data-stu-id="79d05-218">Position this window where the WebView should be.</span></span> <span data-ttu-id="79d05-219">En este caso, use (0,0) para la Bound's esquina superior izquierda de la vista de vista previa (el desplazamiento).</span><span class="sxs-lookup"><span data-stu-id="79d05-219">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="79d05-220">Use la última ventana de la aplicación como el HWND primario de WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-220">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="79d05-221">Establezca la Bound's esquina superior izquierda de la vista previa para que la vista de la vista en la aplicación se coloque correctamente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79d05-221">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="79d05-222">Los valores de la entrada enlazada están en el espacio de coordenadas del host.</span><span class="sxs-lookup"><span data-stu-id="79d05-222">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="79d05-223">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="79d05-223">get_CoreWebView2</span></span> 

<span data-ttu-id="79d05-224">Obtiene el CoreWebView2 asociado a este CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="79d05-224">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>

> <span data-ttu-id="79d05-225">[get_CoreWebView2](#get_corewebview2)(HRESULT) público ([ICoreWebView2](icorewebview2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="79d05-225">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="79d05-226">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="79d05-226">get_IsVisible</span></span> 

<span data-ttu-id="79d05-227">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-227">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="79d05-228">HRESULT público [get_IsVisible](#get_isvisible)(bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="79d05-228">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="79d05-229">Si IsVisible se establece en false, WebView será transparente y no se representará.</span><span class="sxs-lookup"><span data-stu-id="79d05-229">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="79d05-230">Sin embargo, esto no afectará a la ventana que contenga la vista de contenido (el parámetro HWND pasado a CreateCoreWebView2Controller).</span><span class="sxs-lookup"><span data-stu-id="79d05-230">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Controller).</span></span> <span data-ttu-id="79d05-231">Si desea que esta ventana desaparezca también, llame a ShowWindow directamente, además de modificar la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="79d05-231">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="79d05-232">Si la ventana superior está minimizada o restaurada, WebView no recibirá mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="79d05-232">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="79d05-233">Por motivos de rendimiento, desarrollador debe establecer el valor de la propiedad IsVisible de la WebView en falso cuando la ventana de la aplicación está minimizada y volver a ser true cuando se restaura la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79d05-233">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="79d05-234">La ventana de la aplicación puede hacerlo controlando SC_MINIMIZE y SC_RESTORE comando al recibir WM_SYSCOMMAND mensaje.</span><span class="sxs-lookup"><span data-stu-id="79d05-234">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="79d05-235">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="79d05-235">get_ParentWindow</span></span> 

<span data-ttu-id="79d05-236">La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.</span><span class="sxs-lookup"><span data-stu-id="79d05-236">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="79d05-237">[get_ParentWindow](#get_parentwindow)de HRESULT público (HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="79d05-237">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="79d05-238">Esta API inicialmente devuelve la ventana que se pasó a CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="79d05-238">This API initially returns the window passed into CreateCoreWebView2Controller.</span></span>

#### <span data-ttu-id="79d05-239">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="79d05-239">get_ZoomFactor</span></span> 

<span data-ttu-id="79d05-240">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-240">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="79d05-241">[get_ZoomFactor](#get_zoomfactor)de HRESULT público (Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="79d05-241">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="79d05-242">Ten en cuenta que cambiar el factor de zoom podría provocar un `window.innerWidth/innerHeight` cambio en el diseño de página.</span><span class="sxs-lookup"><span data-stu-id="79d05-242">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="79d05-243">Un factor de zoom aplicado por el host mediante una llamada a ZoomFactor se convierte en el nuevo zoom predeterminado para la vista de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-243">A zoom factor that is applied by the host by calling ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="79d05-244">Este factor de zoom se aplica en la navegación y se vuelve al factor de zoom en la vista previa cuando el usuario presiona Ctrl + 0.</span><span class="sxs-lookup"><span data-stu-id="79d05-244">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="79d05-245">Cuando el usuario cambia el factor de zoom (es decir, la aplicación que recibe la ZoomFactorChanged), ese zoom solo se aplica a la página actual.</span><span class="sxs-lookup"><span data-stu-id="79d05-245">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="79d05-246">Cualquier zoom aplicado a un usuario solo es para la página actual y se restablece en una navegación.</span><span class="sxs-lookup"><span data-stu-id="79d05-246">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="79d05-247">No se permite especificar un zoomFactor menor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="79d05-247">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="79d05-248">WebView también tiene un intervalo de factor de zoom compatible interno.</span><span class="sxs-lookup"><span data-stu-id="79d05-248">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="79d05-249">Cuando un factor de zoom especificado está fuera de ese rango, se normalizará para que esté dentro del rango y se desencadenará un evento ZoomFactorChanged para el factor de zoom aplicado real.</span><span class="sxs-lookup"><span data-stu-id="79d05-249">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="79d05-250">Cuando se produzca esta normalización de rango, la propiedad ZoomFactor informará sobre el factor de zoom especificado durante la modificación anterior de la propiedad ZoomFactor hasta que se reciba el evento ZoomFactorChanged después de que la vista previa aplique el factor de zoom normalizado.</span><span class="sxs-lookup"><span data-stu-id="79d05-250">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="79d05-251">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-251">MoveFocus</span></span> 

<span data-ttu-id="79d05-252">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-252">Move focus into WebView.</span></span>

> <span data-ttu-id="79d05-253">[MOVEFOCUS](#movefocus)HRESULT público (razón COREWEBVIEW2_MOVE_FOCUS_REASON)</span><span class="sxs-lookup"><span data-stu-id="79d05-253">public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON reason)</span></span>

<span data-ttu-id="79d05-254">La vista web obtendrá el foco y el foco se establecerá en el elemento de corresponsal de la página hospedada en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="79d05-254">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="79d05-255">Por motivos de programación, el foco se establece en elemento con enfoque anterior o en el elemento predeterminado si no hay ningún elemento con el foco anterior.</span><span class="sxs-lookup"><span data-stu-id="79d05-255">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="79d05-256">Por el siguiente motivo, el foco se establece en el primer elemento.</span><span class="sxs-lookup"><span data-stu-id="79d05-256">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="79d05-257">Por el motivo anterior, el foco se establece en el último elemento.</span><span class="sxs-lookup"><span data-stu-id="79d05-257">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="79d05-258">WebView también puede obtener el foco a través de la interacción del usuario, como hacer clic en la vista previa o en la pestaña en la misma.</span><span class="sxs-lookup"><span data-stu-id="79d05-258">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="79d05-259">Para la tabulación, la aplicación puede llamar a MoveFocus con la función siguiente o anterior para alinear con la tabulación y Mayús + Tab, respectivamente al decidir la vista previa del elemento tabulador.</span><span class="sxs-lookup"><span data-stu-id="79d05-259">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="79d05-260">O bien, la aplicación puede llamar a IsDialogMessage como parte de su bucle de mensajes para permitir que la plataforma maneje automáticamente la tabulación.</span><span class="sxs-lookup"><span data-stu-id="79d05-260">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="79d05-261">La plataforma girará en todas las ventanas con WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="79d05-261">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="79d05-262">Cuando la vista de la vista de la vista de IsDialogMessage, coloca internamente el foco en el primer o el último elemento de Tab y Mayús + Tab, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="79d05-262">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="79d05-263">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="79d05-263">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="79d05-264">Esta es una notificación independiente de los límites que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).</span><span class="sxs-lookup"><span data-stu-id="79d05-264">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="79d05-265">[NOTIFYPARENTWINDOWPOSITIONCHANGED](#notifyparentwindowpositionchanged)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="79d05-265">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="79d05-266">Esto es necesario para que la accesibilidad y determinados cuadros de diálogo de WebView funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="79d05-266">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="79d05-267">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="79d05-267">put_Bounds</span></span> 

<span data-ttu-id="79d05-268">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="79d05-268">Set the Bounds property.</span></span>

> <span data-ttu-id="79d05-269">[put_Bounds](#put_bounds)de HRESULT público (límites Rect)</span><span class="sxs-lookup"><span data-stu-id="79d05-269">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### <span data-ttu-id="79d05-270">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="79d05-270">put_IsVisible</span></span> 

<span data-ttu-id="79d05-271">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="79d05-271">Set the IsVisible property.</span></span>

> <span data-ttu-id="79d05-272">[put_IsVisible](#put_isvisible)de HRESULT público (bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="79d05-272">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="79d05-273">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="79d05-273">put_ParentWindow</span></span> 

<span data-ttu-id="79d05-274">Establezca la ventana principal de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="79d05-274">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="79d05-275">[put_ParentWindow](#put_parentwindow)de HRESULT público (HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="79d05-275">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="79d05-276">Esto hará que la vista de ventana reorigen su ventana a la ventana recién suministrada.</span><span class="sxs-lookup"><span data-stu-id="79d05-276">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="79d05-277">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="79d05-277">put_ZoomFactor</span></span> 

<span data-ttu-id="79d05-278">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="79d05-278">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="79d05-279">[put_ZoomFactor](#put_zoomfactor)de HRESULT público (Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="79d05-279">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="79d05-280">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="79d05-280">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="79d05-281">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="79d05-281">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="79d05-282">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="79d05-282">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="79d05-283">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-283">remove_GotFocus</span></span> 

<span data-ttu-id="79d05-284">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-284">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="79d05-285">[remove_GotFocus](#remove_gotfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="79d05-285">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="79d05-286">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="79d05-286">remove_LostFocus</span></span> 

<span data-ttu-id="79d05-287">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="79d05-287">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="79d05-288">[remove_LostFocus](#remove_lostfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="79d05-288">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="79d05-289">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="79d05-289">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="79d05-290">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="79d05-290">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="79d05-291">[remove_MoveFocusRequested](#remove_movefocusrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="79d05-291">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="79d05-292">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="79d05-292">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="79d05-293">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="79d05-293">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="79d05-294">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="79d05-294">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="79d05-295">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="79d05-295">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="79d05-296">Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="79d05-296">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="79d05-297">HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(rectángulos de rectángulo, doble zoomFactor)</span><span class="sxs-lookup"><span data-stu-id="79d05-297">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds, double zoomFactor)</span></span>

<span data-ttu-id="79d05-298">Esta operación es atómica desde la perspectiva del anfitrión.</span><span class="sxs-lookup"><span data-stu-id="79d05-298">This operation is atomic from the host's perspective.</span></span> <span data-ttu-id="79d05-299">Después de volver de esta función, las propiedades Bounds y ZoomFactor se actualizarán si la función se realiza correctamente, o no se actualizará si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="79d05-299">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="79d05-300">Si los límites y ZoomFactor se actualizan con la misma escala (es decir, los límites y ZoomFactor están duplicados), la página no verá un cambio en la ventana. innerWidth/innerHeight y la WebView representará el contenido en el nuevo tamaño y zoom sin representaciones intermedias.</span><span class="sxs-lookup"><span data-stu-id="79d05-300">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="79d05-301">Esta función también se puede usar para actualizar solo una de ZoomFactor o límites pasando el nuevo valor para uno y el valor actual para el otro.</span><span class="sxs-lookup"><span data-stu-id="79d05-301">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```

