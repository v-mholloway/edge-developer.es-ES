---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Host
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 39566c867c28739d21dd99c369d161d29a308946
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885621"
---
# <span data-ttu-id="ae014-104">0.9.430: ICoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="ae014-104">0.9.430 - interface ICoreWebView2Host</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Host
  : public IUnknown
```

<span data-ttu-id="ae014-105">Esta interfaz es el propietario del objeto CoreWebView2 y proporciona compatibilidad para cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.</span><span class="sxs-lookup"><span data-stu-id="ae014-105">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="ae014-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ae014-106">Summary</span></span>

 <span data-ttu-id="ae014-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae014-107">Members</span></span>                        | <span data-ttu-id="ae014-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ae014-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ae014-109">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="ae014-109">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="ae014-110">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-110">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="ae014-111">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="ae014-111">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="ae014-112">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="ae014-112">Set the IsVisible property.</span></span>
[<span data-ttu-id="ae014-113">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="ae014-113">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="ae014-114">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="ae014-114">The webview bounds.</span></span>
[<span data-ttu-id="ae014-115">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="ae014-115">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="ae014-116">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="ae014-116">Set the Bounds property.</span></span>
[<span data-ttu-id="ae014-117">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ae014-117">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="ae014-118">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-118">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="ae014-119">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ae014-119">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="ae014-120">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="ae014-120">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="ae014-121">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="ae014-121">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="ae014-122">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="ae014-122">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="ae014-123">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="ae014-123">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="ae014-124">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="ae014-124">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="ae014-125">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ae014-125">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="ae014-126">Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ae014-126">Update Bounds and ZoomFactor properties at the same time.</span></span>
[<span data-ttu-id="ae014-127">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-127">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="ae014-128">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-128">Move focus into WebView.</span></span>
[<span data-ttu-id="ae014-129">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="ae014-129">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="ae014-130">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="ae014-130">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="ae014-131">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="ae014-131">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="ae014-132">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="ae014-132">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="ae014-133">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-133">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="ae014-134">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-134">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="ae014-135">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-135">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="ae014-136">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-136">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="ae014-137">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-137">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="ae014-138">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-138">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="ae014-139">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-139">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="ae014-140">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-140">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="ae014-141">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="ae014-141">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="ae014-142">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ae014-142">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="ae014-143">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="ae014-143">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="ae014-144">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ae014-144">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="ae014-145">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="ae014-145">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="ae014-146">La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.</span><span class="sxs-lookup"><span data-stu-id="ae014-146">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="ae014-147">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="ae014-147">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="ae014-148">Establezca la ventana principal de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-148">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="ae014-149">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="ae014-149">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="ae014-150">Esta es una notificación independiente de put_Bounds que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).</span><span class="sxs-lookup"><span data-stu-id="ae014-150">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="ae014-151">Cerrar</span><span class="sxs-lookup"><span data-stu-id="ae014-151">Close</span></span>](#close) | <span data-ttu-id="ae014-152">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="ae014-152">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="ae014-153">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="ae014-153">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="ae014-154">Obtiene el CoreWebView2 asociado a este CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="ae014-154">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>
[<span data-ttu-id="ae014-155">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="ae014-155">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#core_webview2_move_focus_reason) | <span data-ttu-id="ae014-156">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="ae014-156">Reason for moving focus.</span></span>
[<span data-ttu-id="ae014-157">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="ae014-157">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span>](#core_webview2_key_event_kind) | <span data-ttu-id="ae014-158">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ae014-158">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="ae014-159">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="ae014-159">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#core_webview2_physical_key_status) | <span data-ttu-id="ae014-160">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="ae014-160">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="ae014-161">El CoreWebView2Host es propietario de la CoreWebView2 y, si todas las referencias a CoreWebView2Host desaparecen, se cerrará la WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-161">The CoreWebView2Host owns the CoreWebView2, and if all references to the CoreWebView2Host go away, the WebView will be closed.</span></span>

## <span data-ttu-id="ae014-162">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae014-162">Members</span></span>

#### <span data-ttu-id="ae014-163">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="ae014-163">get_IsVisible</span></span> 

<span data-ttu-id="ae014-164">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-164">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="ae014-165">HRESULT público [get_IsVisible](#get_isvisible)(bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="ae014-165">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="ae014-166">Si IsVisible se establece en false, WebView será transparente y no se representará.</span><span class="sxs-lookup"><span data-stu-id="ae014-166">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="ae014-167">Sin embargo, esto no afectará a la ventana que contenga la vista de contenido (el parámetro HWND pasado a CreateCoreWebView2Host).</span><span class="sxs-lookup"><span data-stu-id="ae014-167">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Host).</span></span> <span data-ttu-id="ae014-168">Si desea que esta ventana desaparezca también, llame a ShowWindow directamente, además de modificar la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="ae014-168">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="ae014-169">Si la ventana superior está minimizada o restaurada, WebView no recibirá mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="ae014-169">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="ae014-170">Por motivos de rendimiento, desarrollador debe establecer el valor de la propiedad IsVisible de la WebView en falso cuando la ventana de la aplicación está minimizada y volver a ser true cuando se restaura la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae014-170">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="ae014-171">La ventana de la aplicación puede hacerlo controlando SC_MINIMIZE y SC_RESTORE comando al recibir WM_SYSCOMMAND mensaje.</span><span class="sxs-lookup"><span data-stu-id="ae014-171">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="ae014-172">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="ae014-172">put_IsVisible</span></span> 

<span data-ttu-id="ae014-173">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="ae014-173">Set the IsVisible property.</span></span>

> <span data-ttu-id="ae014-174">[put_IsVisible](#put_isvisible)de HRESULT público (bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="ae014-174">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

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

#### <span data-ttu-id="ae014-175">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="ae014-175">get_Bounds</span></span> 

<span data-ttu-id="ae014-176">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="ae014-176">The webview bounds.</span></span>

> <span data-ttu-id="ae014-177">[get_Boundss](#get_bounds)HRESULT públicos (límites Rect \*)</span><span class="sxs-lookup"><span data-stu-id="ae014-177">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="ae014-178">Los límites son relativos al identificador HWND primario.</span><span class="sxs-lookup"><span data-stu-id="ae014-178">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="ae014-179">La aplicación tiene dos formas en las que puede ubicar una vista en WebView:</span><span class="sxs-lookup"><span data-stu-id="ae014-179">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="ae014-180">Cree un HWND secundario que sea el objeto HWND de la vista < View.</span><span class="sxs-lookup"><span data-stu-id="ae014-180">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="ae014-181">Coloque esta ventana donde debería estar la vista en la vista.</span><span class="sxs-lookup"><span data-stu-id="ae014-181">Position this window where the WebView should be.</span></span> <span data-ttu-id="ae014-182">En este caso, use (0,0) para la Bound's esquina superior izquierda de la vista de vista previa (el desplazamiento).</span><span class="sxs-lookup"><span data-stu-id="ae014-182">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="ae014-183">Use la última ventana de la aplicación como el HWND primario de WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-183">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="ae014-184">Establezca la Bound's esquina superior izquierda de la vista previa para que la vista de la vista en la aplicación se coloque correctamente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae014-184">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="ae014-185">Los valores de la entrada enlazada están en el espacio de coordenadas del host.</span><span class="sxs-lookup"><span data-stu-id="ae014-185">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="ae014-186">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="ae014-186">put_Bounds</span></span> 

<span data-ttu-id="ae014-187">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="ae014-187">Set the Bounds property.</span></span>

> <span data-ttu-id="ae014-188">[put_Bounds](#put_bounds)de HRESULT público (límites Rect)</span><span class="sxs-lookup"><span data-stu-id="ae014-188">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

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

#### <span data-ttu-id="ae014-189">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ae014-189">get_ZoomFactor</span></span> 

<span data-ttu-id="ae014-190">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-190">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="ae014-191">[get_ZoomFactor](#get_zoomfactor)de HRESULT público (Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="ae014-191">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="ae014-192">Ten en cuenta que cambiar el factor de zoom podría provocar un `window.innerWidth/innerHeight` cambio en el diseño de página.</span><span class="sxs-lookup"><span data-stu-id="ae014-192">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="ae014-193">Un factor de zoom aplicado por el host mediante una llamada a put_ZoomFactor se convierte en el nuevo zoom predeterminado para la vista de la vista.</span><span class="sxs-lookup"><span data-stu-id="ae014-193">A zoom factor that is applied by the host by calling put_ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="ae014-194">Este factor de zoom se aplica en la navegación y se vuelve al factor de zoom en la vista previa cuando el usuario presiona Ctrl + 0.</span><span class="sxs-lookup"><span data-stu-id="ae014-194">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="ae014-195">Cuando el usuario cambia el factor de zoom (es decir, la aplicación que recibe la ZoomFactorChanged), ese zoom solo se aplica a la página actual.</span><span class="sxs-lookup"><span data-stu-id="ae014-195">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="ae014-196">Cualquier zoom aplicado a un usuario solo es para la página actual y se restablece en una navegación.</span><span class="sxs-lookup"><span data-stu-id="ae014-196">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="ae014-197">No se permite especificar un zoomFactor menor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="ae014-197">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="ae014-198">WebView también tiene un intervalo de factor de zoom compatible interno.</span><span class="sxs-lookup"><span data-stu-id="ae014-198">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="ae014-199">Cuando un factor de zoom especificado está fuera de ese rango, se normalizará para que esté dentro del rango y se desencadenará un evento ZoomFactorChanged para el factor de zoom aplicado real.</span><span class="sxs-lookup"><span data-stu-id="ae014-199">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="ae014-200">Cuando se produzca esta normalización de rango, la propiedad ZoomFactor informará sobre el factor de zoom especificado durante la modificación anterior de la propiedad ZoomFactor hasta que se reciba el evento ZoomFactorChanged después de que la vista previa aplique el factor de zoom normalizado.</span><span class="sxs-lookup"><span data-stu-id="ae014-200">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="ae014-201">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ae014-201">put_ZoomFactor</span></span> 

<span data-ttu-id="ae014-202">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="ae014-202">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="ae014-203">[put_ZoomFactor](#put_zoomfactor)de HRESULT público (Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="ae014-203">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="ae014-204">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="ae014-204">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="ae014-205">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="ae014-205">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="ae014-206">[add_ZoomFactorChanged](#add_zoomfactorchanged)de HRESULT público ([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="ae014-206">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="ae014-207">El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="ae014-207">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="ae014-208">El evento se podría activar porque el autor de la llamada modificó la propiedad ZoomFactor o debido a que el usuario modificaba manualmente el zoom.</span><span class="sxs-lookup"><span data-stu-id="ae014-208">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="ae014-209">Cuando el autor de la llamada lo modifica a través de la propiedad ZoomFactor, el factor de zoom interno se actualiza inmediatamente y no se producirá ningún evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="ae014-209">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="ae014-210">La vista Web asocia el último factor de zoom usado para cada sitio.</span><span class="sxs-lookup"><span data-stu-id="ae014-210">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="ae014-211">Por lo tanto, es posible que el factor de zoom cambie al navegar a una página diferente.</span><span class="sxs-lookup"><span data-stu-id="ae014-211">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="ae014-212">Cuando el factor de zoom cambia debido a esto, el evento ZoomFactorChanged se activa justo después del evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="ae014-212">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

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

#### <span data-ttu-id="ae014-213">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="ae014-213">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="ae014-214">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="ae014-214">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="ae014-215">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="ae014-215">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="ae014-216">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ae014-216">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="ae014-217">Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ae014-217">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="ae014-218">HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(rectángulos de rectángulo, doble zoomFactor)</span><span class="sxs-lookup"><span data-stu-id="ae014-218">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds,double zoomFactor)</span></span>

<span data-ttu-id="ae014-219">Esta operación es atómica desde la de las características del anfitrión.</span><span class="sxs-lookup"><span data-stu-id="ae014-219">This operation is atomic from the host's perspecive.</span></span> <span data-ttu-id="ae014-220">Después de volver de esta función, las propiedades Bounds y ZoomFactor se actualizarán si la función se realiza correctamente, o no se actualizará si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="ae014-220">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="ae014-221">Si los límites y ZoomFactor se actualizan con la misma escala (es decir, los límites y ZoomFactor están duplicados), la página no verá un cambio en la ventana. innerWidth/innerHeight y la WebView representará el contenido en el nuevo tamaño y zoom sin representaciones intermedias.</span><span class="sxs-lookup"><span data-stu-id="ae014-221">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="ae014-222">Esta función también se puede usar para actualizar solo una de ZoomFactor o límites pasando el nuevo valor para uno y el valor actual para el otro.</span><span class="sxs-lookup"><span data-stu-id="ae014-222">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

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

#### <span data-ttu-id="ae014-223">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-223">MoveFocus</span></span> 

<span data-ttu-id="ae014-224">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-224">Move focus into WebView.</span></span>

> <span data-ttu-id="ae014-225">[MOVEFOCUS](#movefocus)HRESULT público (razón[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) )</span><span class="sxs-lookup"><span data-stu-id="ae014-225">public HRESULT [MoveFocus](#movefocus)([CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="ae014-226">La vista web obtendrá el foco y el foco se establecerá en el elemento de corresponsal de la página hospedada en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="ae014-226">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="ae014-227">Por motivos de programación, el foco se establece en elemento con enfoque anterior o en el elemento predeterminado si no hay ningún elemento con el foco anterior.</span><span class="sxs-lookup"><span data-stu-id="ae014-227">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="ae014-228">Por el siguiente motivo, el foco se establece en el primer elemento.</span><span class="sxs-lookup"><span data-stu-id="ae014-228">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="ae014-229">Por el motivo anterior, el foco se establece en el último elemento.</span><span class="sxs-lookup"><span data-stu-id="ae014-229">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="ae014-230">WebView también puede obtener el foco a través de la interacción del usuario, como hacer clic en la vista previa o en la pestaña en la misma.</span><span class="sxs-lookup"><span data-stu-id="ae014-230">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="ae014-231">Para la tabulación, la aplicación puede llamar a MoveFocus con la función siguiente o anterior para alinear con la tabulación y Mayús + Tab, respectivamente al decidir la vista previa del elemento tabulador.</span><span class="sxs-lookup"><span data-stu-id="ae014-231">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="ae014-232">O bien, la aplicación puede llamar a IsDialogMessage como parte de su bucle de mensajes para permitir que la plataforma maneje automáticamente la tabulación.</span><span class="sxs-lookup"><span data-stu-id="ae014-232">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="ae014-233">La plataforma girará en todas las ventanas con WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="ae014-233">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="ae014-234">Cuando la vista de la vista de la vista de IsDialogMessage, coloca internamente el foco en el primer o el último elemento de Tab y Mayús + Tab, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ae014-234">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

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

#### <span data-ttu-id="ae014-235">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="ae014-235">add_MoveFocusRequested</span></span> 

<span data-ttu-id="ae014-236">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="ae014-236">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="ae014-237">[add_MoveFocusRequested](#add_movefocusrequested)de HRESULT público ([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="ae014-237">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="ae014-238">MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista.</span><span class="sxs-lookup"><span data-stu-id="ae014-238">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="ae014-239">El foco de la vista de WebView no ha cambiado cuando se desencadena este evento.</span><span class="sxs-lookup"><span data-stu-id="ae014-239">The WebView's focus has not changed when this event is fired.</span></span>

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

#### <span data-ttu-id="ae014-240">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="ae014-240">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="ae014-241">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="ae014-241">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="ae014-242">[remove_MoveFocusRequested](#remove_movefocusrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="ae014-242">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="ae014-243">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-243">add_GotFocus</span></span> 

<span data-ttu-id="ae014-244">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-244">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="ae014-245">[add_GotFocus](#add_gotfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="ae014-245">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="ae014-246">GotFocus se desencadena cuando WebView tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="ae014-246">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="ae014-247">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-247">remove_GotFocus</span></span> 

<span data-ttu-id="ae014-248">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-248">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="ae014-249">[remove_GotFocus](#remove_gotfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="ae014-249">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="ae014-250">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-250">add_LostFocus</span></span> 

<span data-ttu-id="ae014-251">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-251">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="ae014-252">[add_LostFocus](#add_lostfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="ae014-252">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="ae014-253">LostFocus se desencadena cuando WebView pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="ae014-253">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="ae014-254">En caso de que se inicie el evento MoveFocusRequested, el foco seguirá en la vista previa cuando se desencadene el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="ae014-254">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="ae014-255">Perder el foco solo se activa cuando el código de la aplicación o la acción predeterminada del evento MoveFocusRequested está lejos de WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-255">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="ae014-256">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="ae014-256">remove_LostFocus</span></span> 

<span data-ttu-id="ae014-257">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="ae014-257">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="ae014-258">[remove_LostFocus](#remove_lostfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="ae014-258">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="ae014-259">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="ae014-259">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="ae014-260">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ae014-260">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="ae014-261">[add_AcceleratorKeyPressed](#add_acceleratorkeypressed)de HRESULT público ([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="ae014-261">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="ae014-262">AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa.</span><span class="sxs-lookup"><span data-stu-id="ae014-262">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="ae014-263">Una clave se considera un acelerador si:</span><span class="sxs-lookup"><span data-stu-id="ae014-263">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="ae014-264">La tecla Ctrl o Alt se está retenida actualmente, o bien</span><span class="sxs-lookup"><span data-stu-id="ae014-264">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="ae014-265">la tecla presionada no se asigna a un carácter.</span><span class="sxs-lookup"><span data-stu-id="ae014-265">the pressed key does not map to a character.</span></span> <span data-ttu-id="ae014-266">Algunas teclas específicas nunca se consideran aceleradores, como Mayús.</span><span class="sxs-lookup"><span data-stu-id="ae014-266">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="ae014-267">La tecla de escape se considera siempre un acelerador.</span><span class="sxs-lookup"><span data-stu-id="ae014-267">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="ae014-268">Los eventos de teclas autorepetidos que se provocan al mantener presionada la tecla también desencadenan este evento.</span><span class="sxs-lookup"><span data-stu-id="ae014-268">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="ae014-269">Puedes filtrarlos comprobando los argumentos del evento ' KeyEventLParam o PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="ae014-269">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="ae014-270">En el modo de ventana, se llama a este controlador de eventos de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="ae014-270">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="ae014-271">Hasta que llames al controlador () en los argumentos del evento o se devuelva el controlador de eventos, el proceso del explorador se bloqueará y las llamadas COM salientes entre procesos generarán un error con RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="ae014-271">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="ae014-272">Sin embargo, todos los métodos de la API de CoreWebView2 funcionarán.</span><span class="sxs-lookup"><span data-stu-id="ae014-272">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="ae014-273">En el modo sin ventana, se llama al controlador de eventos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ae014-273">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="ae014-274">La entrada de datos adicionales no llegará al explorador hasta que el controlador de eventos devuelva o se llame a (), pero el proceso del explorador en sí no se bloqueará y las llamadas COM salientes funcionarán normalmente.</span><span class="sxs-lookup"><span data-stu-id="ae014-274">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="ae014-275">Se recomienda que llame al controlador (TRUE) tan pronto como sepa que desea controlar la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="ae014-275">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

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

#### <span data-ttu-id="ae014-276">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="ae014-276">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="ae014-277">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ae014-277">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="ae014-278">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="ae014-278">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="ae014-279">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="ae014-279">get_ParentWindow</span></span> 

<span data-ttu-id="ae014-280">La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.</span><span class="sxs-lookup"><span data-stu-id="ae014-280">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="ae014-281">[get_ParentWindow](#get_parentwindow)de HRESULT público (HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="ae014-281">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="ae014-282">Esta API inicialmente devuelve la ventana que se pasó a CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="ae014-282">This API initially returns the window passed into CreateCoreWebView2Host.</span></span>

#### <span data-ttu-id="ae014-283">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="ae014-283">put_ParentWindow</span></span> 

<span data-ttu-id="ae014-284">Establezca la ventana principal de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-284">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="ae014-285">[put_ParentWindow](#put_parentwindow)de HRESULT público (HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="ae014-285">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="ae014-286">Esto hará que la vista de ventana reorigen su ventana a la ventana recién suministrada.</span><span class="sxs-lookup"><span data-stu-id="ae014-286">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="ae014-287">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="ae014-287">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="ae014-288">Esta es una notificación independiente de put_Bounds que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).</span><span class="sxs-lookup"><span data-stu-id="ae014-288">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="ae014-289">[NOTIFYPARENTWINDOWPOSITIONCHANGED](#notifyparentwindowpositionchanged)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="ae014-289">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="ae014-290">Esto es necesario para que la accesibilidad y determinados cuadros de diálogo de WebView funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="ae014-290">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="ae014-291">Cerrar</span><span class="sxs-lookup"><span data-stu-id="ae014-291">Close</span></span> 

<span data-ttu-id="ae014-292">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="ae014-292">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="ae014-293">HRESULT público [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="ae014-293">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="ae014-294">Si limpias el explorador instace, se liberarán los recursos que encienden la vista Web.</span><span class="sxs-lookup"><span data-stu-id="ae014-294">Cleaning up the browser instace will release the resources powering the WebView.</span></span> <span data-ttu-id="ae014-295">La instancia del explorador se cerrará si no hay ninguna otra vista previa con ella.</span><span class="sxs-lookup"><span data-stu-id="ae014-295">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="ae014-296">Después de llamar a Close, todas las llamadas a métodos producirán errores y los controladores de eventos dejarán de activarse.</span><span class="sxs-lookup"><span data-stu-id="ae014-296">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="ae014-297">Específicamente, la WebView liberará sus referencias a los controladores de eventos cuando se llama a Close.</span><span class="sxs-lookup"><span data-stu-id="ae014-297">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="ae014-298">Close se llama de forma implícita cuando CoreWebView2Host pierde su referencia final y se destruye.</span><span class="sxs-lookup"><span data-stu-id="ae014-298">Close is implicitly called when the CoreWebView2Host loses its final reference and is destructed.</span></span> <span data-ttu-id="ae014-299">Sin embargo, se recomienda llamar de forma explícita a Close para evitar cualquier ciclo de referencias entre la vista de WebView y el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae014-299">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="ae014-300">En concreto, si capturas una referencia a la vista de la vista en un controlador de eventos, crearás un ciclo de referencia entre la vista en WebView y el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="ae014-300">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="ae014-301">Al llamar a Close se interrumpirá este ciclo liberando todos los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="ae014-301">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="ae014-302">Pero para evitar esta situación, lo mejor es llamar explícitamente a Close en WebView y no capturar una referencia a WebView para asegurarte de que la WebView pueda limpiarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="ae014-302">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

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

#### <span data-ttu-id="ae014-303">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="ae014-303">get_CoreWebView2</span></span> 

<span data-ttu-id="ae014-304">Obtiene el CoreWebView2 asociado a este CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="ae014-304">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>

> <span data-ttu-id="ae014-305">[get_CoreWebView2](#get_corewebview2)(HRESULT) público ([ICoreWebView2](ICoreWebView2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="ae014-305">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="ae014-306">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="ae014-306">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="ae014-307">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="ae014-307">Reason for moving focus.</span></span>

> <span data-ttu-id="ae014-308">[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) enum</span><span class="sxs-lookup"><span data-stu-id="ae014-308">enum [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)</span></span>

 <span data-ttu-id="ae014-309">Los</span><span class="sxs-lookup"><span data-stu-id="ae014-309">Values</span></span>                         | <span data-ttu-id="ae014-310">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ae014-310">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="ae014-311">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="ae014-311">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="ae014-312">El ajuste del foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="ae014-312">Code setting focus into WebView.</span></span>
<span data-ttu-id="ae014-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="ae014-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="ae014-314">Moviendo el foco debido a una resaltado de pestañas hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="ae014-314">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="ae014-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="ae014-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="ae014-316">Moviendo el foco debido a un recorrido de tabulación hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="ae014-316">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="ae014-317">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="ae014-317">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="ae014-318">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ae014-318">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="ae014-319">[CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="ae014-319">enum [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)</span></span>

 <span data-ttu-id="ae014-320">Los</span><span class="sxs-lookup"><span data-stu-id="ae014-320">Values</span></span>                         | <span data-ttu-id="ae014-321">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ae014-321">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="ae014-322">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="ae014-322">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="ae014-323">Corresponde a WM_KEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="ae014-323">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="ae014-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="ae014-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="ae014-325">Corresponde a WM_KEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="ae014-325">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="ae014-326">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="ae014-326">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="ae014-327">Corresponde a WM_SYSKEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="ae014-327">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="ae014-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="ae014-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="ae014-329">Corresponde a WM_SYSKEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="ae014-329">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="ae014-330">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="ae014-330">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="ae014-331">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="ae014-331">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="ae014-332">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="ae014-332">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span></span>

<span data-ttu-id="ae014-333">Para obtener más información, consulte la documentación de WM_KEYDOWN en[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="ae014-333">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

