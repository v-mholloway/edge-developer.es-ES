---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Host
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 9202c17d83ad7d0750dbf76724b550d73ecca434
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881036"
---
# <span data-ttu-id="09c53-104">0.9.430: ICoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="09c53-104">0.9.430 - interface ICoreWebView2Host</span></span> 

> [!NOTE]
> <span data-ttu-id="09c53-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="09c53-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="09c53-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="09c53-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Host
  : public IUnknown
```

<span data-ttu-id="09c53-107">Esta interfaz es el propietario del objeto CoreWebView2 y proporciona compatibilidad para cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.</span><span class="sxs-lookup"><span data-stu-id="09c53-107">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="09c53-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="09c53-108">Summary</span></span>

 <span data-ttu-id="09c53-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="09c53-109">Members</span></span>                        | <span data-ttu-id="09c53-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="09c53-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09c53-111">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="09c53-111">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="09c53-112">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-112">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="09c53-113">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="09c53-113">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="09c53-114">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="09c53-114">Set the IsVisible property.</span></span>
[<span data-ttu-id="09c53-115">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="09c53-115">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="09c53-116">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="09c53-116">The webview bounds.</span></span>
[<span data-ttu-id="09c53-117">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="09c53-117">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="09c53-118">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="09c53-118">Set the Bounds property.</span></span>
[<span data-ttu-id="09c53-119">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="09c53-119">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="09c53-120">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-120">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="09c53-121">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="09c53-121">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="09c53-122">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="09c53-122">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="09c53-123">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="09c53-123">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="09c53-124">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="09c53-124">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="09c53-125">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="09c53-125">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="09c53-126">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="09c53-126">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="09c53-127">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="09c53-127">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="09c53-128">Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="09c53-128">Update Bounds and ZoomFactor properties at the same time.</span></span>
[<span data-ttu-id="09c53-129">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-129">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="09c53-130">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-130">Move focus into WebView.</span></span>
[<span data-ttu-id="09c53-131">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="09c53-131">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="09c53-132">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="09c53-132">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="09c53-133">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="09c53-133">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="09c53-134">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="09c53-134">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="09c53-135">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-135">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="09c53-136">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-136">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="09c53-137">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-137">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="09c53-138">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-138">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="09c53-139">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-139">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="09c53-140">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-140">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="09c53-141">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-141">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="09c53-142">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-142">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="09c53-143">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="09c53-143">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="09c53-144">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="09c53-144">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="09c53-145">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="09c53-145">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="09c53-146">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="09c53-146">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="09c53-147">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="09c53-147">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="09c53-148">La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.</span><span class="sxs-lookup"><span data-stu-id="09c53-148">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="09c53-149">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="09c53-149">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="09c53-150">Establezca la ventana principal de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-150">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="09c53-151">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="09c53-151">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="09c53-152">Esta es una notificación independiente de put_Bounds que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).</span><span class="sxs-lookup"><span data-stu-id="09c53-152">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="09c53-153">Cerrar</span><span class="sxs-lookup"><span data-stu-id="09c53-153">Close</span></span>](#close) | <span data-ttu-id="09c53-154">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="09c53-154">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="09c53-155">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="09c53-155">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="09c53-156">Obtiene el CoreWebView2 asociado a este CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="09c53-156">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>
[<span data-ttu-id="09c53-157">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="09c53-157">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#core_webview2_move_focus_reason) | <span data-ttu-id="09c53-158">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="09c53-158">Reason for moving focus.</span></span>
[<span data-ttu-id="09c53-159">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="09c53-159">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span>](#core_webview2_key_event_kind) | <span data-ttu-id="09c53-160">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="09c53-160">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="09c53-161">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="09c53-161">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#core_webview2_physical_key_status) | <span data-ttu-id="09c53-162">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="09c53-162">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="09c53-163">El CoreWebView2Host es propietario de la CoreWebView2 y, si todas las referencias a CoreWebView2Host desaparecen, se cerrará la WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-163">The CoreWebView2Host owns the CoreWebView2, and if all references to the CoreWebView2Host go away, the WebView will be closed.</span></span>

## <span data-ttu-id="09c53-164">Miembros</span><span class="sxs-lookup"><span data-stu-id="09c53-164">Members</span></span>

#### <span data-ttu-id="09c53-165">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="09c53-165">get_IsVisible</span></span> 

<span data-ttu-id="09c53-166">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-166">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="09c53-167">HRESULT público [get_IsVisible](#get_isvisible)(bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="09c53-167">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="09c53-168">Si IsVisible se establece en false, WebView será transparente y no se representará.</span><span class="sxs-lookup"><span data-stu-id="09c53-168">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="09c53-169">Sin embargo, esto no afectará a la ventana que contenga la vista de contenido (el parámetro HWND pasado a CreateCoreWebView2Host).</span><span class="sxs-lookup"><span data-stu-id="09c53-169">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Host).</span></span> <span data-ttu-id="09c53-170">Si desea que esta ventana desaparezca también, llame a ShowWindow directamente, además de modificar la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="09c53-170">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="09c53-171">Si la ventana superior está minimizada o restaurada, WebView no recibirá mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="09c53-171">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="09c53-172">Por motivos de rendimiento, desarrollador debe establecer el valor de la propiedad IsVisible de la WebView en falso cuando la ventana de la aplicación está minimizada y volver a ser true cuando se restaura la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09c53-172">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="09c53-173">La ventana de la aplicación puede hacerlo controlando SC_MINIMIZE y SC_RESTORE comando al recibir WM_SYSCOMMAND mensaje.</span><span class="sxs-lookup"><span data-stu-id="09c53-173">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="09c53-174">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="09c53-174">put_IsVisible</span></span> 

<span data-ttu-id="09c53-175">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="09c53-175">Set the IsVisible property.</span></span>

> <span data-ttu-id="09c53-176">[put_IsVisible](#put_isvisible)de HRESULT público (bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="09c53-176">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_host->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_host->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="09c53-177">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="09c53-177">get_Bounds</span></span> 

<span data-ttu-id="09c53-178">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="09c53-178">The webview bounds.</span></span>

> <span data-ttu-id="09c53-179">[get_Boundss](#get_bounds)HRESULT públicos (límites Rect \*)</span><span class="sxs-lookup"><span data-stu-id="09c53-179">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="09c53-180">Los límites son relativos al identificador HWND primario.</span><span class="sxs-lookup"><span data-stu-id="09c53-180">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="09c53-181">La aplicación tiene dos formas en las que puede ubicar una vista en WebView:</span><span class="sxs-lookup"><span data-stu-id="09c53-181">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="09c53-182">Cree un HWND secundario que sea el objeto HWND de la vista < View.</span><span class="sxs-lookup"><span data-stu-id="09c53-182">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="09c53-183">Coloque esta ventana donde debería estar la vista en la vista.</span><span class="sxs-lookup"><span data-stu-id="09c53-183">Position this window where the WebView should be.</span></span> <span data-ttu-id="09c53-184">En este caso, use (0,0) para la Bound's esquina superior izquierda de la vista de vista previa (el desplazamiento).</span><span class="sxs-lookup"><span data-stu-id="09c53-184">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="09c53-185">Use la última ventana de la aplicación como el HWND primario de WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-185">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="09c53-186">Establezca la Bound's esquina superior izquierda de la vista previa para que la vista de la vista en la aplicación se coloque correctamente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09c53-186">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="09c53-187">Los valores de la entrada enlazada están en el espacio de coordenadas del host.</span><span class="sxs-lookup"><span data-stu-id="09c53-187">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="09c53-188">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="09c53-188">put_Bounds</span></span> 

<span data-ttu-id="09c53-189">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="09c53-189">Set the Bounds property.</span></span>

> <span data-ttu-id="09c53-190">[put_Bounds](#put_bounds)de HRESULT público (límites Rect)</span><span class="sxs-lookup"><span data-stu-id="09c53-190">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

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

    m_host->put_Bounds(desiredBounds);
}
```

