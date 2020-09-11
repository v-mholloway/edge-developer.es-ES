---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCompositionController
ms.openlocfilehash: 893628746e52ee8501e357f965d49324446d6470
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010218"
---
# <span data-ttu-id="b7815-104">0.9.579: ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="b7815-104">0.9.579 - interface ICoreWebView2ExperimentalCompositionController</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="b7815-105">Esta interfaz es una extensión de la interfaz [ICoreWebView2Controller](icorewebview2controller.md) para admitir hospedajes visuales.</span><span class="sxs-lookup"><span data-stu-id="b7815-105">This interface is an extension of the [ICoreWebView2Controller](icorewebview2controller.md) interface to support visual hosting.</span></span>

## <span data-ttu-id="b7815-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b7815-106">Summary</span></span>

 <span data-ttu-id="b7815-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7815-107">Members</span></span>                        | <span data-ttu-id="b7815-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b7815-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7815-109">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="b7815-109">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="b7815-110">Agregue un controlador de eventos para el evento CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="b7815-110">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="b7815-111">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="b7815-111">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="b7815-112">Una función auxiliar para convertir una pointerId recibida del sistema en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="b7815-112">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="b7815-113">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="b7815-113">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="b7815-114">El cursor actual que la vista en WebView debe tener.</span><span class="sxs-lookup"><span data-stu-id="b7815-114">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="b7815-115">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="b7815-115">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="b7815-116">El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="b7815-116">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="b7815-117">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="b7815-117">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="b7815-118">Devuelve el proveedor de automatización de la interfaz de usuario de WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-118">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="b7815-119">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="b7815-119">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="b7815-120">Establezca la propiedad RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="b7815-120">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="b7815-121">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="b7815-121">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="b7815-122">Quitar un controlador de eventos agregado previamente con add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="b7815-122">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="b7815-123">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="b7815-123">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="b7815-124">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL o COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especifica la cantidad de movimiento de la rueda.</span><span class="sxs-lookup"><span data-stu-id="b7815-124">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="b7815-125">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="b7815-125">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="b7815-126">SendPointerInput acepta la entrada del puntero táctil o de lápiz de los tipos definidos en COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="b7815-126">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="b7815-127">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="b7815-127">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="b7815-128">Matriz que representa una transformación 3D.</span><span class="sxs-lookup"><span data-stu-id="b7815-128">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="b7815-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="b7815-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="b7815-130">Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-130">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="b7815-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="b7815-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="b7815-132">Teclas virtuales de eventos del mouse asociadas con un COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="b7815-132">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="b7815-133">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="b7815-133">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="b7815-134">Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-134">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="b7815-135">Un objeto que implementa la interfaz ICoreWebView2ExperimentalCompositionController también implementará [ICoreWebView2Controller](icorewebview2controller.md).</span><span class="sxs-lookup"><span data-stu-id="b7815-135">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement [ICoreWebView2Controller](icorewebview2controller.md).</span></span> <span data-ttu-id="b7815-136">Se espera que las personas que llaman usen [ICoreWebView2Controller](icorewebview2controller.md) para cambiar el tamaño, la visibilidad, el foco, etc., y, después, usar ICoreWebView2ExperimentalCompositionController para conectarse a un árbol de composición y proporcionar una entrada para la vista de la vista.</span><span class="sxs-lookup"><span data-stu-id="b7815-136">Callers are expected to use [ICoreWebView2Controller](icorewebview2controller.md) for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="b7815-137">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7815-137">Members</span></span>

#### <span data-ttu-id="b7815-138">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="b7815-138">add_CursorChanged</span></span> 

<span data-ttu-id="b7815-139">Agregue un controlador de eventos para el evento CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="b7815-139">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="b7815-140">[add_CursorChanged](#add_cursorchanged)de HRESULT público ([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="b7815-140">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b7815-141">El evento se desencadena cuando WebView considera que se debe cambiar el cursor.</span><span class="sxs-lookup"><span data-stu-id="b7815-141">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="b7815-142">Por ejemplo, cuando el cursor del mouse es actualmente el cursor predeterminado pero, después, se desplaza por el texto, puede intentar cambiar al cursor IBeam.</span><span class="sxs-lookup"><span data-stu-id="b7815-142">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

<span data-ttu-id="b7815-143">Se espera que el desarrollador envíe mensajes de COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE (además de mensajes de COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE) a través de la API SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="b7815-143">It is expected for the developer to send COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE messages (in addition to COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE messages) through the SendMouseInput API.</span></span> <span data-ttu-id="b7815-144">Esto se hace para garantizar que el mouse se encuentre realmente dentro de la vista en WebView que envía eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="b7815-144">This is to ensure that the mouse is actually within the WebView that sends out CursorChanged events.</span></span>

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                    IUnknown* args) -> HRESULT {
                        HCURSOR cursor;
                        CHECK_FAILURE(sender->get_Cursor(&cursor));
                        SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                        return S_OK;
                })
            .Get(),
                    &m_cursorChangedToken));
