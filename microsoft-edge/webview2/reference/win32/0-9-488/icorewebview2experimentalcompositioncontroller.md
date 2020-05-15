---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e6499c77a17fd9ff4563359cdf05dc4a32f19a51
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655281"
---
# <span data-ttu-id="e2766-104">interfaz ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="e2766-104">interface ICoreWebView2ExperimentalCompositionController</span></span> 

> [!NOTE]
> <span data-ttu-id="e2766-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="e2766-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="e2766-106">Esta interfaz es una extensión de la interfaz ICoreWebView2Controller para admitir hospedajes visuales.</span><span class="sxs-lookup"><span data-stu-id="e2766-106">This interface is an extension of the ICoreWebView2Controller interface to support visual hosting.</span></span>

## <span data-ttu-id="e2766-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="e2766-107">Summary</span></span>

 <span data-ttu-id="e2766-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2766-108">Members</span></span>                        | <span data-ttu-id="e2766-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e2766-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e2766-110">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="e2766-110">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="e2766-111">Agregue un controlador de eventos para el evento CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="e2766-111">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="e2766-112">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="e2766-112">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="e2766-113">Una función auxiliar para convertir una pointerId recibida del sistema en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="e2766-113">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="e2766-114">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="e2766-114">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="e2766-115">El cursor actual que la vista en WebView debe tener.</span><span class="sxs-lookup"><span data-stu-id="e2766-115">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="e2766-116">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="e2766-116">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="e2766-117">El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="e2766-117">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="e2766-118">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="e2766-118">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="e2766-119">Devuelve el proveedor de automatización de la interfaz de usuario de WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-119">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="e2766-120">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="e2766-120">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="e2766-121">Establezca la propiedad RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="e2766-121">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="e2766-122">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="e2766-122">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="e2766-123">Quitar un controlador de eventos agregado previamente con add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="e2766-123">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="e2766-124">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="e2766-124">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="e2766-125">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL o COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especifica la cantidad de movimiento de la rueda.</span><span class="sxs-lookup"><span data-stu-id="e2766-125">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="e2766-126">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="e2766-126">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="e2766-127">SendPointerInput acepta la entrada del puntero táctil o de lápiz de los tipos definidos en COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="e2766-127">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="e2766-128">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="e2766-128">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="e2766-129">Matriz que representa una transformación 3D.</span><span class="sxs-lookup"><span data-stu-id="e2766-129">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="e2766-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="e2766-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="e2766-131">Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-131">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="e2766-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="e2766-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="e2766-133">Teclas virtuales de eventos del mouse asociadas con un COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="e2766-133">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="e2766-134">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="e2766-134">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="e2766-135">Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-135">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="e2766-136">Un objeto que implementa la interfaz ICoreWebView2ExperimentalCompositionController también implementará ICoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="e2766-136">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement ICoreWebView2Controller.</span></span> <span data-ttu-id="e2766-137">Se espera que las personas que llaman usen ICoreWebView2Controller para cambiar el tamaño, la visibilidad, el foco, etc., y, después, usar ICoreWebView2ExperimentalCompositionController para conectarse a un árbol de composición y proporcionar una entrada para la vista de la vista.</span><span class="sxs-lookup"><span data-stu-id="e2766-137">Callers are expected to use ICoreWebView2Controller for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="e2766-138">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2766-138">Members</span></span>

#### <span data-ttu-id="e2766-139">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="e2766-139">add_CursorChanged</span></span> 