#### <span data-ttu-id="09c53-191">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="09c53-191">get_ZoomFactor</span></span> 

<span data-ttu-id="09c53-192">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-192">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="09c53-193">[get_ZoomFactor](#get_zoomfactor)de HRESULT público (Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="09c53-193">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="09c53-194">Ten en cuenta que cambiar el factor de zoom podría provocar un `window.innerWidth/innerHeight` cambio en el diseño de página.</span><span class="sxs-lookup"><span data-stu-id="09c53-194">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="09c53-195">Un factor de zoom aplicado por el host mediante una llamada a put_ZoomFactor se convierte en el nuevo zoom predeterminado para la vista de la vista.</span><span class="sxs-lookup"><span data-stu-id="09c53-195">A zoom factor that is applied by the host by calling put_ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="09c53-196">Este factor de zoom se aplica en la navegación y se vuelve al factor de zoom en la vista previa cuando el usuario presiona Ctrl + 0.</span><span class="sxs-lookup"><span data-stu-id="09c53-196">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="09c53-197">Cuando el usuario cambia el factor de zoom (es decir, la aplicación que recibe la ZoomFactorChanged), ese zoom solo se aplica a la página actual.</span><span class="sxs-lookup"><span data-stu-id="09c53-197">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="09c53-198">Cualquier zoom aplicado a un usuario solo es para la página actual y se restablece en una navegación.</span><span class="sxs-lookup"><span data-stu-id="09c53-198">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="09c53-199">No se permite especificar un zoomFactor menor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="09c53-199">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="09c53-200">WebView también tiene un intervalo de factor de zoom compatible interno.</span><span class="sxs-lookup"><span data-stu-id="09c53-200">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="09c53-201">Cuando un factor de zoom especificado está fuera de ese rango, se normalizará para que esté dentro del rango y se desencadenará un evento ZoomFactorChanged para el factor de zoom aplicado real.</span><span class="sxs-lookup"><span data-stu-id="09c53-201">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="09c53-202">Cuando se produzca esta normalización de rango, la propiedad ZoomFactor informará sobre el factor de zoom especificado durante la modificación anterior de la propiedad ZoomFactor hasta que se reciba el evento ZoomFactorChanged después de que la vista previa aplique el factor de zoom normalizado.</span><span class="sxs-lookup"><span data-stu-id="09c53-202">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="09c53-203">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="09c53-203">put_ZoomFactor</span></span> 