```

#### <span data-ttu-id="b7815-145">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="b7815-145">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="b7815-146">Una función auxiliar para convertir una pointerId recibida del sistema en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="b7815-146">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="b7815-147">Public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="b7815-147">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="b7815-148">parentWindow es el HWND que contiene WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-148">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="b7815-149">Puede ser cualquier HWND en el árbol HWND que contenga la vista en vista previa.</span><span class="sxs-lookup"><span data-stu-id="b7815-149">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="b7815-150">El COREWEBVIEW2_MATRIX_4X4 es la transformación de ese HWND a la vista de vista.</span><span class="sxs-lookup"><span data-stu-id="b7815-150">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="b7815-151">El [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) devuelto se usa en SendPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="b7815-151">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="b7815-152">El tipo de puntero debe ser pluma o entrada táctil, o la función dará un error.</span><span class="sxs-lookup"><span data-stu-id="b7815-152">The pointer type must be either pen or touch or the function will fail.</span></span>


#### <span data-ttu-id="b7815-153">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="b7815-153">get_Cursor</span></span> 

<span data-ttu-id="b7815-154">El cursor actual que la vista en WebView debe tener.</span><span class="sxs-lookup"><span data-stu-id="b7815-154">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="b7815-155">[get_Cursor](#get_cursor)de HRESULT público (cursor HCURSOR \*)</span><span class="sxs-lookup"><span data-stu-id="b7815-155">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="b7815-156">El cursor debe establecerse en WM_SETCURSOR a:: SetCursor o establecerse en el HWND primario/antecesor correspondiente de la vista en:: SetClassLongPtr.</span><span class="sxs-lookup"><span data-stu-id="b7815-156">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="b7815-157">El HCURSOR se puede liberar, por lo que se recomienda CopyCursor/DestroyCursor para conservar su propia copia si hace más de lo que hay que establecer inmediatamente el cursor.</span><span class="sxs-lookup"><span data-stu-id="b7815-157">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="b7815-158">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="b7815-158">get_RootVisualTarget</span></span> 

<span data-ttu-id="b7815-159">El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="b7815-159">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="b7815-160">[get_RootVisualTarget](#get_rootvisualtarget)de HRESULT público (IUnknown \* \* Target)</span><span class="sxs-lookup"><span data-stu-id="b7815-160">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="b7815-161">Este objeto visual es el lugar donde la vista en WebView conectará su árbol visual.</span><span class="sxs-lookup"><span data-stu-id="b7815-161">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="b7815-162">La aplicación usa este objeto visual para posicionar la vista en la vista previa dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7815-162">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="b7815-163">La aplicación aún debe usar la propiedad Bounds para cambiar el tamaño de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-163">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="b7815-164">La propiedad RootVisualTarget puede ser una IDCompositionVisual o Windows:: UI:: Composition:: ContainerVisual.</span><span class="sxs-lookup"><span data-stu-id="b7815-164">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="b7815-165">WebView conectará su árbol visual al visual proporcionado antes de volver de la propiedad Setter.</span><span class="sxs-lookup"><span data-stu-id="b7815-165">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="b7815-166">La aplicación debe confirmar en su dispositivo estableciendo la propiedad RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="b7815-166">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="b7815-167">La propiedad RootVisualTarget admite establecerse en nullptr para desconectar el WebView del árbol visual de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7815-167">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### <span data-ttu-id="b7815-168">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="b7815-168">get_UIAProvider</span></span> 

<span data-ttu-id="b7815-169">Devuelve el proveedor de automatización de la interfaz de usuario de WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-169">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="b7815-170">[get_UIAProvider](#get_uiaprovider)de HRESULT público (IUnknown \* \*)</span><span class="sxs-lookup"><span data-stu-id="b7815-170">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="b7815-171">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="b7815-171">put_RootVisualTarget</span></span> 

<span data-ttu-id="b7815-172">Establezca la propiedad RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="b7815-172">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="b7815-173">[put_RootVisualTarget](#put_rootvisualtarget)de HRESULT público (IUnknown \* Target)</span><span class="sxs-lookup"><span data-stu-id="b7815-173">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="b7815-174">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="b7815-174">remove_CursorChanged</span></span> 

<span data-ttu-id="b7815-175">Quitar un controlador de eventos agregado previamente con add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="b7815-175">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="b7815-176">[remove_CursorChanged](#remove_cursorchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="b7815-176">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b7815-177">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="b7815-177">SendMouseInput</span></span> 

<span data-ttu-id="b7815-178">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL o COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especifica la cantidad de movimiento de la rueda.</span><span class="sxs-lookup"><span data-stu-id="b7815-178">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="b7815-179">[SENDMOUSEINPUT](#sendmouseinput)HRESULT público ([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, Point)</span><span class="sxs-lookup"><span data-stu-id="b7815-179">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="b7815-180">Un valor positivo indica que la rueda se giró hacia adelante, alejándose del usuario; un valor negativo indica que la rueda se ha girado hacia atrás, hacia el usuario.</span><span class="sxs-lookup"><span data-stu-id="b7815-180">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="b7815-181">Un clic de rueda se define como WHEEL_DELTA, que es 120.</span><span class="sxs-lookup"><span data-stu-id="b7815-181">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="b7815-182">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN o COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, mouseData especifica qué botones X se han presionado o se han soltado.</span><span class="sxs-lookup"><span data-stu-id="b7815-182">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="b7815-183">Este valor debe ser 1 si se presiona o se suelta el primer botón X y 2 si se presiona o se suelta el segundo botón X.</span><span class="sxs-lookup"><span data-stu-id="b7815-183">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="b7815-184">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, virtualKeys, mouseData y Point deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="b7815-184">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="b7815-185">Si eventKind es cualquier otro valor, mouseData debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b7815-185">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="b7815-186">Se espera que el punto se sitúe en el espacio de coordenadas del cliente de la vista Web.</span><span class="sxs-lookup"><span data-stu-id="b7815-186">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="b7815-187">Para hacer un seguimiento de los eventos del mouse que se inician en la WebView y pueden moverse fuera de la aplicación WebView y host, se recomienda llamar a SetCapture y ReleaseCapture.</span><span class="sxs-lookup"><span data-stu-id="b7815-187">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="b7815-188">Para descartar los elementos emergentes activables, también se recomienda enviar mensajes de COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE.</span><span class="sxs-lookup"><span data-stu-id="b7815-188">To dismiss hover popups, it is also recommended to send COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE messages.</span></span> 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### <span data-ttu-id="b7815-189">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="b7815-189">SendPointerInput</span></span> 

<span data-ttu-id="b7815-190">SendPointerInput acepta la entrada del puntero táctil o de lápiz de los tipos definidos en COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="b7815-190">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="b7815-191">HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="b7815-191">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="b7815-192">Cualquier entrada de puntero del sistema debe convertirse en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="b7815-192">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="b7815-193">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="b7815-193">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="b7815-194">Matriz que representa una transformación 3D.</span><span class="sxs-lookup"><span data-stu-id="b7815-194">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="b7815-195">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span><span class="sxs-lookup"><span data-stu-id="b7815-195">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="b7815-196">Esta transformación se usa para calcular las coordenadas correctas al llamar a CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="b7815-196">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="b7815-197">Es equivalente a una D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="b7815-197">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="b7815-198">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="b7815-198">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="b7815-199">Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-199">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="b7815-200">[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="b7815-200">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="b7815-201">Los</span><span class="sxs-lookup"><span data-stu-id="b7815-201">Values</span></span>                         | <span data-ttu-id="b7815-202">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b7815-202">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b7815-203">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="b7815-203">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="b7815-204">Evento de desplazamiento horizontal de la rueda del mouse, WM_MOUSEHWHEEL.</span><span class="sxs-lookup"><span data-stu-id="b7815-204">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="b7815-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="b7815-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="b7815-206">Botón izquierdo doble clic en evento de mouse, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="b7815-206">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="b7815-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="b7815-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="b7815-208">Botón izquierdo de un evento de mouse, WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="b7815-208">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="b7815-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="b7815-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="b7815-210">Evento de botón arriba del botón izquierdo, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="b7815-210">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="b7815-211">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="b7815-211">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="b7815-212">Evento Leave de mouse, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="b7815-212">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="b7815-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="b7815-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="b7815-214">Botón central doble clic en evento de mouse, WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="b7815-214">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="b7815-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="b7815-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="b7815-216">Botón central de mouse, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="b7815-216">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="b7815-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="b7815-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="b7815-218">Evento de botón arriba del botón central, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="b7815-218">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="b7815-219">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="b7815-219">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="b7815-220">Evento de movimiento del mouse, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="b7815-220">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="b7815-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="b7815-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="b7815-222">Botón secundario doble clic en el evento del mouse WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="b7815-222">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="b7815-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="b7815-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="b7815-224">Botón secundario del mouse, WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="b7815-224">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="b7815-225">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="b7815-225">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="b7815-226">Evento de botón arriba del botón secundario, WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="b7815-226">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="b7815-227">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="b7815-227">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="b7815-228">Evento scroll de la rueda del mouse, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="b7815-228">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="b7815-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="b7815-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="b7815-230">Primer o segundo botón X haga doble clic en evento del mouse, WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="b7815-230">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="b7815-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="b7815-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="b7815-232">Primer o segundo evento de mouse en el botón X presionado, WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="b7815-232">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="b7815-233">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="b7815-233">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="b7815-234">Primer o segundo evento del botón X del botón arriba, WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="b7815-234">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="b7815-235">Los valores de esta enumeración se alinean con los mensajes de ventana WM_ \* coincidentes.</span><span class="sxs-lookup"><span data-stu-id="b7815-235">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="b7815-236">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="b7815-236">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="b7815-237">Teclas virtuales de eventos del mouse asociadas con un COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="b7815-237">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="b7815-238">[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) enum</span><span class="sxs-lookup"><span data-stu-id="b7815-238">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="b7815-239">Los</span><span class="sxs-lookup"><span data-stu-id="b7815-239">Values</span></span>                         | <span data-ttu-id="b7815-240">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b7815-240">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b7815-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="b7815-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="b7815-242">No se han presionado teclas adicionales.</span><span class="sxs-lookup"><span data-stu-id="b7815-242">No additional keys pressed.</span></span>
<span data-ttu-id="b7815-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="b7815-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="b7815-244">El botón primario del mouse está presionado, MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="b7815-244">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="b7815-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="b7815-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="b7815-246">El botón secundario del mouse está presionado, MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="b7815-246">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="b7815-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="b7815-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="b7815-248">La tecla Mayús está presionada, MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="b7815-248">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="b7815-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="b7815-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="b7815-250">La tecla CTRL está presionada, MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="b7815-250">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="b7815-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="b7815-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="b7815-252">El botón central del mouse está presionado, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="b7815-252">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="b7815-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="b7815-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="b7815-254">El primer botón X está presionado, MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="b7815-254">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="b7815-255">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="b7815-255">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="b7815-256">El segundo botón X está presionado, MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="b7815-256">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="b7815-257">Estos valores se pueden combinar en una marca de bit si se presiona más de una tecla virtual para el evento.</span><span class="sxs-lookup"><span data-stu-id="b7815-257">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="b7815-258">Los valores de esta enumeración se alinean con las teclas de mouse \* MK_ \*.</span><span class="sxs-lookup"><span data-stu-id="b7815-258">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="b7815-259">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="b7815-259">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="b7815-260">Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="b7815-260">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="b7815-261">[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="b7815-261">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="b7815-262">Los</span><span class="sxs-lookup"><span data-stu-id="b7815-262">Values</span></span>                         | <span data-ttu-id="b7815-263">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b7815-263">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b7815-264">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="b7815-264">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="b7815-265">Corresponde a WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="b7815-265">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="b7815-266">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="b7815-266">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="b7815-267">Corresponde a WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="b7815-267">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="b7815-268">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="b7815-268">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="b7815-269">Corresponde a WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="b7815-269">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="b7815-270">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="b7815-270">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="b7815-271">Corresponde a WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="b7815-271">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="b7815-272">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="b7815-272">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="b7815-273">Corresponde a WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="b7815-273">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="b7815-274">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="b7815-274">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="b7815-275">Corresponde a WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="b7815-275">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="b7815-276">Los valores de esta enumeración se alinean con los mensajes de ventana WM_POINTER \* coincidentes.</span><span class="sxs-lookup"><span data-stu-id="b7815-276">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>