<span data-ttu-id="e2766-140">Agregue un controlador de eventos para el evento CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="e2766-140">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="e2766-141">[add_CursorChanged](#add_cursorchanged)de HRESULT público ([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="e2766-141">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e2766-142">El evento se desencadena cuando WebView considera que se debe cambiar el cursor.</span><span class="sxs-lookup"><span data-stu-id="e2766-142">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="e2766-143">Por ejemplo, cuando el cursor del mouse es actualmente el cursor predeterminado pero, después, se desplaza por el texto, puede intentar cambiar al cursor IBeam.</span><span class="sxs-lookup"><span data-stu-id="e2766-143">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

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

#### <span data-ttu-id="e2766-144">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="e2766-144">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="e2766-145">Una función auxiliar para convertir una pointerId recibida del sistema en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="e2766-145">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="e2766-146">Public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="e2766-146">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="e2766-147">parentWindow es el HWND que contiene WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-147">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="e2766-148">Puede ser cualquier HWND en el árbol HWND que contenga la vista en vista previa.</span><span class="sxs-lookup"><span data-stu-id="e2766-148">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="e2766-149">El COREWEBVIEW2_MATRIX_4X4 es la transformación de ese HWND a la vista de vista.</span><span class="sxs-lookup"><span data-stu-id="e2766-149">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="e2766-150">El [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) devuelto se usa en SendPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="e2766-150">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="e2766-151">El tipo de puntero debe ser pluma o entrada táctil, o la función dará un error.</span><span class="sxs-lookup"><span data-stu-id="e2766-151">The pointer type must be either pen or touch or the function will fail.</span></span>



#### <span data-ttu-id="e2766-152">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="e2766-152">get_Cursor</span></span> 

<span data-ttu-id="e2766-153">El cursor actual que la vista en WebView debe tener.</span><span class="sxs-lookup"><span data-stu-id="e2766-153">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="e2766-154">[get_Cursor](#get_cursor)de HRESULT público (cursor HCURSOR \*)</span><span class="sxs-lookup"><span data-stu-id="e2766-154">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="e2766-155">El cursor debe establecerse en WM_SETCURSOR a:: SetCursor o establecerse en el HWND primario/antecesor correspondiente de la vista en:: SetClassLongPtr.</span><span class="sxs-lookup"><span data-stu-id="e2766-155">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="e2766-156">El HCURSOR se puede liberar, por lo que se recomienda CopyCursor/DestroyCursor para conservar su propia copia si hace más de lo que hay que establecer inmediatamente el cursor.</span><span class="sxs-lookup"><span data-stu-id="e2766-156">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="e2766-157">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="e2766-157">get_RootVisualTarget</span></span> 

<span data-ttu-id="e2766-158">El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="e2766-158">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="e2766-159">[get_RootVisualTarget](#get_rootvisualtarget)de HRESULT público (IUnknown \* \* Target)</span><span class="sxs-lookup"><span data-stu-id="e2766-159">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="e2766-160">Este objeto visual es el lugar donde la vista en WebView conectará su árbol visual.</span><span class="sxs-lookup"><span data-stu-id="e2766-160">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="e2766-161">La aplicación usa este objeto visual para posicionar la vista en la vista previa dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2766-161">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="e2766-162">La aplicación aún debe usar la propiedad Bounds para cambiar el tamaño de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-162">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="e2766-163">La propiedad RootVisualTarget puede ser una IDCompositionVisual o Windows:: UI:: Composition:: ContainerVisual.</span><span class="sxs-lookup"><span data-stu-id="e2766-163">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="e2766-164">WebView conectará su árbol visual al visual proporcionado antes de volver de la propiedad Setter.</span><span class="sxs-lookup"><span data-stu-id="e2766-164">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="e2766-165">La aplicación debe confirmar en su dispositivo estableciendo la propiedad RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="e2766-165">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="e2766-166">La propiedad RootVisualTarget admite establecerse en nullptr para desconectar el WebView del árbol visual de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2766-166">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
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

#### <span data-ttu-id="e2766-167">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="e2766-167">get_UIAProvider</span></span> 

<span data-ttu-id="e2766-168">Devuelve el proveedor de automatización de la interfaz de usuario de WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-168">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="e2766-169">[get_UIAProvider](#get_uiaprovider)de HRESULT público (IUnknown \* \*)</span><span class="sxs-lookup"><span data-stu-id="e2766-169">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="e2766-170">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="e2766-170">put_RootVisualTarget</span></span> 

<span data-ttu-id="e2766-171">Establezca la propiedad RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="e2766-171">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="e2766-172">[put_RootVisualTarget](#put_rootvisualtarget)de HRESULT público (IUnknown \* Target)</span><span class="sxs-lookup"><span data-stu-id="e2766-172">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="e2766-173">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="e2766-173">remove_CursorChanged</span></span> 

<span data-ttu-id="e2766-174">Quitar un controlador de eventos agregado previamente con add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="e2766-174">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="e2766-175">[remove_CursorChanged](#remove_cursorchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="e2766-175">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e2766-176">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="e2766-176">SendMouseInput</span></span> 

<span data-ttu-id="e2766-177">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL o COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especifica la cantidad de movimiento de la rueda.</span><span class="sxs-lookup"><span data-stu-id="e2766-177">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="e2766-178">[SENDMOUSEINPUT](#sendmouseinput)HRESULT público ([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, Point)</span><span class="sxs-lookup"><span data-stu-id="e2766-178">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="e2766-179">Un valor positivo indica que la rueda se giró hacia adelante, alejándose del usuario; un valor negativo indica que la rueda se ha girado hacia atrás, hacia el usuario.</span><span class="sxs-lookup"><span data-stu-id="e2766-179">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="e2766-180">Un clic de rueda se define como WHEEL_DELTA, que es 120.</span><span class="sxs-lookup"><span data-stu-id="e2766-180">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="e2766-181">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN o COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, mouseData especifica qué botones X se han presionado o se han soltado.</span><span class="sxs-lookup"><span data-stu-id="e2766-181">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="e2766-182">Este valor debe ser 1 si se presiona o se suelta el primer botón X y 2 si se presiona o se suelta el segundo botón X.</span><span class="sxs-lookup"><span data-stu-id="e2766-182">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="e2766-183">Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, virtualKeys, mouseData y Point deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="e2766-183">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="e2766-184">Si eventKind es cualquier otro valor, mouseData debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e2766-184">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="e2766-185">Se espera que el punto se sitúe en el espacio de coordenadas del cliente de la vista Web.</span><span class="sxs-lookup"><span data-stu-id="e2766-185">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="e2766-186">Para hacer un seguimiento de los eventos del mouse que se inician en la WebView y pueden moverse fuera de la aplicación WebView y host, se recomienda llamar a SetCapture y ReleaseCapture.</span><span class="sxs-lookup"><span data-stu-id="e2766-186">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="e2766-187">Para descartar los elementos emergentes activables, también se recomienda enviar mensajes de WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="e2766-187">To dismiss hover popups, it is also recommended to send WM_MOUSELEAVE messages.</span></span> 
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

#### <span data-ttu-id="e2766-188">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="e2766-188">SendPointerInput</span></span> 

<span data-ttu-id="e2766-189">SendPointerInput acepta la entrada del puntero táctil o de lápiz de los tipos definidos en COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="e2766-189">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="e2766-190">HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="e2766-190">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="e2766-191">Cualquier entrada de puntero del sistema debe convertirse en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="e2766-191">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="e2766-192">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="e2766-192">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="e2766-193">Matriz que representa una transformación 3D.</span><span class="sxs-lookup"><span data-stu-id="e2766-193">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="e2766-194">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span><span class="sxs-lookup"><span data-stu-id="e2766-194">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="e2766-195">Esta transformación se usa para calcular las coordenadas correctas al llamar a CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="e2766-195">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="e2766-196">Es equivalente a una D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="e2766-196">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="e2766-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="e2766-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="e2766-198">Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-198">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="e2766-199">[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="e2766-199">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="e2766-200">Los</span><span class="sxs-lookup"><span data-stu-id="e2766-200">Values</span></span>                         | <span data-ttu-id="e2766-201">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e2766-201">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="e2766-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="e2766-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="e2766-203">Evento de desplazamiento horizontal de la rueda del mouse, WM_MOUSEHWHEEL.</span><span class="sxs-lookup"><span data-stu-id="e2766-203">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="e2766-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="e2766-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="e2766-205">Botón izquierdo doble clic en evento de mouse, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="e2766-205">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="e2766-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="e2766-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="e2766-207">Botón izquierdo de un evento de mouse, WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="e2766-207">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="e2766-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="e2766-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="e2766-209">Evento de botón arriba del botón izquierdo, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="e2766-209">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="e2766-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="e2766-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="e2766-211">Evento Leave de mouse, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="e2766-211">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="e2766-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="e2766-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="e2766-213">Botón central doble clic en evento de mouse, WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="e2766-213">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="e2766-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="e2766-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="e2766-215">Botón central de mouse, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="e2766-215">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="e2766-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="e2766-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="e2766-217">Evento de botón arriba del botón central, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="e2766-217">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="e2766-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="e2766-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="e2766-219">Evento de movimiento del mouse, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="e2766-219">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="e2766-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="e2766-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="e2766-221">Botón secundario doble clic en el evento del mouse WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="e2766-221">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="e2766-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="e2766-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="e2766-223">Botón secundario del mouse, WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="e2766-223">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="e2766-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="e2766-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="e2766-225">Evento de botón arriba del botón secundario, WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="e2766-225">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="e2766-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="e2766-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="e2766-227">Evento scroll de la rueda del mouse, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="e2766-227">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="e2766-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="e2766-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="e2766-229">Primer o segundo botón X haga doble clic en evento del mouse, WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="e2766-229">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="e2766-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="e2766-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="e2766-231">Primer o segundo evento de mouse en el botón X presionado, WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="e2766-231">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="e2766-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="e2766-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="e2766-233">Primer o segundo evento del botón X del botón arriba, WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="e2766-233">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="e2766-234">Los valores de esta enumeración se alinean con los mensajes de ventana WM_ \* coincidentes.</span><span class="sxs-lookup"><span data-stu-id="e2766-234">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="e2766-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="e2766-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="e2766-236">Teclas virtuales de eventos del mouse asociadas con un COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="e2766-236">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="e2766-237">[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) enum</span><span class="sxs-lookup"><span data-stu-id="e2766-237">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="e2766-238">Los</span><span class="sxs-lookup"><span data-stu-id="e2766-238">Values</span></span>                         | <span data-ttu-id="e2766-239">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e2766-239">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="e2766-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="e2766-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="e2766-241">No se han presionado teclas adicionales.</span><span class="sxs-lookup"><span data-stu-id="e2766-241">No additional keys pressed.</span></span>
<span data-ttu-id="e2766-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="e2766-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="e2766-243">El botón primario del mouse está presionado, MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="e2766-243">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="e2766-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="e2766-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="e2766-245">El botón secundario del mouse está presionado, MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="e2766-245">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="e2766-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="e2766-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="e2766-247">La tecla Mayús está presionada, MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="e2766-247">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="e2766-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="e2766-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="e2766-249">La tecla CTRL está presionada, MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="e2766-249">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="e2766-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="e2766-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="e2766-251">El botón central del mouse está presionado, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="e2766-251">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="e2766-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="e2766-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="e2766-253">El primer botón X está presionado, MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="e2766-253">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="e2766-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="e2766-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="e2766-255">El segundo botón X está presionado, MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="e2766-255">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="e2766-256">Estos valores se pueden combinar en una marca de bit si se presiona más de una tecla virtual para el evento.</span><span class="sxs-lookup"><span data-stu-id="e2766-256">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="e2766-257">Los valores de esta enumeración se alinean con las teclas de mouse \* MK_ \*.</span><span class="sxs-lookup"><span data-stu-id="e2766-257">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="e2766-258">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="e2766-258">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="e2766-259">Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.</span><span class="sxs-lookup"><span data-stu-id="e2766-259">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="e2766-260">[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="e2766-260">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="e2766-261">Los</span><span class="sxs-lookup"><span data-stu-id="e2766-261">Values</span></span>                         | <span data-ttu-id="e2766-262">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e2766-262">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="e2766-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="e2766-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="e2766-264">Corresponde a WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="e2766-264">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="e2766-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="e2766-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="e2766-266">Corresponde a WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="e2766-266">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="e2766-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="e2766-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="e2766-268">Corresponde a WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="e2766-268">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="e2766-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="e2766-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="e2766-270">Corresponde a WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="e2766-270">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="e2766-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="e2766-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="e2766-272">Corresponde a WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="e2766-272">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="e2766-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="e2766-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="e2766-274">Corresponde a WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="e2766-274">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="e2766-275">Los valores de esta enumeración se alinean con los mensajes de ventana WM_POINTER \* coincidentes.</span><span class="sxs-lookup"><span data-stu-id="e2766-275">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>