<span data-ttu-id="09c53-204">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="09c53-204">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="09c53-205">[put_ZoomFactor](#put_zoomfactor)de HRESULT público (Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="09c53-205">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="09c53-206">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="09c53-206">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="09c53-207">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="09c53-207">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="09c53-208">[add_ZoomFactorChanged](#add_zoomfactorchanged)de HRESULT público ([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="09c53-208">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="09c53-209">El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="09c53-209">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="09c53-210">El evento se podría activar porque el autor de la llamada modificó la propiedad ZoomFactor o debido a que el usuario modificaba manualmente el zoom.</span><span class="sxs-lookup"><span data-stu-id="09c53-210">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="09c53-211">Cuando el autor de la llamada lo modifica a través de la propiedad ZoomFactor, el factor de zoom interno se actualiza inmediatamente y no se producirá ningún evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="09c53-211">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="09c53-212">La vista Web asocia el último factor de zoom usado para cada sitio.</span><span class="sxs-lookup"><span data-stu-id="09c53-212">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="09c53-213">Por lo tanto, es posible que el factor de zoom cambie al navegar a una página diferente.</span><span class="sxs-lookup"><span data-stu-id="09c53-213">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="09c53-214">Cuando el factor de zoom cambia debido a esto, el evento ZoomFactorChanged se activa justo después del evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="09c53-214">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_host->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Host* sender, IUnknown* args) -> HRESULT {
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

#### <span data-ttu-id="09c53-215">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="09c53-215">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="09c53-216">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="09c53-216">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="09c53-217">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="09c53-217">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="09c53-218">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="09c53-218">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="09c53-219">Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="09c53-219">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="09c53-220">HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(rectángulos de rectángulo, doble zoomFactor)</span><span class="sxs-lookup"><span data-stu-id="09c53-220">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds,double zoomFactor)</span></span>

<span data-ttu-id="09c53-221">Esta operación es atómica desde la de las características del anfitrión.</span><span class="sxs-lookup"><span data-stu-id="09c53-221">This operation is atomic from the host's perspecive.</span></span> <span data-ttu-id="09c53-222">Después de volver de esta función, las propiedades Bounds y ZoomFactor se actualizarán si la función se realiza correctamente, o no se actualizará si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="09c53-222">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="09c53-223">Si los límites y ZoomFactor se actualizan con la misma escala (es decir, los límites y ZoomFactor están duplicados), la página no verá un cambio en la ventana. innerWidth/innerHeight y la WebView representará el contenido en el nuevo tamaño y zoom sin representaciones intermedias.</span><span class="sxs-lookup"><span data-stu-id="09c53-223">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="09c53-224">Esta función también se puede usar para actualizar solo una de ZoomFactor o límites pasando el nuevo valor para uno y el valor actual para el otro.</span><span class="sxs-lookup"><span data-stu-id="09c53-224">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_host->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_host->SetBoundsAndZoomFactor(bounds, scale);
}
```

#### <span data-ttu-id="09c53-225">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-225">MoveFocus</span></span> 

<span data-ttu-id="09c53-226">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-226">Move focus into WebView.</span></span>

> <span data-ttu-id="09c53-227">[MOVEFOCUS](#movefocus)HRESULT público (razón[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) )</span><span class="sxs-lookup"><span data-stu-id="09c53-227">public HRESULT [MoveFocus](#movefocus)([CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="09c53-228">La vista web obtendrá el foco y el foco se establecerá en el elemento de corresponsal de la página hospedada en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="09c53-228">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="09c53-229">Por motivos de programación, el foco se establece en elemento con enfoque anterior o en el elemento predeterminado si no hay ningún elemento con el foco anterior.</span><span class="sxs-lookup"><span data-stu-id="09c53-229">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="09c53-230">Por el siguiente motivo, el foco se establece en el primer elemento.</span><span class="sxs-lookup"><span data-stu-id="09c53-230">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="09c53-231">Por el motivo anterior, el foco se establece en el último elemento.</span><span class="sxs-lookup"><span data-stu-id="09c53-231">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="09c53-232">WebView también puede obtener el foco a través de la interacción del usuario, como hacer clic en la vista previa o en la pestaña en la misma.</span><span class="sxs-lookup"><span data-stu-id="09c53-232">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="09c53-233">Para la tabulación, la aplicación puede llamar a MoveFocus con la función siguiente o anterior para alinear con la tabulación y Mayús + Tab, respectivamente al decidir la vista previa del elemento tabulador.</span><span class="sxs-lookup"><span data-stu-id="09c53-233">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="09c53-234">O bien, la aplicación puede llamar a IsDialogMessage como parte de su bucle de mensajes para permitir que la plataforma maneje automáticamente la tabulación.</span><span class="sxs-lookup"><span data-stu-id="09c53-234">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="09c53-235">La plataforma girará en todas las ventanas con WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="09c53-235">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="09c53-236">Cuando la vista de la vista de la vista de IsDialogMessage, coloca internamente el foco en el primer o el último elemento de Tab y Mayús + Tab, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="09c53-236">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

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
            for (int i = 0; i < m_tabbableWindows.size(); i++)
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
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
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
    CHECK_FAILURE(m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="09c53-237">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="09c53-237">add_MoveFocusRequested</span></span> 

<span data-ttu-id="09c53-238">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="09c53-238">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="09c53-239">[add_MoveFocusRequested](#add_movefocusrequested)de HRESULT público ([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="09c53-239">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="09c53-240">MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista.</span><span class="sxs-lookup"><span data-stu-id="09c53-240">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="09c53-241">El foco de la vista de WebView no ha cambiado cuando se desencadena este evento.</span><span class="sxs-lookup"><span data-stu-id="09c53-241">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_host->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    CORE_WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
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

#### <span data-ttu-id="09c53-242">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="09c53-242">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="09c53-243">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="09c53-243">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="09c53-244">[remove_MoveFocusRequested](#remove_movefocusrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="09c53-244">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="09c53-245">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-245">add_GotFocus</span></span> 

<span data-ttu-id="09c53-246">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-246">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="09c53-247">[add_GotFocus](#add_gotfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="09c53-247">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="09c53-248">GotFocus se desencadena cuando WebView tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="09c53-248">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="09c53-249">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-249">remove_GotFocus</span></span> 

<span data-ttu-id="09c53-250">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-250">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="09c53-251">[remove_GotFocus](#remove_gotfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="09c53-251">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="09c53-252">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-252">add_LostFocus</span></span> 

<span data-ttu-id="09c53-253">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-253">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="09c53-254">[add_LostFocus](#add_lostfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="09c53-254">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="09c53-255">LostFocus se desencadena cuando WebView pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="09c53-255">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="09c53-256">En caso de que se inicie el evento MoveFocusRequested, el foco seguirá en la vista previa cuando se desencadene el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="09c53-256">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="09c53-257">Perder el foco solo se activa cuando el código de la aplicación o la acción predeterminada del evento MoveFocusRequested está lejos de WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-257">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="09c53-258">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="09c53-258">remove_LostFocus</span></span> 

<span data-ttu-id="09c53-259">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="09c53-259">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="09c53-260">[remove_LostFocus](#remove_lostfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="09c53-260">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="09c53-261">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="09c53-261">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="09c53-262">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="09c53-262">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="09c53-263">[add_AcceleratorKeyPressed](#add_acceleratorkeypressed)de HRESULT público ([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="09c53-263">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="09c53-264">AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa.</span><span class="sxs-lookup"><span data-stu-id="09c53-264">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="09c53-265">Una clave se considera un acelerador si:</span><span class="sxs-lookup"><span data-stu-id="09c53-265">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="09c53-266">La tecla Ctrl o Alt se está retenida actualmente, o bien</span><span class="sxs-lookup"><span data-stu-id="09c53-266">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="09c53-267">la tecla presionada no se asigna a un carácter.</span><span class="sxs-lookup"><span data-stu-id="09c53-267">the pressed key does not map to a character.</span></span> <span data-ttu-id="09c53-268">Algunas teclas específicas nunca se consideran aceleradores, como Mayús.</span><span class="sxs-lookup"><span data-stu-id="09c53-268">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="09c53-269">La tecla de escape se considera siempre un acelerador.</span><span class="sxs-lookup"><span data-stu-id="09c53-269">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="09c53-270">Los eventos de teclas autorepetidos que se provocan al mantener presionada la tecla también desencadenan este evento.</span><span class="sxs-lookup"><span data-stu-id="09c53-270">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="09c53-271">Puedes filtrarlos comprobando los argumentos del evento ' KeyEventLParam o PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="09c53-271">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="09c53-272">En el modo de ventana, se llama a este controlador de eventos de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="09c53-272">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="09c53-273">Hasta que llames al controlador () en los argumentos del evento o se devuelva el controlador de eventos, el proceso del explorador se bloqueará y las llamadas COM salientes entre procesos generarán un error con RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="09c53-273">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="09c53-274">Sin embargo, todos los métodos de la API de CoreWebView2 funcionarán.</span><span class="sxs-lookup"><span data-stu-id="09c53-274">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="09c53-275">En el modo sin ventana, se llama al controlador de eventos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="09c53-275">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="09c53-276">La entrada de datos adicionales no llegará al explorador hasta que el controlador de eventos devuelva o se llame a (), pero el proceso del explorador en sí no se bloqueará y las llamadas COM salientes funcionarán normalmente.</span><span class="sxs-lookup"><span data-stu-id="09c53-276">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="09c53-277">Se recomienda que llame al controlador (TRUE) tan pronto como sepa que desea controlar la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="09c53-277">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_host->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                CORE_WEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
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
                        CORE_WEBVIEW2_PHYSICAL_KEY_STATUS status;
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

#### <span data-ttu-id="09c53-278">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="09c53-278">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="09c53-279">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="09c53-279">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="09c53-280">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="09c53-280">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="09c53-281">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="09c53-281">get_ParentWindow</span></span> 

<span data-ttu-id="09c53-282">La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.</span><span class="sxs-lookup"><span data-stu-id="09c53-282">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="09c53-283">[get_ParentWindow](#get_parentwindow)de HRESULT público (HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="09c53-283">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="09c53-284">Esta API inicialmente devuelve la ventana que se pasó a CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="09c53-284">This API initially returns the window passed into CreateCoreWebView2Host.</span></span>

#### <span data-ttu-id="09c53-285">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="09c53-285">put_ParentWindow</span></span> 

<span data-ttu-id="09c53-286">Establezca la ventana principal de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-286">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="09c53-287">[put_ParentWindow](#put_parentwindow)de HRESULT público (HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="09c53-287">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="09c53-288">Esto hará que la vista de ventana reorigen su ventana a la ventana recién suministrada.</span><span class="sxs-lookup"><span data-stu-id="09c53-288">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="09c53-289">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="09c53-289">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="09c53-290">Esta es una notificación independiente de put_Bounds que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).</span><span class="sxs-lookup"><span data-stu-id="09c53-290">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="09c53-291">[NOTIFYPARENTWINDOWPOSITIONCHANGED](#notifyparentwindowpositionchanged)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="09c53-291">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="09c53-292">Esto es necesario para que la accesibilidad y determinados cuadros de diálogo de WebView funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="09c53-292">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="09c53-293">Cerrar</span><span class="sxs-lookup"><span data-stu-id="09c53-293">Close</span></span> 

<span data-ttu-id="09c53-294">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="09c53-294">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="09c53-295">HRESULT público [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="09c53-295">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="09c53-296">Si limpias el explorador instace, se liberarán los recursos que encienden la vista Web.</span><span class="sxs-lookup"><span data-stu-id="09c53-296">Cleaning up the browser instace will release the resources powering the WebView.</span></span> <span data-ttu-id="09c53-297">La instancia del explorador se cerrará si no hay ninguna otra vista previa con ella.</span><span class="sxs-lookup"><span data-stu-id="09c53-297">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="09c53-298">Después de llamar a Close, todas las llamadas a métodos producirán errores y los controladores de eventos dejarán de activarse.</span><span class="sxs-lookup"><span data-stu-id="09c53-298">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="09c53-299">Específicamente, la WebView liberará sus referencias a los controladores de eventos cuando se llama a Close.</span><span class="sxs-lookup"><span data-stu-id="09c53-299">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="09c53-300">Close se llama de forma implícita cuando CoreWebView2Host pierde su referencia final y se destruye.</span><span class="sxs-lookup"><span data-stu-id="09c53-300">Close is implicitly called when the CoreWebView2Host loses its final reference and is destructed.</span></span> <span data-ttu-id="09c53-301">Sin embargo, se recomienda llamar de forma explícita a Close para evitar cualquier ciclo de referencias entre la vista de WebView y el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09c53-301">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="09c53-302">En concreto, si capturas una referencia a la vista de la vista en un controlador de eventos, crearás un ciclo de referencia entre la vista en WebView y el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="09c53-302">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="09c53-303">Al llamar a Close se interrumpirá este ciclo liberando todos los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="09c53-303">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="09c53-304">Pero para evitar esta situación, lo mejor es llamar explícitamente a Close en WebView y no capturar una referencia a WebView para asegurarte de que la WebView pueda limpiarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="09c53-304">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_host)
    {
        m_host->Close();
        m_host = nullptr;
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
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2.idl#createwebview2environmentwithdetails
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instnaces.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="09c53-305">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="09c53-305">get_CoreWebView2</span></span> 

<span data-ttu-id="09c53-306">Obtiene el CoreWebView2 asociado a este CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="09c53-306">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>

> <span data-ttu-id="09c53-307">[get_CoreWebView2](#get_corewebview2)(HRESULT) público ([ICoreWebView2](ICoreWebView2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="09c53-307">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="09c53-308">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="09c53-308">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="09c53-309">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="09c53-309">Reason for moving focus.</span></span>

> <span data-ttu-id="09c53-310">[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) enum</span><span class="sxs-lookup"><span data-stu-id="09c53-310">enum [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)</span></span>

 <span data-ttu-id="09c53-311">Los</span><span class="sxs-lookup"><span data-stu-id="09c53-311">Values</span></span>                         | <span data-ttu-id="09c53-312">Descripciones</span><span class="sxs-lookup"><span data-stu-id="09c53-312">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="09c53-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="09c53-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="09c53-314">El ajuste del foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="09c53-314">Code setting focus into WebView.</span></span>
<span data-ttu-id="09c53-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="09c53-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="09c53-316">Moviendo el foco debido a una resaltado de pestañas hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="09c53-316">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="09c53-317">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="09c53-317">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="09c53-318">Moviendo el foco debido a un recorrido de tabulación hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="09c53-318">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="09c53-319">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="09c53-319">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="09c53-320">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="09c53-320">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="09c53-321">[CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="09c53-321">enum [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)</span></span>

 <span data-ttu-id="09c53-322">Los</span><span class="sxs-lookup"><span data-stu-id="09c53-322">Values</span></span>                         | <span data-ttu-id="09c53-323">Descripciones</span><span class="sxs-lookup"><span data-stu-id="09c53-323">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="09c53-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="09c53-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="09c53-325">Corresponde a WM_KEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="09c53-325">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="09c53-326">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="09c53-326">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="09c53-327">Corresponde a WM_KEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="09c53-327">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="09c53-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="09c53-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="09c53-329">Corresponde a WM_SYSKEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="09c53-329">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="09c53-330">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="09c53-330">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="09c53-331">Corresponde a WM_SYSKEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="09c53-331">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="09c53-332">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="09c53-332">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="09c53-333">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="09c53-333">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="09c53-334">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="09c53-334">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span></span>

<span data-ttu-id="09c53-335">Para obtener más información, consulte la documentación de WM_KEYDOWN en[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="09c53-335">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

